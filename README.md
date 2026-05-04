<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Carol — Ana Carolina Daga</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: #fdf0f5;
      font-family: 'DM Sans', sans-serif;
      color: #4a1b2e;
      min-height: 100vh;
      padding: 2rem 1rem;
    }

    .readme-root {
      max-width: 820px;
      margin: 0 auto;
    }

    /* ── HEADER ── */
    .header-card {
      background: linear-gradient(135deg, #fde8f0 0%, #fbc4d8 40%, #f8a8c8 100%);
      border-radius: 24px;
      padding: 2.5rem 2rem 2rem;
      text-align: center;
      position: relative;
      overflow: hidden;
      border: 1.5px solid #f48db4;
      margin-bottom: 1.25rem;
    }

    .cherry-deco {
      position: absolute;
      font-size: 28px;
      opacity: 0.55;
      animation: float 4s ease-in-out infinite;
    }
    .cherry-deco:nth-child(1) { top: 14px; left: 18px; animation-delay: 0s; }
    .cherry-deco:nth-child(2) { top: 10px; right: 22px; animation-delay: 1s; }
    .cherry-deco:nth-child(3) { bottom: 14px; left: 40px; animation-delay: 2s; font-size: 20px; }
    .cherry-deco:nth-child(4) { bottom: 10px; right: 35px; animation-delay: 0.5s; font-size: 22px; }
    .cherry-deco:nth-child(5) { top: 50%; left: 8px; animation-delay: 1.5s; font-size: 18px; }
    .cherry-deco:nth-child(6) { top: 45%; right: 10px; animation-delay: 2.5s; font-size: 18px; }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-6px); }
    }

    .avatar-circle {
      width: 88px;
      height: 88px;
      border-radius: 50%;
      background: linear-gradient(135deg, #e8608a, #c94070);
      border: 3px solid #fff;
      margin: 0 auto 1rem;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 30px;
      color: #fff;
      font-weight: 700;
      box-shadow: 0 4px 16px rgba(201,64,112,0.3);
    }

    .header-name {
      font-family: 'Playfair Display', serif;
      font-size: 26px;
      font-weight: 700;
      color: #7a1a3e;
      margin-bottom: 4px;
    }

    .header-tagline {
      font-size: 14px;
      color: #a0406a;
      font-weight: 400;
      margin-bottom: 1rem;
    }

    .badges-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      justify-content: center;
    }

    .badge {
      background: rgba(255,255,255,0.65);
      border: 1px solid rgba(200,80,120,0.35);
      color: #8c2b52;
      padding: 4px 13px;
      border-radius: 99px;
      font-size: 12px;
      font-weight: 500;
    }

    /* ── CARDS ── */
    .section-card {
      background: #fff8fb;
      border-radius: 18px;
      border: 1.5px solid #f4bcd4;
      padding: 1.4rem 1.5rem;
      margin-bottom: 1.25rem;
    }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: 17px;
      font-weight: 700;
      color: #9c2d55;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    /* ── SOBRE MIM ── */
    .about-text {
      font-size: 14px;
      line-height: 1.8;
      color: #5a2040;
      font-weight: 300;
    }
    .about-text strong {
      font-weight: 500;
      color: #8c2b52;
    }

    /* ── SKILLS ── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 10px;
    }

    .skill-item {
      background: linear-gradient(135deg, #fff0f5, #ffe4ef);
      border: 1px solid #f4bcd4;
      border-radius: 12px;
      padding: 10px 12px;
      display: flex;
      flex-direction: column;
      gap: 5px;
    }

    .skill-name {
      font-size: 12.5px;
      font-weight: 500;
      color: #7a1a3e;
    }

    .skill-bar-bg {
      background: #f4bcd4;
      border-radius: 99px;
      height: 5px;
      overflow: hidden;
    }

    .skill-bar-fill {
      height: 100%;
      border-radius: 99px;
      background: linear-gradient(90deg, #e8608a, #c94070);
      animation: growBar 1.4s ease forwards;
      width: 0%;
    }

    @keyframes growBar {
      to { width: var(--target-width); }
    }

    /* ── ESTUDANDO ── */
    .studying-row {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .studying-chip {
      background: linear-gradient(135deg, #f8d0e4, #f4b8d0);
      border: 1px solid #e890b8;
      border-radius: 99px;
      padding: 6px 16px;
      font-size: 13px;
      font-weight: 500;
      color: #7a1a3e;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .pulse-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: #e8608a;
      animation: pulse 1.5s infinite;
      flex-shrink: 0;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); opacity: 1; }
      50% { transform: scale(1.5); opacity: 0.55; }
    }

    /* ── GRÁFICO ── */
    .chart-area {
      display: flex;
      align-items: flex-end;
      gap: 10px;
      height: 100px;
      padding: 0 4px;
    }

    .bar-wrap {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 5px;
      height: 100%;
      justify-content: flex-end;
    }

    .bar-pct {
      font-size: 11px;
      font-weight: 500;
      color: #9c2d55;
    }

    .bar-col {
      width: 100%;
      border-radius: 6px 6px 3px 3px;
      background: linear-gradient(180deg, #f48db4, #c94070);
      animation: riseBar 1.4s ease forwards;
      height: 0;
    }

    @keyframes riseBar {
      to { height: var(--bar-h); }
    }

    .bar-label {
      font-size: 10px;
      color: #b06080;
      text-align: center;
      line-height: 1.3;
    }

    /* ── STATUS ── */
    .status-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }

    .status-box {
      background: linear-gradient(135deg, #fff0f5, #fce8f0);
      border: 1px solid #f4bcd4;
      border-radius: 12px;
      padding: 12px 14px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .status-icon { font-size: 22px; flex-shrink: 0; }

    .status-label {
      font-size: 11px;
      color: #b06080;
      margin-bottom: 2px;
    }

    .status-value {
      font-size: 13px;
      font-weight: 500;
      color: #7a1a3e;
    }

    /* ── FOOTER ── */
    .footer-note {
      text-align: center;
      font-size: 12.5px;
      color: #b06080;
      margin-top: 0.5rem;
      padding-bottom: 1rem;
      font-weight: 300;
    }
  </style>
</head>
<body>
  <div class="readme-root">

    <!-- HEADER -->
    <div class="header-card">
      <span class="cherry-deco">🍒</span>
      <span class="cherry-deco">🌸</span>
      <span class="cherry-deco">🍒</span>
      <span class="cherry-deco">🌸</span>
      <span class="cherry-deco">🍒</span>
      <span class="cherry-deco">🌸</span>

      <div class="avatar-circle">C</div>
      <div class="header-name">Ana Carolina Daga</div>
      <div class="header-tagline">✨ Desenvolvedora em formação · ADS · São José do Rio Preto, SP</div>

      <div class="badges-row">
        <span class="badge">🎓 Formada Estácio 2025</span>
        <span class="badge">💻 Web Dev</span>
        <span class="badge">🎨 UI/UX</span>
        <span class="badge">🗄️ Banco de Dados</span>
        <span class="badge">☕ Java</span>
      </div>
    </div>

    <!-- SOBRE MIM -->
    <div class="section-card">
      <div class="section-title">🌸 Sobre mim</div>
      <p class="about-text">
        Oi! Sou a <strong>Carol</strong>, programadora em desenvolvimento apaixonada por tecnologia e criação.
        Me formei em <strong>Análise e Desenvolvimento de Sistemas</strong> pela Estácio em dezembro de 2025
        e estou dando os primeiros passos na minha jornada profissional na área de TI.
        <br><br>
        Tenho experiência com <strong>front-end</strong> — HTML, CSS, JavaScript e React — e agora estou
        <strong>focando nos estudos de back-end</strong>, mergulhando em Java e MySQL.
        Adoro transformar ideias em interfaces bonitas e funcionais! 🍒
      </p>
    </div>

    <!-- CONHECIMENTOS -->
    <div class="section-card">
      <div class="section-title">🍒 Conhecimentos</div>
      <div class="skills-grid">
        <div class="skill-item">
          <div class="skill-name">🌐 HTML5</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:88%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">🎨 CSS3</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:82%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">⚡ JavaScript ES6+</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:74%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">⚛️ React.js</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:65%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">🟢 Node.js</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:58%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">🗄️ SQL</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:62%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">🐙 Git / GitHub</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:70%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">🖌️ Figma</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:68%"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-name">📐 Governança TI</div>
          <div class="skill-bar-bg"><div class="skill-bar-fill" style="--target-width:60%"></div></div>
        </div>
      </div>
    </div>

    <!-- ESTUDANDO -->
    <div class="section-card">
      <div class="section-title">🌱 Atualmente estudando</div>
      <div class="studying-row">
        <div class="studying-chip"><span class="pulse-dot"></span> ☕ Java</div>
        <div class="studying-chip"><span class="pulse-dot"></span> 🐬 MySQL</div>
        <div class="studying-chip"><span class="pulse-dot"></span> 🔧 Back-end</div>
      </div>
    </div>

    <!-- GRÁFICO -->
    <div class="section-card">
      <div class="section-title">📊 Foco de estudos</div>
      <div class="chart-area">
        <div class="bar-wrap">
          <div class="bar-pct">85%</div>
          <div class="bar-col" style="--bar-h: 85%"></div>
          <div class="bar-label">Front-end</div>
        </div>
        <div class="bar-wrap">
          <div class="bar-pct">60%</div>
          <div class="bar-col" style="--bar-h: 60%"></div>
          <div class="bar-label">Back-end</div>
        </div>
        <div class="bar-wrap">
          <div class="bar-pct">70%</div>
          <div class="bar-col" style="--bar-h: 70%"></div>
          <div class="bar-label">UI/UX</div>
        </div>
        <div class="bar-wrap">
          <div class="bar-pct">65%</div>
          <div class="bar-col" style="--bar-h: 65%"></div>
          <div class="bar-label">Banco de Dados</div>
        </div>
        <div class="bar-wrap">
          <div class="bar-pct">55%</div>
          <div class="bar-col" style="--bar-h: 55%"></div>
          <div class="bar-label">Java</div>
        </div>
      </div>
    </div>

    <!-- STATUS -->
    <div class="section-card">
      <div class="section-title">🍒 Status atual</div>
      <div class="status-grid">
        <div class="status-box">
          <span class="status-icon">🎓</span>
          <div>
            <div class="status-label">Formação</div>
            <div class="status-value">ADS — Estácio 2025</div>
          </div>
        </div>
        <div class="status-box">
          <span class="status-icon">📍</span>
          <div>
            <div class="status-label">Localização</div>
            <div class="status-value">São José do Rio Preto, SP</div>
          </div>
        </div>
        <div class="status-box">
          <span class="status-icon">🔍</span>
          <div>
            <div class="status-label">Momento</div>
            <div class="status-value">Buscando primeira oportunidade</div>
          </div>
        </div>
        <div class="status-box">
          <span class="status-icon">💡</span>
          <div>
            <div class="status-label">Interesses</div>
            <div class="status-value">Web Dev · UI/UX · TI</div>
          </div>
        </div>
      </div>
    </div>

    <div class="footer-note">🍒 feito com carinho · Carol · ADS 2025</div>

  </div>
</body>
</html>
