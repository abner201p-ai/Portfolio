<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abner — Développeur Web Professionnel au Niger</title>
<meta name="description" content="Abner, développeur web professionnel au Niger. Création de sites vitrines, e-commerce et applications web. Clients locaux et internationaux.">
<meta name="keywords" content="développeur web Niger, création site web Niamey, site web professionnel Niger, développeur web Afrique">
<!-- Open Graph / Facebook -->
<meta property="og:title" content="Abner — Développeur Web Professionnel au Niger">
<meta property="og:description" content="Création de sites vitrines, e-commerce et maintenance — clients locaux & internationaux.">
<meta property="og:type" content="website">
<meta property="og:locale" content="fr_FR">
<meta property="og:image" content="https://i.imgur.com/XzdyshT.png">
<meta name="twitter:image" content="https://i.imgur.com/XzdyshT.png">
<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Abner — Développeur Web Professionnel au Niger">
<meta name="twitter:description" content="Création de sites vitrines, e-commerce et maintenance — clients locaux & internationaux.">
<style>
/* ===================== RESET ===================== */
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:Georgia,serif;background:#08090d;color:#e2e8f0;line-height:1.7;overflow-x:hidden}
a{color:inherit;text-decoration:none}
ul{list-style:none}
img{max-width:100%;display:block}
button{font-family:inherit;cursor:pointer;border:none}

/* ===================== VARIABLES ===================== */
:root{
  --bg:#08090d;
  --bg2:#0f1117;
  --card:#131820;
  --border:#1e2736;
  --text:#e2e8f0;
  --muted:#6b7a8d;
  --green:#00c896;
  --blue:#3b82f6;
  --gold:#d4a843;
  --r:12px;
}

/* ===================== SCROLLBAR ===================== */
::-webkit-scrollbar{width:5px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px}

/* ===================== NAV ===================== */
#nav{
  position:fixed;top:0;left:0;right:0;z-index:999;
  display:flex;align-items:center;justify-content:space-between;
  padding:1rem 2rem;
  background:rgba(8,9,13,0.95);
  border-bottom:1px solid var(--border);
  backdrop-filter:blur(12px);
}
.nav-logo{
  display:flex;align-items:center;gap:.7rem;
  font-size:1.1rem;font-weight:700;letter-spacing:.5px;
}
.nav-avatar{
  width:36px;height:36px;border-radius:50%;
  background:linear-gradient(135deg,var(--green),var(--blue));
  display:flex;align-items:center;justify-content:center;
  font-size:.85rem;font-weight:800;color:#08090d;
  border:2px solid var(--green);flex-shrink:0;
}
.nav-links{display:flex;align-items:center;gap:1.8rem}
.nav-links a{
  font-size:.9rem;color:var(--muted);
  transition:color .2s;cursor:pointer;
}
.nav-links a:hover,.nav-links a.act{color:var(--text)}
.nav-btn{
  background:var(--green);color:#08090d !important;
  padding:.45rem 1.1rem;border-radius:50px;
  font-weight:700;font-size:.82rem !important;
  transition:background .2s,transform .2s;
}
.nav-btn:hover{background:#00e0a8;transform:scale(1.04)}

/* Mobile hamburger */
.ham{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:4px}
.ham span{display:block;width:22px;height:2px;background:var(--text);border-radius:2px;transition:all .3s}

/* ===================== PAGE SYSTEM ===================== */
.pg{display:none}
.pg.on{display:block}

/* ===================== LAYOUT HELPERS ===================== */
.wrap{max-width:1160px;margin:0 auto;padding:0 1.5rem}
.sect{padding:3.5rem 1.5rem;max-width:1160px;margin:0 auto}
.tag{
  display:inline-flex;align-items:center;gap:.5rem;
  color:var(--green);font-size:.75rem;font-weight:700;
  letter-spacing:2px;text-transform:uppercase;margin-bottom:.8rem;
}
.tag::before{content:'';width:18px;height:2px;background:var(--green)}
h2.ttl{
  font-size:clamp(1.6rem,4vw,2.4rem);font-weight:700;
  margin-bottom:.8rem;line-height:1.2;
}
.sub{font-size:1rem;color:var(--muted);max-width:520px;margin-bottom:2rem}

/* ===================== BUTTONS ===================== */
.btn{
  display:inline-flex;align-items:center;gap:.5rem;
  padding:.8rem 1.8rem;border-radius:50px;
  font-weight:700;font-size:.9rem;transition:all .25s;cursor:pointer;
}
.btn-g{background:var(--green);color:#08090d;border:2px solid var(--green)}
.btn-g:hover{background:#00e0a8;transform:translateY(-2px);box-shadow:0 8px 24px rgba(0,200,150,.3)}
.btn-o{background:transparent;color:var(--text);border:2px solid var(--border)}
.btn-o:hover{border-color:var(--green);color:var(--green);transform:translateY(-2px)}

/* ===================== CARDS ===================== */
.card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.5rem;
  transition:border-color .3s,transform .3s;
}
.card:hover{border-color:rgba(0,200,150,.4);transform:translateY(-4px)}

/* ===================== GRID SYSTEMS ===================== */
.g2{display:grid;grid-template-columns:repeat(2,1fr);gap:1.2rem}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:1.2rem}
.g4{display:grid;grid-template-columns:repeat(4,1fr);gap:1rem}

/* ===================== HERO ===================== */
.hero{
  padding:6.5rem 1.5rem 3rem;
  max-width:1160px;margin:0 auto;
}
.hero-badge{
  display:inline-flex;align-items:center;gap:.5rem;
  background:rgba(0,200,150,.08);border:1px solid rgba(0,200,150,.25);
  color:var(--green);padding:.35rem .9rem;border-radius:50px;
  font-size:.75rem;font-weight:600;letter-spacing:1.5px;
  text-transform:uppercase;margin-bottom:1.5rem;
}
.hero-badge::before{
  content:'';width:6px;height:6px;border-radius:50%;
  background:var(--green);animation:blink 2s infinite;
}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.hero h1{
  font-size:clamp(2.2rem,6vw,4rem);font-weight:700;
  line-height:1.1;margin-bottom:1.2rem;
}
.hero h1 em{
  font-style:normal;
  background:linear-gradient(90deg,var(--green),var(--blue));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  background-clip:text;
}
.hero p{font-size:1.05rem;color:var(--muted);max-width:500px;margin-bottom:2rem}
.hero-btns{display:flex;gap:1rem;flex-wrap:wrap}

/* ===================== STATS ===================== */
.stats{
  background:var(--card);border-top:1px solid var(--border);
  border-bottom:1px solid var(--border);padding:1.8rem 1.5rem;
}
.stats-inner{
  max-width:1160px;margin:0 auto;
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:1rem;text-align:center;
}
.stat-n{
  font-size:2rem;font-weight:800;color:var(--green);
  line-height:1;margin-bottom:.25rem;
}
.stat-l{font-size:.8rem;color:var(--muted)}

/* ===================== PROJECT CARDS ===================== */
.proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:1.2rem}
.proj-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);overflow:hidden;
  transition:border-color .3s,transform .3s,box-shadow .3s;
}
.proj-card:hover{
  border-color:var(--green);transform:translateY(-5px);
  box-shadow:0 16px 40px rgba(0,0,0,.4);
}
.proj-img{
  height:160px;display:flex;align-items:center;
  justify-content:center;font-size:3rem;
  background:var(--bg2);position:relative;overflow:hidden;
}
.proj-img::after{
  content:'';position:absolute;inset:0;
  background:linear-gradient(to bottom,transparent 50%,var(--card));
}
.proj-body{padding:1.2rem}
.proj-tags{display:flex;gap:.4rem;flex-wrap:wrap;margin-bottom:.6rem}
.ptag{
  background:rgba(0,200,150,.1);color:var(--green);
  padding:.15rem .6rem;border-radius:50px;font-size:.72rem;font-weight:600;
}
.ptag.b{background:rgba(59,130,246,.1);color:var(--blue)}
.ptag.gold{background:rgba(212,168,67,.1);color:var(--gold)}
.proj-body h3{font-size:1.05rem;font-weight:700;margin-bottom:.4rem}
.proj-body p{color:var(--muted);font-size:.88rem}
.proj-link{
  display:inline-flex;align-items:center;gap:.4rem;
  margin-top:.8rem;color:var(--green);font-size:.82rem;font-weight:600;
  transition:gap .2s;
}
.proj-link:hover{gap:.7rem}

/* ===================== SKILLS ===================== */
.skill-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1rem}
.sk-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.3rem;
  transition:border-color .3s;
}
.sk-card:hover{border-color:rgba(0,200,150,.35)}
.sk-icon{font-size:1.7rem;margin-bottom:.8rem}
.sk-card h4{font-weight:700;font-size:.95rem;margin-bottom:.4rem}
.sk-card p{color:var(--muted);font-size:.83rem}

/* ===================== TESTIMONIALS ===================== */
.test-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:1.2rem}
.test-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.5rem;position:relative;
}
.test-card::before{
  content:'"';font-size:5rem;color:var(--green);opacity:.1;
  position:absolute;top:-.3rem;left:1rem;line-height:1;
}
.stars{color:var(--gold);font-size:.85rem;margin-bottom:.8rem}
.test-card p{color:var(--muted);font-size:.88rem;line-height:1.7;margin-bottom:1rem}
.test-auth{display:flex;align-items:center;gap:.7rem}
.auth-av{
  width:38px;height:38px;border-radius:50%;flex-shrink:0;
  background:linear-gradient(135deg,var(--green),var(--blue));
  display:flex;align-items:center;justify-content:center;
  font-size:.75rem;font-weight:800;color:#08090d;
}
.auth-name strong{display:block;font-size:.85rem;font-weight:700}
.auth-name span{font-size:.78rem;color:var(--muted)}

