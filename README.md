
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;700&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .profile-root {
    font-family: var(--font-sans);
    color: var(--color-text-primary);
    padding: 2rem 1.5rem;
    max-width: 860px;
    margin: 0 auto;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes scaleIn {
    from { opacity: 0; transform: scale(0.88); }
    to   { opacity: 1; transform: scale(1); }
  }
  @keyframes slideRight {
    from { opacity: 0; transform: translateX(-20px); }
    to   { opacity: 1; transform: translateX(0); }
  }
  @keyframes pulse-ring {
    0%   { box-shadow: 0 0 0 0 rgba(55,138,221,0.35); }
    70%  { box-shadow: 0 0 0 10px rgba(55,138,221,0); }
    100% { box-shadow: 0 0 0 0 rgba(55,138,221,0); }
  }
  @keyframes shimmer {
    0%   { background-position: -200% 0; }
    100% { background-position: 200% 0; }
  }
  @keyframes barGrow {
    from { width: 0; }
  }
  @keyframes countUp {
    from { opacity: 0; }
    to   { opacity: 1; }
  }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50%       { transform: translateY(-6px); }
  }

  .hero {
    display: flex;
    align-items: center;
    gap: 2rem;
    padding: 2rem;
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    margin-bottom: 1.5rem;
    animation: fadeUp 0.6s ease both;
  }

  .avatar-wrap {
    position: relative;
    flex-shrink: 0;
  }
  .avatar {
    width: 90px; height: 90px;
    border-radius: 50%;
    background: var(--color-background-info);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Fira Code', monospace;
    font-size: 28px; font-weight: 700;
    color: var(--color-text-info);
    animation: pulse-ring 2.5s ease infinite;
  }
  .status-dot {
    position: absolute; bottom: 5px; right: 5px;
    width: 16px; height: 16px;
    background: #3B6D11;
    border-radius: 50%;
    border: 2.5px solid var(--color-background-primary);
  }

  .hero-text h1 {
    font-size: 22px; font-weight: 500;
    margin-bottom: 4px;
  }
  .hero-text .role {
    font-size: 14px;
    color: var(--color-text-secondary);
    font-family: 'Fira Code', monospace;
    margin-bottom: 12px;
  }
  .role span {
    color: var(--color-text-info);
    font-weight: 500;
  }

  .badges {
    display: flex; flex-wrap: wrap; gap: 8px;
  }
  .badge {
    display: inline-flex; align-items: center; gap: 5px;
    padding: 5px 12px;
    border-radius: var(--border-radius-md);
    font-size: 12px; font-weight: 500;
    border: 0.5px solid var(--color-border-tertiary);
    background: var(--color-background-secondary);
    color: var(--color-text-primary);
    text-decoration: none;
    transition: border-color 0.2s, transform 0.2s;
    animation: scaleIn 0.5s ease both;
  }
  .badge:hover { border-color: var(--color-border-primary); transform: translateY(-2px); }
  .badge i { font-size: 14px; color: var(--color-text-info); }

  .section-title {
    font-size: 13px; font-weight: 500;
    color: var(--color-text-secondary);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-bottom: 0.75rem;
    display: flex; align-items: center; gap: 8px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 0.5px;
    background: var(--color-border-tertiary);
  }

  .about-card {
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    padding: 1.25rem;
    margin-bottom: 1.5rem;
    animation: fadeUp 0.6s 0.1s ease both;
  }
  .about-card p {
    font-size: 14px;
    color: var(--color-text-secondary);
    line-height: 1.75;
  }
  .about-card p + p { margin-top: 8px; }
  .highlight { color: var(--color-text-info); font-weight: 500; }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 10px;
    margin-bottom: 1.5rem;
  }
  .stat-card {
    background: var(--color-background-secondary);
    border-radius: var(--border-radius-md);
    padding: 1rem;
    text-align: center;
    animation: scaleIn 0.5s ease both;
  }
  .stat-card:nth-child(1) { animation-delay: 0.05s; }
  .stat-card:nth-child(2) { animation-delay: 0.1s; }
  .stat-card:nth-child(3) { animation-delay: 0.15s; }
  .stat-card:nth-child(4) { animation-delay: 0.2s; }
  .stat-num {
    font-size: 28px; font-weight: 500;
    font-family: 'Fira Code', monospace;
    color: var(--color-text-info);
    line-height: 1.1;
  }
  .stat-label {
    font-size: 12px;
    color: var(--color-text-secondary);
    margin-top: 4px;
  }

  .skills-card {
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    padding: 1.25rem;
    margin-bottom: 1.5rem;
    animation: fadeUp 0.6s 0.15s ease both;
  }
  .skill-group { margin-bottom: 1rem; }
  .skill-group-label {
    font-size: 12px;
    color: var(--color-text-secondary);
    margin-bottom: 8px;
    font-weight: 500;
  }
  .skill-chips { display: flex; flex-wrap: wrap; gap: 6px; }
  .chip {
    padding: 4px 10px;
    border-radius: var(--border-radius-md);
    font-size: 12px;
    border: 0.5px solid var(--color-border-tertiary);
    background: var(--color-background-secondary);
    color: var(--color-text-primary);
    font-family: 'Fira Code', monospace;
    transition: border-color 0.2s, transform 0.15s;
    animation: slideRight 0.4s ease both;
  }
  .chip:hover { border-color: var(--color-border-info); transform: translateY(-2px); }
  .chip.accent { border-color: var(--color-border-info); background: var(--color-background-info); color: var(--color-text-info); }

  .skill-bar-row {
    display: flex; align-items: center; gap: 10px; margin-bottom: 8px;
  }
  .skill-bar-label { font-size: 12px; color: var(--color-text-secondary); width: 80px; flex-shrink: 0; font-family: 'Fira Code', monospace; }
  .skill-bar-track {
    flex: 1; height: 5px;
    background: var(--color-background-secondary);
    border-radius: 9999px;
    overflow: hidden;
  }
  .skill-bar-fill {
    height: 100%; border-radius: 9999px;
    background: var(--color-background-info);
    animation: barGrow 1s ease both;
  }
  .skill-bar-pct { font-size: 12px; color: var(--color-text-secondary); font-family: 'Fira Code', monospace; width: 34px; text-align: right; }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 12px;
    margin-bottom: 1.5rem;
  }
  .project-card {
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    padding: 1.1rem;
    cursor: pointer;
    transition: border-color 0.2s, transform 0.2s;
    animation: fadeUp 0.5s ease both;
    display: flex; flex-direction: column; gap: 8px;
  }
  .project-card:hover { border-color: var(--color-border-info); transform: translateY(-3px); }
  .project-card:nth-child(1) { animation-delay: 0.05s; }
  .project-card:nth-child(2) { animation-delay: 0.1s; }
  .project-card:nth-child(3) { animation-delay: 0.15s; }
  .project-card:nth-child(4) { animation-delay: 0.2s; }
  .project-card:nth-child(5) { animation-delay: 0.25s; }
  .project-card:nth-child(6) { animation-delay: 0.3s; }
  .project-header { display: flex; align-items: center; gap: 10px; }
  .project-icon {
    width: 36px; height: 36px;
    border-radius: var(--border-radius-md);
    background: var(--color-background-info);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .project-icon i { font-size: 18px; color: var(--color-text-info); }
  .project-title { font-size: 14px; font-weight: 500; }
  .project-desc { font-size: 12px; color: var(--color-text-secondary); line-height: 1.6; }
  .project-footer { display: flex; align-items: center; justify-content: space-between; margin-top: auto; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 4px; }
  .project-tag {
    font-size: 11px; padding: 2px 7px;
    border-radius: var(--border-radius-md);
    background: var(--color-background-secondary);
    color: var(--color-text-secondary);
    border: 0.5px solid var(--color-border-tertiary);
    font-family: 'Fira Code', monospace;
  }
  .project-links { display: flex; gap: 6px; flex-shrink: 0; }
  .project-link {
    display: inline-flex; align-items: center; gap: 4px;
    font-size: 11px; padding: 3px 8px;
    border-radius: var(--border-radius-md);
    border: 0.5px solid var(--color-border-secondary);
    color: var(--color-text-secondary);
    text-decoration: none;
    transition: border-color 0.2s, color 0.2s;
  }
  .project-link:hover { border-color: var(--color-border-info); color: var(--color-text-info); }
  .project-link i { font-size: 12px; }

  .floating-code {
    background: var(--color-background-secondary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    padding: 1rem 1.25rem;
    margin-bottom: 1.5rem;
    font-family: 'Fira Code', monospace;
    font-size: 13px;
    line-height: 1.8;
    animation: fadeUp 0.6s 0.2s ease both;
  }
  .code-comment { color: var(--color-text-secondary); }
  .code-key { color: var(--color-text-info); }
  .code-val { color: #3B6D11; }
  .code-str { color: #854F0B; }

  .connect-row {
    display: flex; flex-wrap: wrap; gap: 10px;
    margin-bottom: 1.5rem;
    animation: fadeUp 0.6s 0.25s ease both;
  }
  .connect-btn {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 8px 16px;
    border-radius: var(--border-radius-md);
    border: 0.5px solid var(--color-border-secondary);
    background: var(--color-background-primary);
    color: var(--color-text-primary);
    font-size: 13px; font-weight: 500;
    text-decoration: none;
    cursor: pointer;
    transition: border-color 0.2s, transform 0.2s;
  }
  .connect-btn:hover { border-color: var(--color-border-info); transform: translateY(-2px); }
  .connect-btn i { font-size: 16px; color: var(--color-text-info); }

  .footer {
    text-align: center;
    font-size: 12px;
    color: var(--color-text-secondary);
    font-family: 'Fira Code', monospace;
    padding-top: 1rem;
    border-top: 0.5px solid var(--color-border-tertiary);
    animation: fadeUp 0.5s 0.3s ease both;
  }
  .footer span { color: var(--color-text-info); }
</style>

<h2 class="sr-only">Sumanth — Full-Stack MERN Developer GitHub profile</h2>

<div class="profile-root">

  <div class="hero">
    <div class="avatar-wrap">
      <div class="avatar">S</div>
      <div class="status-dot" title="Available for opportunities"></div>
    </div>
    <div class="hero-text">
      <h1>Sumanth</h1>
      <p class="role">&lt;<span>Full-Stack</span> MERN Developer /&gt;</p>
      <div class="badges">
        <a href="https://portfolio-sumanth-wiee.onrender.com/" class="badge" target="_blank">
          <i class="ti ti-world" aria-hidden="true"></i> Portfolio
        </a>
        <a href="https://github.com/sumanth965" class="badge" target="_blank">
          <i class="ti ti-brand-github" aria-hidden="true"></i> GitHub
        </a>
        <a href="https://leetcode.com/sumanth965" class="badge" target="_blank">
          <i class="ti ti-code" aria-hidden="true"></i> LeetCode
        </a>
      </div>
    </div>
  </div>

  <div class="about-card">
    <p class="section-title">about</p>
    <p>I build full-stack applications with the <span class="highlight">MERN stack</span>, focusing on clean frontend experiences backed by robust APIs and secure authentication flows.</p>
    <p>Currently leveling up in <span class="highlight">scalable backend architecture</span>, <span class="highlight">performance optimization</span>, and <span class="highlight">cloud deployment</span> (AWS EC2, S3, Lambda, CloudFront).</p>
    <p>Career goal: ship production-ready software that matters.</p>
  </div>

  <p class="section-title">key metrics</p>
  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-num">10+</div>
      <div class="stat-label">Projects shipped</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">5+</div>
      <div class="stat-label">Tech stacks</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">DSA</div>
      <div class="stat-label">Daily practice</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">4+</div>
      <div class="stat-label">Cloud services</div>
    </div>
  </div>

  <div class="skills-card">
    <p class="section-title">core skills</p>
    <div class="skill-group">
      <div class="skill-group-label">languages &amp; frameworks</div>
      <div class="skill-chips">
        <span class="chip accent">JavaScript</span>
        <span class="chip accent">TypeScript</span>
        <span class="chip accent">React</span>
        <span class="chip accent">Node.js</span>
        <span class="chip accent">Express.js</span>
        <span class="chip">Python</span>
        <span class="chip">Java</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">databases &amp; cloud</div>
      <div class="skill-chips">
        <span class="chip accent">MongoDB</span>
        <span class="chip">AWS EC2</span>
        <span class="chip">S3</span>
        <span class="chip">Lambda</span>
        <span class="chip">CloudFront</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">tooling &amp; practices</div>
      <div class="skill-chips">
        <span class="chip">Redux</span>
        <span class="chip">Git</span>
        <span class="chip">JWT Auth</span>
        <span class="chip">REST APIs</span>
        <span class="chip">WebSocket</span>
        <span class="chip">Render</span>
        <span class="chip">Vercel</span>
        <span class="chip">Netlify</span>
      </div>
    </div>
    <div style="margin-top: 1rem;">
      <div class="skill-group-label">proficiency</div>
      <div class="skill-bar-row">
        <span class="skill-bar-label">React / JS</span>
        <div class="skill-bar-track"><div class="skill-bar-fill" style="width:90%; animation-delay:0.2s;"></div></div>
        <span class="skill-bar-pct">90%</span>
      </div>
      <div class="skill-bar-row">
        <span class="skill-bar-label">Node / API</span>
        <div class="skill-bar-track"><div class="skill-bar-fill" style="width:85%; animation-delay:0.3s;"></div></div>
        <span class="skill-bar-pct">85%</span>
      </div>
      <div class="skill-bar-row">
        <span class="skill-bar-label">MongoDB</span>
        <div class="skill-bar-track"><div class="skill-bar-fill" style="width:80%; animation-delay:0.4s;"></div></div>
        <span class="skill-bar-pct">80%</span>
      </div>
      <div class="skill-bar-row">
        <span class="skill-bar-label">TypeScript</span>
        <div class="skill-bar-track"><div class="skill-bar-fill" style="width:75%; animation-delay:0.5s;"></div></div>
        <span class="skill-bar-pct">75%</span>
      </div>
      <div class="skill-bar-row">
        <span class="skill-bar-label">AWS</span>
        <div class="skill-bar-track"><div class="skill-bar-fill" style="width:65%; animation-delay:0.6s;"></div></div>
        <span class="skill-bar-pct">65%</span>
      </div>
    </div>
  </div>

  <p class="section-title">featured projects</p>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="ti ti-building-office" aria-hidden="true"></i></div>
        <span class="project-title">Employee Leave Management</span>
      </div>
      <p class="project-desc">Enterprise leave tracking with multi-role auth, approval workflows, and dashboard analytics.</p>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">MERN</span>
          <span class="project-tag">JWT</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/sumanth965/Employee-Leave-Management-System" class="project-link" target="_blank"><i class="ti ti-brand-github"></i> code</a>
          <a href="https://elms-management.onrender.com/" class="project-link" target="_blank"><i class="ti ti-external-link"></i> demo</a>
        </div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="ti ti-target" aria-hidden="true"></i></div>
        <span class="project-title">Smart Student Productivity</span>
      </div>
      <p class="project-desc">Task management, deadline tracking, and schedule optimization for students.</p>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">React</span>
          <span class="project-tag">Node.js</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/sumanth965/smart-student-productivity-system" class="project-link" target="_blank"><i class="ti ti-brand-github"></i> code</a>
          <a href="https://smart-student-productivity-system.onrender.com/" class="project-link" target="_blank"><i class="ti ti-external-link"></i> demo</a>
        </div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="ti ti-gavel" aria-hidden="true"></i></div>
        <span class="project-title">Online Art Auction</span>
      </div>
      <p class="project-desc">Real-time digital art auction platform with WebSocket bidding and curated galleries.</p>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">MERN</span>
          <span class="project-tag">WebSocket</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/sumanth965/Online-Art-Auction" class="project-link" target="_blank"><i class="ti ti-brand-github"></i> code</a>
          <a href="https://online-art-auction.vercel.app/" class="project-link" target="_blank"><i class="ti ti-external-link"></i> demo</a>
        </div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="ti ti-chart-bar" aria-hidden="true"></i></div>
        <span class="project-title">MERN Excel Analytics</span>
      </div>
      <p class="project-desc">Converts Excel datasets into visual charts and report-ready insights.</p>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">Chart.js</span>
          <span class="project-tag">Express</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/sumanth965/MERN-excel-analytics-" class="project-link" target="_blank"><i class="ti ti-brand-github"></i> code</a>
          <a href="https://excel-analytic-sumanth09.onrender.com" class="project-link" target="_blank"><i class="ti ti-external-link"></i> demo</a>
        </div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="ti ti-shopping-bag" aria-hidden="true"></i></div>
        <span class="project-title">Foodify</span>
      </div>
      <p class="project-desc">Food delivery platform with menu handling, order flow, and admin controls.</p>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">Redux</span>
          <span class="project-tag">MERN</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/sumanth965/Foodify" class="project-link" target="_blank"><i class="ti ti-brand-github"></i> code</a>
          <a href="https://foodify-frontend-4vlo.onrender.com" class="project-link" target="_blank"><i class="ti ti-external-link"></i> demo</a>
        </div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="ti ti-device-laptop" aria-hidden="true"></i></div>
        <span class="project-title">TST Gadgets</span>
      </div>
      <p class="project-desc">E-commerce gadget storefront + admin panel for inventory and product management.</p>
      <div class="project-footer">
        <div class="project-tags">
          <span class="project-tag">E-commerce</span>
          <span class="project-tag">MERN</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/sumanth965/TST_Electronic_Gadgets-" class="project-link" target="_blank"><i class="ti ti-brand-github"></i> code</a>
          <a href="https://tst-electronic-gadgets-su-manth09.onrender.com" class="project-link" target="_blank"><i class="ti ti-external-link"></i> demo</a>
        </div>
      </div>
    </div>
  </div>

  <div class="floating-code">
    <span class="code-comment">// current focus</span><br>
    <span class="code-key">const</span> sumanth = {<br>
    &nbsp;&nbsp;stack: [<span class="code-str">"React"</span>, <span class="code-str">"Node.js"</span>, <span class="code-str">"MongoDB"</span>, <span class="code-str">"Express"</span>],<br>
    &nbsp;&nbsp;solving: <span class="code-str">"DSA daily on LeetCode"</span>,<br>
    &nbsp;&nbsp;learning: [<span class="code-str">"AWS"</span>, <span class="code-str">"TypeScript"</span>, <span class="code-str">"System Design"</span>],<br>
    &nbsp;&nbsp;goal: <span class="code-str">"High-impact Full Stack Engineer"</span><br>
    };
  </div>

  <p class="section-title">connect</p>
  <div class="connect-row">
    <a href="https://github.com/sumanth965" class="connect-btn" target="_blank">
      <i class="ti ti-brand-github" aria-hidden="true"></i> sumanth965
    </a>
    <a href="https://portfolio-sumanth-wiee.onrender.com/" class="connect-btn" target="_blank">
      <i class="ti ti-world" aria-hidden="true"></i> Portfolio
    </a>
    <a href="https://leetcode.com/sumanth965" class="connect-btn" target="_blank">
      <i class="ti ti-code" aria-hidden="true"></i> LeetCode
    </a>
    <a href="https://github.com/sumanth965/leetcode-dsa-solutions" class="connect-btn" target="_blank">
      <i class="ti ti-git-branch" aria-hidden="true"></i> DSA repo
    </a>
  </div>

  <div class="footer">
    <span>⭐ Code. Create. Contribute.</span> — if my work helps you, drop a star.
  </div>

</div>
