
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Talha Ibne Anich — Cybersecurity Portfolio</title>
  <meta name="description" content="Portfolio of Talha Ibne Anich — aspiring cybersecurity professional (Jr. Penetration Tester)." />
  <meta name="color-scheme" content="light dark">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b1015;
      --panel: #0f1720;
      --text: #e6edf3;
      --muted: #9fb0c3;
      --brand: #5eead4; /* teal-300 */
      --brand-2: #60a5fa; /* blue-400 */
      --chip: rgba(94,234,212,0.12);
      --border: rgba(148,163,184,0.2);
      --shadow: 0 10px 25px rgba(0,0,0,.35);
    }
    @media (prefers-color-scheme: light) {
      :root { --bg: #f7fafc; --panel: #ffffff; --text: #0b1015; --muted: #475569; --border: rgba(2,6,23,0.08); --chip: rgba(99,102,241,0.08);} 
    }
    * { box-sizing: border-box; }
    html, body { height: 100%; }
    body {
      margin: 0; font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      background: radial-gradient(1200px 600px at 80% -10%, rgba(96,165,250,.18), transparent),
                  radial-gradient(1200px 600px at -10% 10%, rgba(94,234,212,.14), transparent),
                  var(--bg);
      color: var(--text);
      line-height: 1.65;
    }
    a { color: inherit; text-decoration: none; }
    .container { max-width: 1080px; margin: 0 auto; padding: 24px; }
    header {
      position: sticky; top: 0; z-index: 50;
      backdrop-filter: saturate(140%) blur(8px);
      background: color-mix(in oklab, var(--bg) 90%, transparent);
      border-bottom: 1px solid var(--border);
    }
    nav { display: flex; align-items: center; justify-content: space-between; gap: 16px; }
    .brand { font-weight: 800; letter-spacing: .5px; }
    .brand span { background: linear-gradient(90deg, var(--brand), var(--brand-2)); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .navlinks { display: flex; gap: 16px; flex-wrap: wrap; }
    .navlinks a { padding: 8px 12px; border-radius: 999px; border: 1px solid transparent; }
    .navlinks a:hover { border-color: var(--border); background: color-mix(in oklab, var(--panel) 85%, transparent); }
    .btn { display: inline-flex; align-items: center; gap: 10px; padding: 12px 16px; border-radius: 14px; border: 1px solid var(--border); background: linear-gradient(180deg, color-mix(in oklab, var(--panel) 93%, transparent), color-mix(in oklab, var(--panel) 98%, transparent)); box-shadow: var(--shadow); }
    .btn:hover { transform: translateY(-1px); box-shadow: 0 14px 28px rgba(0,0,0,.35); }
    .hero { display: grid; grid-template-columns: 1.2fr .8fr; gap: 28px; padding: 48px 0; align-items: center; }
    .badge { display: inline-block; padding: 6px 10px; border-radius: 999px; background: var(--chip); border: 1px solid var(--border); color: var(--brand); font-weight: 600; font-size: 12px; letter-spacing:.3px; }
    h1 { font-size: clamp(28px, 4vw, 46px); line-height: 1.15; margin: 12px 0 8px; }
    .subtitle { color: var(--muted); font-size: clamp(14px, 1.8vw, 18px); }
    .kpis { display: flex; gap: 16px; margin-top: 18px; flex-wrap: wrap; }
    .kpis .chip { padding: 10px 12px; border-radius: 999px; background: var(--chip); border: 1px solid var(--border); color: var(--text); }
    .card { background: color-mix(in oklab, var(--panel) 92%, transparent); border: 1px solid var(--border); border-radius: 18px; padding: 20px; box-shadow: var(--shadow); }
    section { padding: 16px 0 40px; }
    h2 { font-size: 22px; margin: 0 0 14px; }
    .grid { display: grid; gap: 16px; }
    .grid.cols-3 { grid-template-columns: repeat(3,minmax(0,1fr)); }
    .grid.cols-2 { grid-template-columns: repeat(2,minmax(0,1fr)); }
    .skills { display:flex; flex-wrap: wrap; gap: 10px; }
    .skills .pill { padding: 8px 12px; border-radius: 999px; border: 1px solid var(--border); background: color-mix(in oklab, var(--panel) 90%, transparent); }
    .item { display: grid; grid-template-columns: 1fr auto; gap: 6px; }
    .item .role { font-weight: 600; }
    .item .org { color: var(--muted); }
    .item .meta { color: var(--muted); font-size: 14px; }
    .list { display: grid; gap: 10px; }
    footer { border-top: 1px solid var(--border); padding: 24px 0 40px; color: var(--muted); }
    .contact-btns { display:flex; gap:12px; flex-wrap: wrap; margin-top: 18px; }
    .avatar {
      width: 180px; height: 180px; border-radius: 24px; border: 1px solid var(--border);
      background: linear-gradient(135deg, rgba(96,165,250,.18), rgba(94,234,212,.10));
      display: grid; place-items: center; font-weight: 700; letter-spacing: 1px;
    }
    .sr-only { position: absolute; width: 1px; height: 1px; padding: 0; margin: -1px; overflow: hidden; clip: rect(0,0,0,0); white-space: nowrap; border: 0; }
    .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
    @media (max-width: 900px){ .hero{ grid-template-columns: 1fr; } .grid.cols-3{ grid-template-columns: 1fr; } .grid.cols-2{ grid-template-columns: 1fr; } .two-col{ grid-template-columns: 1fr; } }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav aria-label="Main">
        <div class="brand">Talha <span>Ibne Anich</span></div>
        <div class="navlinks">
          <a href="#about">About</a>
          <a href="#skills">Skills</a>
          <a href="#experience">Experience</a>
          <a href="#education">Education</a>
          <a href="#certs">Certifications</a>
          <a href="#references">References</a>
          <a href="#contact" class="btn">Contact</a>
        </div>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div>
        <span class="badge">Jr. Penetration Tester • Cybersecurity Enthusiast</span>
        <h1>Securing what matters, one vulnerability at a time.</h1>
        <p class="subtitle">Aspiring cybersecurity professional with a creative mindset and strong teamwork skills, eager to contribute to securing digital assets and driving innovation.</p>
        <div class="kpis">
          <span class="chip">Windows &amp; Linux Admin</span>
          <span class="chip">Python • C/C++ (academic)</span>
          <span class="chip">Networking: IP, Subnetting, DNS, DHCP</span>
        </div>
        <div class="contact-btns">
          <a class="btn" href="mailto:talhaanich121@gmail.com" aria-label="Send email">📧 Email</a>
          <a class="btn" href="tel:+8801725354196" aria-label="Call phone">📞 Call</a>
          <a class="btn" href="https://linkedin.com/in/talha-ibne-anich-" target="_blank" rel="noopener" aria-label="Open LinkedIn">🔗 LinkedIn</a>
          <!-- Replace the href below with the public URL to your PDF resume when you publish -->
          <a class="btn" href="/home/piki/Downloads/Talha cv.pdf" download>⬇️ Download CV</a>
        </div>
      </div>
      <div class="card avatar" aria-hidden="true">
        <img src="/home/talha/Downloads/6188211880082916439.jpg" alt="Talha Ibne Anich photo" style="width:100%; height:auto; border-radius:12px;">
      </div>
      
    </section>

    <section id="about">
      <div class="two-col card">
        <div>
          <h2>About</h2>
          <p>I thrive in collaborative environments, bringing dedication, problem‑solving, and continuous learning to create value for both the organization and my own growth.</p>
        </div>
        <div>
          <h2>Contact</h2>
          <ul class="list" style="margin:0; padding-left: 18px;">
            <li><strong>Phone:</strong> +880 1725‑354196</li>
            <li><strong>Email:</strong> <a href="mailto:talhaanich121@gmail.com">talhaanich121@gmail.com</a></li>
            <li><strong>Address:</strong> Kolabagan Bus Stand, Dhanmondi</li>
            <li><strong>LinkedIn:</strong> <a target="_blank" rel="noopener" href="https://linkedin.com/in/talha-ibne-anich-">linkedin.com/in/talha-ibne-anich-</a></li>
          </ul>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="card">
        <h2>Skills</h2>
        <div class="skills">
          <span class="pill">Ethical Hacking (beginner)</span>
          <span class="pill">Network Security Fundamentals</span>
          <span class="pill">Windows Administration</span>
          <span class="pill">Linux Administration</span>
          <span class="pill">Virtual Machines (VMware, VirtualBox)</span>
          <span class="pill">Python (basic scripting)</span>
          <span class="pill">C / C++ (academic)</span>
          <span class="pill">Troubleshooting (HW/SW)</span>
          <span class="pill">Computer Networking</span>
          <span class="pill">MS Office / Google Workspace</span>
        </div>
      </div>
    </section>

    <section id="experience">
      <div class="card">
        <h2>Experience</h2>
        <div class="list">
          <div class="item">
            <div>
              <div class="role">Cybersecurity Intern</div>
              <div class="org">Byte Capsule</div>
              <div class="meta">Running</div>
              <ul>
                <li>Assist in real‑world cybersecurity projects; contribute to system security and threat analysis.</li>
                <li>Support senior professionals in identifying vulnerabilities and applying security measures.</li>
                <li>Practice teamwork, problem‑solving, and professional communication.</li>
              </ul>
            </div>
            <div class="meta">Present</div>
          </div>
        </div>
      </div>
    </section>

    <section id="education" class="grid cols-2">
      <div class="card">
        <h2>Education</h2>
        <div class="list">
          <div class="item">
            <div>
              <div class="role">Diploma in Computer Science &amp; Engineering</div>
              <div class="org">Bangladesh Sweden Polytechnic Institute</div>
              <div class="meta">2021 – Present </div>
              
            </div>
          </div>
          <div class="item">
            <div>
              <div class="role">Secondary Education</div>
              <div class="org">Hosna‑Hossain Technical Institute</div>
              <div class="meta">2016 – 2021• GPA: 4.71</div>
              <div class="meta">Computer Technology</div>
            </div>
          </div>
        </div>
      </div>

      <div class="card" id="certs">
        <h2>Achievements &amp; Certifications</h2>
        <ul class="list">
          <li><strong>ISC2 – CC (Domain 1: Security Principles)</strong> — Valid 3 years</li>
          <li><strong>Hack &amp; Fix Academy</strong> — Certified Governance Risk and Compliance Analyst (CGRCA), Mar 9, 2025</li>
          <li><strong>Hack &amp; Fix Academy</strong> — Certified Cybersecurity Fundamentals Specialist (CCFS), Mar 8, 2025</li>
          <li><strong>Muktopaath</strong> — ICT &amp; Digital Skills (ID: MC‑D1P9105557O106L)</li>
          <li><strong>BCS ICT Fest 2025</strong> — CTF Participation (Feb 15, 2025)</li>
        </ul>
      </div>
    </section>

    <section id="references">
      <div class="card">
        <h2>References</h2>
        <div class="grid cols-2">
          <div>
            <div class="role">ENGR. MOHAMMAD TAREQUL ISLAM</div>
            <div class="org">Head, Dept. of Computer Science &amp; Technology</div>
            <div class="meta">Bangladesh Sweden Polytechnic Institute</div>
            <div>Email: <a href="mailto:tareq.bspi@gmail.com">tareq.bspi@gmail.com</a></div>
            <div>Phone: 01811‑88342</div>
          </div>
          <div>
            <div class="role">Engr. Sakib Haque Zisan</div>
            <div class="org">Cybersecurity Team Lead &amp; CEO, Byte Capsule</div>
            <div>Email: <a href="mailto:pentest@bytecapsuleit.com">pentest@bytecapsuleit.com</a></div>
            <div>Phone: 01796‑934898</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Optional Projects section: uncomment and add when ready -->
    <!--
    <section id="projects">
      <div class="card">
        <h2>Projects</h2>
        <div class="grid cols-3">
          <article class="card">
            <h3>Lab: Vulnerability Scan Walkthrough</h3>
            <p>Short description of tools & findings.</p>
            <a class="btn" href="#">View</a>
          </article>
          <article class="card">
            <h3>TryHackMe / HTB Notes</h3>
            <p>Curated notes and writeups.</p>
            <a class="btn" href="#">View</a>
          </article>
          <article class="card">
            <h3>Python: Log Parser</h3>
            <p>Simple parser for auth logs.</p>
            <a class="btn" href="#">GitHub</a>
          </article>
        </div>
      </div>
    </section>
    -->

    <section id="contact">
      <div class="card">
        <h2>Contact</h2>
        <p>Open for internships, entry‑level roles, and collaboration.</p>
        <div class="contact-btns">
          <a class="btn" href="mailto:talhaanich121@gmail.com">📧 talhaanich121@gmail.com</a>
          <a class="btn" href="https://linkedin.com/in/talha-ibne-anich-" target="_blank" rel="noopener">🔗 LinkedIn</a>
          <a class="btn" href="tel:+8801725354196">📞 +880 1725‑354196</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div style="display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap;">
        <div>© <span id="year"></span> Talha Ibne Anich</div>
        <div>Built with semantic HTML • Responsive • Single file</div>
      </div>
    </div>
  </footer>

  <script>
    // current year
    document.getElementById('year').textContent = new Date().getFullYear();
    // smooth scroll for internal links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id=a.getAttribute('href');
        if(id.length>1){ e.preventDefault(); document.querySelector(id).scrollIntoView({behavior:'smooth'}); }
      });
    });
  </script>
</body>
</html>
