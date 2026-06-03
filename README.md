# Meu-site
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Nexus | Inovação Digital</title>
  <!-- Font Awesome 6 (ícones) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts: Inter + fallback -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
      background-color: #fefefe;
      color: #1e293b;
      line-height: 1.5;
      scroll-behavior: smooth;
    }

    /* Variáveis de cor */
    :root {
      --primary: #4f46e5;
      --primary-dark: #4338ca;
      --secondary: #0ea5e9;
      --accent: #8b5cf6;
      --gray-100: #f8fafc;
      --gray-200: #e2e8f0;
      --gray-700: #334155;
      --gray-900: #0f172a;
      --shadow-sm: 0 10px 25px -5px rgba(0, 0, 0, 0.05), 0 8px 10px -6px rgba(0, 0, 0, 0.02);
      --shadow-md: 0 20px 25px -12px rgba(0, 0, 0, 0.08);
      --radius-lg: 1.5rem;
      --radius-md: 1rem;
    }

    /* Container centralizado */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* Header / Navegação */
    .navbar {
      background-color: rgba(255, 255, 255, 0.96);
      backdrop-filter: blur(8px);
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.03);
      position: sticky;
      top: 0;
      z-index: 50;
      border-bottom: 1px solid rgba(226, 232, 240, 0.6);
    }

    .nav-container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      padding: 1rem 1.5rem;
      max-width: 1280px;
      margin: 0 auto;
    }

    .logo {
      font-size: 1.7rem;
      font-weight: 800;
      background: linear-gradient(135deg, #4f46e5, #8b5cf6);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      letter-spacing: -0.02em;
    }

    .logo span {
      background: none;
      color: #1e293b;
      background-clip: unset;
      -webkit-background-clip: unset;
    }

    /* Botão menu mobile */
    .menu-toggle {
      background: none;
      border: none;
      font-size: 1.8rem;
      color: #1e293b;
      cursor: pointer;
      display: none;
      transition: transform 0.2s;
    }

    .menu-toggle:hover {
      color: #4f46e5;
    }

    /* Links de navegação */
    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
      align-items: center;
    }

    .nav-links a {
      text-decoration: none;
      font-weight: 500;
      color: #334155;
      transition: color 0.2s ease;
      font-size: 1rem;
    }

    .nav-links a:hover {
      color: #4f46e5;
    }

    .btn-outline-light {
      background: transparent;
      border: 1.5px solid #cbd5e1;
      padding: 0.5rem 1.2rem;
      border-radius: 2rem;
      font-weight: 600;
    }

    .btn-outline-light:hover {
      border-color: #4f46e5;
      background: #f5f3ff;
    }

    /* Botões globais */
    .btn-primary {
      display: inline-block;
      background: linear-gradient(105deg, #4f46e5, #7c3aed);
      color: white;
      font-weight: 600;
      padding: 0.9rem 2rem;
      border-radius: 3rem;
      text-decoration: none;
      box-shadow: 0 4px 10px rgba(79, 70, 229, 0.25);
      transition: all 0.25s ease;
      border: none;
      cursor: pointer;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 20px -10px rgba(79, 70, 229, 0.4);
      background: linear-gradient(105deg, #4338ca, #6d28d9);
    }

    .btn-secondary {
      background: white;
      color: #4f46e5;
      font-weight: 600;
      padding: 0.85rem 2rem;
      border-radius: 3rem;
      text-decoration: none;
      border: 1.5px solid #e2e8f0;
      transition: all 0.2s;
      display: inline-block;
    }

    .btn-secondary:hover {
      border-color: #4f46e5;
      background: #f8fafc;
      transform: translateY(-2px);
    }

    /* Hero */
    .hero {
      padding: 5rem 0 5rem 0;
      background: linear-gradient(125deg, #ffffff 0%, #f1f5fe 100%);
    }

    .hero-grid {
      display: flex;
      align-items: center;
      gap: 3rem;
      flex-wrap: wrap;
    }

    .hero-content {
      flex: 1.2;
    }

    .hero-badge {
      background: #e0e7ff;
      color: #4f46e5;
      display: inline-block;
      padding: 0.3rem 1rem;
      border-radius: 2rem;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 1.5rem;
    }

    .hero-content h1 {
      font-size: 3.5rem;
      font-weight: 800;
      line-height: 1.2;
      letter-spacing: -0.02em;
      background: linear-gradient(to right, #0f172a, #4f46e5);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 1.2rem;
    }

    .hero-content p {
      font-size: 1.2rem;
      color: #475569;
      max-width: 90%;
      margin-bottom: 2rem;
    }

    .hero-buttons {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .hero-image {
      flex: 0.9;
      background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 400"><rect width="500" height="400" fill="%23eef2ff" rx="30"/><circle cx="250" cy="180" r="70" fill="%238b5cf6" opacity="0.2"/><circle cx="350" cy="270" r="50" fill="%234f46e5" opacity="0.2"/><path d="M150,280 L350,280 L300,340 L200,340 Z" fill="%234f46e5" opacity="0.3"/><rect x="200" y="140" width="100" height="30" rx="12" fill="%234f46e5" opacity="0.4"/></svg>');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: center;
      min-height: 280px;
      border-radius: 2rem;
    }

    /* Seções padrão */
    section {
      padding: 5rem 0;
    }

    .section-title {
      font-size: 2.2rem;
      font-weight: 700;
      text-align: center;
      margin-bottom: 1rem;
      letter-spacing: -0.01em;
    }

    .section-sub {
      text-align: center;
      color: #5b6e8c;
      max-width: 680px;
      margin: 0 auto 3rem auto;
      font-size: 1.1rem;
    }

    /* Features cards */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
      margin-top: 1rem;
    }

    .feature-card {
      background: white;
      border-radius: var(--radius-md);
      padding: 2rem 1.5rem;
      box-shadow: var(--shadow-sm);
      transition: all 0.3s ease;
      border: 1px solid #edf2f7;
      text-align: center;
    }

    .feature-card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow-md);
      border-color: #cbdffc;
    }

    .icon-bg {
      background: #eef2ff;
      width: 70px;
      height: 70px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 2rem;
      margin: 0 auto 1.5rem auto;
    }

    .icon-bg i {
      font-size: 2rem;
      color: #4f46e5;
    }

    .feature-card h3 {
      font-size: 1.5rem;
      margin-bottom: 0.75rem;
    }

    .feature-card p {
      color: #475569;
    }

    /* Projetos */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    .project-card {
      background: white;
      border-radius: 1.2rem;
      overflow: hidden;
      transition: all 0.25s;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
      border: 1px solid #eef2ff;
    }

    .project-card:hover {
      transform: scale(1.02);
      box-shadow: 0 20px 30px -12px rgba(0, 0, 0, 0.1);
    }

    .project-img {
      background: linear-gradient(145deg, #c7d2fe, #a5b4fc);
      height: 180px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .project-img i {
      font-size: 3.5rem;
      color: white;
      text-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .project-info {
      padding: 1.5rem;
    }

    .project-info h3 {
      font-size: 1.35rem;
      margin-bottom: 0.5rem;
    }

    .tag {
      background: #eef2ff;
      color: #4f46e5;
      padding: 0.2rem 0.8rem;
      border-radius: 2rem;
      font-size: 0.75rem;
      font-weight: 600;
      display: inline-block;
      margin-top: 0.8rem;
    }

    /* Sobre + contato mix */
    .about-contact {
      background: #f8fafd;
    }

    .flex-about {
      display: flex;
      flex-wrap: wrap;
      gap: 3rem;
      align-items: center;
    }

    .about-text {
      flex: 1;
    }

    .about-text h3 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    .stats {
      display: flex;
      gap: 2rem;
      margin: 2rem 0 0;
    }

    .stat-item h4 {
      font-size: 2rem;
      color: #4f46e5;
    }

    .contact-form {
      flex: 1;
      background: white;
      padding: 2rem;
      border-radius: 1.5rem;
      box-shadow: var(--shadow-sm);
    }

    .form-group {
      margin-bottom: 1.25rem;
    }

    .form-group input, .form-group textarea {
      width: 100%;
      padding: 0.9rem 1rem;
      border: 1px solid #e2e8f0;
      border-radius: 1rem;
      font-family: inherit;
      transition: 0.2s;
    }

    .form-group input:focus, .form-group textarea:focus {
      outline: none;
      border-color: #4f46e5;
      box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.1);
    }

    button[type="submit"] {
      width: 100%;
      cursor: pointer;
      font-size: 1rem;
    }

    /* Footer */
    footer {
      background: #0f172a;
      color: #cbd5e1;
      padding: 2rem 0;
      text-align: center;
    }

    .footer-social {
      display: flex;
      justify-content: center;
      gap: 1.8rem;
      margin-bottom: 1.2rem;
    }

    .footer-social a {
      color: #94a3b8;
      font-size: 1.4rem;
      transition: color 0.2s;
    }

    .footer-social a:hover {
      color: #a78bfa;
    }

    /* Responsivo */
    @media (max-width: 768px) {
      .nav-container {
        flex-wrap: wrap;
      }
      .menu-toggle {
        display: block;
      }
      .nav-links {
        display: none;
        width: 100%;
        flex-direction: column;
        gap: 1.2rem;
        padding: 1.5rem 0 1rem 0;
        background: white;
      }
      .nav-links.show {
        display: flex;
      }
      .hero-content h1 {
        font-size: 2.4rem;
      }
      .hero-content p {
        max-width: 100%;
      }
      .hero-grid {
        flex-direction: column;
      }
      .section-title {
        font-size: 1.9rem;
      }
      .stats {
        flex-direction: column;
        gap: 1rem;
      }
    }

    @media (min-width: 769px) {
      .nav-links {
        display: flex !important;
      }
    }
  </style>
</head>
<body>

<!-- Navegação fixa -->
<header class="navbar">
  <div class="nav-container">
    <div class="logo">NEXUS<span>.</span></div>
    <button class="menu-toggle" id="mobileMenuBtn" aria-label="Menu">
      <i class="fas fa-bars"></i>
    </button>
    <ul class="nav-links" id="navLinks">
      <li><a href="#home">Início</a></li>
      <li><a href="#features">Recursos</a></li>
      <li><a href="#projects">Projetos</a></li>
      <li><a href="#contact">Contato</a></li>
      <li><a href="#" class="btn-outline-light">Área do Cliente</a></li>
    </ul>
  </div>
</header>

<main>
  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="container hero-grid">
      <div class="hero-content">
        <span class="hero-badge"><i class="fas fa-rocket"></i> Inovação sem limites</span>
        <h1>Criamos o futuro <br> digital para sua empresa</h1>
        <p>Soluções inteligentes, design imersivo e tecnologia de ponta. Transforme sua presença online com quem entende de performance e criatividade.</p>
        <div class="hero-buttons">
          <a href="#contact" class="btn-primary"><i class="fas fa-arrow-right"></i> Começar projeto</a>
          <a href="#features" class="btn-secondary"><i class="fas fa-play"></i> Explorar soluções</a>
        </div>
      </div>
      <div class="hero-image"></div>
    </div>
  </section>

  <!-- Features / Diferenciais -->
  <section id="features">
    <div class="container">
      <h2 class="section-title">Por que escolher a Nexus?</h2>
      <p class="section-sub">Tecnologia, design e estratégia alinhados para resultados extraordinários</p>
      <div class="cards-grid">
        <div class="feature-card">
          <div class="icon-bg"><i class="fas fa-mobile-alt"></i></div>
          <h3>Design Responsivo</h3>
          <p>Experiência perfeita em qualquer dispositivo, do mobile ao desktop, com foco em usabilidade.</p>
        </div>
        <div class="feature-card">
          <div class="icon-bg"><i class="fas fa-bolt"></i></div>
          <h3>Alta Performance</h3>
          <p>Código otimizado e arquitetura eficiente, garantindo velocidade e SEO imbatível.</p>
        </div>
        <div class="feature-card">
          <div class="icon-bg"><i class="fas fa-headset"></i></div>
          <h3>Suporte Dedicado</h3>
          <p>Atendimento humanizado e suporte 24/7 com time especializado para sua tranquilidade.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Projetos Recentes -->
  <section id="projects" style="background: #ffffff;">
    <div class="container">
      <h2 class="section-title">Cases de sucesso</h2>
      <p class="section-sub">Ideias que ganham vida através da tecnologia inovadora</p>
      <div class="projects-grid">
        <div class="project-card">
          <div class="project-img"><i class="fas fa-store"></i></div>
          <div class="project-info">
            <h3>E-comm Luxe</h3>
            <p>Plataforma completa de e-commerce com inteligência de vendas e integração com marketplaces.</p>
            <span class="tag"><i class="fas fa-tag"></i> E-commerce</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-img"><i class="fas fa-chart-line"></i></div>
          <div class="project-info">
            <h3>Dashboard Fintech</h3>
            <p>Sistema analítico em tempo real, gestão de dados e visualização de métricas avançadas.</p>
            <span class="tag"><i class="fas fa-chart-simple"></i> Data Science</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-img"><i class="fas fa-hand-peace"></i></div>
          <div class="project-info">
            <h3>App Saúde Vital</h3>
            <p>Aplicativo mobile para telemedicina com agendamentos, prontuário e notificações push.</p>
            <span class="tag"><i class="fas fa-heartbeat"></i> HealthTech</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Sobre + Formulário de Contato -->
  <section id="contact" class="about-contact">
    <div class="container flex-about">
      <div class="about-text">
        <h3><i class="fas fa-lightbulb"></i> Inovação que conecta pessoas</h3>
        <p>Com mais de 5 anos no mercado, já impactamos mais de 120 empresas com soluções digitais exclusivas. Nosso DNA é criar experiências que unem design e performance.</p>
        <div class="stats">
          <div class="stat-item"><h4>120+</h4><p>Clientes ativos</p></div>
          <div class="stat-item"><h4>98%</h4><p>Retenção anual</p></div>
          <div class="stat-item"><h4>24/7</h4><p>Suporte ágil</p></div>
        </div>
      </div>
      <div class="contact-form">
        <h3 style="font-size: 1.7rem; margin-bottom: 1rem;">Vamos conversar</h3>
        <form id="formContato">
          <div class="form-group">
            <input type="text" id="nome" placeholder="Seu nome completo" required>
          </div>
          <div class="form-group">
            <input type="email" id="email" placeholder="Email corporativo" required>
          </div>
          <div class="form-group">
            <textarea rows="3" placeholder="Conte sobre seu projeto ou ideia..." id="mensagem" required></textarea>
          </div>
          <button type="submit" class="btn-primary"><i class="fas fa-paper-plane"></i> Enviar mensagem</button>
        </form>
        <p class="tiny-text" style="font-size: 0.75rem; margin-top: 1rem; color: #6c757d;"><i class="fas fa-lock"></i> Seus dados estão seguros. Respondemos em até 24h.</p>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="container">
    <div class="footer-social">
      <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
      <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
      <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
    </div>
    <p>© 2025 Nexus Digital — Transformação criativa. Todos os direitos reservados.</p>
    <p style="margin-top: 0.5rem; font-size: 0.8rem;"><i class="fas fa-map-marker-alt"></i> Brasília - São Paulo | contato@nexusdigital.com</p>
  </div>
</footer>

<script>
  // Menu Mobile Toggle
  const menuBtn = document.getElementById('mobileMenuBtn');
  const navLinks = document.getElementById('navLinks');

  if (menuBtn) {
    menuBtn.addEventListener('click', () => {
      navLinks.classList.toggle('show');
      // alternar ícone
      const icon = menuBtn.querySelector('i');
      if (navLinks.classList.contains('show')) {
        icon.classList.remove('fa-bars');
        icon.classList.add('fa-times');
      } else {
        icon.classList.remove('fa-times');
        icon.classList.add('fa-bars');
      }
    });
  }

  // Fechar menu ao clicar em qualquer link (evitar overlaps)
  const allNavLinks = document.querySelectorAll('.nav-links a');
  allNavLinks.forEach(link => {
    link.addEventListener('click', () => {
      if (navLinks.classList.contains('show')) {
        navLinks.classList.remove('show');
        const icon = menuBtn.querySelector('i');
        if (icon) {
          icon.classList.remove('fa-times');
          icon.classList.add('fa-bars');
        }
      }
    });
  });

  // Ao redimensionar para desktop, garantir que o menu mobile seja resetado visualmente
  window.addEventListener('resize', function() {
    if (window.innerWidth > 768) {
      if (navLinks.classList.contains('show')) {
        navLinks.classList.remove('show');
        const icon = menuBtn.querySelector('i');
        if (icon) {
          icon.classList.remove('fa-times');
          icon.classList.add('fa-bars');
        }
      }
      navLinks.style.display = ''; // remove inline style, css cuida
    } else {
      // apenas garante que display fique padrão sem conflito
      if (!navLinks.classList.contains('show')) {
        navLinks.style.display = '';
      }
    }
  });

  // Formulário com alerta e reset (simulação de envio)
  const form = document.getElementById('formContato');
  if (form) {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const nome = document.getElementById('nome').value.trim();
      const email = document.getElementById('email').value.trim();
      const mensagem = document.getElementById('mensagem').value.trim();
      if (!nome || !email || !mensagem) {
        alert('Por favor, preencha todos os campos antes de enviar.');
        return;
      }
      if (!email.includes('@') || !email.includes('.')) {
        alert('Insira um e-mail válido.');
        return;
      }
      // simular envio bem-sucedido
      alert(`✨ Obrigado, ${nome}! Sua mensagem foi enviada com sucesso. Em breve nosso time entrará em contato.`);
      form.reset();
    });
  }

  // Smooth scroll para todos os links internos (hash)
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      const targetId = this.getAttribute('href');
      if (targetId === "#" || targetId === "") return;
      const targetElement = document.querySelector(targetId);
      if (targetElement) {
        e.preventDefault();
        targetElement.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        });
        // atualizar URL sem empurrar histórico agressivo?
        history.pushState(null, null, targetId);
      }
    });
  });
</script>
</body>
</html>
