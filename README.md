<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Gokul M – Java & MERN Stack Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700;800&family=Figtree:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #f1f4fb; --surface: #ffffff; --ink: #0f1b3d; --muted: #566180; --line: #dbe2f1;
    --blue: #2753d6; --blue-soft: #e3eaff; --teal: #0e8a8c; --teal-soft: #d9f3f3;
    --amber: #f2a20c; --amber-soft: #fff0cd; --rose: #d6336c; --rose-soft: #ffe3ee;
    --shadow: 0 14px 40px rgba(20,40,110,.12);
    --display: "Bricolage Grotesque", "Trebuchet MS", system-ui, sans-serif;
    --body: "Figtree", system-ui, -apple-system, "Segoe UI", sans-serif;
    box-sizing: border-box;
    padding-top: env(safe-area-inset-top, 0px);
    padding-bottom: env(safe-area-inset-bottom, 0px);
  }
  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      --bg:#0b1126; --surface:#131b37; --ink:#eaf0ff; --muted:#9ba8ca; --line:#27335c;
      --blue:#86a2ff; --blue-soft:#1c2b60; --teal:#55d6d8; --teal-soft:#10383b;
      --amber:#ffbb3d; --amber-soft:#3a2c0d; --rose:#ff7aa8; --rose-soft:#43182c;
      --shadow: 0 14px 40px rgba(0,0,0,.4);
    }
  }
  :root[data-theme="dark"] {
    --bg:#0b1126; --surface:#131b37; --ink:#eaf0ff; --muted:#9ba8ca; --line:#27335c;
    --blue:#86a2ff; --blue-soft:#1c2b60; --teal:#55d6d8; --teal-soft:#10383b;
    --amber:#ffbb3d; --amber-soft:#3a2c0d; --rose:#ff7aa8; --rose-soft:#43182c;
    --shadow: 0 14px 40px rgba(0,0,0,.4);
  }
  html { scroll-padding-top: env(safe-area-inset-top, 0px); scroll-behavior: smooth; }
  *, *::before, *::after { box-sizing: border-box; }
  body { margin:0; background:var(--bg); color:var(--ink); font-family:var(--body); font-size:17px; line-height:1.6; overflow-x:hidden; }
  a { color: inherit; }
  :focus-visible { outline: 3px solid var(--amber); outline-offset: 3px; border-radius: 8px; }
  .wrap { max-width: 1080px; margin: 0 auto; padding: 0 22px; }

  /* ---------- HERO ---------- */
  .hero-band { position:relative; color:#f4f7ff; overflow:hidden;
    background: radial-gradient(900px 500px at 85% 10%, rgba(94,234,212,.28), transparent 60%),
                radial-gradient(700px 500px at 0% 100%, rgba(255,185,56,.20), transparent 60%),
                linear-gradient(135deg, #0a1233 0%, #1a2a7a 55%, #0d6a78 100%);
    padding-bottom: 120px; }
  .hero-band::before { content:""; position:absolute; inset:0; opacity:.18; pointer-events:none;
    background-image: radial-gradient(rgba(255,255,255,.9) 1px, transparent 1.4px); background-size: 26px 26px;
    mask-image: linear-gradient(180deg, #000, transparent 85%); -webkit-mask-image: linear-gradient(180deg, #000, transparent 85%); }
  .bar { position:relative; display:flex; justify-content:space-between; align-items:center; padding:20px 0; font-family:var(--display); font-weight:700; }
  .bar nav { display:flex; align-items:center; gap:22px; font-family:var(--body); font-weight:500; font-size:15px; }
  .bar nav a { text-decoration:none; color:rgba(244,247,255,.8); }
  .bar nav a:hover { color:#fff; }
  .theme { border:1px solid rgba(255,255,255,.35); background:rgba(255,255,255,.1); color:#fff; border-radius:999px; padding:6px 14px; font:inherit; font-size:14px; cursor:pointer; }

  .hero { position:relative; display:grid; grid-template-columns: 1.2fr 1fr; gap:40px; align-items:center; padding:40px 0 10px; }
  .hello { display:inline-flex; align-items:center; gap:10px; background:rgba(255,255,255,.12); border:1px solid rgba(255,255,255,.25); padding:6px 16px; border-radius:999px; font-size:15px; font-weight:500; margin-bottom:18px; }
  .hello i { width:9px; height:9px; border-radius:50%; background:#5eead4; box-shadow:0 0 0 0 rgba(94,234,212,.7); animation:pulse 2s infinite; }
  @keyframes pulse { 70% { box-shadow:0 0 0 10px rgba(94,234,212,0); } 100% { box-shadow:0 0 0 0 rgba(94,234,212,0); } }
  .hero h1 { font-family:var(--display); font-weight:800; font-size:clamp(3rem, 9vw, 6rem); line-height:.95; letter-spacing:-.035em; margin:0 0 16px; }
  .hero h1 span { background:linear-gradient(90deg,#ffd27a,#5eead4); -webkit-background-clip:text; background-clip:text; color:transparent; }
  .typed { font-family:var(--display); font-weight:700; font-size:clamp(1.3rem, 3.4vw, 1.9rem); min-height:1.4em; margin:0 0 16px; color:#ffd27a; }
  .typed::after { content:"|"; margin-left:3px; animation:blink 1s steps(1) infinite; color:#5eead4; }
  @keyframes blink { 50% { opacity:0; } }
  .lead { font-size:1.12rem; color:rgba(244,247,255,.85); max-width:46ch; margin:0 0 28px; }
  .links { display:flex; flex-wrap:wrap; gap:12px; }
  .btn { display:inline-flex; align-items:center; gap:8px; padding:13px 22px; border-radius:14px; font-weight:600; text-decoration:none; border:2px solid #fff; transition:transform .15s ease, box-shadow .15s ease; }
  .btn:hover { transform:translateY(-3px); box-shadow:0 10px 24px rgba(0,0,0,.3); }
  .btn.primary { background:#ffbb3d; border-color:#ffbb3d; color:#241800; }
  .btn.ghost { background:rgba(255,255,255,.08); color:#fff; }

  .photo-wrap { position:relative; justify-self:center; width:min(100%, 360px); aspect-ratio:1; }
  .glow { position:absolute; inset:-14%; border-radius:50%; background:radial-gradient(circle, rgba(94,234,212,.45), rgba(255,185,56,.18) 45%, transparent 68%); filter:blur(14px); }
  .ring { position:absolute; inset:0; border-radius:50%; background:conic-gradient(from 0deg, #ffbb3d, #5eead4, #86a2ff, #ff7aa8, #ffbb3d); animation:spin 12s linear infinite; }
  @keyframes spin { to { transform:rotate(360deg); } }
  .face { position:absolute; inset:10px; border-radius:50%; overflow:hidden; background:#fff; border:6px solid #0d1740; }
  .face img { width:100%; height:100%; object-fit:cover; object-position:center 18%; display:block; }
  .float { position:absolute; background:#fff; color:#10204f; font-weight:600; font-size:14px; padding:8px 14px; border-radius:12px; box-shadow:0 10px 26px rgba(0,0,0,.3); animation:bob 5s ease-in-out infinite; white-space:nowrap; }
  .float.f1 { top:6%; left:-8%; } .float.f2 { top:34%; right:-10%; animation-delay:-1.6s; }
  .float.f3 { bottom:6%; left:-4%; animation-delay:-3.2s; } 
  @keyframes bob { 50% { transform:translateY(-9px); } }

  .hero > div:first-child, .photo-wrap { animation:rise .8s cubic-bezier(.2,.7,.2,1) both; }
  .photo-wrap { animation-delay:.15s; }
  @keyframes rise { from { opacity:0; transform:translateY(22px); } to { opacity:1; transform:none; } }

  /* tech marquee */
  .marquee { position:relative; margin-top:56px; overflow:hidden; border-block:1px solid rgba(255,255,255,.18); padding:14px 0; background:rgba(0,0,0,.14); }
  .track { display:flex; gap:44px; width:max-content; animation:slide 28s linear infinite; font-family:var(--display); font-weight:700; font-size:1.15rem; color:rgba(244,247,255,.9); }
  .track span::before { content:"✦"; color:#ffbb3d; margin-right:44px; }
  @keyframes slide { to { transform:translateX(-50%); } }

  /* facts */
  .facts { position:relative; margin-top:-62px; display:grid; grid-template-columns:repeat(4,1fr); background:var(--surface); border:1px solid var(--line); border-radius:22px; box-shadow:var(--shadow); overflow:hidden; }
  .fact { padding:24px 24px; border-right:1px solid var(--line); }
  .fact:last-child { border-right:0; }
  .fact b { display:block; font-family:var(--display); font-size:2rem; line-height:1.1; letter-spacing:-.02em; color:var(--blue); }
  .fact:nth-child(2) b { color:var(--teal); } .fact:nth-child(3) b { color:var(--rose); } .fact:nth-child(4) b { color:var(--amber); }
  .fact span { color:var(--muted); font-size:14.5px; }

  section { padding:84px 0 0; }
  h2 { font-family:var(--display); font-weight:800; font-size:clamp(2rem,5vw,3rem); letter-spacing:-.025em; line-height:1.05; margin:0 0 10px; }
  h2::after { content:""; display:block; width:64px; height:6px; border-radius:6px; margin-top:14px; background:linear-gradient(90deg,var(--blue),var(--teal),var(--amber)); }
  .sub { color:var(--muted); margin:14px 0 34px; max-width:56ch; }

  /* skills */
  .skills { display:grid; grid-template-columns:repeat(2,1fr); gap:20px; }
  .group { background:var(--surface); border:1px solid var(--line); border-radius:22px; padding:26px; box-shadow:var(--shadow); position:relative; overflow:hidden; }
  .group::before { content:""; position:absolute; left:0; top:0; bottom:0; width:6px; background:var(--blue); }
  .group.b::before { background:var(--teal); } .group.c::before { background:var(--amber); } .group.d::before { background:var(--rose); }
  .group h3 { font-family:var(--display); font-size:1.2rem; margin:0 0 16px; display:flex; align-items:center; gap:10px; }
  .group h3 em { font-style:normal; display:grid; place-items:center; width:38px; height:38px; border-radius:12px; background:var(--blue-soft); font-size:19px; }
  .group.b h3 em { background:var(--teal-soft); } .group.c h3 em { background:var(--amber-soft); } .group.d h3 em { background:var(--rose-soft); }
  .chips { display:flex; flex-wrap:wrap; gap:9px; }
  .chip { padding:7px 15px; border-radius:999px; font-weight:600; font-size:15px; background:var(--blue-soft); color:var(--blue); transition:transform .15s; }
  .chip:hover { transform:translateY(-3px) scale(1.04); }
  .group.b .chip { background:var(--teal-soft); color:var(--teal); }
  .group.c .chip { background:var(--amber-soft); color:#8a5700; }
  .group.d .chip { background:var(--rose-soft); color:var(--rose); }
  :root[data-theme="dark"] .group.c .chip { color:var(--amber); }
  @media (prefers-color-scheme: dark) { :root:not([data-theme="light"]) .group.c .chip { color:var(--amber); } }

  /* projects */
  .projects { display:grid; grid-template-columns:repeat(2,1fr); gap:22px; }
  .project { background:var(--surface); border:1px solid var(--line); border-radius:22px; overflow:hidden; display:flex; flex-direction:column; box-shadow:var(--shadow); transition:transform .2s ease; }
  .project:hover { transform:translateY(-6px); }
  .project .top { padding:22px 26px; color:#fff; display:flex; justify-content:space-between; align-items:center; gap:12px; font-family:var(--display); font-weight:700; }
  .project .top small { font-family:var(--body); font-weight:600; font-size:13px; background:rgba(255,255,255,.22); padding:4px 12px; border-radius:999px; white-space:nowrap; }
  .project .top .ic { font-size:1.9rem; }
  .t1 { background:linear-gradient(120deg,#2753d6,#7a4dff); } .t2 { background:linear-gradient(120deg,#0e8a8c,#2bb673); }
  .t3 { background:linear-gradient(120deg,#d6336c,#ff8a4c); } .t4 { background:linear-gradient(120deg,#1b2a78,#0e8a8c); }
  .project .body { padding:24px 26px 26px; display:flex; flex-direction:column; gap:12px; flex:1; }
  .project h3 { font-family:var(--display); font-size:1.4rem; margin:0; line-height:1.2; }
  .project p { margin:0; color:var(--muted); }
  .project .stack { display:flex; flex-wrap:wrap; gap:7px; margin-top:auto; padding-top:8px; }
  .project .stack span { font-size:13px; font-weight:500; padding:4px 11px; border-radius:8px; background:var(--bg); border:1px solid var(--line); color:var(--muted); }
  .project a.open { font-weight:600; color:var(--blue); text-decoration:none; }
  .project a.open:hover { text-decoration:underline; }
  .project.wide { grid-column:1 / -1; }

  /* journey */
  .timeline { position:relative; margin:0; padding:0 0 0 38px; list-style:none; }
  .timeline::before { content:""; position:absolute; left:11px; top:10px; bottom:10px; width:3px; border-radius:3px; background:linear-gradient(var(--blue),var(--teal),var(--amber)); }
  .timeline li { position:relative; padding:0 0 22px; }
  .timeline li:last-child { padding-bottom:0; }
  .timeline li::before { content:""; position:absolute; left:-37px; top:22px; width:22px; height:22px; border-radius:50%; background:var(--surface); border:5px solid var(--blue); box-shadow:0 0 0 5px var(--blue-soft); }
  .timeline li:nth-child(2)::before { border-color:var(--teal); box-shadow:0 0 0 5px var(--teal-soft); }
  .timeline li:nth-child(3)::before { border-color:var(--amber); box-shadow:0 0 0 5px var(--amber-soft); }
  .timeline li:nth-child(4)::before { border-color:var(--rose); box-shadow:0 0 0 5px var(--rose-soft); }
  .tl-card { background:var(--surface); border:1px solid var(--line); border-radius:18px; padding:18px 22px; box-shadow:var(--shadow); }
  .timeline .when { color:var(--teal); font-weight:600; font-size:14.5px; }
  .timeline h3 { font-family:var(--display); font-size:1.2rem; margin:2px 0 0; }
  .timeline p { margin:6px 0 0; color:var(--muted); max-width:62ch; }

  .certs { display:grid; grid-template-columns:repeat(3,1fr); gap:20px; }
  .cert { background:var(--surface); border:1px solid var(--line); border-radius:22px; padding:24px; box-shadow:var(--shadow); }
  .cert .medal { width:52px; height:52px; border-radius:16px; display:grid; place-items:center; font-size:26px; margin-bottom:14px; background:var(--amber-soft); }
  .cert:nth-child(2) .medal { background:var(--blue-soft); } .cert:nth-child(3) .medal { background:var(--teal-soft); }
  .cert b { font-family:var(--display); font-size:1.12rem; display:block; line-height:1.25; margin-bottom:4px; }
  .cert span { color:var(--muted); font-size:15px; }

  .contact { margin:84px 0 0; border-radius:30px; padding:clamp(30px,6vw,64px); color:#f4f7ff; position:relative; overflow:hidden;
    background: radial-gradient(500px 300px at 90% 0%, rgba(94,234,212,.35), transparent 60%), linear-gradient(135deg,#0a1233,#1a2a7a 60%,#0d6a78); }
  .contact h2 { margin-bottom:10px; } .contact h2::after { background:#ffbb3d; }
  .contact p { margin:14px 0 26px; color:rgba(244,247,255,.85); max-width:50ch; }
  footer { padding:34px 0 44px; color:var(--muted); font-size:14px; text-align:center; }

  @media (max-width: 860px) {
    .hero { grid-template-columns:1fr; gap:34px; padding-top:20px; }
    .photo-wrap { order:-1; width:min(78%, 290px); }
    .float.f1 { left:-4%; } .float.f2 { right:-4%; } .float.f3 { left:0; }
    .facts { grid-template-columns:repeat(2,1fr); }
    .fact:nth-child(2) { border-right:0; } .fact:nth-child(-n+2) { border-bottom:1px solid var(--line); }
    .skills, .projects, .certs { grid-template-columns:1fr; }
    .bar nav a.hide-sm { display:none; }
  }
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after { animation:none !important; transition:none !important; }
    html { scroll-behavior:auto; }
    .typed::after { animation:none; }
  }
</style>
</head>
<body>

<div class="hero-band">
  <div class="wrap">
    <header class="bar">
      <span>gokul27108</span>
      <nav aria-label="Sections">
        <a class="hide-sm" href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a class="hide-sm" href="#journey">Journey</a>
        <a href="#contact">Contact</a>
        <button class="theme" id="themeBtn" type="button" aria-label="Switch between light and dark theme">Theme</button>
      </nav>
    </header>

    <div class="hero">
      <div>
        <div class="hello"><i></i> Open to entry-level roles</div>
        <h1>Hi, I'm <span>Gokul M</span></h1>
        <p class="typed" id="typed" aria-label="Java Developer, MERN Stack Developer, Problem Solver">Java Developer</p>
        <p class="lead">I'm an Information Technology student from Namakkal who builds full-stack web apps and Java projects, from the database to the screen.</p>
        <div class="links">
          <a class="btn primary" href="#projects">See my projects</a>
          <a class="btn ghost" href="https://github.com/gokul27108" target="_blank" rel="noopener">GitHub</a>
          <a class="btn ghost" href="https://www.linkedin.com/in/gokul-m-a4b08b314/" target="_blank" rel="noopener">LinkedIn</a>
          <a class="btn ghost" href="https://leetcode.com/u/gokul_5048/" target="_blank" rel="noopener">LeetCode</a>
        </div>
      </div>
      <div class="photo-wrap">
        <div class="glow"></div>
        <div class="ring"></div>
        <div class="face"><img src="data:image/jpeg;base64,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" alt="Gokul M in a black suit and blue tie" width="520" height="520"></div>
        <span class="float f1">☕ Java</span>
        <span class="float f2">⚛️ MERN stack</span>
        <span class="float f3">☁️ AWS certified learner</span>
      </div>
    </div>
  </div>

  <div class="marquee" aria-hidden="true">
    <div class="track">
      <span>Java</span><span>JavaScript</span><span>React.js</span><span>Node.js</span><span>Express.js</span><span>MongoDB</span><span>MySQL</span><span>SQL</span><span>AWS</span><span>OOP</span><span>DBMS</span><span>REST APIs</span>
      <span>Java</span><span>JavaScript</span><span>React.js</span><span>Node.js</span><span>Express.js</span><span>MongoDB</span><span>MySQL</span><span>SQL</span><span>AWS</span><span>OOP</span><span>DBMS</span><span>REST APIs</span>
    </div>
  </div>
</div>

<div class="wrap">
  <main>
    <div class="facts" role="list">
      <div class="fact" role="listitem"><b data-count="15">15</b><span>public repositories</span></div>
      <div class="fact" role="listitem"><b data-count="8.14" data-dec="2">8.14</b><span>CGPA, B.Tech IT</span></div>
      <div class="fact" role="listitem"><b>Infosys</b><span>Springboard Internship 6.0</span></div>
      <div class="fact" role="listitem"><b data-count="3">3</b><span>certifications</span></div>
    </div>

    <section id="skills">
      <h2>Technical skills</h2>
      <p class="sub">The tools I use to build complete applications.</p>
      <div class="skills">
        <div class="group">
          <h3><em>💻</em> Languages</h3>
          <div class="chips"><span class="chip">Java</span><span class="chip">JavaScript</span><span class="chip">SQL</span><span class="chip">HTML</span><span class="chip">CSS</span></div>
        </div>
        <div class="group b">
          <h3><em>⚛️</em> MERN stack</h3>
          <div class="chips"><span class="chip">MongoDB</span><span class="chip">Express.js</span><span class="chip">React.js</span><span class="chip">Node.js</span><span class="chip">REST APIs</span></div>
        </div>
        <div class="group c">
          <h3><em>🗄️</em> Databases</h3>
          <div class="chips"><span class="chip">MySQL</span><span class="chip">MongoDB</span></div>
        </div>
        <div class="group d">
          <h3><em>🧠</em> Core areas and cloud</h3>
          <div class="chips"><span class="chip">Object-oriented programming</span><span class="chip">DBMS</span><span class="chip">AWS</span><span class="chip">Problem solving</span></div>
        </div>
        <div class="group b" style="grid-column:1 / -1">
          <h3><em>🤝</em> Working style</h3>
          <div class="chips"><span class="chip">Communication</span><span class="chip">Teamwork</span><span class="chip">Quick learner</span></div>
        </div>
      </div>
    </section>

    <section id="projects">
      <h2>Projects</h2>
      <p class="sub">Applications I designed and built.</p>
      <div class="projects">
        <article class="project wide">
          <div class="top t1"><span class="ic">📜</span><small>Pinned on GitHub</small></div>
          <div class="body">
            <h3>Bulk Certificate Generator API</h3>
            <p>A REST API that generates certificates in bulk from structured input data. It validates each request, creates PDFs, and processes large batches efficiently.</p>
            <div class="stack"><span>REST API</span><span>PDF generation</span><span>Validation</span><span>Bulk processing</span></div>
            <a class="open" href="https://github.com/gokul27108/bulk-certificate-generator-api-" target="_blank" rel="noopener">Open the repository</a>
          </div>
        </article>
        <article class="project">
          <div class="top t2"><span class="ic">🏛️</span><small>Full stack</small></div>
          <div class="body">
            <h3>Government Scheme Identifier</h3>
            <p>Helps people find government schemes they are eligible for, and shows scheme details and how to apply in a simple, easy-to-follow format.</p>
            <div class="stack"><span>MongoDB</span><span>Express.js</span><span>React.js</span><span>Node.js</span><span>API</span></div>
          </div>
        </article>
        <article class="project">
          <div class="top t3"><span class="ic">💬</span><small>Full stack</small></div>
          <div class="body">
            <h3>Q&amp;A Social Learning Platform</h3>
            <p>A Q&amp;A site for programming, mathematics and technical topics. Answers are validated by votes, the interface is multilingual, and equations and code snippets are formatted.</p>
            <div class="stack"><span>MongoDB</span><span>Express.js</span><span>React.js</span><span>Node.js</span></div>
          </div>
        </article>
        <article class="project wide">
          <div class="top t4"><span class="ic">🛡️</span><small>Infosys internship</small></div>
          <div class="body">
            <h3>Fraud Detection and Transaction Simulation Engine</h3>
            <p>A Java engine for digital banking. I worked on transaction monitoring, fraud analysis and risk detection logic.</p>
            <div class="stack"><span>Java</span><span>Transaction monitoring</span><span>Fraud analysis</span><span>Risk detection</span></div>
          </div>
        </article>
      </div>
    </section>

    <section id="journey">
      <h2>Journey</h2>
      <p class="sub">Where I have studied and worked so far.</p>
      <ol class="timeline">
        <li><div class="tl-card"><span class="when">Dec 2025 – Feb 2026</span><h3>Infosys Springboard Internship 6.0</h3><p>Remote internship. Built a fraud detection and transaction simulation engine for digital banking in Java.</p></div></li>
        <li><div class="tl-card"><span class="when">2023 – 2027</span><h3>B.Tech in Information Technology</h3><p>V.S.B. Engineering College, Karur (Anna University). CGPA 8.14 out of 10.</p></div></li>
        <li><div class="tl-card"><span class="when">March 2023</span><h3>Class XII (HSC)</h3><p>Government Higher Secondary School, Kabilarmalai. Score: 72.33%.</p></div></li>
        <li><div class="tl-card"><span class="when">March 2021</span><h3>Class X (SSLC)</h3><p>Malar Matric Higher Secondary School, Paramathi. All pass.</p></div></li>
      </ol>
    </section>

    <section id="certs">
      <h2>Certifications</h2>
      <p class="sub">Courses I completed to back up the hands-on work.</p>
      <div class="certs">
        <div class="cert"><div class="medal">🏅</div><b>Programming in Java</b><span>NPTEL · Elite + Silver, 78%</span></div>
        <div class="cert"><div class="medal">☕</div><b>Java Foundation Certificate</b><span>Infosys</span></div>
        <div class="cert"><div class="medal">☁️</div><b>AWS Cloud Practitioner Essentials</b><span>Amazon Web Services</span></div>
      </div>
    </section>

    <section class="contact" id="contact">
      <h2>Let's work together</h2>
      <p>I'm looking for an entry-level software development role where I can apply Java, the MERN stack and databases. Email me or message me on LinkedIn.</p>
      <div class="links">
        <a class="btn primary" href="mailto:gokulmathiyalagan27@gmail.com">Email me</a>
        <a class="btn ghost" href="https://www.linkedin.com/in/gokul-m-a4b08b314/" target="_blank" rel="noopener">Message on LinkedIn</a>
        <a class="btn ghost" href="https://github.com/gokul27108" target="_blank" rel="noopener">See all repositories</a>
      </div>
    </section>
  </main>
  <footer>Gokul M · Namakkal, Tamil Nadu, India</footer>
</div>

<script>
(function () {
  var root = document.documentElement;
  document.getElementById("themeBtn").addEventListener("click", function () {
    var dark = root.getAttribute("data-theme") === "dark" ||
      (!root.getAttribute("data-theme") && window.matchMedia("(prefers-color-scheme: dark)").matches);
    root.setAttribute("data-theme", dark ? "light" : "dark");
  });

  var reduce = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

  // typing role line
  var el = document.getElementById("typed");
  var roles = ["Java Developer", "MERN Stack Developer", "Problem Solver"];
  if (!reduce) {
    var r = 0, c = 0, del = false;
    (function tick() {
      var word = roles[r];
      el.textContent = word.slice(0, c);
      var wait = del ? 40 : 85;
      if (!del && c === word.length) { del = true; wait = 1400; }
      else if (del && c === 0) { del = false; r = (r + 1) % roles.length; wait = 350; }
      else { c += del ? -1 : 1; }
      setTimeout(tick, wait);
    })();
  }

  // count-up numbers
  if (!reduce && "IntersectionObserver" in window) {
    var io = new IntersectionObserver(function (entries) {
      entries.forEach(function (e) {
        if (!e.isIntersecting) return;
        io.unobserve(e.target);
        var n = e.target, end = parseFloat(n.dataset.count), dec = parseInt(n.dataset.dec || "0", 10), t0 = null;
        function step(t) {
          if (!t0) t0 = t;
          var p = Math.min((t - t0) / 1200, 1), ease = 1 - Math.pow(1 - p, 3);
          n.textContent = (end * ease).toFixed(dec);
          if (p < 1) requestAnimationFrame(step);
        }
        requestAnimationFrame(step);
      });
    }, { threshold: 0.6 });
    document.querySelectorAll("[data-count]").forEach(function (n) { io.observe(n); });
  }
})();
</script>
</body>
</html>
