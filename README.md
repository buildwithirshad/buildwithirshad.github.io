# buildwithirshad.github.io
My portfolio
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Irshad · Data & Software</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=DM+Mono:wght@300;400&display=swap"
    rel="stylesheet" />
  <style>
    *,
    *::before,
    *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0
    }

    :root {
      --bg: #111;
      --bg2: #181818;
      --bg3: #1f1f1f;
      --text: #f0f0ee;
      --muted: #888;
      --border: #252525;
      --border2: #303030;
      --green: #3dff6e;
    }

    html {
      scroll-behavior: smooth
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      font-size: 15px;
      line-height: 1.65;
      overflow-x: hidden
    }

    /* NAV */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 100;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 2.5rem;
      height: 52px;
      background: rgba(17, 17, 17, 0.94);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border2);
    }

    .nav-logo {
      font-family: 'DM Mono', monospace;
      font-size: 14px;
      font-weight: 400;
      color: var(--text);
      text-decoration: none;
    }

    .nav-logo em {
      color: var(--green);
      font-style: normal
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
      align-items: center
    }

    .nav-links a {
      font-size: 13px;
      font-weight: 400;
      color: var(--muted);
      text-decoration: none;
      transition: color 0.15s;
    }

    .nav-links a:hover {
      color: var(--text)
    }

    .nav-gh {
      font-size: 12.5px;
      font-weight: 500;
      color: var(--text);
      text-decoration: none;
      border: 1px solid var(--border2);
      padding: 5px 14px;
      transition: all 0.15s;
    }

    .nav-gh:hover {
      border-color: var(--green);
      color: var(--green)
    }

    /* HERO */
    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 6rem 2.5rem 4rem;
      border-bottom: 1px solid var(--border2);
    }

    .hero-label {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      font-weight: 300;
      color: var(--green);
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 1.5rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .hero-label::before {
      content: '';
      display: block;
      width: 18px;
      height: 1px;
      background: var(--green)
    }

    h1 {
      font-size: clamp(3rem, 7vw, 6rem);
      font-weight: 600;
      line-height: 1.0;
      letter-spacing: -2px;
      color: var(--text);
      margin-bottom: 1.8rem;
    }

    h1 span {
      color: var(--green)
    }

    .hero-sub {
      font-size: 14.5px;
      color: var(--muted);
      line-height: 1.85;
      max-width: 420px;
      margin-bottom: 2.2rem;
      font-weight: 300;
    }

    .hero-ctas {
      display: flex;
      gap: 10px;
      margin-bottom: 2.8rem
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 9px 20px;
      font-size: 13px;
      font-weight: 500;
      text-decoration: none;
      cursor: pointer;
      transition: all 0.15s;
      border: 1px solid transparent;
    }

    .btn-primary {
      background: var(--green);
      color: #111;
      border-color: var(--green)
    }

    .btn-primary:hover {
      background: #5aff84
    }

    .btn-ghost {
      background: transparent;
      color: var(--text);
      border-color: var(--border2)
    }

    .btn-ghost:hover {
      border-color: var(--muted);
      color: var(--text)
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px
    }

    .tag {
      font-family: 'DM Mono', monospace;
      font-size: 10.5px;
      font-weight: 300;
      padding: 4px 10px;
      background: var(--bg2);
      border: 1px solid var(--border2);
      color: var(--muted);
      letter-spacing: 0.03em;
    }

    /* SECTIONS */
    .sec {
      border-bottom: 1px solid var(--border2)
    }

    .sec-inner {
      max-width: 1080px;
      margin: 0 auto;
      padding: 4.5rem 2.5rem
    }

    .sec-label {
      font-family: 'DM Mono', monospace;
      font-size: 10.5px;
      font-weight: 300;
      color: var(--green);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 0.5rem;
    }

    .sec-title {
      font-size: 1.5rem;
      font-weight: 600;
      letter-spacing: -0.5px;
      color: var(--text);
      margin-bottom: 2.5rem;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1px;
      background: var(--border2)
    }

    .project-card {
      background: var(--bg);
      padding: 1.8rem;
      display: flex;
      flex-direction: column;
      transition: background 0.15s;
    }

    .project-card:hover {
      background: var(--bg2)
    }

    .project-num {
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      font-weight: 300;
      color: var(--border2);
      letter-spacing: 0.1em;
      margin-bottom: 0.9rem;
    }

    .project-title {
      font-size: 0.95rem;
      font-weight: 600;
      margin-bottom: 0.5rem;
      line-height: 1.3;
      color: var(--text);
    }

    .project-desc {
      font-size: 12.5px;
      color: var(--muted);
      line-height: 1.75;
      flex: 1;
      margin-bottom: 1.2rem;
      font-weight: 300;
    }

    .project-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 5px;
      margin-bottom: 1.2rem
    }

    .stack-tag {
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      font-weight: 300;
      padding: 3px 7px;
      background: var(--bg3);
      border: 1px solid var(--border2);
      color: var(--muted);
    }

    .project-link {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      font-size: 12px;
      font-weight: 500;
      color: var(--green);
      text-decoration: none;
      transition: gap 0.15s;
    }

    .project-link:hover {
      gap: 9px
    }

    .project-link svg {
      width: 11px;
      height: 11px
    }

    /* CHATBOT */
    #chatbot {
      background: var(--bg)
    }

    .chat-wrap {
      max-width: 540px;
      border: 1px solid var(--border2);
    }

    .chat-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 11px 15px;
      border-bottom: 1px solid var(--border2);
      background: var(--bg2);
    }

    .chat-name {
      font-size: 13px;
      font-weight: 500;
      color: var(--text)
    }

    .chat-status {
      font-family: 'DM Mono', monospace;
      font-size: 10.5px;
      font-weight: 300;
      color: var(--green);
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .sdot {
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: var(--green);
      animation: pulse 2.5s ease-in-out infinite
    }

    @keyframes pulse {

      0%,
      100% {
        opacity: 1
      }

      50% {
        opacity: 0.25
      }
    }

    .chat-messages {
      padding: 14px;
      min-height: 150px;
      max-height: 250px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 9px;
    }

    .chat-messages::-webkit-scrollbar {
      width: 3px
    }

    .chat-messages::-webkit-scrollbar-thumb {
      background: var(--border2)
    }

    .msg {
      max-width: 85%;
      font-size: 13px;
      line-height: 1.65;
      padding: 9px 12px;
      animation: up 0.22s ease;
    }

    @keyframes up {
      from {
        opacity: 0;
        transform: translateY(4px)
      }

      to {
        opacity: 1;
        transform: translateY(0)
      }
    }

    .msg-bot {
      background: var(--bg2);
      color: var(--text);
      border: 1px solid var(--border2);
      align-self: flex-start
    }

    .msg-user {
      background: var(--bg3);
      color: var(--text);
      border: 1px solid var(--border2);
      align-self: flex-end
    }

    .chat-qs {
      padding: 11px 14px 14px;
      border-top: 1px solid var(--border2);
      background: var(--bg2)
    }

    .qs-label {
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      font-weight: 300;
      color: var(--muted);
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .qs-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5px
    }

    .q-btn {
      background: var(--bg);
      border: 1px solid var(--border2);
      color: var(--muted);
      font-family: 'Inter', sans-serif;
      font-size: 12px;
      font-weight: 400;
      padding: 7px 10px;
      cursor: pointer;
      text-align: left;
      transition: all 0.12s;
      line-height: 1.35;
    }

    .q-btn:hover {
      border-color: var(--green);
      color: var(--green);
      background: var(--bg)
    }

    /* FOOTER */
    footer {
      padding: 1.8rem 2.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .footer-l {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      font-weight: 300;
      color: var(--muted)
    }

    .footer-links {
      display: flex;
      gap: 1.8rem
    }

    .footer-links a {
      font-size: 12.5px;
      font-weight: 400;
      color: var(--muted);
      text-decoration: none;
      transition: color 0.15s;
    }

    .footer-links a:hover {
      color: var(--green)
    }

    @media(max-width:680px) {
      nav {
        padding: 0 1.2rem
      }

      .hero,
      .sec-inner {
        padding-left: 1.2rem;
        padding-right: 1.2rem
      }

      .projects-grid {
        grid-template-columns: 1fr
      }

      .qs-grid {
        grid-template-columns: 1fr
      }

      footer {
        padding: 1.4rem 1.2rem
      }
    }
  </style>
</head>

<body>

  <nav>
    <a class="nav-logo" href="#">Irshad Mohiuddin<em>.</em></a>
    <ul class="nav-links">
      <li><a href="#projects">Projects</a></li>
      <li><a href="#chatbot">Q&amp;A</a></li>
      <li><a href="https://github.com/buildwithirshad" target="_blank" class="nav-gh">GitHub ↗</a></li>
    </ul>
  </nav>

  <section class="hero">
    <div class="hero-label">Information Systems · Data Science</div>
    <h1>Build with<br />Irshad<span>.</span></h1>
    <p class="hero-sub">Graduate student building data pipelines, ML models, and intelligent applications. Focused on
      turning real-world data problems into working systems.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn btn-primary">View Projects</a>
      <a href="https://github.com/buildwithirshad" target="_blank" class="btn btn-ghost">GitHub ↗</a>
    </div>
    <div class="hero-tags">
      <span class="tag">Python</span>
      <span class="tag">XGBoost</span>
      <span class="tag">FastAPI</span>
      <span class="tag">PostgreSQL</span>
      <span class="tag">Docker</span>
      <span class="tag">RAG</span>
      <span class="tag">Scikit-learn</span>
      <span class="tag">React</span>
    </div>
  </section>

  <section class="sec" id="projects">
    <div class="sec-inner">
      <div class="sec-title">Projects</div>
      <div class="projects-grid">

        <div class="project-card">
          <div class="project-num">01</div>
          <div class="project-title">Intelligent Document Retrieval System</div>
          <p class="project-desc">Production-ready RAG pipeline with hybrid search via Reciprocal Rank Fusion, async
            document ingestion, Redis caching, and a Streamlit frontend.</p>
          <div class="project-stack">
            <span class="stack-tag">Python</span><span class="stack-tag">FastAPI</span>
            <span class="stack-tag">pgvector</span><span class="stack-tag">Redis</span>
            <span class="stack-tag">Celery</span><span class="stack-tag">Docker</span>
          </div>
          <a href="https://github.com/dev294" target="_blank" class="project-link">
            View on GitHub
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M7 17L17 7M17 7H7M17 7v10" />
            </svg>
          </a>
        </div>

        <div class="project-card">
          <div class="project-num">02</div>
          <div class="project-title">Credit Card Fraud Detection</div>
          <p class="project-desc">ML pipeline comparing Logistic Regression, Random Forest, and XGBoost on real
            transaction data, with SHAP explainability and cost-based threshold optimization.</p>
          <div class="project-stack">
            <span class="stack-tag">Python</span><span class="stack-tag">XGBoost</span>
            <span class="stack-tag">SHAP</span><span class="stack-tag">Scikit-learn</span>
          </div>
          <a href="https://github.com/dev294" target="_blank" class="project-link">
            View on GitHub
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M7 17L17 7M17 7H7M17 7v10" />
            </svg>
          </a>
        </div>


      </div>
    </div>
  </section>

  <section class="sec" id="chatbot">
    <div class="sec-inner">
      <div class="sec-label">Q&amp;A</div>
      <div class="sec-title">Ask me anything</div>
      <div class="chat-wrap">
        <div class="chat-header">
          <span class="chat-name">Irshad's assistant</span>
          <span class="chat-status"><span class="sdot"></span>online</span>
        </div>
        <div class="chat-messages" id="chatMessages">
          <div class="msg msg-bot">Hey! Click a question below to learn more about me.</div>
        </div>
        <div class="chat-qs">
          <div class="qs-label">Suggested</div>
          <div class="qs-grid">
            <button class="q-btn" onclick="ask(this)">What are you good at?</button>
            <button class="q-btn" onclick="ask(this)">What are you studying?</button>
            <button class="q-btn" onclick="ask(this)">What's your best project?</button>
            <button class="q-btn" onclick="ask(this)">What's your tech stack?</button>
            <button class="q-btn" onclick="ask(this)">Are you open to work?</button>
            <button class="q-btn" onclick="ask(this)">How can I contact you?</button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <span class="footer-l"></span>
    <div class="footer-links">
      <a href="https://github.com/dev294" target="_blank">GitHub</a>
      <a href="https://www.linkedin.com/in/irshad-mohiuddin/" target="_blank">LinkedIn</a>
      <a href="mailto:irshadmohiuddin01@gmail.com">Email</a>
    </div>
  </footer>

  <script>
    const answers = {
      "What are you good at?": "Building data pipelines and applied ML end-to-end — from data prep and model training to deployment. I'm comfortable across the stack: backends, APIs, and dashboards.",
      "What are you studying?": "Graduate student in Information Systems with a focus on data science. My work covers machine learning, data engineering, and NLP — always aimed at building real, working systems.",
      "What's your best project?": "The Intelligent Document Retrieval System — a production-grade RAG pipeline with hybrid search, async ingestion, and a FastAPI backend. It brings together vector databases, Redis caching, and clean software architecture.",
      "What's your tech stack?": "Python for data and ML — Scikit-learn, XGBoost, SHAP, Pandas. FastAPI and PostgreSQL for backends. Docker for deployment. React and Streamlit for frontends.",
      "Are you open to work?": "Yes — actively looking for data engineering or data science roles. Most interested in positions involving production data systems and applied ML.",
      "How can I contact you?": "LinkedIn or GitHub — links are in the footer. Happy to chat about projects and roles."
    };

    function ask(btn) {
      const q = btn.textContent.trim();
      const msgs = document.getElementById('chatMessages');
      const u = document.createElement('div');
      u.className = 'msg msg-user';
      u.textContent = q;
      msgs.appendChild(u);
      msgs.scrollTop = msgs.scrollHeight;
      setTimeout(() => {
        const b = document.createElement('div');
        b.className = 'msg msg-bot';
        b.textContent = answers[q] || "Feel free to reach out directly.";
        msgs.appendChild(b);
        msgs.scrollTop = msgs.scrollHeight;
      }, 280);
    }
  </script>
</body>

</html>
