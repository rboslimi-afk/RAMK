<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>RAMK | نصنع مواقع لا تُنسى</title>
<meta name="description" content="RAMK مجموعة متخصصة في تصميم وبرمجة المواقع الاحترافية. مواقع سريعة، فخمة، ومبنية لتُبهر.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Reem+Kufi:wght@400;500;600;700&family=IBM+Plex+Sans+Arabic:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --espresso:#241209;
  --walnut:#4A2C1A;
  --caramel:#A8713F;
  --sand:#E9DCCB;
  --paper:#FFFFFF;
  --mist:#F7F2EC;
  --display:'Reem Kufi','IBM Plex Sans Arabic',serif;
  --body:'IBM Plex Sans Arabic','Segoe UI',Tahoma,sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:var(--body);background:var(--paper);color:var(--espresso);line-height:1.85;font-size:17px;-webkit-font-smoothing:antialiased;overflow-x:hidden}
a{color:inherit;text-decoration:none}
:focus-visible{outline:3px solid var(--caramel);outline-offset:3px}
.wrap{width:min(1180px,92%);margin-inline:auto}

/* NAV */
.nav{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.92);backdrop-filter:blur(10px);border-bottom:1px solid var(--sand)}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;height:72px}
.logo{font-family:var(--display);font-weight:700;font-size:1.7rem;letter-spacing:.14em;color:var(--espresso);direction:ltr}
.nav ul{display:flex;gap:34px;list-style:none;font-size:.98rem}
.nav ul a{padding:6px 0;border-bottom:2px solid transparent;transition:border-color .2s}
.nav ul a:hover{border-color:var(--caramel)}
.btn{display:inline-flex;align-items:center;gap:10px;font-family:var(--body);font-weight:600;font-size:1rem;padding:14px 30px;border-radius:2px;border:2px solid var(--espresso);cursor:pointer;transition:background .2s,color .2s,transform .2s}
.btn-dark{background:var(--espresso);color:var(--paper)}
.btn-dark:hover{background:var(--walnut);border-color:var(--walnut)}
.btn-line{background:transparent;color:var(--espresso)}
.btn-line:hover{background:var(--espresso);color:var(--paper)}
.btn-sand{background:var(--sand);border-color:var(--sand);color:var(--espresso)}
.btn-sand:hover{background:var(--paper);border-color:var(--paper)}
.nav .btn{padding:9px 20px;font-size:.92rem}

/* HERO */
.hero{position:relative;padding:90px 0 150px;overflow:hidden;background:var(--paper)}
.hero-grid{display:grid;grid-template-columns:1.05fr 1fr;gap:60px;align-items:center;position:relative;z-index:2}
.hero h1{font-family:var(--display);font-weight:700;font-size:clamp(2.6rem,6vw,4.9rem);line-height:1.25;color:var(--espresso)}
.hero h1 span{display:block;color:var(--caramel)}
.hero p.lead{margin-top:26px;max-width:34em;font-size:1.15rem;color:var(--walnut);font-weight:300}
.hero .actions{margin-top:38px;display:flex;flex-wrap:wrap;gap:14px}
.giant{position:absolute;inset-inline:0;bottom:-.24em;text-align:center;font-family:var(--display);font-weight:700;font-size:clamp(9rem,27vw,23rem);line-height:1;letter-spacing:.04em;direction:ltr;color:transparent;-webkit-text-stroke:2px var(--sand);user-select:none;pointer-events:none;z-index:1}