/* ===================== WHY ME ===================== */
.why-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1rem;margin-top:2rem}
.why-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.5rem;text-align:center;
  transition:border-color .3s,transform .3s;
}
.why-card:hover{border-color:rgba(0,200,150,.4);transform:translateY(-3px)}
.why-icon{font-size:1.8rem;margin-bottom:.8rem}
.why-card h4{font-weight:700;font-size:.92rem;margin-bottom:.4rem}
.why-card p{color:var(--muted);font-size:.8rem}

/* ===================== CTA BANNER ===================== */
.cta-box{
  background:linear-gradient(135deg,rgba(0,200,150,.07),rgba(59,130,246,.05));
  border:1px solid rgba(0,200,150,.2);border-radius:var(--r);
  padding:2.5rem 2rem;text-align:center;
  max-width:1160px;margin:0 auto 3rem;
}
.cta-box h2{font-size:clamp(1.4rem,3vw,2rem);font-weight:700;margin-bottom:.8rem}
.cta-box p{color:var(--muted);margin-bottom:1.5rem}

/* ===================== DIVIDER ===================== */
.divider{height:1px;background:var(--border);max-width:1160px;margin:0 auto}

/* ===================== FOOTER ===================== */
footer{
  border-top:1px solid var(--border);
  padding:2.5rem 1.5rem;max-width:1160px;margin:0 auto;
}
.foot-grid{
  display:grid;grid-template-columns:2fr 1fr 1fr;
  gap:2.5rem;margin-bottom:2rem;
}
.foot-brand h4{font-size:1.1rem;font-weight:700;margin-bottom:.6rem}
.foot-brand p{color:var(--muted);font-size:.85rem;max-width:260px}
.foot-links{margin-top:.8rem;display:flex;gap:.8rem;flex-wrap:wrap}
.foot-links a{color:var(--green);font-size:.83rem}
.foot-col h5{
  font-size:.75rem;font-weight:700;text-transform:uppercase;
  letter-spacing:1.5px;color:var(--muted);margin-bottom:.8rem;
}
.foot-col li{margin-bottom:.4rem}
.foot-col li a{color:var(--muted);font-size:.85rem;transition:color .2s;cursor:pointer}
.foot-col li a:hover{color:var(--green)}
.foot-bottom{
  border-top:1px solid var(--border);padding-top:1.2rem;
  display:flex;justify-content:space-between;align-items:center;
  font-size:.78rem;color:var(--muted);
}

