
/* ── VARIABLES ── */
:root{
  --bg:#F4F6F9;
  --card:#ffffff;
  --dark:#0D2D4A;
  --dark2:#1A3D5C;
  --accent:#0099AA;
  --accent2:#007A8A;
  --gold:#0099AA;
  --gold2:#4DC9A8;
  --silver:#6B7A8D;
  --red:#C0392B;
  --green:#0B7A6E;
  --orange:#E67E22;
  --info:#1A6BB5;
  --shadow:0 1px 6px rgba(13,45,74,0.08);
  --shadow-md:0 4px 16px rgba(13,45,74,0.1);
  --r:9px;
  --font-body:'DM Sans','Segoe UI',system-ui,sans-serif;
  --font-title:'DM Sans','Segoe UI',system-ui,sans-serif;
}

/* ── RESET ── */
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:var(--font-body);background:var(--bg);color:var(--dark);min-height:100vh;overflow-x:hidden}
button{cursor:pointer;font-family:var(--font-body)}
input,select,textarea{font-family:var(--font-body)}

/* ── LOGIN ── */
#login-page{position:fixed;top:0;left:0;right:0;bottom:0;width:100vw;height:100vh;background:var(--dark);z-index:9999;display:flex;align-items:center;justify-content:center;overflow-y:auto}
#login-page.hidden{display:none!important}
.lp-wrap{width:100%;max-width:500px;padding:32px 24px;display:flex;flex-direction:column;align-items:center;gap:26px}
.lp-logo{font-size:22px;font-weight:500;color:#fff;text-align:center;letter-spacing:-.3px}
.lp-logo span{color:var(--gold2)}
.lp-sub{font-size:11px;color:rgba(255,255,255,0.45);letter-spacing:2px;text-transform:uppercase;text-align:center;margin-top:2px}
.lp-cards{display:grid;grid-template-columns:1fr 1fr;gap:12px;width:100%}
.lp-card{background:rgba(255,255,255,0.06);border:1px solid rgba(255,255,255,0.12);border-radius:12px;padding:22px 16px;text-align:center;cursor:pointer;transition:all .2s;color:#fff}
.lp-card:hover{background:rgba(77,201,168,0.12);border-color:var(--gold2);transform:translateY(-2px)}
.lp-card-icon{width:42px;height:42px;border-radius:10px;margin:0 auto 10px;display:flex;align-items:center;justify-content:center;font-size:20px}
.lp-card-icon.user{background:rgba(77,201,168,0.15);color:var(--gold2)}
.lp-card-icon.team{background:rgba(255,185,55,0.15);color:#FFB937}
.lp-card-title{font-size:14px;font-weight:500;margin-bottom:5px;color:#fff}
.lp-card-desc{font-size:11px;color:rgba(255,255,255,0.45);line-height:1.5}
.lp-sites{display:grid;grid-template-columns:1fr 1fr;gap:9px;width:100%}
.lp-site{background:rgba(255,255,255,0.07);border:1px solid rgba(255,255,255,0.12);border-radius:9px;padding:10px;font-size:13px;color:rgba(255,255,255,0.8);text-align:center;cursor:pointer;transition:all .2s;font-weight:500}
.lp-site:hover{background:rgba(77,201,168,0.15);border-color:var(--gold2);color:#fff}
.lp-site.span2{grid-column:1/-1;max-width:48%;margin:0 auto}
.lp-back{background:none;border:none;color:rgba(255,255,255,0.4);font-size:13px;text-decoration:underline;margin-top:6px;cursor:pointer}
.lp-back:hover{color:rgba(255,255,255,0.7)}
#lp-step2,#lp-step3{width:100%}
#lp-site-select,#lp-auth-form{width:100%}

.guide-btn{background:rgba(255,255,255,0.07);border:1px solid rgba(255,255,255,0.12);border-radius:9px;color:rgba(255,255,255,0.6);font-size:12px;padding:8px 16px;display:flex;align-items:center;gap:7px;transition:all .2s}
.guide-btn:hover{background:rgba(77,201,168,0.15);border-color:var(--gold2);color:#fff}

/* Auth inputs */
.lp-auth-input{width:100%;padding:10px 14px;background:rgba(255,255,255,0.09);border:1px solid rgba(255,255,255,0.15);border-radius:9px;color:#fff;font-size:13px;outline:none;transition:border .2s}
.lp-auth-input:focus{border-color:var(--gold2);background:rgba(77,201,168,0.1)}
.lp-auth-input::placeholder{color:rgba(255,255,255,0.3)}
.lp-auth-label{color:rgba(255,255,255,0.55);font-size:10px;font-weight:500;text-transform:uppercase;letter-spacing:.6px;display:block;margin-bottom:5px}
.lp-connect-btn{width:100%;padding:11px;background:var(--accent);border:none;border-radius:9px;color:#fff;font-size:14px;font-weight:500;cursor:pointer;transition:all .2s}
.lp-connect-btn:hover{background:var(--accent2);transform:translateY(-1px)}
.lp-auth-error{display:none;color:#FF8080;font-size:12px;text-align:center;background:rgba(192,57,43,0.15);border:1px solid rgba(192,57,43,0.3);padding:8px 12px;border-radius:7px}
.lp-reset-link{background:none;border:none;color:rgba(77,201,168,0.7);font-size:11px;cursor:pointer;text-decoration:underline;padding:0}
.lp-reset-link:hover{color:var(--gold2)}

/* Modal mot de passe */
#pwd-modal{position:fixed;inset:0;background:rgba(0,0,0,0.5);z-index:600;display:none;align-items:center;justify-content:center}
#pwd-modal.open{display:flex}
.pm-box{background:#fff;border-radius:12px;padding:28px;width:100%;max-width:360px;box-shadow:var(--shadow-md)}
.pm-box h3{font-size:17px;font-weight:500;margin-bottom:6px;color:var(--dark)}
.pm-box p{font-size:13px;color:var(--silver);margin-bottom:18px}
.pm-error{font-size:12px;color:var(--red);margin-top:5px;display:none}

/* ── HEADER ── */
header{background:#ffffff;border-bottom:1px solid #E2E8EF;position:sticky;top:0;z-index:100;box-shadow:0 1px 4px rgba(13,45,74,0.06);transition:transform .3s ease;will-change:transform}
header.header-hidden{transform:translateY(-100%)}
.h-top{display:flex;align-items:center;justify-content:space-between;padding:0 28px;height:52px}
.h-logo{font-size:15px;font-weight:500;color:var(--dark)}
.h-logo span{color:var(--accent)}
.h-nav{display:flex;gap:4px}
.nav-tab{padding:7px 14px;border-radius:7px;font-size:13px;color:var(--silver);cursor:pointer;transition:all .15s;display:flex;align-items:center;gap:6px;border:none;background:none;font-weight:500}
.nav-tab.active{background:#EAF8F5;color:var(--accent);font-weight:500}
.nav-tab:hover:not(.active){background:#F0F4F7;color:var(--dark)}
.h-r{display:flex;align-items:center;gap:10px}
#h-user{display:flex;align-items:center;gap:9px}
.h-role{font-size:11px;font-weight:500;color:#8A5A00;background:#FFF8E8;padding:4px 10px;border-radius:20px;border:1px solid #FFD98C}
#h-site-name{font-size:12px;color:#0B7A6E;font-weight:500;background:#EAF8F5;padding:4px 11px;border-radius:20px;border:1px solid #80D4C8}
.h-alert{font-size:11px;background:#FFF3E0;color:#E65100;padding:4px 10px;border-radius:20px;border:1px solid #FFCC80}
.btn-deconnect{background:#fff;border:1px solid #D4DCE5;border-radius:7px;color:var(--silver);font-size:12px;padding:6px 12px;display:flex;align-items:center;gap:5px;transition:all .2s}
.btn-deconnect:hover{background:#FEF0F0;border-color:#F0A0A0;color:var(--red)}

/* Site bar */
#site-bar{border-top:1px solid #E2E8EF;padding:8px 28px;background:#F7FAFB}
.s-btns{display:flex;gap:7px;flex-wrap:wrap}
.s-btn{background:#fff;border:1px solid #D4DCE5;border-radius:7px;color:var(--silver);font-size:12px;padding:5px 13px;cursor:pointer;transition:all .15s;font-weight:500}
.s-btn.active{background:var(--accent);border-color:var(--accent);color:#fff}
.s-btn:hover:not(.active){background:#EAF8F5;border-color:#80D4C8;color:var(--dark)}

/* ── PAGES ── */
.page{display:none}
.page.active{display:block}
.page-wrap{max-width:840px;margin:0 auto;padding:22px 20px}

/* ── FORM TABS ── */
.form-tabs{display:flex;gap:8px;padding:18px 0 4px}
.form-tab{padding:9px 18px;border-radius:8px;font-size:13px;font-weight:500;border:1.5px solid transparent;cursor:pointer;transition:all .2s;display:flex;align-items:center;gap:7px}
.form-tab.active{background:var(--dark);color:var(--gold2);border-color:rgba(77,201,168,0.2)}
.form-tab:not(.active){background:var(--card);color:var(--silver);border-color:#D4DCE5}
.form-tab:hover:not(.active){border-color:#80D4C8;color:var(--dark)}

/* Btn copier */
.btn-copy-kulanz{background:#EAF8F5;border:1px solid #80D4C8;border-radius:8px;color:#0B7A6E;font-size:12px;padding:7px 14px;display:flex;align-items:center;gap:6px;margin-bottom:16px;font-weight:500;transition:all .2s}
.btn-copy-kulanz:hover{background:#D5F0EA}

/* ── FORM CARD ── */
.form-card{background:var(--card);border-radius:10px;border:1px solid #E2E8EF;box-shadow:var(--shadow);margin-bottom:12px;overflow:hidden}
.fc-head{display:flex;align-items:center;gap:10px;padding:12px 18px;background:#F7FAFB;border-bottom:2px solid var(--accent)}
.fc-num{width:24px;height:24px;background:var(--accent);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:500;color:#fff;flex-shrink:0}
.fc-title{font-size:13px;font-weight:500;color:var(--dark)}
.fc-body{padding:16px}

/* ── FIELDS ── */
.fields{display:grid;grid-template-columns:1fr 1fr;gap:11px}
.field{display:flex;flex-direction:column;gap:4px}
.field.full{grid-column:1/-1}
.field label{font-size:10px;font-weight:500;text-transform:uppercase;letter-spacing:.6px;color:var(--silver)}
.field input,.field textarea,.field select{border:1.5px solid #D4DCE5;border-radius:7px;padding:8px 11px;font-size:13px;color:var(--dark);background:#fff;transition:all .2s}
.field input:focus,.field textarea:focus,.field select:focus{outline:none;border-color:var(--accent);box-shadow:0 0 0 3px rgba(0,153,170,0.1)}
.field input[readonly]{background:#EAF8F5;border-color:#80D4C8;color:var(--green);font-weight:500}
.field textarea{resize:vertical;min-height:70px;line-height:1.5}
.chassis-valid{font-size:11px;color:var(--green);margin-top:3px;display:none;font-weight:500}
.or-count{font-size:11px;color:var(--silver);margin-top:3px}

/* ── CATEGORIES ── */
.cat-btns{display:flex;flex-wrap:wrap;gap:7px}
.cat-btn{display:flex;align-items:center;gap:6px;padding:7px 12px;border-radius:7px;border:1.5px solid #D4DCE5;background:#fff;font-size:12px;color:var(--silver);cursor:pointer;transition:all .2s;font-weight:500}
.cat-btn.active{background:var(--dark);color:var(--gold2);border-color:transparent}
.cat-btn:hover:not(.active){border-color:var(--accent);color:var(--dark);background:#EAF8F5}
.cat-icon{font-size:15px}
.saisie-libre-wrap{margin-top:10px;display:none}
.saisie-libre-wrap.show{display:block}

/* ── DROPDOWN SEARCH ── */
.ss-wrap{position:relative;width:100%}
.ss-input-wrap{display:flex;align-items:center;border:1.5px solid #D4DCE5;border-radius:7px;background:#fff;overflow:hidden;transition:all .2s}
.ss-input-wrap:focus-within{border-color:var(--accent);box-shadow:0 0 0 3px rgba(0,153,170,0.1)}
.ss-icon{padding:0 8px 0 10px;color:var(--silver);font-size:14px;flex-shrink:0}
.ss-input{border:none;background:transparent;padding:8px 6px 8px 0;font-size:13px;color:var(--dark);width:100%;outline:none}
.ss-arrow{padding:0 10px;color:var(--silver);font-size:11px;cursor:pointer;flex-shrink:0}
.ss-drop{position:absolute;top:calc(100% + 4px);left:0;right:0;background:#fff;border:1.5px solid #D4DCE5;border-radius:9px;box-shadow:0 6px 20px rgba(13,45,74,0.12);z-index:200;max-height:220px;overflow-y:auto;overflow-x:visible;display:none}
.ss-drop.open{display:block}
.ss-item{padding:9px 14px;font-size:13px;cursor:pointer;color:var(--dark);border-bottom:.5px solid #F0F4F7;transition:background .1s}
.ss-item:last-child{border-bottom:none}
.ss-item:hover{background:#EAF8F5}
.ss-item.selected{background:#EAF8F5;color:var(--green);font-weight:500}
.ss-empty{padding:10px 14px;font-size:13px;color:var(--silver)}
input[name="ava-val"]:disabled,.ss-input:disabled{opacity:.5;cursor:not-allowed}

/* ── VERIFS KULANZ ── */
.verifblock{display:flex;flex-direction:column;gap:8px}
.chk-row{display:flex;flex-direction:column;gap:6px}
.chk-label{font-size:10px;font-weight:500;text-transform:uppercase;letter-spacing:.6px;color:var(--silver);padding:4px 0;border-bottom:1px solid #EEF2F5;margin-bottom:2px}
.chk-item{display:flex;align-items:center;gap:8px;font-size:13px;color:var(--dark);cursor:pointer;padding:2px 0}
.chk-item input[type=checkbox]{width:15px;height:15px;accent-color:var(--accent);cursor:pointer}
.tpi-block{display:none;margin-top:6px}
.tpi-block.show{display:block}
.tpi-input{width:100%;border:1.5px solid #D4DCE5;border-radius:7px;padding:8px 12px;font-size:13px;color:var(--dark)}
.tpi-input:focus{outline:none;border-color:var(--accent)}
.nok-zone{display:none}
.nok-zone.show{display:block}
.knok-box{border-radius:8px;padding:12px 14px;margin-top:8px;font-size:13px;line-height:1.5;font-weight:500}
.knok-box.rouge{background:#FCEAEA;border:1.5px solid #F0A0A0;color:#8B1A1A}
.knok-box.jaune{background:#FFF8E8;border:1.5px solid #FFD98C;color:#7A5800}
.knok-box.orange{background:#FFF3E0;border:1.5px solid #FFCC80;color:#7A3800}

/* ── BOUTON ENVOYER ── */
.btn-primary{display:flex;align-items:center;justify-content:center;gap:8px;width:100%;padding:13px;background:var(--accent);color:#fff;border:none;border-radius:9px;font-size:14px;font-weight:500;cursor:pointer;transition:all .2s;margin-top:8px}
.btn-primary:hover{background:var(--accent2);transform:translateY(-1px);box-shadow:0 4px 14px rgba(0,153,170,0.25)}

/* ── HISTORIQUE ── */
.histo-filters{display:flex;gap:8px;margin-bottom:14px;flex-wrap:wrap;align-items:center}
.hf-select{border:1.5px solid #D4DCE5;border-radius:7px;padding:7px 12px;font-size:13px;background:#fff;color:var(--dark);cursor:pointer;font-weight:500}
.hf-select:focus{outline:none;border-color:var(--accent)}
.btn-vider-histo{background:#FEF0F0;border:1.5px solid #F0A0A0;border-radius:7px;color:#8B1A1A;font-size:12px;padding:7px 12px;display:flex;align-items:center;gap:5px;font-weight:500;margin-left:auto}
.btn-vider-histo:hover{background:#FCEAEA}
.histo-table-wrap{background:var(--card);border-radius:10px;border:1px solid #E2E8EF;box-shadow:var(--shadow);overflow:hidden}
.table-box{overflow-x:auto}
table{width:100%;border-collapse:collapse}
th{padding:11px 14px;text-align:left;font-size:10px;font-weight:500;text-transform:uppercase;letter-spacing:.6px;color:#fff;background:var(--dark)}
th:first-child{border-left:3px solid var(--accent)}
td{padding:11px 14px;border-bottom:1px solid #F0F4F7;font-size:13px;vertical-align:middle;color:var(--dark)}
tr:last-child td{border-bottom:none}
tr:hover td{background:#F7FAFB}
.badge{padding:3px 9px;border-radius:6px;font-size:11px;font-weight:500;display:inline-flex;align-items:center;gap:4px;white-space:nowrap}
.badge-ok,.b-ok{background:#EAF8F5;color:#0B7A6E;border:1px solid #80D4C8}
.badge-nok,.b-no{background:#FCEAEA;color:#8B1A1A;border:1px solid #F0A0A0}
.badge-wait,.b-wait{background:#FFF8E8;color:#8A5A00;border:1px solid #FFD98C}
.badge-warn,.b-comp{background:#EAF2FB;color:#0C447C;border:1px solid #85B7EB}
.btn-valider{background:var(--dark);color:var(--gold2);border:none;border-radius:6px;padding:5px 11px;font-size:12px;font-weight:500;cursor:pointer;transition:all .2s;white-space:nowrap}
.btn-valider:hover{background:var(--accent);color:#fff}

/* Stats dashboard */
.dash-wrap{display:none;margin-bottom:18px}
.dash-wrap.on{display:block}
.sites-grid{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:14px}
.site-card{background:var(--card);border-radius:9px;border:1px solid #E2E8EF;padding:14px 16px;min-width:160px;box-shadow:var(--shadow);border-top:3px solid var(--accent)}
.site-card h4{font-size:11px;font-weight:500;color:var(--dark);margin-bottom:8px;text-transform:uppercase;letter-spacing:.5px}
.stat-row{display:flex;gap:12px}
.stat-n{font-size:22px;font-weight:500;color:var(--dark)}
.stat-n.green{color:var(--green)}
.stat-n.red{color:var(--red)}
.stat-l{font-size:10px;color:var(--silver);margin-top:2px;font-weight:500;text-transform:uppercase;letter-spacing:.3px}
.stat-col{display:flex;flex-direction:column;align-items:center}

/* ── SIDE PANEL ── */
#sp-overlay{position:fixed;inset:0;background:rgba(13,45,74,0.4);z-index:700;display:none}
#sp-overlay.open{display:block}
#side-panel{position:fixed;top:0;right:0;bottom:0;width:490px;max-width:100vw;background:#fff;box-shadow:-6px 0 32px rgba(13,45,74,0.12);z-index:701;transform:translateX(100%);transition:transform .32s cubic-bezier(.25,.46,.45,.94);display:flex;flex-direction:column}
#side-panel.open{transform:translateX(0)}
.sp-head{background:#fff;border-bottom:2px solid var(--accent);padding:16px 20px;display:flex;align-items:center;gap:12px;flex-shrink:0}
.sp-head-icon{width:36px;height:36px;background:#EAF8F5;border-radius:8px;display:flex;align-items:center;justify-content:center;color:var(--accent);font-size:18px;flex-shrink:0}
.sp-head-text{flex:1}
.sp-head-text h3{font-size:15px;font-weight:500;color:var(--dark);margin-bottom:2px}
.sp-head-text p{font-size:11px;color:var(--silver)}
.sp-close{background:none;border:none;color:var(--silver);font-size:20px;cursor:pointer;padding:4px;line-height:1;transition:color .2s}
.sp-close:hover{color:var(--dark)}
.sp-body{flex:1;overflow-y:auto;padding:16px 20px;min-height:0;background:#F7FAFB}
.sp-sec{margin-bottom:12px;background:#fff;border-radius:9px;padding:14px;border:1px solid #E2E8EF;box-shadow:0 1px 3px rgba(13,45,74,0.05)}
.sp-sec-title{font-size:10px;font-weight:500;text-transform:uppercase;letter-spacing:.7px;color:var(--silver);margin-bottom:10px;padding-bottom:8px;border-bottom:1px solid #EEF2F5}
.sp-info-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.sp-info{display:flex;flex-direction:column;gap:3px;background:#F7FAFB;padding:8px 10px;border-radius:7px;border:1px solid #EAF0F5}
.sp-info-l{font-size:9px;color:var(--silver);text-transform:uppercase;letter-spacing:.5px;font-weight:500}
.sp-info-v{font-size:13px;font-weight:500;color:var(--dark)}
select#sp-statut{width:100%;border:1.5px solid #D4DCE5;border-radius:7px;padding:9px 12px;font-size:13px;background:#fff;cursor:pointer;font-weight:500;color:var(--dark)}
select#sp-statut:focus{outline:none;border-color:var(--accent);box-shadow:0 0 0 3px rgba(0,153,170,0.1)}
#sp-comment{width:100%;border:1.5px solid #D4DCE5;border-radius:7px;padding:9px 12px;font-size:13px;resize:vertical;min-height:70px;line-height:1.5;color:var(--dark)}
#sp-comment:focus{outline:none;border-color:var(--accent);box-shadow:0 0 0 3px rgba(0,153,170,0.1)}
.sp-pwd-err{font-size:12px;color:var(--red);display:none;padding:6px 0;font-weight:500}
#sp-commerce{display:none}
.commerce-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.commerce-field{display:flex;flex-direction:column;gap:4px}
.commerce-field label{font-size:11px;color:var(--silver);font-weight:500;text-transform:uppercase;letter-spacing:.4px}
.commerce-field input{border:1.5px solid #D4DCE5;border-radius:7px;padding:8px 12px;font-size:13px;width:100%;color:var(--dark)}
.commerce-field input:focus{outline:none;border-color:var(--accent)}
.sp-footer{padding:14px 20px;border-top:1px solid #E2E8EF;display:flex;gap:9px;flex-shrink:0;background:#fff}
#sp-ok-btn{flex:1;background:var(--accent);color:#fff;border:none;border-radius:8px;padding:11px;font-size:14px;font-weight:500;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:7px;transition:all .2s}
#sp-ok-btn:hover{background:var(--accent2);transform:translateY(-1px);box-shadow:0 4px 12px rgba(0,153,170,0.25)}
#sp-ok-btn:disabled{opacity:.5;cursor:not-allowed;transform:none;box-shadow:none}
.sp-cancel-btn{background:#fff;border:1.5px solid #D4DCE5;border-radius:8px;color:var(--silver);font-size:14px;padding:11px 16px;cursor:pointer;font-weight:500;transition:all .2s}
.sp-cancel-btn:hover{background:#F0F4F7}

/* ── SUCCESS OVERLAY ── */
#success-overlay{position:fixed;inset:0;background:rgba(13,45,74,0.5);z-index:800;display:none;align-items:center;justify-content:center}
#success-overlay.show{display:flex}
.success-box{background:#fff;border-radius:14px;padding:36px;text-align:center;max-width:380px;width:90%;box-shadow:var(--shadow-md);border-top:4px solid var(--accent)}
.success-icon{font-size:52px;margin-bottom:12px}
.success-title{font-size:20px;font-weight:500;color:var(--dark);margin-bottom:6px}
.success-sub{font-size:14px;color:var(--silver);line-height:1.6;margin-bottom:20px}
.success-btn{background:var(--accent);color:#fff;border:none;border-radius:8px;padding:11px 24px;font-size:14px;font-weight:500;cursor:pointer}
.success-btn:hover{background:var(--accent2)}

/* ── TOAST ── */
#toast{position:fixed;bottom:24px;right:24px;background:var(--dark);color:var(--gold2);padding:12px 18px;border-radius:9px;font-size:13px;font-weight:500;box-shadow:var(--shadow-md);z-index:900;opacity:0;transition:opacity .3s;pointer-events:none;display:flex;align-items:center;gap:8px;border-left:3px solid var(--accent)}
#toast.show{opacity:1}

/* ── VIDER MODAL ── */
#vider-modal{position:fixed;inset:0;background:rgba(13,45,74,0.5);z-index:800;display:none;align-items:center;justify-content:center}
#vider-modal.open{display:flex}
.vm-box{background:#fff;border-radius:12px;padding:28px;max-width:400px;width:90%;box-shadow:var(--shadow-md)}
.vm-box h3{font-size:17px;font-weight:500;margin-bottom:8px;color:var(--dark)}
.vm-box p{font-size:13px;color:var(--silver);margin-bottom:20px;line-height:1.5}
.vm-btns{display:flex;gap:10px;justify-content:flex-end}
.vm-cancel{background:#fff;border:1.5px solid #D4DCE5;border-radius:7px;color:var(--silver);font-size:13px;padding:9px 18px;cursor:pointer;font-weight:500}
.vm-confirm{background:var(--red);border:none;border-radius:7px;color:#fff;font-size:13px;font-weight:500;padding:9px 18px;cursor:pointer}

/* ── HIDDEN / UTILS ── */
.hidden{display:none!important}
.req{color:var(--red);font-weight:500}
.opt{color:var(--silver);font-weight:400;font-size:10px}
.muted{color:var(--silver)}