/* BUILD MOCKUP */
.stage{position:relative;height:440px;direction:ltr}
.win{position:absolute;background:var(--paper);border:1.5px solid var(--espresso);border-radius:6px;box-shadow:14px 14px 0 var(--sand);overflow:hidden}
.win .bar{height:30px;background:var(--espresso);display:flex;align-items:center;gap:6px;padding:0 12px}
.win .bar i{width:8px;height:8px;border-radius:50%;background:var(--caramel);display:block}
.win .bar b{margin-inline-start:auto;font:500 .7rem/1 var(--body);color:var(--sand);letter-spacing:.06em}
.w1{width:82%;height:330px;inset-inline-start:0;top:0}
.w2{width:46%;height:200px;inset-inline-end:0;bottom:0;box-shadow:10px 10px 0 var(--caramel)}
.canvas{padding:18px;display:grid;gap:12px}
.blk{background:var(--mist);border-radius:3px;opacity:0;transform:translateY(10px)}
.blk.dk{background:var(--walnut)}
.blk.cr{background:var(--caramel)}
.go .blk{animation:place .6s cubic-bezier(.2,.8,.2,1) forwards;animation-delay:calc(var(--d) * .28s + .4s)}
@keyframes place{to{opacity:1;transform:none}}
.c1{grid-template-columns:1.3fr 1fr}
.c1 .hero-b{grid-column:1/-1;height:98px}
.c1 .t1{height:14px;width:70%}
.c1 .row3{grid-column:1/-1;display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
.c1 .row3 .blk{height:76px}
.c1 .line{height:10px}
.cursor{position:absolute;inset-inline-start:52%;top:46%;width:22px;height:22px;z-index:5;opacity:0}
.go .cursor{animation:mv 3.4s .5s ease-in-out forwards}
@keyframes mv{0%{opacity:1;transform:translate(-120px,-90px)}30%{opacity:1;transform:translate(60px,20px)}60%{opacity:1;transform:translate(-40px,110px)}100%{opacity:1;transform:translate(90px,130px)}}
.cursor svg{width:100%;height:100%;fill:var(--espresso);stroke:#fff;stroke-width:1.5}
.w2 .canvas{grid-template-columns:1fr 1fr}
.w2 .blk{height:44px}
.w2 .wide{grid-column:1/-1;height:64px}

/* SECTION BASE */
section{position:relative}
.pad{padding:110px 0}
.head{max-width:640px;margin-bottom:60px}
.head h2{font-family:var(--display);font-weight:600;font-size:clamp(2rem,4vw,3rem);line-height:1.35}
.head p{margin-top:14px;color:var(--walnut);font-weight:300;font-size:1.08rem}

/* MANIFESTO (dark) */
.dark{background:var(--espresso);color:var(--paper)}
.manifesto .wrap{display:grid;grid-template-columns:1fr 1.4fr;gap:70px;align-items:start}
.manifesto h2{font-family:var(--display);font-weight:600;font-size:clamp(2rem,4vw,3.1rem);line-height:1.4}
.manifesto .txt p{font-size:1.15rem;font-weight:300;color:var(--sand);margin-bottom:22px}
.pills{display:flex;flex-wrap:wrap;gap:12px;margin-top:34px}
.pills span{border:1px solid var(--caramel);color:var(--sand);padding:8px 20px;border-radius:40px;font-size:.95rem}

/* SERVICES */
.svc{border-top:1.5px solid var(--espresso)}
.row{display:grid;grid-template-columns:90px 1.1fr 1.6fr;gap:30px;align-items:center;padding:34px 12px;border-bottom:1px solid var(--sand);transition:background .25s,padding .25s}
.row:hover,.row:focus-within{background:var(--mist);padding-inline:26px}
.row .ic{width:56px;height:56px;border:1.5px solid var(--espresso);border-radius:50%;display:grid;place-items:center;transition:background .25s}
.row:hover .ic{background:var(--espresso)}
.row:hover .ic svg{stroke:var(--sand)}
.ic svg{width:26px;height:26px;fill:none;stroke:var(--espresso);stroke-width:1.6;stroke-linecap:round;stroke-linejoin:round;transition:stroke .25s}
.row h3{font-family:var(--display);font-weight:600;font-size:1.55rem}
.row p{color:var(--walnut);font-weight:300}

/* WORK */
.work{background:var(--mist)}
.cases{display:grid;grid-template-columns:1.3fr 1fr;grid-template-rows:auto auto;gap:26px}
.case{background:var(--paper);border:1.5px solid var(--espresso);border-radius:4px;overflow:hidden;display:flex;flex-direction:column}
.case.big{grid-row:span 2}
.shot{flex:1;min-height:220px;position:relative;direction:ltr;padding:20px;display:flex;flex-direction:column;gap:10px;justify-content:center}
.shot.s1{background:var(--walnut)}
.shot.s2{background:var(--sand)}
.shot.s3{background:var(--caramel)}
.shot .nv{height:8px;width:38%;background:rgba(255,255,255,.5);border-radius:4px}
.shot.s2 .nv{background:rgba(36,18,9,.35)}
.shot .h{font-family:var(--display);font-size:2.2rem;line-height:1.1;color:var(--paper);font-weight:700}
.shot.s2 .h{color:var(--espresso)}
.shot .bt{width:110px;height:30px;background:var(--paper);border-radius:2px}
.shot.s2 .bt{background:var(--espresso)}
.shot .g{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:8px}
.shot .g i{height:64px;background:rgba(255,255,255,.18);border-radius:3px;display:block}
.info{padding:22px 26px;border-top:1.5px solid var(--espresso)}
.info h3{font-family:var(--display);font-size:1.3rem;font-weight:600}
.info p{color:var(--walnut);font-size:.95rem;font-weight:300}
.note{margin-top:26px;color:var(--walnut);font-size:.92rem}

/* PROCESS */
.steps{display:grid;grid-template-columns:repeat(4,1fr);gap:0;position:relative}
.step{padding:0 26px 0 0;position:relative}
.step:first-child{padding-right:0}
.step .n{width:52px;height:52px;border-radius:50%;background:var(--espresso);color:var(--paper);font-family:var(--display);font-size:1.25rem;display:grid;place-items:center;position:relative;z-index:2}
.steps::before{content:"";position:absolute;top:26px;inset-inline:26px;height:1.5px;background:var(--caramel);z-index:1}
.step h3{font-family:var(--display);font-weight:600;font-size:1.35rem;margin:22px 0 8px}
.step p{color:var(--walnut);font-weight:300;font-size:.98rem}

/* WHY */
.why{background:var(--espresso);color:var(--paper)}
.why .head p{color:var(--sand)}
.pillars{display:grid;grid-template-columns:repeat(3,1fr);gap:0;border:1px solid var(--walnut)}
.pillar{padding:44px 34px;border-inline-start:1px solid var(--walnut)}
.pillar:first-child{border-inline-start:0}
.pillar h3{font-family:var(--display);font-weight:600;font-size:1.5rem;color:var(--caramel);margin-bottom:12px}
.pillar p{color:var(--sand);font-weight:300}

/* CTA */
.cta{background:var(--sand)}
.cta-box{display:grid;grid-template-columns:1.3fr 1fr;gap:60px;align-items:center}
.cta h2{font-family:var(--display);font-weight:700;font-size:clamp(2.1rem,4.4vw,3.4rem);line-height:1.3}
.cta p{margin-top:16px;font-size:1.1rem;color:var(--walnut)}
.contact{background:var(--paper);border:1.5px solid var(--espresso);padding:34px;box-shadow:12px 12px 0 var(--walnut)}
.contact .btn{width:100%;justify-content:center;margin-bottom:16px}
.contact .ph{display:flex;justify-content:space-between;align-items:center;padding-top:18px;border-top:1px solid var(--sand);font-size:1rem}
.contact .ph a{font-family:var(--display);font-size:1.4rem;letter-spacing:.06em;direction:ltr}
.wa{width:22px;height:22px;fill:currentColor}

/* FOOTER */
footer{background:var(--espresso);color:var(--sand);padding:50px 0;font-size:.92rem}
footer .wrap{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px}
footer .logo{color:var(--paper);font-size:1.4rem}


/* PAGES */
.page{display:none}
.page.on{display:block}
section[id]{scroll-margin-top:110px}
.mist{background:var(--mist)}
.more{margin-top:38px}
.whohead h1{font-family:var(--display);font-weight:700;font-size:clamp(2.2rem,5vw,3.8rem);line-height:1.3}
.whohead p{margin-top:16px;color:var(--sand);font-size:1.15rem;font-weight:300;max-width:30em}
.trio{display:grid;grid-template-columns:repeat(3,1fr);gap:30px}
.do{border-top:3px solid var(--caramel);padding-top:22px}
.do h3{font-family:var(--display);font-weight:600;font-size:1.5rem;margin-bottom:6px}
.do p{color:var(--walnut);font-weight:300}
.aud{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--sand);border:1.5px solid var(--espresso)}
.tile{background:var(--paper);padding:36px 28px;transition:background .25s,color .25s}
.tile h3{font-family:var(--display);font-weight:600;font-size:1.4rem;margin-bottom:6px}
.tile p{color:var(--walnut);font-weight:300;font-size:.98rem;transition:color .25s}
.tile:hover{background:var(--walnut);color:var(--paper)}
.tile:hover p{color:var(--sand)}
.tile.last{background:var(--espresso);color:var(--paper)}
.tile.last p{color:var(--sand)}
.tile.last h3{color:var(--caramel)}

/* RESPONSIVE */
@media(max-width:920px){
  .nav .wrap{flex-wrap:wrap;height:auto;padding:12px 0 6px}
  .nav ul{display:flex;order:3;width:100%;gap:24px;overflow-x:auto;white-space:nowrap;font-size:.92rem;padding:8px 0 6px}
  .trio,.aud{grid-template-columns:1fr 1fr}
  .hero{padding:56px 0 110px}
  .hero-grid,.manifesto .wrap,.cta-box,.cases{grid-template-columns:1fr}
  .case.big{grid-row:auto}
  .stage{height:380px}
  .row{grid-template-columns:64px 1fr;gap:16px}
  .row p{grid-column:1/-1}
  .steps{grid-template-columns:1fr 1fr;gap:44px 0}
  .steps::before{display:none}
  .pillars{grid-template-columns:1fr}
  .pillar{border-inline-start:0;border-top:1px solid var(--walnut)}
  .pillar:first-child{border-top:0}
  .pad{padding:80px 0}
}
@media(max-width:520px){
  .steps,.trio,.aud{grid-template-columns:1fr}
  .stage{height:330px}
}
@media(prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}
  .blk{opacity:1;transform:none;animation:none!important}
  .cursor{display:none}
}
</style>
</head>
<body>

