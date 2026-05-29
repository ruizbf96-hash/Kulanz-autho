# 🔒 Guide de sécurité Firebase — Team Garantie GEA – VW

Ce guide explique comment protéger les données clients (châssis, noms, e-mails, demandes)
stockées dans votre base **Realtime Database** `kulanz-autho`.

> **À retenir** : la clé API dans `app.js` n'est **pas** un secret — c'est normal qu'elle soit
> visible. La vraie sécurité repose sur **les règles de la base** et sur la **restriction de la clé**.
> Tant que les règles sont ouvertes, n'importe qui sur Internet peut lire et modifier toutes vos demandes.

---

## Étape 1 — Vérifier l'état actuel (urgent)

1. Allez sur https://console.firebase.google.com → projet **kulanz-autho**.
2. Menu **Realtime Database** → onglet **Règles**.
3. Si vous voyez ceci, **vos données sont publiques** :
   ```json
   { "rules": { ".read": true, ".write": true } }
   ```
   ou une version avec une date d'expiration (mode test). → Passez à l'étape 3 sans attendre.

---

## Étape 2 — Activer l'authentification par e-mail

Si ce n'est pas déjà fait :

1. Console Firebase → **Authentication** → **Sign-in method**.
2. Activez **E-mail/Mot de passe**.
3. Onglet **Users** : créez les comptes `prenom.nom@geauto.fr` (usagers et TeamGarantie).

> L'application utilise déjà cette méthode (`signInWithEmailAndPassword`). Aucun changement de code nécessaire.

---

## Étape 3 — Désigner les comptes TeamGarantie (les « admins »)

Les règles distinguent deux niveaux :
- **Usager** (`@geauto.fr`) : peut **créer** et **lire** les demandes.
- **TeamGarantie / admin** : peut en plus **valider** (changer le statut) et **supprimer**.

Pour qu'un compte soit admin, on l'ajoute sous le nœud `/admins` avec son **UID** :

1. **Authentication → Users** : pour chaque membre TeamGarantie, copiez son **User UID**
   (colonne de droite, ex. `a1B2c3D4...`).
2. **Realtime Database → Données**, créez manuellement cette structure :
   ```
   admins
     ├─ a1B2c3D4...   : true     ← UID de Omar
     ├─ e5F6g7H8...   : true     ← UID de Tahir
     └─ ...           : true
   ```
   (Bouton **+** à la racine → clé `admins`, puis sous-clés = UID, valeur = `true` de type booléen.)

> Avantage : la liste des admins est **dans la base protégée**, plus dans le code JavaScript public.
> Vous pouvez garder `TEAM_EMAILS` dans `app.js` pour l'affichage, mais l'autorisation **réelle**
> vient désormais des règles.

---

## Étape 4 — Publier les règles

1. **Realtime Database → Règles**.
2. Remplacez tout le contenu par celui du fichier **`database.rules.json`** fourni.
3. Cliquez sur **Publier**.

Ces règles garantissent que :
- seuls les comptes `@geauto.fr` connectés peuvent lire les demandes ;
- tout usager connecté peut créer une demande, mais **pas** modifier celles des autres ;
- seuls les **admins** peuvent valider (statut, commerce, commentaire) ou supprimer ;
- chaque champ est borné en longueur (protection contre l'injection de données massives).

---

## Étape 5 — Restreindre la clé API (Google Cloud)

Pour empêcher l'usage de votre clé depuis un autre site :

1. https://console.cloud.google.com → projet **kulanz-autho** → **APIs et services → Identifiants**.
2. Cliquez sur la clé **Browser key (auto created by Firebase)**.
3. Sous **Restrictions liées aux applications** → **Sites web (HTTP referrers)**, ajoutez :
   ```
   https://VOTRE-UTILISATEUR.github.io/*
   https://VOTRE-UTILISATEUR.github.io/NOM-DU-DEPOT/*
   ```
   (Remplacez par votre adresse GitHub Pages réelle. Ajoutez `http://localhost:*` si vous testez en local.)
4. **Enregistrer**.

---

## Étape 6 — Domaines autorisés pour la connexion

1. **Authentication → Settings → Authorized domains**.
2. Vérifiez que `VOTRE-UTILISATEUR.github.io` y figure (ajoutez-le sinon).
   Sans cela, la connexion renvoie une erreur 400.

---

## ⚠️ Point d'attention sur `email_verified`

Les règles fournies exigent `email_verified == true` en lecture. Les comptes créés **à la main**
dans la console **ne sont pas vérifiés** par défaut → ils ne pourraient pas lire les demandes.

Deux options :

- **Option simple (recommandée au démarrage)** : retirez la condition. Dans `database.rules.json`,
  sur la ligne `.read` de `demandes`, supprimez :
  ```
  && auth.token.email_verified == true
  ```
- **Option robuste** : demandez à chaque utilisateur de vérifier son e-mail. Vous pouvez déclencher
  l'envoi via `firebase.auth().currentUser.sendEmailVerification()` après la première connexion.

---

## Recommandations complémentaires (hygiène RGPD & poste partagé)

Ces demandes contiennent des **données personnelles clients**. En plus des règles :

1. **Cache local** : l'app stocke `gea_demandes` et les brouillons dans le navigateur.
   Sur un poste de concession partagé, pensez à **vous déconnecter** en fin de session
   (la déconnexion peut être complétée pour purger ce cache — dites-le-moi si vous voulez ce correctif).
2. **Durée de conservation** : définissez une politique (ex. suppression des demandes traitées
   après 12–24 mois) pour ne pas conserver indéfiniment des données clients.
3. **Sauvegardes** : activez les exports automatiques de la base (Console → Realtime Database → ⋮ → Sauvegardes).
4. **Web3Forms** : la clé `WEB3_KEY` est visible dans le code. Activez les protections anti-spam
   côté Web3Forms, ou faites passer l'envoi KULANZ par le seul flux Firebase + mail.

---

## Test rapide après configuration

1. Connectez-vous en **usager** : vous devez pouvoir créer une demande et voir l'historique,
   mais **pas** de bouton « Valider » fonctionnel sur les autres (le clic échouera côté base).
2. Connectez-vous en **TeamGarantie** (compte admin) : validation et suppression doivent fonctionner.
3. Déconnecté, essayez d'ouvrir l'URL de la base
   `https://kulanz-autho-default-rtdb.europe-west1.firebasedatabase.app/demandes.json`
   dans un navigateur : vous devez obtenir **`Permission denied`** (et non vos données).

Si le test 3 renvoie `Permission denied`, vos données sont protégées. ✅

---

### Évolution possible (plus tard)

Pour une sécurité encore plus forte, on peut remplacer le nœud `/admins` par des **custom claims**
Firebase (rôle stocké dans le jeton d'authentification). Cela demande une petite **Cloud Function**
(donc un plan Blaze). Le système `/admins` proposé ici fonctionne sans backend et suffit largement
pour votre usage.
