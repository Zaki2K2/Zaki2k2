<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Syed Zaki Ahmad | Full-Stack Developer</title>
<style>
  :root{--bg:#0b0f1a;--card:#121828;--line:#232b42;--text:#e6eaf5;--muted:#9aa4bf;--c1:#00f7ff;--c2:#7c3aed;--c3:#ff00c8}
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{background:var(--bg);color:var(--text);font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;line-height:1.6}
  a{color:inherit;text-decoration:none}
  .wrap{max-width:1000px;margin:0 auto;padding:0 24px}

  /* nav */
  nav{position:sticky;top:0;z-index:10;background:rgba(11,15,26,.85);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
  nav .wrap{display:flex;justify-content:space-between;align-items:center;height:60px}
  .logo{font-weight:700;background:linear-gradient(90deg,var(--c1),var(--c3));-webkit-background-clip:text;background-clip:text;color:transparent}
  nav ul{display:flex;gap:22px;list-style:none;font-size:14px;color:var(--muted)}
  nav ul a:hover{color:var(--c1)}

  /* hero */
  header{background:linear-gradient(135deg,rgba(0,247,255,.18),rgba(124,58,237,.28) 50%,rgba(255,0,200,.18));border-bottom:1px solid var(--line);text-align:center;padding:96px 24px 84px}
  .tag{display:inline-block;font-size:13px;padding:6px 14px;border:1px solid var(--line);border-radius:999px;background:rgba(18,24,40,.7);color:var(--c1);margin-bottom:22px}
  h1{font-size:clamp(38px,7vw,64px);line-height:1.1;letter-spacing:-1px}
  h1 span{background:linear-gradient(90deg,var(--c1),var(--c2) 55%,var(--c3));-webkit-background-clip:text;background-clip:text;color:transparent}
  .sub{margin:18px auto 0;max-width:620px;color:var(--muted);font-size:18px}
  .btns{margin-top:32px;display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
  .btn{padding:12px 24px;border-radius:10px;font-weight:600;font-size:15px;border:1px solid var(--line);background:var(--card);transition:.2s}
  .btn:hover{transform:translateY(-2px);border-color:var(--c1)}
  .btn.primary{border:0;color:#fff;background:linear-gradient(90deg,var(--c2),var(--c3))}
  .stats{margin-top:48px;display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
  .stat{background:rgba(18,24,40,.75);border:1px solid var(--line);border-radius:14px;padding:14px 26px;min-width:140px}
  .stat b{display:block;font-size:26px;color:var(--c1)}
  .stat small{color:var(--muted)}

  /* sections */
  section{padding:76px 0 0}
  h2{font-size:28px;margin-bottom:28px;display:flex;align-items:center;gap:12px}
  h2::after{content:"";flex:1;height:1px;background:linear-gradient(90deg,var(--line),transparent)}
  p.lead{color:var(--muted);font-size:17px;max-width:760px}
  .grid{display:grid;gap:18px}
  .g2{grid-template-columns:repeat(auto-fit,minmax(300px,1fr))}
  .g3{grid-template-columns:repeat(auto-fit,minmax(250px,1fr))}
  .card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:24px;transition:.25s}
  .card:hover{transform:translateY(-4px);border-color:var(--c2);box-shadow:0 10px 30px rgba(124,58,237,.18)}
  .card h3{font-size:18px;margin-bottom:6px}
  .card p{color:var(--muted);font-size:15px}
  .icon{width:48px;height:48px;border-radius:12px;display:flex;align-items:center;justify-content:center;margin-bottom:14px;color:#fff;background:linear-gradient(135deg,var(--c2),var(--c3));box-shadow:0 6px 16px rgba(124,58,237,.35)}
  .icon svg{width:24px;height:24px}

  /* skills */
  .skillbox h3{font-size:15px;color:var(--c1);margin-bottom:12px;text-transform:uppercase;letter-spacing:1px}
  .chips{display:flex;flex-wrap:wrap;gap:8px}
  .chip{font-size:13px;padding:6px 12px;border-radius:8px;background:#0e1424;border:1px solid var(--line);color:var(--text)}

  /* projects */
  .proj .chips{margin:14px 0}
  .proj a.link{color:var(--c1);font-size:14px;font-weight:600}
  .proj a.link:hover{color:var(--c3)}
  .note{font-size:12px;color:var(--muted);margin-top:6px;font-style:italic}

  /* timeline */
  .timeline{border-left:2px solid var(--line);margin-left:8px}
  .item{position:relative;padding:0 0 30px 28px}
  .item::before{content:"";position:absolute;left:-8px;top:6px;width:14px;height:14px;border-radius:50%;background:linear-gradient(135deg,var(--c1),var(--c3))}
  .item h3{font-size:18px}
  .item .role{color:var(--c1);font-size:14px}
  .item .date{color:var(--muted);font-size:13px;margin:2px 0 8px}
  .item ul{padding-left:18px;color:var(--muted);font-size:15px}

  /* contact + footer */
  .contact{text-align:center;background:linear-gradient(135deg,rgba(124,58,237,.2),rgba(255,0,200,.12));border:1px solid var(--line);border-radius:20px;padding:48px 24px}
  .contact h2::after{display:none}
  .contact p{color:var(--muted);margin:10px auto 24px;max-width:540px}
  footer{margin-top:76px;padding:28px;text-align:center;color:var(--muted);font-size:13px;border-top:1px solid var(--line)}

  @media(max-width:640px){nav ul{display:none}header{padding:64px 20px}}
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <a class="logo" href="#top">Syed Zaki Ahmad</a>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<header id="top">
  <span class="tag">Open to MSc programmes in Computer Science / AI &middot; 2027/28</span>
  <h1>Hi, I'm <span>Syed Zaki Ahmad</span></h1>
  <p class="sub">Full-stack developer building scalable fintech web applications with Angular, TypeScript and Node.js, with a strong interest in artificial intelligence.</p>
  <div class="btns">
    <a class="btn primary" href="#projects">View Projects</a>
    <a class="btn" href="mailto:syedzaki2kk2@gmail.com">Email Me</a>
    <a class="btn" href="https://www.linkedin.com/in/syed-zaki-ahmad-742b741aa">LinkedIn</a>
  </div>
  <div class="stats">
    <div class="stat"><b>2+</b><small>Years experience</small></div>
    <div class="stat"><b>3.62</b><small>CGPA / 4.0</small></div>
    <div class="stat"><b>3</b><small>Companies</small></div>
  </div>
</header>

<main class="wrap">

  <section id="about">
    <h2>About Me</h2>
    <p class="lead">I am a Computer Science graduate of Federal Urdu University of Arts, Science and Technology, Islamabad (2024). At NovaCTO I work on CustomerCore, a Swiss fintech SaaS platform for accounting, invoicing and VAT management. My work covers reusable Angular components, Node.js REST APIs, code reviews and CI/CD. I plan to continue with a master's degree focused on AI and research.</p>
    <div class="grid g3" style="margin-top:28px">
      <div class="card"><div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg></div><h3>Full-Stack Development</h3><p>Angular front ends and Node.js back ends with MongoDB and SQL.</p></div>
      <div class="card"><div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><line x1="6" y1="3" x2="6" y2="15"/><circle cx="18" cy="6" r="3"/><circle cx="6" cy="18" r="3"/><path d="M18 9a9 9 0 0 1-9 9"/></svg></div><h3>CI/CD &amp; Teamwork</h3><p>Git, Bitbucket and Azure pipelines, Agile sprints and code reviews.</p></div>
      <div class="card"><div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="4" y="4" width="16" height="16" rx="2"/><rect x="9" y="9" width="6" height="6"/><path d="M9 1v3M15 1v3M9 20v3M15 20v3M20 9h3M20 14h3M1 9h3M1 14h3"/></svg></div><h3>Interest in AI</h3><p>Looking to deepen my knowledge and build research skills in a master's programme.</p></div>
    </div>
  </section>

  <section id="skills">
    <h2>Tech Stack</h2>
    <div class="grid g2">
      <div class="card skillbox"><h3>Frontend</h3><div class="chips"><span class="chip">Angular</span><span class="chip">TypeScript</span><span class="chip">JavaScript</span><span class="chip">HTML5</span><span class="chip">CSS3</span><span class="chip">Tailwind CSS</span><span class="chip">Material UI</span></div></div>
      <div class="card skillbox"><h3>Backend &amp; Data</h3><div class="chips"><span class="chip">Node.js</span><span class="chip">REST APIs</span><span class="chip">MongoDB</span><span class="chip">SQL</span></div></div>
      <div class="card skillbox"><h3>Tools &amp; DevOps</h3><div class="chips"><span class="chip">Git</span><span class="chip">GitHub</span><span class="chip">Bitbucket</span><span class="chip">Microsoft Azure</span><span class="chip">CI/CD</span><span class="chip">Jira</span></div></div>
      <div class="card skillbox"><h3>Practices</h3><div class="chips"><span class="chip">Code reviews</span><span class="chip">Debugging</span><span class="chip">Testing</span><span class="chip">OOP</span><span class="chip">Agile / Scrum</span></div></div>
    </div>
  </section>

  <section id="projects">
    <h2>Featured Projects</h2>
    <div class="grid g2">
      <div class="card proj">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polygon points="12 2 2 7 12 12 22 7 12 2"/><polyline points="2 17 12 22 22 17"/><polyline points="2 12 12 17 22 12"/></svg></div>
        <h3>Full-Stack App</h3>
        <p>Angular, Node.js and MongoDB app with authentication, CRUD and tests. Replace with a one-line description.</p>
        <div class="chips"><span class="chip">Angular</span><span class="chip">Node.js</span><span class="chip">MongoDB</span></div>
        <a class="link" href="https://github.com/Zaki2K2/REPO_NAME">View Repository &rarr;</a>
      </div>
      <div class="card proj">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="4" y="4" width="16" height="16" rx="2"/><rect x="9" y="9" width="6" height="6"/><path d="M9 1v3M15 1v3M9 20v3M15 20v3M20 9h3M20 14h3M1 9h3M1 14h3"/></svg></div>
        <h3>AI / ML Project</h3>
        <p>Describe the problem, dataset, method and result. Replace with your project.</p>
        <div class="chips"><span class="chip">Python</span><span class="chip">scikit-learn</span><span class="chip">Jupyter</span></div>
        <a class="link" href="https://github.com/Zaki2K2/REPO_NAME">View Repository &rarr;</a>
      </div>
      <div class="card proj">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg></div>
        <h3>Portfolio Website</h3>
        <p>My personal portfolio with projects and contact details.</p>
        <div class="chips"><span class="chip">Vercel</span></div>
        <a class="link" href="https://zaki-shah-portfolio.vercel.app">Visit Site &rarr;</a>
      </div>
      <div class="card proj">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="2" y="7" width="20" height="14" rx="2"/><path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"/></svg></div>
        <h3>CustomerCore (Work)</h3>
        <p>Multi-module Swiss fintech SaaS for accounting, invoicing, VAT, expense tracking and document workflows.</p>
        <div class="chips"><span class="chip">Angular</span><span class="chip">Node.js</span><span class="chip">Tailwind CSS</span></div>
        <div class="note">Proprietary, so no public code.</div>
      </div>
    </div>
  </section>

  <section id="experience">
    <h2>Experience</h2>
    <div class="timeline">
      <div class="item">
        <h3>Software Developer</h3><div class="role">NovaCTO &middot; Islamabad</div><div class="date">Jun 2025 &ndash; Present</div>
        <ul><li>Build reusable Angular components and responsive dashboards with Tailwind CSS and Material UI.</li><li>Develop Node.js REST APIs with input validation and optimised database queries.</li><li>Take part in sprint planning, code reviews and CI/CD with Git and Bitbucket.</li></ul>
      </div>
      <div class="item">
        <h3>Junior Web Developer</h3><div class="role">Volpea Solutions &middot; Islamabad</div><div class="date">Nov 2024 &ndash; Jun 2025</div>
        <ul><li>Converted Figma designs into accessible Angular and React interfaces.</li><li>Maintained a reusable component library and supported Azure deployments.</li></ul>
      </div>
      <div class="item">
        <h3>Junior Web Developer</h3><div class="role">Easytect UG &middot; Islamabad</div><div class="date">Jan 2022 &ndash; Feb 2023</div> <!-- confirm end date matches your CV -->
        <ul><li>Built responsive websites with HTML5, CSS3, JavaScript and PHP.</li><li>Integrated REST APIs and applied on-page SEO and performance improvements.</li></ul>
      </div>
    </div>
  </section>

  <section id="education">
    <h2>Education</h2>
    <div class="card">
      <h3>Bachelor of Science in Computer Science</h3>
      <p>Federal Urdu University of Arts, Science and Technology, Islamabad &middot; Sep 2020 &ndash; Jul 2024 &middot; CGPA 3.62 / 4.0</p>
    </div>
  </section>

  <section id="contact">
    <div class="contact">
      <h2 style="justify-content:center;margin-bottom:0">Get in Touch</h2>
      <p>Open to conversations about master's programmes, research and collaboration.</p>
      <div class="btns">
        <a class="btn primary" href="mailto:syedzaki2kk2@gmail.com">syedzaki2kk2@gmail.com</a>
        <a class="btn" href="https://www.linkedin.com/in/syed-zaki-ahmad-742b741aa">LinkedIn</a>
        <a class="btn" href="https://zaki-shah-portfolio.vercel.app">Portfolio</a>
        <a class="btn" href="https://stackoverflow.com/users/23067132/zaki-shah">Stack Overflow</a>
      </div>
    </div>
  </section>

</main>

<footer>&copy; 2026 Syed Zaki Ahmad &middot; Islamabad, Pakistan</footer>

</body>
</html>