<header class="nav">
  <div class="wrap">
    <a href="#top" class="logo" aria-label="RAMK">RAMK</a>
    <nav aria-label="القائمة الرئيسية">
      <ul>
        <li><a href="#about">من نحن</a></li>
        <li><a href="#services">خدماتنا</a></li>
        <li><a href="#who">لمن نخدم</a></li>
        <li><a href="#work">أعمالنا</a></li>
        <li><a href="#process">طريقة العمل</a></li>
      </ul>
    </nav>
    <a class="btn btn-dark" href="https://whatsapp.com/channel/0029Vb8ENFMDp2QCotHxaP0c" target="_blank" rel="noopener">قناة الواتساب</a>
  </div>
</header>

<main id="top">
<div class="page on" id="page-home">

<section class="hero">
  <div class="wrap hero-grid">
    <div>
      <h1>نبني مواقع<span>تُخلَّد في الذاكرة</span></h1>
      <p class="lead">نحن RAMK، مجموعة تصميم وبرمجة مواقع. نحوّل فكرتك إلى موقع فخم وسريع.</p>
      <div class="actions">
        <a class="btn btn-dark" href="https://whatsapp.com/channel/0029Vb8ENFMDp2QCotHxaP0c" target="_blank" rel="noopener">
          <svg class="wa" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 2a10 10 0 0 0-8.6 15.1L2 22l5-1.3A10 10 0 1 0 12 2zm5.2 14.2c-.2.6-1.3 1.2-1.8 1.2-.5.1-1 .2-3.3-.7-2.8-1.1-4.6-4-4.7-4.2-.1-.2-1.1-1.5-1.1-2.8 0-1.4.7-2 1-2.3.2-.3.5-.3.7-.3h.5c.2 0 .4 0 .6.5.2.6.8 2 .9 2.1.1.1.1.3 0 .4l-.3.5-.4.4c-.1.1-.3.3-.1.6.2.3.7 1.2 1.5 1.9 1 .9 1.8 1.2 2.1 1.3.3.1.4.1.6-.1.2-.2.7-.8.9-1.1.2-.3.4-.2.6-.1l2 1c.3.1.5.2.6.3.1.2.1.8-.2 1.4z"/></svg>
          انضم لقناتنا
        </a>
        <a class="btn btn-line" href="#services">شوف خدماتنا</a>
      </div>
    </div>

    <div class="stage" id="stage" aria-hidden="true">
      <div class="win w1">
        <div class="bar"><i></i><i></i><i></i><b>ramk.site</b></div>
        <div class="canvas c1">
          <div class="blk dk hero-b" style="--d:0"></div>
          <div class="blk t1" style="--d:1"></div>
          <div class="blk cr t1" style="--d:2;width:50%"></div>
          <div class="row3">
            <div class="blk" style="--d:3"></div>
            <div class="blk dk" style="--d:4"></div>
            <div class="blk cr" style="--d:5"></div>
          </div>
        </div>
      </div>
      <div class="win w2">
        <div class="bar"><i></i><i></i><i></i><b>mobile</b></div>
        <div class="canvas">
          <div class="blk wide dk" style="--d:6"></div>
          <div class="blk" style="--d:7"></div>
          <div class="blk cr" style="--d:8"></div>
        </div>
      </div>
      <div class="cursor"><svg viewBox="0 0 24 24"><path d="M4 2l16 9-7 2-3 7z"/></svg></div>
    </div>
  </div>
  <div class="giant" aria-hidden="true">RAMK</div>
