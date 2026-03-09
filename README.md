<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Saif Eddine Saadaoui – Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet"/>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Poppins', sans-serif;
      background: #0f1117;
      color: #e0e0e0;
    }

    /* HERO */
    .hero {
      background: linear-gradient(135deg, #1a1f2e 0%, #0f1117 60%, #1a2744 100%);
      padding: 80px 40px 60px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(30,115,255,0.15), transparent 70%);
      top: -100px; right: -100px;
      border-radius: 50%;
    }
    .avatar {
      width: 120px; height: 120px;
      border-radius: 50%;
      border: 3px solid #1e73ff;
      object-fit: cover;
      margin-bottom: 20px;
      box-shadow: 0 0 30px rgba(30,115,255,0.4);
    }
    .hero h1 {
      font-size: 2.4rem;
      font-weight: 700;
      color: #ffffff;
      margin-bottom: 8px;
    }
    .hero h1 span { color: #1e73ff; }
    .hero .subtitle {
      font-size: 1rem;
      color: #8899aa;
      margin-bottom: 24px;
    }
    .tags {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-bottom: 30px;
    }
    .tag {
      background: rgba(30,115,255,0.15);
      border: 1px solid rgba(30,115,255,0.4);
      color: #7eb8ff;
      padding: 6px 16px;
      border-radius: 20px;
      font-size: 0.82rem;
    }
    .btn-group { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }
    .btn {
      padding: 10px 24px;
      border-radius: 8px;
      font-size: 0.88rem;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s;
    }
    .btn-primary { background: #1e73ff; color: #fff; }
    .btn-primary:hover { background: #1558cc; transform: translateY(-2px); }
    .btn-outline { border: 1px solid #1e73ff; color: #1e73ff; }
    .btn-outline:hover { background: rgba(30,115,255,0.1); transform: translateY(-2px); }

    /* SECTIONS */
    section { padding: 60px 40px; max-width: 1000px; margin: 0 auto; }
    section h2 {
      font-size: 1.5rem;
      font-weight: 700;
      color: #ffffff;
      margin-bottom: 32px;
      padding-bottom: 10px;
      border-bottom: 2px solid #1e73ff;
      display: inline-block;
    }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }
    .about-card {
      background: #1a1f2e;
      border: 1px solid #2a3050;
      border-radius: 12px;
      padding: 24px;
    }
    .about-card h3 { color: #1e73ff; font-size: 0.9rem; margin-bottom: 10px; text-transform: uppercase; letter-spacing: 1px; }
    .about-card p, .about-card li { color: #aabbcc; font-size: 0.88rem; line-height: 1.7; }
    .about-card ul { padding-left: 16px; }

    /* SKILLS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 20px;
    }
    .skill-card {
      background: #1a1f2e;
      border: 1px solid #2a3050;
      border-radius: 12px;
      padding: 24px;
      transition: border-color 0.3s;
    }
    .skill-card:hover { border-color: #1e73ff; }
    .skill-card h3 { color: #ffffff; font-size: 0.95rem; margin-bottom: 14px; }
    .skill-list { display: flex; flex-wrap: wrap; gap: 8px; }
    .skill-badge {
      background: #0f1117;
      border: 1px solid #2a3050;
      color: #7eb8ff;
      padding: 4px 12px;
      border-radius: 6px;
      font-size: 0.8rem;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 24px;
    }
    .project-card {
      background: #1a1f2e;
      border: 1px solid #2a3050;
      border-radius: 12px;
      padding: 28px;
      transition: all 0.3s;
      position: relative;
      overflow: hidden;
    }
    .project-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(90deg, #1e73ff, #00c2ff);
    }
    .project-card:hover { border-color: #1e73ff; transform: translateY(-4px); }
    .project-card h3 { color: #ffffff; font-size: 1rem; margin-bottom: 10px; }
    .project-card p { color: #8899aa; font-size: 0.85rem; line-height: 1.6; margin-bottom: 16px; }
    .project-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 18px; }
    .project-tag {
      background: rgba(30,115,255,0.1);
      color: #7eb8ff;
      padding: 3px 10px;
      border-radius: 4px;
      font-size: 0.76rem;
    }
    .project-link {
      color: #1e73ff;
      text-decoration: none;
      font-size: 0.85rem;
      font-weight: 600;
    }
    .project-link:hover { color: #7eb8ff; }

    /* CONTACT */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 16px;
    }
    .contact-card {
      background: #1a1f2e;
      border: 1px solid #2a3050;
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      text-decoration: none;
      transition: all 0.3s;
    }
    .contact-card:hover { border-color: #1e73ff; transform: translateY(-3px); }
    .contact-card .icon { font-size: 1.8rem; margin-bottom: 8px; }
    .contact-card span { display: block; color: #aabbcc; font-size: 0.85rem; }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 40px;
      color: #445566;
      font-size: 0.82rem;
      border-top: 1px solid #1a1f2e;
    }

    @media (max-width: 600px) {
      .hero h1 { font-size: 1.6rem; }
      .about-grid { grid-template-columns: 1fr; }
      section { padding: 40px 20px; }
    }
  </style>
</head>
<body>

  <!-- HERO -->
  <div class="hero">
    <img src="images/profile.jpg" alt="Saif" class="avatar" onerror="this.src='https://ui-avatars.com/api/?name=Saif+Saadaoui&background=1e73ff&color=fff&size=120'"/>
    <h1>Saif Eddine <span>Saadaoui</span></h1>
    <p class="subtitle">Étudiant en Développement des Systèmes d'Information — ISET</p>
    <div class="tags">
      <span class="tag">🤖 IA Générative</span>
      <span class="tag">🎙️ STT / TTS</span>
      <span class="tag">📞 IPBX / Asterisk</span>
      <span class="tag">⚛️ React & Angular</span>
      <span class="tag">🔷 .NET / ASP.NET Core</span>
    </div>
    <div class="btn-group">
      <a href="https://github.com/saadaoui123" class="btn btn-primary" target="_blank">GitHub</a>
      <a href="https://github.com/saadaoui123/saif-pfe-repondeur-intelligent" class="btn btn-outline" target="_blank">Projet PFE</a>
    </div>
  </div>

  <!-- ABOUT -->
  <section>
    <h2>👤 À propos</h2>
    <div class="about-grid">
      <div class="about-card">
        <h3>Profil</h3>
        <p>Étudiant en fin de cycle en Développement des Systèmes d'Information à l'ISET. Passionné par la création de systèmes intelligents et interactifs, notamment dans les domaines de l'IA générative et des solutions IPBX.</p>
      </div>
      <div class="about-card">
        <h3>Centres d'intérêt</h3>
        <ul>
          <li>IA générative & LLM (Mistral, GPT)</li>
          <li>Systèmes STT / TTS en temps réel</li>
          <li>Solutions IPBX & Asterisk</li>
          <li>Développement Web Full Stack</li>
          <li>Automatisation & pipelines intelligents</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section>
    <h2>🛠️ Compétences</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <h3>Frontend</h3>
        <div class="skill-list">
          <span class="skill-badge">React</span>
          <span class="skill-badge">Angular</span>
          <span class="skill-badge">HTML5</span>
          <span class="skill-badge">CSS3</span>
          <span class="skill-badge">JavaScript</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>Backend</h3>
        <div class="skill-list">
          <span class="skill-badge">Node.js</span>
          <span class="skill-badge">ASP.NET Core</span>
          <span class="skill-badge">.NET</span>
          <span class="skill-badge">Python</span>
          <span class="skill-badge">REST API</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>IA & Voix</h3>
        <div class="skill-list">
          <span class="skill-badge">Vosk STT</span>
          <span class="skill-badge">Mistral 7B</span>
          <span class="skill-badge">Ollama</span>
          <span class="skill-badge">edge-tts</span>
          <span class="skill-badge">Prompt Engineering</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>Téléphonie & Outils</h3>
        <div class="skill-list">
          <span class="skill-badge">Asterisk</span>
          <span class="skill-badge">AudioSocket</span>
          <span class="skill-badge">Zoiper5</span>
          <span class="skill-badge">Git</span>
          <span class="skill-badge">Linux</span>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section>
    <h2>🚀 Projets</h2>
    <div class="projects-grid">
      <div class="project-card">
        <h3>Répondeur Téléphonique Intelligent</h3>
        <p>Système de réponse automatique pour cabinet dentaire. Pipeline complet STT → LLM → TTS intégré avec Asterisk PBX. 158 scénarios patients, détection d'intent, réponses contextuelles.</p>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">Vosk</span>
          <span class="project-tag">Mistral 7B</span>
          <span class="project-tag">Asterisk</span>
          <span class="project-tag">edge-tts</span>
        </div>
        <a href="https://github.com/saadaoui123/saif-pfe-repondeur-intelligent" class="project-link" target="_blank">→ Voir sur GitHub</a>
      </div>
      <div class="project-card">
        <h3>Portfolio Professionnel</h3>
        <p>Portfolio interactif moderne développé en HTML & CSS. Responsive design, déployé sur GitHub Pages.</p>
        <div class="project-tags">
          <span class="project-tag">HTML5</span>
          <span class="project-tag">CSS3</span>
          <span class="project-tag">GitHub Pages</span>
        </div>
        <a href="https://github.com/saadaoui123" class="project-link" target="_blank">→ Voir sur GitHub</a>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section>
    <h2>📬 Contact</h2>
    <div class="contact-grid">
      <a href="https://github.com/saadaoui123" class="contact-card" target="_blank">
        <div class="icon">🐙</div>
        <span>GitHub</span>
        <span>saadaoui123</span>
      </a>
      <a href="mailto:saif@example.com" class="contact-card">
        <div class="icon">📧</div>
        <span>Email</span>
        <span>saif@example.com</span>
      </a>
      <a href="https://linkedin.com/in/saif-saadaoui" class="contact-card" target="_blank">
        <div class="icon">💼</div>
        <span>LinkedIn</span>
        <span>saif-saadaoui</span>
      </a>
      <a href="https://github.com/saadaoui123/saif-pfe-repondeur-intelligent" class="contact-card" target="_blank">
        <div class="icon">🤖</div>
        <span>Projet PFE</span>
        <span>Répondeur IA</span>
      </a>
    </div>
  </section>

  <footer>
    <p>© 2026 Saif Eddine Saadaoui — Développé avec ❤️ | ISET / DKSoft</p>
  </footer>

</body>
</html>
