# chowdaryrekhakommineni.github.io
My personal portfolio website showcasing my skills, projects, and experience as a Salesforce Developer.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Kommineni Rekha Chowdary — Salesforce Developer</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <meta name="description" content="Kommineni Rekha Chowdary — Salesforce Developer | 2+ years at Bruhashith OPC Pvt Ltd — Apex, LWC, Flows.">
  <style>
    :root{
      --bg:#ffffff;
      --card:#fbfbfd;
      --muted:#6b7280;
      --accent:#1e40af;
      --accent-2:#0f172a;
      --radius:12px;
      --max-width:1100px;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:'Poppins',system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;
      background:var(--bg);
      color:var(--accent-2);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.55;
    }

    /* Header / Nav */
    header{
      position:sticky;
      top:0;
      backdrop-filter: blur(6px);
      background:rgba(255,255,255,0.8);
      border-bottom:1px solid rgba(15,23,42,0.04);
      z-index:1200;
    }
    .container{
      max-width:var(--max-width);
      margin:0 auto;
      padding:18px 20px;
      display:flex;
      align-items:center;
      gap:18px;
      justify-content:space-between;
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .brand h1{
      margin:0;
      font-size:1rem;
      font-weight:700;
      letter-spacing:0.4px;
      color:var(--accent-2);
    }
    .brand .sub{font-size:12px;color:var(--muted);margin-top:2px}

    nav.primary{
      display:flex;
      gap:14px;
      align-items:center;
    }
    nav.primary a{
      color:var(--accent-2);
      text-decoration:none;
      font-weight:600;
      font-size:14px;
      padding:8px 10px;
      border-radius:8px;
    }
    nav.primary a:hover{background:rgba(30,64,175,0.06); color:var(--accent);}
    .cta{display:inline-flex;gap:8px;align-items:center}
    .btn{
      background:var(--accent);
      color:#fff;
      border:none;
      padding:8px 14px;
      border-radius:999px;
      font-weight:600;
      cursor:pointer;
      text-decoration:none;
      font-size:14px;
    }
    .btn.secondary{
      background:transparent;
      color:var(--accent-2);
      border:1px solid rgba(15,23,42,0.06);
      padding:8px 12px;
    }

    /* Mobile hamburger */
    .hamburger{
      display:none;
      width:40px;height:40px;
      align-items:center;justify-content:center;
      border-radius:8px;
      cursor:pointer;
      background:transparent;
      border:1px solid rgba(15,23,42,0.03);
    }

    /* Hero */
    .hero{
      max-width:var(--max-width);
      margin:32px auto;
      padding:30px 20px;
      display:grid;
      grid-template-columns:220px 1fr;
      gap:28px;
      align-items:center;
    }
    .profile{
      display:flex;
      align-items:center;
      justify-content:center;
      flex-direction:column;
      gap:12px;
    }
    .profile img{
      width:180px;height:180px;
      border-radius:999px;
      object-fit:cover;
      border:4px solid rgba(30,64,175,0.12);
      background:linear-gradient(180deg,#fff,#f8fafc);
    }
    .profile .contact-mini{font-size:13px;color:var(--muted);text-align:center;line-height:1.3}

    .hero-content h2{
      margin:0;
      font-size:1.45rem;
      color:var(--accent-2);
    }
    .headline{
      font-size:18px;
      font-weight:600;
      margin:8px 0 12px 0;
      color:var(--accent);
    }
    .tagline{
      color:var(--muted);
      margin-bottom:16px;
      font-size:15px;
    }
    .hero-actions{display:flex;gap:12px;flex-wrap:wrap}

    /* Section base */
    main{padding:10px 0 80px 0}
    section.card{
      max-width:var(--max-width);
      margin:28px auto;
      padding:22px;
      background:var(--card);
      border-radius:var(--radius);
      box-shadow: 0 6px 20px rgba(15,23,42,0.04);
    }
    section.card h3{margin:0 0 8px 0;color:var(--accent-2)}
    .divider{height:3px;width:70px;background:var(--accent);border-radius:8px;margin:10px 0 18px 0}

    /* Flex groups */
    .grid{display:grid;gap:18px}
    .two-col{grid-template-columns:1fr 1fr}
    .skill-badges{display:flex;flex-wrap:wrap;gap:10px}
    .badge{
      padding:8px 12px;
      background:#fff;
      border-radius:10px;
      border:1px solid rgba(15,23,42,0.04);
      font-weight:600;
      font-size:13px;
    }

    /* Experience list */
    .exp-item{padding:12px;border-radius:10px;background:#fff;border:1px solid rgba(15,23,42,0.04)}
    .exp-item h4{margin:0 0 6px 0;font-size:15px}
    .exp-item p.meta{margin:0;color:var(--muted);font-size:13px}

    /* Projects/Lists */
    ul.clean{margin:10px 0;padding-left:18px}
    ul.clean li{margin-bottom:8px;color:var(--accent-2)}

    /* Footer */
    footer{max-width:var(--max-width);margin:28px auto 60px auto;padding:18px;color:var(--muted);text-align:center;font-size:14px}

    /* Responsive */
    @media(max-width:920px){
      .hero{grid-template-columns:160px 1fr;padding:18px 20px}
      .profile img{width:140px;height:140px}
      nav.primary{display:none}
      .hamburger{display:flex}
    }
    @media(max-width:720px){
      .hero{grid-template-columns:1fr; text-align:center}
      .profile{flex-direction:column}
      .hero-content{order:2}
      .grid.two-col{grid-template-columns:1fr}
      .container{padding:12px}
    }

    /* Mobile nav overlay */
    .mobile-menu{
      display:none;
      position:fixed;
      inset:56px 18px auto 18px;
      background:var(--card);
      border-radius:12px;
      padding:14px;
      box-shadow:0 12px 40px rgba(2,6,23,0.12);
      z-index:1300;
    }
    .mobile-menu a{display:block;padding:10px 8px;border-radius:8px;color:var(--accent-2);text-decoration:none;font-weight:600}
    .mobile-menu a:hover{background:rgba(30,64,175,0.05)}
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="container">
      <div class="brand">
        <div>
          <h1>Kommineni Rekha Chowdary</h1>
          <div class="sub">Salesforce Developer &amp; Administrator</div>
        </div>
      </div>

      <nav class="primary" aria-label="Primary navigation">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#experience">Experience</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#certifications">Certifications</a>
        <a href="#education">Education</a>
        <a href="#contact">Contact</a>
      </nav>

      <div class="cta">
        <a class="btn" href="https://drive.google.com/file/d/1Wlxas7qHzKAZUDBNhBPFf6LxrMLMefMG/view?usp=drive_link" target="_blank" rel="noopener">Download Resume</a>
        <div class="hamburger" id="hamburger" aria-label="Menu" title="Menu">
          <svg width="18" height="12" viewBox="0 0 18 12" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="18" height="2" rx="1" fill="#0f172a"/><rect y="5" width="18" height="2" rx="1" fill="#0f172a"/><rect y="10" width="18" height="2" rx="1" fill="#0f172a"/></svg>
        </div>
      </div>
    </div>

    <!-- Mobile menu -->
    <div class="mobile-menu" id="mobileMenu" role="menu" aria-hidden="true">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#certifications">Certifications</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </div>
  </header>

  <!-- Hero / Home -->
  <main>
    <section id="home" class="hero" aria-labelledby="homeHeading">
      <div class="profile" role="region" aria-label="Profile">
        <img src="https://i.ibb.co/Q7T3dndL/IMG-20250514-103030.jpg" alt="Kommineni Rekha Chowdary — Profile photo">
        <div class="contact-mini">Mangalam, Tirupati • 517507</div>
        <div style="font-size:13px;color:var(--muted);margin-top:8px;">Phone: 7901266761</div>
      </div>

      <div class="hero-content">
        <h2 id="homeHeading">Kommineni Rekha Chowdary</h2>
        <div class="headline">Salesforce Developer &amp; Administrator | CRM Specialist | Apex, LWC &amp; Flows | CRM Automation &amp; Process Optimization | Java, Python, SQL &amp; Cloud Enthusiast</div>
        <div class="tagline">Salesforce Developer | 2+ years at Bruhashith OPC Pvt Ltd — Apex, LWC, Flows.</div>
        <div class="hero-actions">
          <a class="btn" href="#contact">Get In Touch</a>
          <a class="btn secondary" href="https://drive.google.com/file/d/1Wlxas7qHzKAZUDBNhBPFf6LxrMLMefMG/view?usp=drive_link" target="_blank" rel="noopener">Download Resume</a>
          <a class="btn secondary" href="https://github.com/Komminenirekha" target="_blank" rel="noopener">GitHub</a>
          <a class="btn secondary" href="https://www.linkedin.com/in/kommineni-rekha-chowdary" target="_blank" rel="noopener">LinkedIn</a>
          <a class="btn secondary" href="mailto:chowdaryrekhakommineni@gmail.com" target="_blank" rel="noopener">Email</a>

 </div>
      </div>
    </section>

    <!-- About -->
    <section id="about" class="card" aria-labelledby="aboutHeading">
      <h3 id="aboutHeading">About Me</h3>
      <div class="divider" aria-hidden="true"></div>
      <p style="margin:0;color:var(--muted);">
        I am a Salesforce Developer with 2+ years of hands-on experience in building scalable CRM solutions using Apex, Lightning Web Components (LWC), Flows, and Salesforce automation tools.
        I specialize in developing custom components, optimizing business processes, and improving CRM efficiency through secure, user-friendly configurations.
        At Bruhashith (OPC) Pvt. Ltd., I have worked on end-to-end Salesforce implementations, including process automation, user management, data security, integrations, and complex reporting needs.
      </p>
    </section>

    <!-- Experience -->
    <section id="experience" class="card" aria-labelledby="expHeading">
      <h3 id="expHeading">Professional Experience</h3>
      <div class="divider" aria-hidden="true"></div>

      <div class="grid two-col">
        <div class="exp-item">
          <h4>Salesforce Developer | Bruhashith (OPC) Pvt. Ltd., Tirupati</h4>
          <p class="meta"><strong>Oct 2023 – Present</strong></p>
          <ul class="clean">
            <li>Built and customized Lightning Web Components (LWC) and Apex classes for scalable business solutions.</li>
            <li>Automated processes using Flows, Workflows, and Approval Processes to reduce manual tasks.</li>
            <li>Managed profiles, roles, permission sets, and data security for smooth user operations.</li>
            <li>Created reports and dashboards to support data-driven decision-making.</li>
            <li>Integrated Salesforce with external systems using REST APIs and Data Loader.</li>
            <li>Performed data import/export, cleansing, and sandbox testing for stable deployments.</li>
          </ul>
        </div>

        <!-- Additional internships -->
        <div>
          <div class="exp-item" style="margin-bottom:12px;">
  <h4>Salesforce Developer Intern</h4>
  <p class="meta">Salesforce | Aug 2022 – Oct 2022</p>

  <ul class="clean">
    <li>Workflow Creation</li>
    <li>Record Management</li>
  </ul>

  <!-- View My Report Link -->
  <a href="https://drive.google.com/file/d/1FzrXradssdd0mUGUzk1hSJEgvNRoW_qX/view?usp=drive_link" 
     target="_blank"
     style="color:#1e40af; font-weight:600; text-decoration:none; display:inline-block; margin-top:6px;">
     📄View My Report
  </a>
</div>


          <div class="exp-item">
            <h4>Salesforce Administrator Intern</h4>
            <p class="meta">Salesforce | Apr 2023 – May 2023</p>
            <ul class="clean">
              <li>User Accounts Management</li>
              <li>Dashboard and Reports Creation</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills" class="card" aria-labelledby="skillsHeading">
      <h3 id="skillsHeading">Technical Skills</h3>
      <div class="divider" aria-hidden="true"></div>

      <div class="grid two-col" style="align-items:start">
        <div>
          <h4 style="margin-top:0;margin-bottom:8px">Salesforce Development</h4>
          <div class="skill-badges">
            <div class="badge">Apex</div>
            <div class="badge">Triggers</div>
            <div class="badge">Lightning Web Components (LWC)</div>
            <div class="badge">SOQL</div>
            <div class="badge">Flows</div>
          </div>

          <h4 style="margin:18px 0 8px 0">Salesforce Administration</h4>
          <div class="skill-badges">
            <div class="badge">User Management</div>
            <div class="badge">Profiles &amp; Permission Sets</div>
            <div class="badge">Validation Rules</div>
            <div class="badge">Reports &amp; Dashboards</div>
          </div>
        </div>

        <div>
          <h4 style="margin-top:0;margin-bottom:8px">Integrations &amp; Tools</h4>
          <div class="skill-badges">
            <div class="badge">REST APIs</div>
            <div class="badge">Data Loader</div>
            <div class="badge">GitHub</div>
            <div class="badge">VS Code</div>
            <div class="badge">Salesforce CLI (SFDX)</div>
          </div>

          <h4 style="margin:18px 0 8px 0">Web Technologies</h4>
          <div class="skill-badges">
            <div class="badge">HTML</div>
            <div class="badge">CSS</div>
            <div class="badge">JavaScript</div>
            <div class="badge">Java</div>
            <div class="badge">Python</div>
            <div class="badge">SQL</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects / Key Implementations -->
    <section id="projects" class="card" aria-labelledby="projectsHeading">
      <h3 id="projectsHeading">Key Implementations / Projects</h3>
      <div class="divider" aria-hidden="true"></div>

      <div class="grid">
        <div class="exp-item">
          <h4>Lead Assignment & Auto-Nurture System — Sales Cloud</h4>
<ul class="clean">
  <li>Flows & Validation Rules</li>
  <li>Reports & Dashboards</li>
</ul>

<a href="https://drive.google.com/file/d/11bCPdt8c-P0yfCQ57n4YDAj5Phf6i_Cx/view?usp=drive_link"
   target="_blank"
   style="color:#1e40af; font-weight:600; text-decoration:none; display:inline-block; margin-top:6px;">
   📄View My Report
</a>

        </div>

        <div class="exp-item">
          <h4>Case Management & Auto-Escalation — Service Cloud</h4>
<ul class="clean">
  <li>Case Automation</li>
  <li>Escalation Process</li>
</ul>

<a href="https://drive.google.com/file/d/1sLO5Bp4uKOEs3tcrDTGpSGhtSU0C8Vht/view?usp=drive_link"
   target="_blank"
   style="color:#1e40af; font-weight:600; text-decoration:none; display:inline-block; margin-top:6px;">
   📄View My Report
</a>

        </div>
      </div>
    </section>

    <!-- Certifications -->
    <section id="certifications" class="card" aria-labelledby="certsHeading">
      <h3 id="certsHeading">Certifications / Internships</h3>
      <div class="divider" aria-hidden="true"></div>

      <div class="grid two-col">
        <div class="exp-item">
          <h4>Salesforce Developer Intern</h4>
<p class="meta">Salesforce | Aug 2022 – Oct 2022</p>

<ul class="clean">
  <li>Workflow Creation</li>
  <li>Record Management</li>
</ul>

<a class="report-link" 
   href="https://smartinternz.com/internships/salesforce_certificates/8c19c8f5a3b029dbbb74fa00624201ed" 
   target="_blank"
   style="text-decoration:none; color:#1e40af; font-weight:600;">
   👉 View Certification
</a>


        </div>

        <div class="exp-item">
          <h4>Salesforce Administrator Intern</h4>
<p class="meta">Salesforce | Apr 2023 – May 2023</p>

<ul class="clean">
  <li>User Accounts Management</li>
  <li>Dashboard and Reports Creation</li>
</ul>

<a class="report-link"
   href="https://smartinternz.com/internships/salesforce_certificates/f7754be662854988d966e0e317d5553f"
   target="_blank"
   style="text-decoration:none; color:#1e40af; font-weight:600;">
   👉 View Certification
</a>

        </div>
      </div>
    </section>

    <!-- Education -->
    <section id="education" class="card" aria-labelledby="eduHeading">
      <h3 id="eduHeading">Education</h3>
      <div class="divider" aria-hidden="true"></div>

      <div class="grid two-col">
        <div class="exp-item">
          <h4>B.Com (Computer Applications)</h4>
          <p class="meta">Dr. AER Degree/PG College, Sri Venkateswara University — Sep 2023</p>
          <p style="margin:8px 0 0 0;font-weight:700">CGPA: 8.6</p>
    </section>

    <!-- Contact -->
    <section id="contact" class="card" aria-labelledby="contactHeading">
      <h3 id="contactHeading">Contact</h3>
      <div class="divider" aria-hidden="true"></div>

      <div class="grid two-col">
        <div>
          <div>
          <p style="margin:0 0 10px 0"><strong>Phone:</strong> 7901266761</p>
          <p style="margin:0 0 10px 0"><strong>Email:</strong> <a href="mailto:chowdaryrekhakommineni@gmail.com">chowdaryrekhakommineni@gmail.com</a></p>
          <p style="margin:0 0 10px 0"><strong>Location:</strong> Mangalam, Tirupati — 517507</p>
        <p style="margin:0 0 8px 0"><strong>GitHub</strong> — <a href="https://github.com/Komminenirekha" target="_blank" rel="noopener">github.com/komminenirekha</a></p>
          <p style="margin:0 0 8px 0"><strong>LinkedIn</strong> — <a href="https://www.linkedin.com/in/kommineni-rekha-chowdary" target="_blank" rel="noopener">linkedin.com/in/kommineni-rekha-chowdary</a></p>
        </div>
      

            </div>
    </section>

    <footer>
      © 2025 Kommineni Rekha Chowdary — Built with care.
    </footer>
  </main>

  <!-- Smooth scroll & Mobile menu script -->
  <script>
    // Smooth scroll for anchors
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click',function(e){
        const target = document.querySelector(this.getAttribute('href'));
        if(target){
          e.preventDefault();
          target.scrollIntoView({behavior:'smooth',block:'start'});
          // close mobile menu if open
          const menu = document.getElementById('mobileMenu');
          if(menu && menu.style.display === 'block') menu.style.display = 'none';
        }
      });
    });

    // Mobile menu toggle
    const hamburger = document.getElementById('hamburger');
    const mobileMenu = document.getElementById('mobileMenu');
    if(hamburger){
      hamburger.addEventListener('click', ()=>{
        if(mobileMenu.style.display === 'block') mobileMenu.style.display = 'none';
        else mobileMenu.style.display = 'block';
      });
    }

    // Close mobile menu on outside click
    document.addEventListener('click', function(e){
      const menu = document.getElementById('mobileMenu');
      const ham = document.getElementById('hamburger');
      if(!menu || !ham) return;
      if(e.target !== menu && !menu.contains(e.target) && e.target !== ham && !ham.contains(e.target)){
        menu.style.display = 'none';
      }
    });
  </script>
</body>
</html>