</section>

<section class="dark pad manifesto" id="about">
  <div class="wrap">
    <h2>الموقع ليس صفحة،<br>الموقع هو واجهتك أمام العالم.</h2>
    <div class="txt">
      <p>كل موقع نصممه يُبنى من الصفر بهوية خاصة، بدون قوالب جاهزة، وبأداء سريع على الجوال والحاسوب.</p>
      <div class="pills">
        <span>تصميم حصري</span>
        <span>سرعة عالية</span>
        <span>متوافق مع الجوال</span>
        <span>جاهز لمحركات البحث</span>
      </div>
    </div>
  </div>
</section>

<section class="pad" id="services">
  <div class="wrap">
    <div class="head">
      <h2>ما الذي نصنعه لك</h2>
      <p>من موقع بسيط إلى منصة متكاملة.</p>
    </div>
    <div class="svc">
      <div class="row" tabindex="0">
        <div class="ic"><svg viewBox="0 0 24 24"><rect x="3" y="4" width="18" height="14" rx="2"/><path d="M8 21h8M12 18v3"/></svg></div>
        <h3>مواقع الشركات والأعمال</h3>
        <p>موقع رسمي يبني الثقة من أول زيارة.</p>
      </div>
      <div class="row" tabindex="0">
        <div class="ic"><svg viewBox="0 0 24 24"><path d="M6 6h15l-1.5 9h-12z"/><path d="M6 6L5 3H2"/><circle cx="9" cy="20" r="1.3"/><circle cx="18" cy="20" r="1.3"/></svg></div>
        <h3>المتاجر الإلكترونية</h3>
        <p>متجر سلس تعرض فيه منتجاتك وتستقبل الطلبات.</p>
      </div>
      <div class="row" tabindex="0">
        <div class="ic"><svg viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4 4-6 8-6s8 2 8 6"/></svg></div>
        <h3>المعارض الشخصية</h3>
        <p>موقع يعرض أعمالك وسيرتك بشكل يليق بك.</p>
      </div>
      <div class="row" tabindex="0">
        <div class="ic"><svg viewBox="0 0 24 24"><path d="M4 4h16v10H4z"/><path d="M8 20h8M12 14v6"/><path d="M8 9l2 2 4-4"/></svg></div>
        <h3>صفحات الهبوط</h3>
        <p>صفحة واحدة تحوّل الزائر إلى عميل.</p>
      </div>
      <div class="row" tabindex="0">
        <div class="ic"><svg viewBox="0 0 24 24"><path d="M8 8l-5 4 5 4M16 8l5 4-5 4M14 5l-4 14"/></svg></div>
        <h3>تطبيقات ويب مخصصة</h3>
        <p>لوحات تحكم وأنظمة حسب فكرتك.</p>
      </div>
    </div>
    <div class="more"><a class="btn btn-line" href="#who">لمن نقدم خدماتنا</a></div>
  </div>