/* ===================== BLOG ===================== */
.blog-top{padding:5.5rem 1.5rem 2rem;max-width:1160px;margin:0 auto}
.blog-top h1{font-size:clamp(1.8rem,5vw,3rem);font-weight:700;margin-bottom:.8rem}
.blog-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(310px,1fr));
  gap:1.3rem;padding:0 1.5rem 3rem;
  max-width:1160px;margin:0 auto;
}
.blog-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);overflow:hidden;
  transition:border-color .3s,transform .3s,box-shadow .3s;
  cursor:pointer;
}
.blog-card:hover{
  border-color:rgba(0,200,150,.4);transform:translateY(-5px);
  box-shadow:0 16px 40px rgba(0,0,0,.35);
}
.blog-thumb{
  height:130px;display:flex;align-items:center;
  justify-content:center;font-size:3rem;
}
.t1{background:linear-gradient(135deg,#0a1f1a,#091520)}
.t2{background:linear-gradient(135deg,#1a0d20,#10091f)}
.t3{background:linear-gradient(135deg,#1f1a0d,#1e100a)}
.t4{background:linear-gradient(135deg,#0d1a1f,#0a101e)}
.t5{background:linear-gradient(135deg,#1a1f0d,#101e0a)}
.t6{background:linear-gradient(135deg,#1f0d0d,#1e0a0a)}
.t7{background:linear-gradient(135deg,#0d0d1f,#0a0a1e)}
.blog-body{padding:1.2rem}
.blog-meta{display:flex;gap:.8rem;font-size:.75rem;color:var(--muted);margin-bottom:.6rem}
.blog-meta .cat{color:var(--green);font-weight:600}
.blog-body h3{font-size:1rem;font-weight:700;line-height:1.4;margin-bottom:.5rem}
.blog-body p{color:var(--muted);font-size:.85rem;line-height:1.6}
.blog-more{
  display:inline-flex;align-items:center;gap:.4rem;
  margin-top:.8rem;color:var(--green);font-size:.82rem;font-weight:600;
}

/* ===================== ARTICLE ===================== */
#art-wrap{display:none;max-width:760px;margin:0 auto;padding:5.5rem 1.5rem 4rem}
.art-back{
  display:inline-flex;align-items:center;gap:.5rem;
  color:var(--muted);font-size:.88rem;cursor:pointer;
  margin-bottom:1.8rem;transition:color .2s;border:none;background:none;
  font-family:inherit;
}
.art-back:hover{color:var(--green)}
#art-wrap h1{font-size:clamp(1.6rem,4vw,2.4rem);font-weight:700;line-height:1.2;margin-bottom:1rem}
#art-wrap .art-intro{font-size:1rem;color:var(--muted);margin-bottom:2.5rem;padding-bottom:2rem;border-bottom:1px solid var(--border)}
.art-body h2{font-size:1.3rem;font-weight:700;margin:2rem 0 .8rem;color:var(--text)}
.art-body h3{font-size:1.1rem;font-weight:700;margin:1.5rem 0 .6rem;color:var(--green)}
.art-body p{color:var(--muted);margin-bottom:1rem;line-height:1.8}
.art-body ul{margin:1rem 0 1.3rem;display:grid;gap:.5rem}
.art-body ul li{display:flex;align-items:flex-start;gap:.6rem;color:var(--muted);font-size:.92rem}
.art-body ul li::before{content:'→';color:var(--green);flex-shrink:0}
.art-callout{
  background:rgba(0,200,150,.06);border-left:3px solid var(--green);
  padding:1rem 1.3rem;border-radius:0 8px 8px 0;margin:1.5rem 0;
}
.art-callout p{color:var(--text);font-style:italic;margin:0}
.art-cta{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.8rem;text-align:center;margin-top:3rem;
}
.art-cta h3{font-size:1.1rem;font-weight:700;margin-bottom:.6rem}
.art-cta p{color:var(--muted);font-size:.9rem;margin-bottom:1.2rem}

/* ===================== SERVICES ===================== */
.serv-top{padding:5.5rem 1.5rem 2rem;max-width:1160px;margin:0 auto}
.serv-top h1{font-size:clamp(1.8rem,5vw,3rem);font-weight:700;margin-bottom:.8rem}
.price-grid{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:1.2rem;padding:0 1.5rem;
  max-width:1160px;margin:0 auto 2.5rem;
}
.price-card{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.8rem;position:relative;
  transition:transform .3s,box-shadow .3s;
}
.price-card:hover{transform:translateY(-5px);box-shadow:0 16px 40px rgba(0,0,0,.3)}
.price-card.best{
  border-color:var(--green);
  background:linear-gradient(180deg,rgba(0,200,150,.05),var(--card));
}
.best-badge{
  position:absolute;top:-12px;left:50%;transform:translateX(-50%);
  background:var(--green);color:#08090d;
  padding:.2rem .9rem;border-radius:50px;
  font-size:.72rem;font-weight:800;white-space:nowrap;
}
.price-icon{font-size:1.8rem;margin-bottom:.8rem}
.price-card h3{font-size:1.3rem;font-weight:800;margin-bottom:.4rem}
.price-desc{
  color:var(--muted);font-size:.85rem;margin-bottom:1.2rem;
  padding-bottom:1.2rem;border-bottom:1px solid var(--border);
}
.price-lbl{font-size:.72rem;color:var(--muted);text-transform:uppercase;letter-spacing:1px;margin-bottom:.2rem}
.price-row{display:flex;align-items:baseline;gap:.4rem;margin-bottom:.15rem}
.price-amt{font-size:1.6rem;font-weight:800;color:var(--green)}
.price-cur{font-size:.82rem;color:var(--muted)}
.price-note{font-size:.75rem;color:var(--muted);margin:.6rem 0 1.3rem}
.feat-list{display:grid;gap:.55rem;margin-bottom:1.5rem}
.feat-item{display:flex;align-items:flex-start;gap:.6rem;font-size:.85rem;color:var(--muted)}
.feat-item .ck{color:var(--green);flex-shrink:0;font-size:.8rem}
.card-btn{
  width:100%;padding:.8rem;border-radius:8px;
  font-weight:700;font-size:.9rem;cursor:pointer;
  transition:all .25s;font-family:inherit;
}
.card-btn-g{background:var(--green);color:#08090d;border:2px solid var(--green)}
.card-btn-g:hover{background:#00e0a8}
.card-btn-o{background:transparent;color:var(--text);border:2px solid var(--border)}
.card-btn-o:hover{border-color:var(--green);color:var(--green)}

.addon-grid{
  display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
  gap:1rem;padding:0 1.5rem;max-width:1160px;margin:0 auto 3rem;
}
.addon{
  background:var(--card);border:1px solid var(--border);
  border-radius:8px;padding:1.1rem 1.2rem;
  display:flex;align-items:flex-start;gap:.9rem;
  transition:border-color .3s;
}
.addon:hover{border-color:rgba(0,200,150,.35)}
.addon-ic{font-size:1.4rem;flex-shrink:0}
.addon strong{display:block;font-size:.88rem;margin-bottom:.15rem}
.addon .addon-price{font-size:.78rem;color:var(--green)}
.addon .addon-desc{font-size:.78rem;color:var(--muted);margin-top:.15rem}

/* ===================== CONTACT ===================== */
.contact-wrap{
  display:grid;grid-template-columns:1fr 1fr;
  gap:3rem;align-items:start;
}
.contact-info h3{font-size:1.2rem;font-weight:700;margin-bottom:.8rem}
.contact-info p{color:var(--muted);font-size:.9rem;margin-bottom:1.5rem}
.c-links{display:flex;flex-direction:column;gap:.8rem}
.c-link{
  display:flex;align-items:center;gap:.9rem;
  padding:.9rem 1.1rem;background:var(--card);
  border:1px solid var(--border);border-radius:8px;
  transition:border-color .3s,transform .25s;cursor:pointer;
}
.c-link:hover{border-color:var(--green);transform:translateX(4px)}
.c-link-ic{font-size:1.2rem}
.c-link strong{display:block;font-size:.88rem}
.c-link span{font-size:.78rem;color:var(--muted)}

/* ===================== FORMS ===================== */
.form-wrap{display:grid;gap:.9rem}
.frow{display:grid;grid-template-columns:1fr 1fr;gap:.9rem}
.fg{display:flex;flex-direction:column;gap:.35rem}
.fg label{font-size:.8rem;color:var(--muted);font-weight:600}
.fg input,.fg textarea,.fg select{
  background:var(--card);border:1px solid var(--border);
  border-radius:8px;padding:.7rem .95rem;
  color:var(--text);font-family:inherit;font-size:.88rem;
  outline:none;transition:border-color .2s;
}
.fg input:focus,.fg textarea:focus,.fg select:focus{border-color:var(--green)}
.fg select option{background:var(--bg2)}
.fg textarea{min-height:110px;resize:vertical}
.success{
  display:none;background:rgba(0,200,150,.08);
  border:1px solid var(--green);border-radius:8px;
  padding:.9rem 1.2rem;color:var(--green);
  font-size:.88rem;margin-top:.5rem;
  align-items:center;gap:.6rem;
}
.success.show{display:flex}

/* ===================== QUESTIONNAIRE ===================== */
.q-wrap{max-width:760px;margin:0 auto;padding:5.5rem 1.5rem 4rem}
.q-head{margin-bottom:2.5rem}
.q-head h1{font-size:clamp(1.8rem,4vw,2.6rem);font-weight:700;margin-bottom:.8rem}
.q-head p{color:var(--muted);font-size:.95rem;max-width:500px}
.progress{background:var(--border);height:4px;border-radius:2px;margin-bottom:2.5rem}
.prog-fill{
  background:linear-gradient(90deg,var(--green),var(--blue));
  height:100%;border-radius:2px;transition:width .5s ease;width:0%;
}
.q-section{
  background:var(--card);border:1px solid var(--border);
  border-radius:var(--r);padding:1.5rem;margin-bottom:1.2rem;
}
.q-stitle{
  display:flex;align-items:center;gap:.6rem;
  color:var(--green);font-size:.8rem;font-weight:800;
  text-transform:uppercase;letter-spacing:1.5px;margin-bottom:1.2rem;
}
.q-num{
  background:rgba(0,200,150,.15);width:26px;height:26px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-size:.75rem;flex-shrink:0;
}
.q-fields{display:grid;gap:1rem}
.q-submit{margin-top:1.5rem}
.q-hint{text-align:center;font-size:.78rem;color:var(--muted);margin-top:.6rem}

/* ===================== RESPONSIVE ===================== */
@media(max-width:900px){
  .price-grid{grid-template-columns:1fr;max-width:420px}
  .contact-wrap{grid-template-columns:1fr}
  .foot-grid{grid-template-columns:1fr 1fr}
  .stats-inner{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:750px){
  .hero-photo-wrap{display:none!important}
}
@media(max-width:650px){
  .nav-links{display:none}
  .nav-links.open{
    display:flex;flex-direction:column;position:fixed;
    top:64px;left:0;right:0;
    background:rgba(8,9,13,.97);backdrop-filter:blur(12px);
    padding:1.5rem;border-bottom:1px solid var(--border);
    gap:1.2rem;z-index:998;
  }
  .ham{display:flex}
  .frow{grid-template-columns:1fr}
  .blog-grid{grid-template-columns:1fr;padding:0 1rem 2rem}
  .foot-grid{grid-template-columns:1fr}
  .foot-bottom{flex-direction:column;gap:.4rem;text-align:center}
  .g2,.g3,.g4{grid-template-columns:1fr}
  .hero-btns{flex-direction:column}
  .hero-btns .btn{text-align:center;justify-content:center}
}
</style>
</head>
<body>

<noscript>
  <style>.pg{display:block!important}nav{position:static}</style>
  <div style="padding:.8rem 1.5rem;background:#1a1f2e;color:#e2e8f0;text-align:center;font-size:.85rem;border-bottom:1px solid #1e2736;">
    ⚠️ JavaScript est désactivé — la navigation et les formulaires peuvent ne pas fonctionner correctement.
  </div>
</noscript>

<!-- =================== NAV =================== -->
<nav id="nav">
  <div class="nav-logo">
    <img src="data:image/png;base64,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" alt="Abner Moctar Logo" style="height:36px;width:auto;border-radius:0;border:none;background:transparent;">
    <span>Abner Moctar</span>
  </div>
  <div class="nav-links" id="navLinks">
    <a id="lnk-home" class="act" onclick="goTo('home')">Accueil</a>
    <a id="lnk-blog" onclick="goTo('blog')">Blog</a>
    <a id="lnk-services" onclick="goTo('services')">Services & Tarifs</a>
    <a id="lnk-contact" onclick="goTo('contact')">Contact</a>
    <a class="nav-btn" onclick="goTo('questionnaire')">Démarrer un projet</a>
  </div>
  <div class="ham" id="ham" onclick="toggleNav()">
    <span></span><span></span><span></span>
  </div>
</nav>


<!-- =================== HOME =================== -->
<div class="pg on" id="pg-home">

  <!-- Hero -->
  <div class="hero" style="display:flex;align-items:center;gap:3rem;justify-content:space-between;">
    <div style="max-width:580px;flex:1">
      <div class="hero-badge">Développeur Web · Niger & International</div>
      <h1>Je crée des sites web qui <em>transforment</em> votre business</h1>
      <p>Des sites professionnels, rapides et optimisés pour attirer des clients et développer votre présence en ligne.</p>
      <div class="hero-btns">
        <button class="btn btn-g" onclick="goTo('questionnaire')">Démarrer mon projet →</button>
        <button class="btn btn-o" onclick="goTo('services')">Voir les tarifs</button>
      </div>
    </div>
    <div style="flex-shrink:0;display:flex;align-items:center;justify-content:center;" class="hero-photo-wrap">
      <div style="position:relative;">
        <div style="width:280px;height:320px;border-radius:24px;overflow:hidden;border:2px solid var(--green);box-shadow:0 20px 60px rgba(0,200,150,0.15);">
          <img src="data:image/jpeg;base64,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" alt="Abner Moctar — Développeur Web" style="width:100%;height:100%;object-fit:cover;object-position:center top;">
        </div>
        <div style="position:absolute;bottom:-12px;left:50%;transform:translateX(-50%);background:var(--green);color:#08090d;padding:.3rem .9rem;border-radius:50px;font-size:.72rem;font-weight:800;white-space:nowrap;">Disponible ✓</div>
      </div>
    </div>
  </div>

  <!-- Stats -->
  <div class="stats">
    <div class="stats-inner">
      <div><div class="stat-n">15+</div><div class="stat-l">Projets livrés</div></div>
      <div><div class="stat-n">100%</div><div class="stat-l">Clients satisfaits</div></div>
      <div><div class="stat-n">3</div><div class="stat-l">Pays servis</div></div>
      <div><div class="stat-n">48h</div><div class="stat-l">Délai de réponse</div></div>
    </div>
  </div>

  <!-- Projets -->
  <div class="sect">
    <div class="tag">Réalisations</div>
    <h2 class="ttl">Projets sélectionnés</h2>
    <p class="sub">Des solutions sur mesure pour des entreprises qui veulent se démarquer en ligne.</p>
    <div class="proj-grid">
      <div class="proj-card">
        <div class="proj-img t1">🍽️</div>
        <div class="proj-body">
          <div class="proj-tags"><span class="ptag">Site vitrine</span><span class="ptag b">SEO</span></div>
          <h3>Sahel Lounge — Niamey</h3>
          <p>Site vitrine avec menu en ligne, galerie et formulaire de réservation. +60% de réservations en 3 mois.</p>
          <span class="proj-link">Voir le projet →</span>
        </div>
      </div>
      <div class="proj-card">
        <div class="proj-img t2">🏢</div>
        <div class="proj-body">
          <div class="proj-tags"><span class="ptag">Site corporate</span><span class="ptag gold">Premium</span></div>
          <h3>ORION Consulting</h3>
          <p>Site corporate avec espace client sécurisé et prise de rendez-vous en ligne pour cabinet stratégique.</p>
          <span class="proj-link">Voir le projet →</span>
        </div>
      </div>
      <div class="proj-card">
        <div class="proj-img t3">👗</div>
        <div class="proj-body">
          <div class="proj-tags"><span class="ptag">E-commerce</span></div>
          <h3>Aïcha Mode — Boutique</h3>
          <p>Boutique en ligne avec catalogue produits, paiement et gestion des commandes intégrée.</p>
          <span class="proj-link">Voir le projet →</span>
        </div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Compétences -->
  <div class="sect">
    <div class="tag">Expertises</div>
    <h2 class="ttl">Ce que je maîtrise</h2>
    <p class="sub">Des technologies modernes pour des sites performants et durables.</p>
    <div class="skill-grid">
      <div class="sk-card"><div class="sk-icon">⚡</div><h4>Développement Web</h4><p>HTML5, CSS3, JavaScript — des sites rapides et accessibles sur tous les appareils.</p></div>
      <div class="sk-card"><div class="sk-icon">📱</div><h4>Design Responsive</h4><p>Parfaitement adapté mobile, tablette et desktop. 70% des visites viennent du mobile.</p></div>
      <div class="sk-card"><div class="sk-icon">🔍</div><h4>Référencement SEO</h4><p>Optimisation pour Google afin que vos clients vous trouvent avant vos concurrents.</p></div>
      <div class="sk-card"><div class="sk-icon">🛒</div><h4>E-commerce</h4><p>Boutiques avec paiement sécurisé, gestion de stock et tableau de bord admin.</p></div>
      <div class="sk-card"><div class="sk-icon">🎨</div><h4>UI/UX Design</h4><p>Interfaces intuitives qui inspirent confiance et convertissent les visiteurs en clients.</p></div>
      <div class="sk-card"><div class="sk-icon">🔧</div><h4>Maintenance & Support</h4><p>Suivi régulier, mises à jour sécurité et accompagnement après mise en ligne.</p></div>
    </div>
  </div>

  <!-- Témoignages -->
  <div style="background:var(--card);border-top:1px solid var(--border);border-bottom:1px solid var(--border)">
    <div class="sect">
      <div class="tag">Témoignages</div>
      <h2 class="ttl">Ce que disent mes clients</h2>
      <div class="test-grid">
        <div class="test-card">
          <div class="stars">★★★★★</div>
          <p>Abner a compris exactement ce dont j'avais besoin. Un site qui dépasse mes attentes. Mes clients adorent le design !</p>
          <div class="test-auth"><div class="auth-av">MA</div><div class="auth-name"><strong>Moussa Abdou</strong><span>Sahel Lounge</span></div></div>
        </div>
        <div class="test-card">
          <div class="stars">★★★★★</div>
          <p>Très professionnel et réactif. Mon site est en ligne en moins de 2 semaines, optimisé pour Google et les demandes arrivent.</p>
          <div class="test-auth"><div class="auth-av">SK</div><div class="auth-name"><strong>Sarah Koné</strong><span>Aïcha Mode</span></div></div>
        </div>
        <div class="test-card">
          <div class="stars">★★★★★</div>
          <p>Investissement rentabilisé en 2 mois. Notre site génère plus de leads que toutes nos actions marketing réunies.</p>
          <div class="test-auth"><div class="auth-av">OI</div><div class="auth-name"><strong>Omar Issoufou</strong><span>ORION Consulting</span></div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- Pourquoi moi -->
  <div class="sect">
    <div class="tag">Pourquoi moi</div>
    <h2 class="ttl">Une relation de confiance, pas juste un site</h2>
    <p class="sub">Je ne livre pas juste un site web — je m'investis dans la réussite de votre entreprise.</p>
    <div class="why-grid">
      <div class="why-card"><div class="why-icon">👂</div><h4>Écoute attentive</h4><p>Je prends le temps de comprendre votre activité avant de commencer.</p></div>
      <div class="why-card"><div class="why-icon">💰</div><h4>Budget adapté</h4><p>Des solutions professionnelles adaptées à la réalité des entreprises africaines.</p></div>
      <div class="why-card"><div class="why-icon">🚀</div><h4>Livraison rapide</h4><p>Sites livrés en 7 à 21 jours selon la complexité.</p></div>
      <div class="why-card"><div class="why-icon">🤝</div><h4>Accompagnement</h4><p>Disponible après la mise en ligne pour vous aider à tirer le meilleur de votre site.</p></div>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta-box" style="padding:1.5rem">
    <div class="cta-box" style="margin:0">
      <h2>Prêt à développer votre présence en ligne ?</h2>
      <p>Répondez à 20 questions en 5 minutes — je prépare une proposition personnalisée gratuitement.</p>
      <button class="btn btn-g" onclick="goTo('questionnaire')">Démarrer le questionnaire gratuit →</button>
    </div>
  </div>

  <footer>
    <div class="foot-grid">
      <div class="foot-brand">
        <h4>Abner — Développeur Web</h4>
        <p>Création de sites web professionnels pour entreprises au Niger et à l'international.</p>
        <div class="foot-links">
          <a href="https://wa.me/22782392912">WhatsApp →</a>
          <a href="mailto:abner201p@gmail.com">Email →</a>
        </div>
      </div>
      <div class="foot-col">
        <h5>Navigation</h5>
        <ul>
          <li><a onclick="goTo('home')">Accueil</a></li>
          <li><a onclick="goTo('services')">Services & Tarifs</a></li>
          <li><a onclick="goTo('blog')">Blog</a></li>
          <li><a onclick="goTo('contact')">Contact</a></li>
        </ul>
      </div>
      <div class="foot-col">
        <h5>Services</h5>
        <ul>
          <li><a onclick="goTo('services')">Site vitrine</a></li>
          <li><a onclick="goTo('services')">E-commerce</a></li>
          <li><a onclick="goTo('services')">SEO</a></li>
          <li><a onclick="goTo('questionnaire')">Démarrer un projet</a></li>
        </ul>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© 2026 Abner — Développeur Web Professionnel au Niger</span>
      <span>Fait avec ❤️ à Niamey</span>
    </div>
  </footer>
</div>


<!-- =================== BLOG =================== -->
<div class="pg" id="pg-blog">
  <!-- Liste articles -->
  <div id="blog-list">
    <div class="blog-top">
      <div class="tag">Blog</div>
      <h1>Ressources & Conseils Web</h1>
      <p style="color:var(--muted);font-size:.95rem;max-width:520px">Des articles pratiques pour comprendre l'importance du digital et aider votre entreprise à se développer en ligne.</p>
    </div>
    <div class="blog-grid">
      <div class="blog-card" onclick="openArticle(0)">
        <div class="blog-thumb t1">🌍</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Stratégie digitale</span><span>8 min</span></div>
          <h3>Pourquoi les entreprises nigériennes ont absolument besoin d'un site web en 2026</h3>
          <p>Le marché change. Vos clients cherchent en ligne avant d'acheter. Voici pourquoi ne pas avoir de site vous coûte des clients chaque jour.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
      <div class="blog-card" onclick="openArticle(1)">
        <div class="blog-thumb t2">💼</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Cas concrets</span><span>6 min</span></div>
          <h3>Comment un site web peut transformer une petite entreprise au Niger</h3>
          <p>Restaurant, boutique, agence — des exemples concrets de transformation digitale et les résultats obtenus.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
      <div class="blog-card" onclick="openArticle(2)">
        <div class="blog-thumb t3">⚠️</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Bonnes pratiques</span><span>7 min</span></div>
          <h3>Les 7 erreurs que font les entreprises africaines avec leur site web</h3>
          <p>Site trop lent, non adapté au mobile, pas de SEO... Ces erreurs coûtent cher. Apprenez à les éviter.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
      <div class="blog-card" onclick="openArticle(3)">
        <div class="blog-thumb t4">🛠️</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Création web</span><span>9 min</span></div>
          <h3>Comment créer un site web professionnel qui attire des clients</h3>
          <p>Design, vitesse, SEO, UX, confiance — les 5 piliers d'un site qui convertit des visiteurs en clients.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
      <div class="blog-card" onclick="openArticle(4)">
        <div class="blog-thumb t5">🔮</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Vision</span><span>7 min</span></div>
          <h3>L'avenir du digital au Niger : pourquoi les entreprises doivent se digitaliser</h3>
          <p>L'Afrique est en pleine transformation digitale. Les entreprises qui s'y préparent maintenant prendront une avance décisive.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
      <div class="blog-card" onclick="openArticle(5)">
        <div class="blog-thumb t6">💰</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Budget & Tarifs</span><span>6 min</span></div>
          <h3>Combien coûte un site web au Niger et pourquoi c'est un investissement</h3>
          <p>Comprenez la différence entre un site amateur et professionnel, et pourquoi investir change tout.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
      <div class="blog-card" onclick="openArticle(6)">
        <div class="blog-thumb t7">🤝</div>
        <div class="blog-body">
          <div class="blog-meta"><span class="cat">Guide pratique</span><span>5 min</span></div>
          <h3>Comment choisir un bon développeur web au Niger</h3>
          <p>Les critères essentiels, les questions à poser et les pièges à éviter pour trouver le bon partenaire.</p>
          <span class="blog-more">Lire l'article →</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Article ouvert -->
  <div id="art-wrap">
    <button class="art-back" onclick="closeArticle()">← Retour au blog</button>
    <div class="blog-meta" id="art-meta"></div>
    <h1 id="art-title"></h1>
    <p class="art-intro" id="art-intro"></p>
    <div class="art-body" id="art-body"></div>
    <div class="art-cta">
      <h3>Vous avez un projet web ?</h3>
      <p>Démarrez gratuitement avec notre questionnaire de découverte.</p>
      <button class="btn btn-g" onclick="goTo('questionnaire')">Démarrer le questionnaire →</button>
    </div>
  </div>

  <footer>
    <div class="foot-bottom">
      <span>© 2026 Abner — Développeur Web Professionnel au Niger</span>
      <a onclick="goTo('home')" style="cursor:pointer;color:var(--muted)">Retour à l'accueil</a>
    </div>
  </footer>
</div>


<!-- =================== SERVICES =================== -->
<div class="pg" id="pg-services">
  <div class="serv-top">
    <div class="tag">Tarifs</div>
    <h1>Services & Tarifs transparents</h1>
    <p style="color:var(--muted);font-size:.95rem;max-width:520px">Des offres claires pour chaque étape de votre développement. Tarifs locaux (FCFA) et internationaux (€).</p>
  </div>

  <div class="price-grid">
    <!-- Essentiel -->
    <div class="price-card">
      <div class="price-icon">💻</div>
      <h3>Essentiel</h3>
      <p class="price-desc">Pour les entrepreneurs qui veulent une présence en ligne simple et professionnelle.</p>
      <div class="price-lbl">Clients locaux</div>
      <div class="price-row"><span class="price-amt">120 000</span><span class="price-cur">FCFA</span></div>
      <div class="price-lbl" style="margin-top:.5rem">Clients internationaux</div>
      <div class="price-row"><span class="price-amt">400</span><span class="price-cur">€</span></div>
      <div class="price-note">Entretien annuel : 40 000 FCFA / 100 €</div>
      <div class="feat-list">
        <div class="feat-item"><span class="ck">✓</span>3 à 4 pages</div>
        <div class="feat-item"><span class="ck">✓</span>Design professionnel</div>
        <div class="feat-item"><span class="ck">✓</span>Site responsive (mobile/tablette)</div>
        <div class="feat-item"><span class="ck">✓</span>Formulaire de contact</div>
        <div class="feat-item"><span class="ck">✓</span>Intégration réseaux sociaux</div>
      </div>
      <button class="card-btn card-btn-o" onclick="goTo('questionnaire')">Choisir cette offre</button>
    </div>

    <!-- Professionnel -->
    <div class="price-card best">
      <div class="best-badge">⭐ La plus choisie</div>
      <div class="price-icon">🌐</div>
      <h3>Professionnel</h3>
      <p class="price-desc">Pour les entreprises qui veulent développer leur visibilité et attirer des clients en ligne.</p>
      <div class="price-lbl">Clients locaux</div>
      <div class="price-row"><span class="price-amt">240 000</span><span class="price-cur">FCFA</span></div>
      <div class="price-lbl" style="margin-top:.5rem">Clients internationaux</div>
      <div class="price-row"><span class="price-amt">800</span><span class="price-cur">€</span></div>
      <div class="price-note">Entretien annuel : 70 000 FCFA / 180 €</div>
      <div class="feat-list">
        <div class="feat-item"><span class="ck">✓</span>5 à 7 pages</div>
        <div class="feat-item"><span class="ck">✓</span>Design personnalisé</div>
        <div class="feat-item"><span class="ck">✓</span>Optimisation SEO de base</div>
        <div class="feat-item"><span class="ck">✓</span>Blog ou section actualités</div>
        <div class="feat-item"><span class="ck">✓</span>Formulaire de contact avancé</div>
        <div class="feat-item"><span class="ck">✓</span>Connexion réseaux sociaux</div>
      </div>
      <button class="card-btn card-btn-g" onclick="goTo('questionnaire')">Choisir cette offre</button>
    </div>

    <!-- Business -->
    <div class="price-card">
      <div class="price-icon">🚀</div>
      <h3>Business</h3>
      <p class="price-desc">Pour les entreprises qui veulent vendre en ligne ou automatiser leurs services.</p>
      <div class="price-lbl">Clients locaux</div>
      <div class="price-row"><span class="price-amt">450 000</span><span class="price-cur">FCFA</span></div>
      <div class="price-lbl" style="margin-top:.5rem">Clients internationaux</div>
      <div class="price-row"><span class="price-amt">1 500</span><span class="price-cur">€</span></div>
      <div class="price-note">Entretien annuel : 100 000 FCFA / 300 €</div>
      <div class="feat-list">
        <div class="feat-item"><span class="ck">✓</span>Jusqu'à 10 pages</div>
        <div class="feat-item"><span class="ck">✓</span>Design premium</div>
        <div class="feat-item"><span class="ck">✓</span>SEO avancé</div>
        <div class="feat-item"><span class="ck">✓</span>Intégration marketing</div>
        <div class="feat-item"><span class="ck">✓</span>Boutique ou réservation en ligne</div>
        <div class="feat-item"><span class="ck">✓</span>Tableau de bord administrateur</div>
      </div>
      <button class="card-btn card-btn-o" onclick="goTo('questionnaire')">Choisir cette offre</button>
    </div>
  </div>

  <!-- Addons -->
  <div style="padding:0 1.5rem 1rem;max-width:1160px;margin:0 auto">
    <h2 style="font-size:1.3rem;font-weight:700;margin-bottom:1.2rem">Services complémentaires</h2>
  </div>
  <div class="addon-grid">
    <div class="addon"><div class="addon-ic">🔍</div><div><strong>SEO Avancé</strong><div class="addon-price">100 000 – 300 000 FCFA</div><div class="addon-desc">Audit complet + optimisation pour dominer Google.</div></div></div>
    <div class="addon"><div class="addon-ic">✍️</div><div><strong>Rédaction articles SEO</strong><div class="addon-price">20 000 FCFA / article · 40 € / article</div><div class="addon-desc">Articles optimisés pour attirer du trafic.</div></div></div>
    <div class="addon"><div class="addon-ic">🔧</div><div><strong>Maintenance mensuelle</strong><div class="addon-price">15 000 FCFA / mois</div><div class="addon-desc">Mises à jour, sécurité et support technique.</div></div></div>
    <div class="addon"><div class="addon-ic">🎨</div><div><strong>Logo & Identité visuelle</strong><div class="addon-price">50 000 – 120 000 FCFA</div><div class="addon-desc">Création de votre identité de marque.</div></div></div>
    <div class="addon"><div class="addon-ic">🌐</div><div><strong>Nom de domaine</strong><div class="addon-price">10 000 – 15 000 FCFA / an</div><div class="addon-desc">Enregistrement et gestion de votre domaine.</div></div></div>
    <div class="addon"><div class="addon-ic">☁️</div><div><strong>Hébergement web</strong><div class="addon-price">25 000 – 60 000 FCFA / an</div><div class="addon-desc">Serveurs rapides et fiables.</div></div></div>
  </div>

  <!-- Pourquoi moi -->
  <div style="background:var(--card);border-top:1px solid var(--border);border-bottom:1px solid var(--border)">
    <div class="sect">
      <div class="tag">Pourquoi me choisir</div>
      <h2 class="ttl">Pourquoi travailler avec moi ?</h2>
      <div class="why-grid">
        <div class="why-card"><div class="why-icon">👂</div><h4>Écoute attentive</h4><p>Chaque projet commence par comprendre votre activité.</p></div>
        <div class="why-card"><div class="why-icon">💡</div><h4>Solutions adaptées</h4><p>Toujours adaptées à votre budget et vos besoins réels.</p></div>
        <div class="why-card"><div class="why-icon">🎯</div><h4>Design moderne</h4><p>Des designs actuels qui inspirent confiance.</p></div>
        <div class="why-card"><div class="why-icon">🤝</div><h4>Relation long terme</h4><p>Je privilégie une relation de confiance durable.</p></div>
      </div>
    </div>
  </div>

  <div style="padding:2.5rem 1.5rem 3rem;max-width:1160px;margin:0 auto">
    <div class="cta-box" style="margin:0">
      <h2>Vous ne savez pas quelle offre choisir ?</h2>
      <p>Remplissez le questionnaire et je vous recommande la meilleure solution.</p>
      <button class="btn btn-g" onclick="goTo('questionnaire')">Remplir le questionnaire gratuit →</button>
    </div>
  </div>

  <footer>
    <div class="foot-bottom">
      <span>© 2026 Abner — Développeur Web Professionnel au Niger</span>
      <a onclick="goTo('home')" style="cursor:pointer;color:var(--muted)">Retour à l'accueil</a>
    </div>
  </footer>
</div>


<!-- =================== CONTACT =================== -->
<div class="pg" id="pg-contact">
  <div class="sect" style="padding-top:5.5rem">
    <div class="tag">Contact</div>
    <h1 style="font-size:clamp(1.8rem,5vw,2.8rem);font-weight:700;margin-bottom:.8rem">Parlons de votre projet</h1>
    <p style="color:var(--muted);margin-bottom:2.5rem;max-width:480px">Une question ou un devis ? Je réponds en 24 à 48h. WhatsApp pour une réponse rapide.</p>

    <div class="contact-wrap">
      <div class="contact-info">
        <h3>Me contacter directement</h3>
        <p>Plusieurs façons de me joindre selon votre préférence.</p>
        <div class="c-links">
          <a href="https://wa.me/22782392912" class="c-link">
            <div class="c-link-ic">📱</div>
            <div><strong>WhatsApp</strong><span>+227 82 39 29 12 — Réponse rapide</span></div>
          </a>
          <a href="mailto:abner201p@gmail.com" class="c-link">
            <div class="c-link-ic">✉️</div>
            <div><strong>Email</strong><span>abner201p@gmail.com</span></div>
          </a>
          <div class="c-link" onclick="goTo('questionnaire')">
            <div class="c-link-ic">📋</div>
            <div><strong>Questionnaire projet</strong><span>Pour un devis précis et personnalisé</span></div>
          </div>
        </div>
      </div>

      <div>
        <h3 style="font-size:1.1rem;font-weight:700;margin-bottom:1.2rem">Envoyer un message</h3>
        <form id="contactForm" class="form-wrap" onsubmit="sendContact(event)">
          <div class="frow">
            <div class="fg"><label>Votre prénom *</label><input type="text" name="name" placeholder="Ex: Moussa" required></div>
            <div class="fg"><label>Email ou WhatsApp *</label><input type="text" name="contact" placeholder="votre@email.com" required></div>
          </div>
          <div class="fg">
            <label>Sujet</label>
            <select name="subject">
              <option value="">Sélectionnez un sujet</option>
              <option>Demande de devis</option>
              <option>Question sur un service</option>
              <option>Autre</option>
            </select>
          </div>
          <div class="fg"><label>Votre message *</label><textarea name="message" placeholder="Décrivez votre question ou projet..." required></textarea></div>
          <button type="submit" class="btn btn-g" style="width:100%;justify-content:center">Envoyer le message →</button>
          <div class="success" id="contactOk">✓ Message envoyé ! Je vous réponds sous 24-48h.</div>
        </form>
      </div>
    </div>
  </div>

  <footer>
    <div class="foot-bottom">
      <span>© 2026 Abner — Développeur Web Professionnel au Niger</span>
      <a onclick="goTo('home')" style="cursor:pointer;color:var(--muted)">Retour à l'accueil</a>
    </div>
  </footer>
</div>


<!-- =================== QUESTIONNAIRE =================== -->
<div class="pg" id="pg-questionnaire">
  <div class="q-wrap">
    <div class="q-head">
      <div class="tag">Questionnaire projet</div>
      <h1>Parlez-moi de votre projet</h1>
      <p>Répondez à ces 20 questions (5 min) — je vous prépare une proposition personnalisée et gratuite sous 48h.</p>
    </div>

    <div class="progress"><div class="prog-fill" id="progFill"></div></div>

    <form id="projForm" onsubmit="sendQuestionnaire(event)">

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">1</span>Informations générales</div>
        <div class="q-fields">
          <div class="fg"><label>1. Nom de votre entreprise ou projet *</label><input type="text" name="q1" placeholder="Ex: Sahel Lounge" required></div>
          <div class="fg"><label>2. Activité principale *</label><input type="text" name="q2" placeholder="Ex: Restaurant, boutique, cabinet de conseil..." required></div>
          <div class="fg"><label>3. Qui sont vos clients cibles ?</label><input type="text" name="q3" placeholder="Ex: Professionnels 25-45 ans à Niamey..."></div>
          <div class="fg"><label>4. Principaux concurrents ?</label><input type="text" name="q4" placeholder="Ex: noms de concurrents ou sites similaires"></div>
        </div>
      </div>

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">2</span>Objectifs du site</div>
        <div class="q-fields">
          <div class="fg">
            <label>5. Objectif principal du site web *</label>
            <select name="q5" required>
              <option value="">Sélectionnez</option>
              <option>Vendre des produits ou services en ligne</option>
              <option>Présenter mon activité et attirer des clients</option>
              <option>Générer des contacts et des demandes</option>
              <option>Informer et fidéliser mes clients existants</option>
              <option>Autre</option>
            </select>
          </div>
          <div class="fg"><label>6. Quels résultats souhaitez-vous obtenir ?</label><textarea name="q6" placeholder="Ex: Augmenter mes ventes, être trouvé sur Google..."></textarea></div>
          <div class="fg"><label>7. Quels problèmes le site doit-il résoudre ?</label><textarea name="q7" placeholder="Ex: Les gens ne savent pas que j'existe..."></textarea></div>
        </div>
      </div>

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">3</span>Contenu du site</div>
        <div class="q-fields">
          <div class="fg"><label>8. Quelles pages souhaitez-vous ?</label><input type="text" name="q8" placeholder="Ex: Accueil, Services, À propos, Contact..."></div>
          <div class="fg">
            <label>9. Avez-vous déjà les textes et images ?</label>
            <select name="q9">
              <option value="">Sélectionnez</option>
              <option>Oui, j'ai tout le contenu prêt</option>
              <option>J'ai une partie du contenu</option>
              <option>Non, j'aurai besoin d'aide</option>
            </select>
          </div>
          <div class="fg">
            <label>10. Souhaitez-vous un blog ?</label>
            <select name="q10">
              <option value="">Sélectionnez</option>
              <option>Oui</option>
              <option>Non</option>
              <option>Peut-être, à voir</option>
            </select>
          </div>
        </div>
      </div>

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">4</span>Design & Image de marque</div>
        <div class="q-fields">
          <div class="fg">
            <label>11. Avez-vous déjà un logo ?</label>
            <select name="q11">
              <option value="">Sélectionnez</option>
              <option>Oui, j'ai un logo et une charte graphique</option>
              <option>J'ai un logo mais pas de charte</option>
              <option>Non, j'ai besoin d'un logo</option>
            </select>
          </div>
          <div class="fg"><label>12. Couleurs ou style souhaité ?</label><input type="text" name="q12" placeholder="Ex: Tons chauds, style moderne et épuré..."></div>
          <div class="fg"><label>13. Sites web que vous aimez en inspiration ?</label><input type="text" name="q13" placeholder="Ex: www.exemple.com — j'aime ce design car..."></div>
        </div>
      </div>

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">5</span>Fonctionnalités</div>
        <div class="q-fields">
          <div class="fg"><label>14. Fonctionnalités souhaitées ?</label><textarea name="q14" placeholder="Ex: Paiement en ligne, réservation, galerie photos, carte Maps..."></textarea></div>
          <div class="fg">
            <label>15. Souhaitez-vous modifier vous-même le contenu ?</label>
            <select name="q15">
              <option value="">Sélectionnez</option>
              <option>Oui, je veux pouvoir modifier facilement</option>
              <option>Non, je ferai appel à vous pour les mises à jour</option>
              <option>Je ne sais pas encore</option>
            </select>
          </div>
        </div>
      </div>

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">6</span>Technique & Marketing</div>
        <div class="q-fields">
          <div class="fg">
            <label>16. Avez-vous un nom de domaine et hébergement ?</label>
            <select name="q16">
              <option value="">Sélectionnez</option>
              <option>Oui, j'ai les deux</option>
              <option>J'ai seulement un nom de domaine</option>
              <option>Non, j'ai besoin d'aide pour ça</option>
            </select>
          </div>
          <div class="fg">
            <label>17. Le site doit-il être optimisé pour Google (SEO) ?</label>
            <select name="q17">
              <option value="">Sélectionnez</option>
              <option>Oui, c'est important pour moi</option>
              <option>Non, pas pour l'instant</option>
              <option>Je ne comprends pas encore le SEO</option>
            </select>
          </div>
          <div class="fg">
            <label>18. Connecter le site aux réseaux sociaux ?</label>
            <select name="q18">
              <option value="">Sélectionnez</option>
              <option>Oui (Facebook, Instagram, etc.)</option>
              <option>Non</option>
            </select>
          </div>
        </div>
      </div>

      <div class="q-section">
        <div class="q-stitle"><span class="q-num">7</span>Organisation du projet</div>
        <div class="q-fields">
          <div class="fg">
            <label>19. Budget approximatif ?</label>
            <select name="q19">
              <option value="">Sélectionnez</option>
              <option>Moins de 120 000 FCFA (400 €)</option>
              <option>120 000 – 240 000 FCFA (400–800 €)</option>
              <option>240 000 – 450 000 FCFA (800–1500 €)</option>
              <option>Plus de 450 000 FCFA (1500 €+)</option>
              <option>Pas encore défini</option>
            </select>
          </div>
          <div class="fg">
            <label>20. Délai souhaité pour la mise en ligne ?</label>
            <select name="q20">
              <option value="">Sélectionnez</option>
              <option>Le plus vite possible (urgent)</option>
              <option>Dans les 2 semaines</option>
              <option>Dans le mois</option>
              <option>Dans 2 à 3 mois</option>
              <option>Pas de délai précis</option>
            </select>
          </div>
          <div class="fg"><label>Email ou WhatsApp pour vous recontacter *</label><input type="text" name="contact" placeholder="votre@email.com ou +227..." required></div>
        </div>
      </div>

      <div class="q-submit">
        <button type="submit" class="btn btn-g" style="width:100%;justify-content:center;font-size:1rem;padding:.95rem">
          Envoyer mon questionnaire →
        </button>
        <p class="q-hint">Proposition personnalisée sous 48h. Gratuit, sans engagement.</p>
        <div class="success" id="projOk" style="justify-content:center;margin-top:1rem">
          ✓ Questionnaire envoyé ! Je vous contacte sous 48h avec une proposition personnalisée.
        </div>
      </div>

    </form>
  </div>

  <footer>
    <div class="foot-bottom">
      <span>© 2026 Abner — Développeur Web Professionnel au Niger</span>
      <a onclick="goTo('home')" style="cursor:pointer;color:var(--muted)">Retour à l'accueil</a>
    </div>
  </footer>
</div>


<!-- =================== JAVASCRIPT =================== -->
<script>
// ===== NAVIGATION =====
function goTo(page) {
  // Cache toutes les pages
  document.querySelectorAll('.pg').forEach(function(p){ p.classList.remove('on'); });
  // Affiche la bonne
  var el = document.getElementById('pg-' + page);
  if(el) el.classList.add('on');

  // Met à jour les liens actifs
  document.querySelectorAll('.nav-links a[id^=lnk-]').forEach(function(a){ a.classList.remove('act'); });
  var lnk = document.getElementById('lnk-' + page);
  if(lnk) lnk.classList.add('act');

  // Ferme le menu mobile
  document.getElementById('navLinks').classList.remove('open');

  // Reset blog si on revient
  if(page === 'blog'){
    document.getElementById('blog-list').style.display = 'block';
    document.getElementById('art-wrap').style.display = 'none';
  }

  window.scrollTo(0, 0);
}

// ===== MENU MOBILE =====
function toggleNav() {
  document.getElementById('navLinks').classList.toggle('open');
}

// ===== DONNÉES ARTICLES =====
var articles = [
  {
    cat: 'Stratégie digitale', time: '8 min de lecture',
    title: 'Pourquoi les entreprises nigériennes ont absolument besoin d\'un site web en 2026',
    intro: 'Le marché change profondément. Vos clients cherchent des informations en ligne avant même de sortir de chez eux. Sans site web, vous êtes invisible à ceux qui ont le plus d\'argent à dépenser.',
    body: '<h2>La réalité du marché nigérien en 2026</h2><p>Aujourd\'hui, lorsqu\'un entrepreneur à Niamey cherche un comptable, un consultant ou un restaurateur, son premier réflexe est de sortir son smartphone. L\'accès à internet au Niger a explosé ces cinq dernières années, porté par la progression de la 4G et l\'essor des smartphones moins chers. Pourtant, la grande majorité des entreprises locales n\'ont toujours pas de présence en ligne.</p><h2>Pourquoi beaucoup d\'entreprises ne sont pas en ligne</h2><p>Les raisons sont compréhensibles : perception que c\'est trop cher, méconnaissance des outils, sentiment que cela ne marche pas pour elles. Certains pensent que les réseaux sociaux suffisent.</p><ul><li>Idée reçue que les sites web sont réservés aux grandes entreprises</li><li>Manque d\'information sur les coûts réels, qui ont fortement baissé</li><li>Confusion entre présence sur Facebook et vrai site professionnel</li><li>Absence de développeurs web accessibles et locaux</li></ul><div class="art-callout"><p>Plus de 60% des consommateurs urbains recherchent un service en ligne avant de l\'acheter. Votre absence sur le web est une opportunité offerte directement à vos concurrents.</p></div><h2>Les opportunités perdues sans site web</h2><p>Sans site web, vous ne pouvez pas être trouvé sur Google. Vous ne pouvez pas présenter vos services 24h/24. Vous ne pouvez pas recevoir des demandes pendant que vous dormez. Et vous ne pouvez pas vous adresser aux clients qui recherchent des prestataires fiables en ligne.</p><ul><li>Clients potentiels qui passent chez le concurrent qui a un site</li><li>Impossibilité d\'accéder aux marchés hors du Niger</li><li>Image moins professionnelle comparée aux concurrents en ligne</li><li>Dépendance totale au bouche à oreille</li></ul><h2>Comment un site web augmente vos ventes</h2><p>Un site web bien conçu travaille pour vous 7j/7, 24h/24. Il présente vos services, répond aux questions fréquentes, montre vos réalisations et incite les visiteurs à vous contacter. Plusieurs entreprises nigériennes ont multiplié leurs demandes par deux ou trois dans les six premiers mois après la mise en ligne.</p>'
  },
  {
    cat: 'Cas concrets', time: '6 min de lecture',
    title: 'Comment un site web peut transformer une petite entreprise au Niger',
    intro: 'Restaurant, boutique, agence ou entrepreneur solo — des exemples concrets de transformation digitale et les résultats obtenus en quelques semaines seulement.',
    body: '<h2>Le restaurant qui a doublé ses réservations</h2><p>Prenons l\'exemple d\'un restaurant familial à Niamey. Avant d\'avoir un site web, tous ses clients venaient par recommandation ou par hasard. La salle était souvent à moitié vide en semaine.</p><p>Après la création d\'un site vitrine avec menu en ligne, galerie photo et formulaire de réservation, les résultats ont été immédiats. En trois mois, les réservations du week-end affichaient complet une semaine à l\'avance. Des clients d\'autres quartiers et même des expatriés avaient trouvé le restaurant via Google.</p><h2>La boutique qui vend maintenant dans tout le pays</h2><p>Une boutique de mode à Niamey était limitée par sa localisation physique. Avec un site e-commerce simple, elle a commencé à recevoir des commandes depuis d\'autres villes du Niger. Le chiffre d\'affaires a augmenté de 40% en six mois, sans employé supplémentaire.</p><div class="art-callout"><p>Un site web, c\'est votre boutique ouverte en permanence. Quand vous dormez, vos clients peuvent encore parcourir vos produits et passer commande.</p></div><h2>L\'agence qui attire des clients internationaux</h2><p>Un consultant basé à Niamey peinait à convaincre des clients internationaux sans site professionnel. Après la mise en ligne d\'un site avec portfolio, témoignages et blog, il a décroché ses premiers contrats avec des ONG et entreprises européennes.</p><h2>L\'entrepreneur solo qui reçoit des demandes automatiquement</h2><p>Un électricien indépendant passait beaucoup de temps à chercher des chantiers. Avec un simple site vitrine, il reçoit aujourd\'hui plusieurs demandes par semaine sans aucune prospection active.</p>'
  },
  {
    cat: 'Bonnes pratiques', time: '7 min de lecture',
    title: 'Les 7 erreurs que font les entreprises africaines avec leur site web',
    intro: 'Avoir un site web ne suffit pas. Un mauvais site web peut même faire fuir vos clients. Voici les 7 erreurs les plus fréquentes et comment les éviter.',
    body: '<h2>Erreur 1 : Un site trop lent</h2><p>En Afrique, beaucoup d\'internautes accèdent au web via des connexions mobiles limitées. Un site qui prend plus de 3 secondes à charger perd en moyenne 50% de ses visiteurs. Des images non optimisées ou un hébergement de mauvaise qualité peuvent ruiner même le plus beau des sites.</p><h2>Erreur 2 : Un site non adapté au mobile</h2><p>Plus de 70% des visites en Afrique subsaharienne se font depuis un smartphone. Si votre site n\'est pas responsive, vous perdez la majorité de vos visiteurs. C\'est une erreur impardonnable en 2026.</p><div class="art-callout"><p>Un site non adapté au mobile n\'est pas seulement inconfortable — Google le pénalise activement dans ses résultats de recherche. Vous perdez sur tous les fronts.</p></div><h2>Erreur 3 : Un mauvais design</h2><p>Le design est votre première impression. Un site avec des couleurs criardes ou une mise en page désordonnée renvoie une image d\'amateurisme. Vos visiteurs font un jugement en moins de 50 millisecondes.</p><h2>Erreur 4 : Aucune optimisation SEO</h2><p>Un site sans SEO est comme un magasin sans enseigne dans une ruelle sans éclairage. Votre site peut être magnifique — si personne ne le trouve sur Google, il ne vous rapportera rien.</p><h2>Erreur 5 : Pas de formulaire de contact</h2><p>Beaucoup de visiteurs préfèrent envoyer un message en ligne plutôt qu\'appeler un inconnu. L\'absence d\'un formulaire de contact fait fuir une partie significative de vos leads.</p><h2>Erreur 6 : Un contenu vague et générique</h2><p>Des phrases comme "Nous offrons des services de qualité" ne disent rien. Votre site doit clairement expliquer ce que vous faites, pour qui, comment et à quel prix.</p><h2>Erreur 7 : Un site jamais mis à jour</h2><p>Un site avec des informations datant de plusieurs années donne l\'impression que l\'entreprise n\'existe peut-être plus. Un site web doit être un outil vivant.</p>'
  },
  {
    cat: 'Création web', time: '9 min de lecture',
    title: 'Comment créer un site web professionnel qui attire des clients',
    intro: 'Un site web qui attire des clients repose sur 5 piliers fondamentaux. Voici ce que tout développeur sérieux doit maîtriser — et ce que vous devez savoir pour évaluer son travail.',
    body: '<h2>Pilier 1 : Un design qui inspire confiance</h2><p>Le design n\'est pas seulement une question d\'esthétique — c\'est une question de confiance. Un bon design professionnel utilise une palette de couleurs cohérente, des typographies lisibles et une mise en page qui guide le regard vers l\'essentiel.</p><ul><li>Couleurs cohérentes avec l\'identité de votre marque</li><li>Typographies lisibles sur tous les appareils</li><li>Hiérarchie visuelle claire qui guide l\'utilisateur</li><li>Photos et visuels de qualité professionnelle</li></ul><h2>Pilier 2 : Une vitesse de chargement optimale</h2><p>Google utilise la vitesse du site comme critère de classement. Les images doivent être compressées, le code optimisé et l\'hébergement performant. Un bon développeur vous livrera un site qui charge en moins de 2 secondes.</p><div class="art-callout"><p>Pour chaque seconde supplémentaire de chargement, vous perdez 11% de vos visiteurs. La performance n\'est pas un luxe — c\'est une nécessité commerciale.</p></div><h2>Pilier 3 : Le référencement SEO intégré dès la création</h2><p>Le SEO doit être pensé dès le départ : structure logique, titres optimisés, contenu riche et architecture technique correcte. Un site bien référencé continue de vous apporter des clients gratuitement pendant des années.</p><h2>Pilier 4 : Une expérience utilisateur intuitive</h2><p>Le menu doit être simple, les appels à l\'action visibles, et le chemin vers le formulaire de contact aussi court que possible. Chaque clic supplémentaire est une occasion de perdre un visiteur.</p><h2>Pilier 5 : Les éléments de confiance</h2><p>Témoignages clients, certifications, page "À propos" honnête, informations de contact claires — ces éléments font la différence entre un visiteur qui part et un client qui prend contact.</p>'
  },
  {
    cat: 'Vision', time: '7 min de lecture',
    title: 'L\'avenir du digital au Niger : pourquoi les entreprises doivent se digitaliser maintenant',
    intro: 'L\'Afrique vit sa révolution digitale. Les entreprises qui s\'y préparent aujourd\'hui prendront une avance décisive. Celles qui attendent risquent d\'être définitivement dépassées.',
    body: '<h2>Une révolution silencieuse en cours</h2><p>En dix ans, le taux de pénétration d\'internet en Afrique subsaharienne a été multiplié par cinq. Au Niger, la 4G s\'étend progressivement et les smartphones sont devenus accessibles à des prix toujours plus bas. Cette transformation change radicalement les comportements des consommateurs.</p><h2>Le futur du commerce en Afrique est digital</h2><p>Le commerce en ligne africain connaît une croissance annuelle à deux chiffres. La vraie opportunité se trouve dans les centaines de milliers de PME qui peuvent désormais atteindre leurs clients directement via internet, sans intermédiaire et sans les coûts d\'une présence physique étendue.</p><div class="art-callout"><p>L\'économie numérique africaine devrait représenter plusieurs milliards de dollars dans les prochaines années. Les entreprises qui se digitalisent aujourd\'hui positionnent leur avenir.</p></div><h2>Les opportunités concrètes pour les entrepreneurs</h2><ul><li>Accès aux marchés de la diaspora africaine dans le monde</li><li>Possibilité de travailler avec des entreprises internationales</li><li>Vente de produits nigériens à l\'export (artisanat, mode, alimentation)</li><li>Construction d\'une audience locale fidèle via le contenu en ligne</li></ul><h2>Pourquoi agir maintenant</h2><p>La digitalisation est un processus qui prend du temps : construire une réputation en ligne, accumuler des avis clients, améliorer son référencement. Chaque mois sans présence digitale est un mois de retard sur vos concurrents qui ont déjà commencé.</p>'
  },
  {
    cat: 'Budget & Tarifs', time: '6 min de lecture',
    title: 'Combien coûte un site web au Niger et pourquoi c\'est un investissement',
    intro: 'La question du budget est souvent le premier frein. Mais avant de regarder le coût, il faut comprendre la valeur. Un site web n\'est pas une dépense — c\'est un outil commercial qui travaille pour vous en permanence.',
    body: '<h2>Les différents types de sites et leurs coûts</h2><ul><li><strong>Site vitrine</strong> : 3 à 5 pages, présentation et formulaire de contact. 120 000 – 200 000 FCFA.</li><li><strong>Site professionnel complet</strong> : 5 à 8 pages, SEO, blog, design personnalisé. 200 000 – 350 000 FCFA.</li><li><strong>Site e-commerce</strong> : boutique en ligne, paiements. 350 000 – 600 000 FCFA.</li><li><strong>Application web sur mesure</strong> : fonctionnalités complexes. Budget sur devis.</li></ul><h2>Pourquoi un site web a de la valeur</h2><p>Calculons simplement. Si votre site vous apporte deux clients supplémentaires par mois, et que la valeur moyenne d\'un client est de 50 000 FCFA, votre site génère 100 000 FCFA mensuel. Un site à 240 000 FCFA est donc rentabilisé en 2,4 mois — et continue pendant des années.</p><div class="art-callout"><p>Un commercial humain coûte 80 000 à 150 000 FCFA par mois et ne travaille pas la nuit. Votre site web, lui, travaille 24h/24 pour un coût annuel équivalent à 1 à 2 mois de salaire.</p></div><h2>La différence entre site amateur et professionnel</h2><p>Des offres à 30 000 ou 50 000 FCFA existent. Mais derrière : template générique, aucun SEO, performances médiocres sur mobile, pas de support. Un site professionnel est un investissement sur plusieurs années, maintenu et optimisé pour convertir vos visiteurs.</p><h2>Comment financer son site</h2><p>Plusieurs entrepreneurs commencent par un site vitrine simple pour établir leur présence, puis évoluent vers une solution plus complète quand les revenus générés le permettent. C\'est une approche sage et progressive.</p>'
  },
  {
    cat: 'Guide pratique', time: '5 min de lecture',
    title: 'Comment choisir un bon développeur web au Niger',
    intro: 'Confier la création de votre site web est une décision importante. Voici les critères essentiels, les questions à poser et les pièges à éviter pour trouver le bon partenaire.',
    body: '<h2>Les critères essentiels à évaluer</h2><ul><li><strong>Portfolio vérifiable</strong> : Le développeur doit montrer des sites réels que vous pouvez visiter et tester.</li><li><strong>Maîtrise du mobile et du SEO</strong> : Non négociables en 2026. Vérifiez ses réalisations sur mobile.</li><li><strong>Clarté sur le processus</strong> : Il doit expliquer comment il travaille et ce qui est inclus dans son offre.</li><li><strong>Références clients</strong> : Des témoignages vérifiables sont un gage sérieux de qualité.</li></ul><h2>Les questions à poser avant de signer</h2><ul><li>Puis-je voir des exemples de sites que vous avez créés ?</li><li>Le site sera-t-il adapté au mobile et rapide à charger ?</li><li>Incluez-vous une optimisation SEO de base ?</li><li>Que se passe-t-il si j\'ai besoin de modifications après la livraison ?</li><li>Qui sera propriétaire du nom de domaine et du code ?</li><li>Proposez-vous une maintenance après la mise en ligne ?</li></ul><div class="art-callout"><p>Méfiez-vous des développeurs qui promettent un site en 24 heures ou des tarifs trois fois inférieurs au marché. La qualité a un coût.</p></div><h2>Les erreurs à éviter</h2><p>Ne choisissez pas uniquement sur le prix. Un site à 30 000 FCFA qui ne génère aucun client ne vaut rien, tandis qu\'un site à 240 000 FCFA qui vous rapporte des clients chaque semaine est une excellente affaire.</p><h2>Comment je travaille</h2><p>Je commence toujours par comprendre votre activité, vos clients et vos objectifs. Je soumets une proposition détaillée avant de commencer. Je livre un site optimisé pour mobile, rapide et bien référencé. Et je reste disponible après la mise en ligne pour vous accompagner.</p>'
  }
];

// ===== BLOG ARTICLE =====
function openArticle(i) {
  var a = articles[i];
  document.getElementById('art-meta').innerHTML = '<span style="color:var(--green);font-weight:600">' + a.cat + '</span>&nbsp;&nbsp;<span>' + a.time + '</span>';
  document.getElementById('art-title').textContent = a.title;
  document.getElementById('art-intro').textContent = a.intro;
  document.getElementById('art-body').innerHTML = a.body;
  document.getElementById('blog-list').style.display = 'none';
  document.getElementById('art-wrap').style.display = 'block';
  window.scrollTo(0, 0);
}

function closeArticle() {
  document.getElementById('blog-list').style.display = 'block';
  document.getElementById('art-wrap').style.display = 'none';
  window.scrollTo(0, 0);
}

// ===== PROGRESS BAR =====
function updateProgress() {
  var form = document.getElementById('projForm');
  if (!form) return;
  var req = form.querySelectorAll('input[required], select[required], textarea[required]');
  var filled = 0;
  req.forEach(function(el){ if(el.value.trim() !== '') filled++; });
  var pct = req.length ? Math.round(filled / req.length * 100) : 0;
  var bar = document.getElementById('progFill');
  if(bar) bar.style.width = pct + '%';
}
document.addEventListener('input', updateProgress);
document.addEventListener('change', updateProgress);

// ===== CONTACT FORM =====
function sendContact(e) {
  e.preventDefault();
  var form = e.target;
  var btn = form.querySelector('button[type=submit]');
  btn.textContent = 'Envoi en cours...';
  btn.disabled = true;

  var name = form.querySelector('[name=name]').value;
  var contact = form.querySelector('[name=contact]').value;
  var subject = form.querySelector('[name=subject]').value;
  var message = form.querySelector('[name=message]').value;

  var body = 'Nom: ' + name + '\nContact: ' + contact + '\nSujet: ' + subject + '\n\nMessage:\n' + message;
  var mailLink = 'mailto:abner201p@gmail.com?subject=' + encodeURIComponent('Message - ' + (subject || 'Contact')) + '&body=' + encodeURIComponent(body);

  window.location.href = mailLink;

  setTimeout(function(){
    document.getElementById('contactOk').classList.add('show');
    form.reset();
    btn.textContent = 'Envoyer le message →';
    btn.disabled = false;
  }, 500);
}

// ===== QUESTIONNAIRE FORM =====
function sendQuestionnaire(e) {
  e.preventDefault();
  var form = e.target;
  var btn = form.querySelector('button[type=submit]');
  btn.textContent = 'Envoi en cours...';
  btn.disabled = true;

  var labels = ['','Nom entreprise','Activité principale','Clients cibles','Concurrents','Objectif principal','Résultats souhaités','Problèmes à résoudre','Pages souhaitées','Contenu disponible','Blog souhaité','Logo existant','Style/couleurs','Sites inspiration','Fonctionnalités','Gestion contenu','Domaine/hébergement','SEO','Réseaux sociaux','Budget','Délai'];
  var body = 'QUESTIONNAIRE PROJET WEB\n\n';
  for(var i = 1; i <= 20; i++){
    var el = form.querySelector('[name=q'+i+']');
    body += 'Q'+i+'. '+labels[i]+': '+(el ? el.value : '')+'\n';
  }
  var contact = form.querySelector('[name=contact]');
  body += '\nContact: '+(contact ? contact.value : '');

  var q1 = form.querySelector('[name=q1]');
  var mailLink = 'mailto:abner201p@gmail.com?subject=' + encodeURIComponent('Questionnaire projet - ' + (q1 ? q1.value : 'Nouveau projet')) + '&body=' + encodeURIComponent(body);
  window.location.href = mailLink;

  setTimeout(function(){
    document.getElementById('progFill').style.width = '100%';
    document.getElementById('projOk').classList.add('show');
    btn.textContent = '✓ Questionnaire envoyé !';
  }, 600);
}

// Accessibilité clavier — active Enter/Space sur tous les éléments onclick
document.querySelectorAll('[onclick]').forEach(function(el){
  if(!el.hasAttribute('tabindex')) el.setAttribute('tabindex','0');
  el.addEventListener('keydown', function(e){
    if(e.key === 'Enter' || e.key === ' '){
      e.preventDefault();
      el.click();
    }
  });
});
</script>
</body>
</html>
