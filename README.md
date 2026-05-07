<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Omar Elghamry – GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0e17;
    --surface: #0f1623;
    --border: #1e2d42;
    --accent: #00d4ff;
    --accent2: #7c3aed;
    --accent3: #10b981;
    --text: #e2e8f0;
    --muted: #64748b;
    --glow: rgba(0, 212, 255, 0.15);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px;
    position: relative;
    z-index: 1;
  }

  /* HEADER */
  .header {
    text-align: center;
    margin-bottom: 48px;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards;
  }

  .header .greeting {
    font-family: 'Syne', sans-serif;
    font-size: clamp(28px, 5vw, 48px);
    font-weight: 800;
    letter-spacing: -1px;
    line-height: 1.1;
  }

  .greeting .name {
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .header .tagline {
    margin-top: 12px;
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .header .tagline span {
    color: var(--accent3);
  }

  /* Typing cursor */
  .cursor {
    display: inline-block;
    width: 2px;
    height: 1em;
    background: var(--accent);
    animation: blink 1s step-end infinite;
    vertical-align: text-bottom;
    margin-left: 2px;
  }

  @keyframes blink { 50% { opacity: 0; } }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin-top: 20px;
  }

  .badge {
    padding: 4px 12px;
    border: 1px solid var(--border);
    border-radius: 4px;
    font-size: 11px;
    color: var(--muted);
    background: var(--surface);
    transition: all 0.2s;
    cursor: default;
  }

  .badge:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: 0 0 12px var(--glow);
  }

  /* SECTION */
  .section {
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.8s ease forwards;
  }

  .section:nth-child(2) { animation-delay: 0.1s; }
  .section:nth-child(3) { animation-delay: 0.2s; }
  .section:nth-child(4) { animation-delay: 0.3s; }
  .section:nth-child(5) { animation-delay: 0.4s; }
  .section:nth-child(6) { animation-delay: 0.5s; }
  .section:nth-child(7) { animation-delay: 0.6s; }

  .section-label {
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ABOUT CARDS */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  @media (max-width: 600px) { .about-grid { grid-template-columns: 1fr; } }

  .about-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    font-size: 12px;
    line-height: 1.7;
    color: var(--muted);
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
  }

  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: var(--accent);
    transform: scaleY(0);
    transition: transform 0.3s;
    transform-origin: bottom;
  }

  .about-card:hover { border-color: var(--accent); box-shadow: 0 0 20px var(--glow); }
  .about-card:hover::before { transform: scaleY(1); }
  .about-card:hover { color: var(--text); }

  .about-card .icon { font-size: 18px; margin-bottom: 8px; display: block; }
  .about-card strong { color: var(--text); font-weight: 600; }

  /* EXPERIENCE */
  .exp-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 12px;
    transition: all 0.3s;
    position: relative;
  }

  .exp-card:hover {
    border-color: var(--accent2);
    box-shadow: 0 0 24px rgba(124, 58, 237, 0.15);
    transform: translateX(4px);
  }

  .exp-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 12px;
  }

  .exp-title {
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: var(--text);
  }

  .exp-company { color: var(--accent); font-size: 12px; margin-top: 2px; }

  .exp-date {
    font-size: 10px;
    color: var(--muted);
    border: 1px solid var(--border);
    padding: 3px 8px;
    border-radius: 4px;
    white-space: nowrap;
  }

  .exp-bullets {
    list-style: none;
    font-size: 12px;
    color: var(--muted);
    line-height: 1.8;
  }

  .exp-bullets li::before {
    content: '▸ ';
    color: var(--accent3);
  }

  .exp-bullets li strong { color: var(--text); }

  /* SKILLS */
  .skill-group { margin-bottom: 20px; }

  .skill-group-label {
    font-size: 11px;
    color: var(--accent2);
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .skill-tag {
    padding: 6px 14px;
    border-radius: 4px;
    font-size: 11px;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--muted);
    cursor: default;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .skill-tag:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 16px rgba(0,0,0,0.3);
  }

  .skill-tag.backend:hover  { border-color: var(--accent);  color: var(--accent);  box-shadow: 0 4px 16px var(--glow); }
  .skill-tag.ai:hover       { border-color: var(--accent2); color: var(--accent2); box-shadow: 0 4px 16px rgba(124,58,237,0.2); }
  .skill-tag.devops:hover   { border-color: var(--accent3); color: var(--accent3); box-shadow: 0 4px 16px rgba(16,185,129,0.2); }

  /* STATS */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .stat-img {
    width: 100%;
    border-radius: 8px;
    border: 1px solid var(--border);
    display: block;
  }

  /* CONNECT */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .connect-link {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 10px 18px;
    border: 1px solid var(--border);
    border-radius: 6px;
    background: var(--surface);
    color: var(--muted);
    text-decoration: none;
    font-size: 12px;
    transition: all 0.2s;
  }

  .connect-link:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: 0 0 16px var(--glow);
    transform: translateY(-2px);
  }

  /* FOOTER */
  .footer {
    text-align: center;
    font-size: 11px;
    color: var(--muted);
    margin-top: 48px;
    padding-top: 24px;
    border-top: 1px solid var(--border);
    opacity: 0;
    animation: fadeUp 0.8s ease 0.8s forwards;
  }

  .footer span { color: var(--accent3); }

  /* README RAW SECTION */
  .readme-toggle {
    margin-top: 40px;
    text-align: center;
  }

  .toggle-btn {
    background: none;
    border: 1px solid var(--border);
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    padding: 10px 24px;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.2s;
  }

  .toggle-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: 0 0 12px var(--glow);
  }

  .readme-raw {
    display: none;
    margin-top: 20px;
    background: #060a10;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 24px;
    font-size: 11px;
    line-height: 1.8;
    color: #7dd3fc;
    white-space: pre-wrap;
    word-break: break-word;
    max-height: 500px;
    overflow-y: auto;
    text-align: left;
  }

  .readme-raw::-webkit-scrollbar { width: 4px; }
  .readme-raw::-webkit-scrollbar-track { background: var(--surface); }
  .readme-raw::-webkit-scrollbar-thumb { background: var(--border); border-radius: 2px; }

  .copy-btn {
    background: var(--accent);
    color: var(--bg);
    border: none;
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    font-weight: 700;
    padding: 8px 20px;
    border-radius: 4px;
    cursor: pointer;
    margin-top: 12px;
    transition: opacity 0.2s;
    display: none;
  }

  .copy-btn:hover { opacity: 0.8; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* Scrollbar */
  ::-webkit-scrollbar { width: 6px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }
</style>
</head>
<body>

<div class="container">

  <!-- HEADER -->
  <div class="header section">
    <div class="greeting">
      Hi, I'm <span class="name">Omar Elghamry</span> <span id="wave">👋</span>
    </div>
    <div class="tagline">
      <span id="typed-text"></span><span class="cursor"></span>
    </div>
    <div class="badge-row">
      <span class="badge">🎓 CS Student · Egypt · 2026</span>
      <span class="badge">💻 Software Engineer</span>
      <span class="badge">🤖 Agentic AI</span>
      <span class="badge">⚡ NestJS · FastAPI</span>
      <span class="badge">🌍 Open to Remote</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-label">// about me</div>
    <div class="about-grid">
      <div class="about-card">
        <span class="icon">🔧</span>
        <strong>Backend Engineering</strong><br>
        NestJS, FastAPI, PostgreSQL, RabbitMQ, Docker — building real systems for real clients.
      </div>
      <div class="about-card">
        <span class="icon">🤖</span>
        <strong>Agentic AI</strong><br>
        LangChain, LangGraph, RAG, OpenAI API, AWS Bedrock — multi-agent pipelines in production.
      </div>
      <div class="about-card">
        <span class="icon">⚡</span>
        <strong>End-to-End Ownership</strong><br>
        From architecture decisions to deployment. I own features, ship fast, and figure things out.
      </div>
      <div class="about-card">
        <span class="icon">📡</span>
        <strong>Real-time Systems</strong><br>
        Socket.IO, WebSockets, event-driven microservices with RabbitMQ topic exchanges.
      </div>
    </div>
  </div>

  <!-- EXPERIENCE -->
  <div class="section">
    <div class="section-label">// experience</div>

    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-title">Software Engineer Intern</div>
          <div class="exp-company">Techkhana</div>
        </div>
        <div class="exp-date">Jun – Nov 2025 · 360h</div>
      </div>
      <ul class="exp-bullets">
        <li>Primary engineer on <strong>Agentic AI microservice</strong> — FastAPI, LangChain, LangGraph, OpenAI, AWS Bedrock. Owned from architecture to deployment on real client systems.</li>
        <li>Built the <strong>Construction Management Platform</strong> backend — Node.js REST APIs, PostgreSQL, business logic modules.</li>
        <li>Delivered <strong>CI/CD pipelines</strong> via GitHub Actions. Containerized everything with Docker & Docker Compose.</li>
        <li>Delivered internal session: <strong>"Introduction to Deep Learning for Software Engineers"</strong>.</li>
      </ul>
    </div>

    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-title">The Smart Fashion Platform</div>
          <div class="exp-company">Graduation Project · MUST University</div>
        </div>
        <div class="exp-date">2025 – 2026</div>
      </div>
      <ul class="exp-bullets">
        <li><strong>Sole owner</strong> of the social media backend (NestJS, TypeScript, PostgreSQL, TypeORM) — 40+ REST endpoints, feeds, chat, notifications, follow system.</li>
        <li>Built <strong>Flutter mobile app</strong> for the social media service end-to-end.</li>
        <li>Designed <strong>RabbitMQ event infrastructure</strong> — durable topic exchange, auto-reconnect, message buffering across all microservices.</li>
        <li>AI recommendation engine: <strong>AUC-ROC 0.93 · 92.87% accuracy</strong> (Neural CF + content-based hybrid).</li>
      </ul>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section">
    <div class="section-label">// tech stack</div>

    <div class="skill-group">
      <div class="skill-group-label">Backend & APIs</div>
      <div class="skill-tags">
        <span class="skill-tag backend">⚡ NestJS</span>
        <span class="skill-tag backend">🐍 FastAPI</span>
        <span class="skill-tag backend">🟢 Node.js</span>
        <span class="skill-tag backend">🌱 SpringBoot</span>
        <span class="skill-tag backend">🗄 PostgreSQL</span>
        <span class="skill-tag backend">🔐 JWT Auth</span>
        <span class="skill-tag backend">📡 REST API</span>
        <span class="skill-tag backend">🔁 TypeORM</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">Messaging & Real-time</div>
      <div class="skill-tags">
        <span class="skill-tag backend">🐇 RabbitMQ</span>
        <span class="skill-tag backend">🔌 Socket.IO</span>
        <span class="skill-tag backend">📨 Event-Driven</span>
        <span class="skill-tag backend">📦 Message Buffering</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">AI & ML</div>
      <div class="skill-tags">
        <span class="skill-tag ai">🦜 LangChain</span>
        <span class="skill-tag ai">🕸 LangGraph</span>
        <span class="skill-tag ai">📚 RAG</span>
        <span class="skill-tag ai">🤖 OpenAI API</span>
        <span class="skill-tag ai">☁️ AWS Bedrock</span>
        <span class="skill-tag ai">🧠 Deep Learning</span>
        <span class="skill-tag ai">🎯 Agentic AI</span>
        <span class="skill-tag ai">🤝 Claude · Claude Code</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">DevOps & Cloud</div>
      <div class="skill-tags">
        <span class="skill-tag devops">🐳 Docker</span>
        <span class="skill-tag devops">⚙️ GitHub Actions</span>
        <span class="skill-tag devops">🚀 Heroku</span>
        <span class="skill-tag devops">☁️ AWS</span>
        <span class="skill-tag devops">🧪 Testcontainers</span>
        <span class="skill-tag devops">✅ Jest</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">Mobile</div>
      <div class="skill-tags">
        <span class="skill-tag backend">📱 Flutter</span>
        <span class="skill-tag backend">🎯 Dart</span>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-label">// github stats</div>
    <div class="stats-grid">
      <img class="stat-img" src="https://github-readme-stats.vercel.app/api?username=omaaarsh&show_icons=true&count_private=true&hide=prs&theme=tokyonight&border_color=1e2d42&bg_color=0f1623" alt="GitHub Stats" />
      <img class="stat-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=omaaarsh&layout=compact&theme=tokyonight&border_color=1e2d42&bg_color=0f1623" alt="Top Languages" />
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-label">// connect</div>
    <div class="connect-row">
      <a class="connect-link" href="mailto:omarsherifelghamry@gmail.com">📧 omarsherifelghamry@gmail.com</a>
      <a class="connect-link" href="https://www.linkedin.com/in/omar-elghamry-3a7256248/" target="_blank">🔗 LinkedIn</a>
      <a class="connect-link" href="https://github.com/omaaarsh" target="_blank">🐙 GitHub</a>
    </div>
  </div>

  <!-- README RAW -->
  <div class="readme-toggle section">
    <div class="section-label">// copy readme.md</div>
    <button class="toggle-btn" onclick="toggleReadme()">📋 Show Raw README.md</button>
    <div>
      <button class="copy-btn" id="copy-btn" onclick="copyReadme()">⎘ Copy to Clipboard</button>
    </div>
    <pre class="readme-raw" id="readme-raw"></pre>
  </div>

  <div class="footer">
    ✨ Always exploring <span>AI + Systems</span> to push boundaries 🚀
  </div>

</div>

<script>
// Typing animation
const phrases = [
  'Software Engineer · NestJS · Microservices',
  'Agentic AI Engineer · LangChain · RAG',
  'Building real products for real users',
  'FastAPI · RabbitMQ · Socket.IO · Docker',
];
let pi = 0, ci = 0, deleting = false;
const el = document.getElementById('typed-text');

function type() {
  const phrase = phrases[pi];
  if (!deleting) {
    el.textContent = phrase.slice(0, ++ci);
    if (ci === phrase.length) { deleting = true; setTimeout(type, 2000); return; }
  } else {
    el.textContent = phrase.slice(0, --ci);
    if (ci === 0) { deleting = false; pi = (pi + 1) % phrases.length; }
  }
  setTimeout(type, deleting ? 40 : 70);
}
setTimeout(type, 1000);

// Wave animation
let waving = false;
document.getElementById('wave').addEventListener('mouseenter', function() {
  if (waving) return;
  waving = true;
  this.style.display = 'inline-block';
  let t = 0;
  const interval = setInterval(() => {
    this.style.transform = `rotate(${Math.sin(t) * 25}deg)`;
    t += 0.3;
    if (t > Math.PI * 4) { clearInterval(interval); this.style.transform = ''; waving = false; }
  }, 30);
});

// README raw content
const readme = `<div align="center">

# Hi, I'm Omar Sherif Elghamry 👋

**Software Engineer · NestJS · Microservices · Agentic AI**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/omar-elghamry-3a7256248/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/omaaarsh)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:omarsherifelghamry@gmail.com)

![](https://komarev.com/ghpvc/?username=omaaarsh&color=00d4ff&style=flat)

</div>

---

## 🌟 About Me

- ⚡ Specializing in **NestJS and microservices architecture** — building scalable, event-driven backend systems
- 🤖 Hands-on **Agentic AI engineering** with LangChain, LangGraph, RAG, OpenAI API, and AWS Bedrock
- 📡 Experienced with **RabbitMQ**, **Socket.IO**, and real-time systems in production
- 🚀 I own features **end-to-end** — from architecture decisions to deployment
- 🎓 CS Student at MUST University · GPA 3.8 · Expected 2026

---

## 💼 Experience

### 🏢 Software Engineer Intern — Techkhana *(Jun – Nov 2025 · 360h)*
- Primary engineer on **Agentic AI microservice** (FastAPI, LangChain, LangGraph, OpenAI, AWS Bedrock) used by real clients
- Built the **Construction Management Platform** backend — Node.js REST APIs, PostgreSQL
- Owned **CI/CD pipelines** via GitHub Actions · Containerized with Docker & Docker Compose
- Delivered internal session: *"Introduction to Deep Learning for Software Engineers"*

### 🎓 The Smart Fashion Platform — Graduation Project *(2025 – 2026)*
- **Sole owner** of social media backend (NestJS, TypeScript, PostgreSQL) — 40+ REST endpoints
- Built **Flutter mobile app** end-to-end for the social media service
- Designed **RabbitMQ event infrastructure** — durable topic exchange, auto-reconnect, message buffering
- AI recommendation engine: **AUC-ROC 0.93 · 92.87% accuracy** (Neural CF + content-based hybrid)

---

## 🛠️ Tech Stack

**Backend & APIs**
\`NestJS\` \`FastAPI\` \`Node.js\` \`SpringBoot\` \`PostgreSQL\` \`TypeORM\` \`JWT\` \`REST API\`

**Messaging & Real-time**
\`RabbitMQ\` \`Socket.IO\` \`WebSocket\` \`Event-Driven Architecture\`

**AI & ML**
\`LangChain\` \`LangGraph\` \`RAG\` \`OpenAI API\` \`AWS Bedrock\` \`Agentic AI\` \`Deep Learning\` \`Claude\`

**DevOps & Cloud**
\`Docker\` \`Docker Compose\` \`GitHub Actions\` \`Heroku\` \`AWS\` \`Testcontainers\` \`Jest\`

**Mobile**
\`Flutter\` \`Dart\`

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=omaaarsh&show_icons=true&count_private=true&hide=prs&theme=tokyonight" />
  <br/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=omaaarsh&layout=compact&theme=tokyonight" />
</p>

---

<div align="center">
  <i>✨ Always exploring AI + Systems to push boundaries 🚀</i>
</div>`;

function toggleReadme() {
  const raw = document.getElementById('readme-raw');
  const copyBtn = document.getElementById('copy-btn');
  const btn = document.querySelector('.toggle-btn');
  if (raw.style.display === 'block') {
    raw.style.display = 'none';
    copyBtn.style.display = 'none';
    btn.textContent = '📋 Show Raw README.md';
  } else {
    raw.style.display = 'block';
    copyBtn.style.display = 'inline-block';
    raw.textContent = readme;
    btn.textContent = '✕ Hide README.md';
  }
}

function copyReadme() {
  navigator.clipboard.writeText(readme).then(() => {
    const btn = document.getElementById('copy-btn');
    btn.textContent = '✓ Copied!';
    setTimeout(() => btn.textContent = '⎘ Copy to Clipboard', 2000);
  });
}
</script>
</body>
</html>