</section>

<section class="pad work" id="work">
  <div class="wrap">
    <div class="head">
      <h2>لمحة من أسلوبنا</h2>
      <p>مفاهيم تصميم توضح مستوى شغلنا.</p>
    </div>
    <div class="cases">
      <article class="case big">
        <div class="shot s1">
          <div class="nv"></div>
          <div class="h">Your Brand,<br>Elevated.</div>
          <div class="bt"></div>
          <div class="g"><i></i><i></i><i></i></div>
        </div>
        <div class="info"><h3>موقع شركة</h3><p>واجهة داكنة فخمة.</p></div>
      </article>
      <article class="case">
        <div class="shot s2">
          <div class="nv"></div>
          <div class="h">Shop.</div>
          <div class="bt"></div>
        </div>
        <div class="info"><h3>متجر إلكتروني</h3><p>عرض منتجات نظيف.</p></div>
      </article>
      <article class="case">
        <div class="shot s3">
          <div class="nv"></div>
          <div class="h">Portfolio</div>
          <div class="g"><i></i><i></i><i></i></div>
        </div>
        <div class="info"><h3>معرض أعمال</h3><p>مساحة تعرض إبداعك.</p></div>
      </article>
    </div>
    <p class="note">نماذج توضيحية. تواصل معنا لمشاهدة أعمالنا.</p>
  </div>
</section>

<section class="pad" id="process">
  <div class="wrap">
    <div class="head">
      <h2>من الفكرة إلى الإطلاق</h2>
      <p>أربع خطوات واضحة.</p>
    </div>
    <div class="steps">
      <div class="step"><div class="n">1</div><h3>نفهم فكرتك</h3><p>نعرف هدفك وما تحتاجه.</p></div>
      <div class="step"><div class="n">2</div><h3>نصمم الهوية</h3><p>نرسم شكل الموقع ليناسب علامتك.</p></div>
      <div class="step"><div class="n">3</div><h3>نبرمج ونختبر</h3><p>نبني الموقع ونجربه على كل الأجهزة.</p></div>
      <div class="step"><div class="n">4</div><h3>نطلق ونتابع</h3><p>ننشر الموقع ونبقى معك للدعم.</p></div>
    </div>
  </div>
</section>

<section class="why pad">
  <div class="wrap">
    <div class="head">
      <h2>ليش تختار RAMK</h2>
      <p>لأن التفاصيل تصنع الفرق.</p>
    </div>
    <div class="pillars">
      <div class="pillar"><h3>هوية لا تشبه غيرك</h3><p>كل مشروع يبدأ من ورقة بيضاء.</p></div>
      <div class="pillar"><h3>أداء يسبق التوقعات</h3><p>مواقع خفيفة وسريعة التحميل.</p></div>
      <div class="pillar"><h3>تواصل مباشر وصريح</h3><p>نرد بسرعة ونشرح كل خطوة.</p></div>
    </div>
  </div>
</section>

</div><!-- /page-home -->

<div class="page" id="page-who">
  <section class="dark pad whohead">
    <div class="wrap">
      <h1>ماذا نسوي ولمن نقدم خدماتنا</h1>
      <p>نصمم ونبرمج ونطلق مواقع لكل من يحتاج حضورًا رقميًا قويًا.</p>
    </div>
  </section>

  <section class="pad">
    <div class="wrap">
      <div class="head"><h2>ماذا نسوي</h2></div>
      <div class="trio">
        <div cl
