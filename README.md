[site vision pixel studio.html](https://github.com/user-attachments/files/26844197/site.vision.pixel.studio.html)
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vision Pixel Studio - Design Graphique & Communication</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700;800&family=Playfair+Display:wght@700;800&family=Roboto:wght@400;500;700&family=Montserrat:wght@500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #1e3a8a;
      --secondary: #3b82f6;
      --accent: #0ea5e9;
      --dark: #0f172a;
      --light: #f8fafc;
      --text: #1f2937;
      --muted: #6b7280;
      --border: #e5e7eb;
      --success: #10b981;
    }

    /* Animations */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes slideInRight {
      from {
        opacity: 0;
        transform: translateX(-50px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    @keyframes bounceIn {
      0% {
        opacity: 0;
        transform: scale(0.3);
      }
      50% {
        opacity: 1;
        transform: scale(1.05);
      }
      70% {
        transform: scale(0.9);
      }
      100% {
        transform: scale(1);
      }
    }

    @keyframes glow {
      0%, 100% {
        text-shadow: 0 0 10px rgba(96, 165, 250, 0.5);
      }
      50% {
        text-shadow: 0 0 20px rgba(96, 165, 250, 0.8);
      }
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0px);
      }
      50% {
        transform: translateY(-10px);
      }
    }

    @keyframes pulse {
      0%, 100% {
        opacity: 1;
      }
      50% {
        opacity: 0.7;
      }
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', 'Segoe UI', sans-serif;
      background: #ffffff;
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    body::before {
      display: none;
    }

    /* Navigation */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: #ffffff;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      z-index: 1000;
      border-bottom: 1px solid var(--border);
      padding: 0 20px;
    }

    nav .container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 70px;
      flex-wrap: nowrap;
    }

    .logo {
      font-size: 24px;
      font-weight: 700;
      color: var(--primary);
      font-family: 'Poppins', sans-serif;
      text-decoration: none;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 40px;
    }

    nav a {
      color: var(--text);
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s;
      font-size: 14px;
    }

    nav a:hover {
      color: var(--secondary);
    }

    .software-icons {
      display: flex;
      gap: 15px;
      align-items: center;
    }

    .software-icon {
      width: 36px;
      height: 36px;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      cursor: pointer;
      transition: all 0.3s;
      background: rgba(60, 130, 246, 0.15);
      border: 1px solid var(--border);
    }

    .software-icon:hover {
      background: rgba(96, 165, 250, 0.3);
      border-color: var(--accent);
      transform: translateY(-3px);
    }

    /* Container */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Hero Section */
    .hero {
      margin-top: 70px;
      padding: 120px 20px;
      text-align: center;
      position: relative;
      background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
    }

    .hero h1 {
      font-size: 56px;
      font-weight: 800;
      margin-bottom: 20px;
      color: var(--primary);
      line-height: 1.2;
      font-family: 'Poppins', sans-serif;
    }

    .hero p {
      font-size: 18px;
      color: var(--muted);
      margin-bottom: 50px;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
    }

    .btn-group {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn {
      padding: 14px 36px;
      border: none;
      border-radius: 8px;
      font-size: 15px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s;
      text-decoration: none;
      display: inline-block;
    }

    .btn-primary {
      background: var(--primary);
      color: white;
      box-shadow: 0 4px 12px rgba(30, 58, 138, 0.2);
    }

    .btn-primary:hover {
      background: #1a2563;
      transform: translateY(-2px);
      box-shadow: 0 6px 16px rgba(30, 58, 138, 0.3);
    }

    .btn-secondary {
      background: transparent;
      color: var(--primary);
      border: 2px solid var(--primary);
    }

    .btn-secondary:hover {
      background: #f0f4ff;
      transform: translateY(-2px);
    }

    /* Services */
    .services-section {
      padding: 100px 20px;
      background: #ffffff;
    }

    .section-title {
      text-align: center;
      margin-bottom: 60px;
    }

    .section-title h2 {
      font-size: 42px;
      font-weight: 800;
      margin-bottom: 15px;
      color: var(--primary);
      font-family: 'Poppins', sans-serif;
    }

    .section-title p {
      color: var(--muted);
      font-size: 16px;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .service-card {
      background: #ffffff;
      border: 2px solid var(--border);
      border-radius: 12px;
      padding: 40px 30px;
      transition: all 0.3s;
      position: relative;
      overflow: hidden;
    }

    .service-card:hover {
      border-color: var(--secondary);
      box-shadow: 0 12px 32px rgba(59, 130, 246, 0.15);
      transform: translateY(-8px);
    }

    .service-icon {
      font-size: 48px;
      margin-bottom: 20px;
      width: 100%;
      height: 200px;
      background: linear-gradient(135deg, #f0f4ff, #e5e7eb);
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      background-size: cover;
      background-position: center;
    }

    .service-card h3 {
      font-size: 22px;
      margin-bottom: 15px;
      color: var(--primary);
      font-weight: 700;
    }

    .service-card p {
      color: var(--muted);
      line-height: 1.7;
      font-size: 14px;
    }

    .contact-info {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      margin-top: 50px;
    }

    .color-palette {
      display: flex;
      gap: 10px;
      margin-top: 20px;
      padding-top: 15px;
      border-top: 1px solid var(--border);
    }

    .color-swatch {
      width: 40px;
      height: 40px;
      border-radius: 8px;
      border: 1px solid var(--border);
      transition: transform 0.3s;
      cursor: pointer;
    }

    .color-swatch:hover {
      transform: scale(1.15);
    }

    /* Portfolio/Galerie */
    .portfolio-section {
      padding: 100px 20px;
      background: #f9fafb;
    }

    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .portfolio-item {
      background: linear-gradient(135deg, #e5e7eb, #d1d5db);
      border-radius: 12px;
      overflow: hidden;
      aspect-ratio: 1;
      position: relative;
      cursor: pointer;
      transition: all 0.3s;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 280px;
      background-size: cover;
      background-position: center;
      border: 2px solid var(--border);
    }

    .portfolio-item::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(30, 58, 138, 0.2);
      z-index: 1;
      transition: all 0.3s;
    }

    .portfolio-item:hover::before {
      background: rgba(30, 58, 138, 0.4);
    }

    .portfolio-item:hover {
      transform: scale(1.03);
      border-color: var(--secondary);
    }

    .portfolio-item h4 {
      font-size: 20px;
      text-align: center;
      z-index: 2;
      position: relative;
      font-weight: 700;
      color: var(--primary);
      text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    /* Stats */
    .stats-section {
      padding: 80px 20px;
      background: var(--primary);
      color: white;
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 40px;
      max-width: 1000px;
      margin: 0 auto;
      text-align: center;
    }

    .stat {
      padding: 30px;
    }

    .stat-number {
      font-size: 48px;
      font-weight: 800;
      color: white;
      margin-bottom: 10px;
    }

    .stat-label {
      color: rgba(255, 255, 255, 0.9);
      font-size: 15px;
    }

    /* Contact Section */
    .contact-section {
      padding: 100px 20px;
      background: #ffffff;
    }

    .contact-content {
      max-width: 800px;
      margin: 0 auto;
      text-align: center;
    }

    .contact-content h2 {
      font-size: 42px;
      margin-bottom: 20px;
      color: var(--primary);
      font-weight: 800;
    }

    .contact-content p {
      color: var(--muted);
      font-size: 16px;
      margin-bottom: 50px;
    }

    .contact-info {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      margin-top: 50px;
    }

    .info-box {
      background: #f9fafb;
      border: 2px solid var(--border);
      border-radius: 12px;
      padding: 30px;
      transition: all 0.3s;
    }

    .info-box:hover {
      border-color: var(--secondary);
      box-shadow: 0 8px 24px rgba(59, 130, 246, 0.1);
    }

    .info-box h3 {
      margin-bottom: 10px;
      color: var(--primary);
      font-size: 18px;
    }

    .info-box p {
      color: var(--text);
      font-weight: 600;
    }

    /* Footer */
    footer {
      background: var(--primary);
      color: white;
      padding: 50px 20px 20px;
      text-align: center;
    }

    footer p {
      margin-bottom: 20px;
      opacity: 0.9;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 30px;
    }

    .social-links a {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-decoration: none;
      transition: all 0.3s;
      font-size: 18px;
    }

    .social-links a:hover {
      background: rgba(255, 255, 255, 0.4);
      transform: translateY(-3px);
    }

    /* Responsive */
    @media (max-width: 768px) {
      nav ul {
        gap: 15px;
        font-size: 12px;
      }

      .software-icons {
        gap: 10px;
      }

      .software-icon {
        width: 32px;
        height: 32px;
        font-size: 16px;
      }

      .hero h1 {
        font-size: 40px;
      }

      .hero p {
        font-size: 16px;
      }

      .section-title h2 {
        font-size: 36px;
      }

      .services-grid {
        grid-template-columns: 1fr;
      }

      .portfolio-grid {
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      }

      .btn-group {
        flex-direction: column;
        align-items: center;
      }

      .btn {
        width: 100%;
        max-width: 300px;
      }
    }

    /* Floating Button & Modal */
    .floating-btn {
      position: fixed;
      bottom: 30px;
      right: 30px;
      width: 60px;
      height: 60px;
      background: linear-gradient(135deg, #3b82f6, #1e40af);
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      box-shadow: 0 5px 20px rgba(59, 130, 246, 0.4);
      transition: all 0.3s;
      z-index: 999;
    }

    .floating-btn:hover {
      transform: scale(1.1);
      box-shadow: 0 8px 30px rgba(59, 130, 246, 0.6);
    }

    .modal {
      display: none;
      position: fixed;
      z-index: 10000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.7);
      animation: fadeIn 0.3s;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .modal-content {
      background: linear-gradient(135deg, #0f172a, #1a2744);
      margin: 10% auto;
      padding: 40px;
      border: 1px solid var(--border);
      border-radius: 20px;
      width: 90%;
      max-width: 500px;
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
      animation: slideIn 0.3s;
    }

    @keyframes slideIn {
      from { transform: translateY(-50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    .close-btn {
      color: var(--muted);
      float: right;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
      transition: color 0.3s;
    }

    .close-btn:hover {
      color: var(--text);
    }

    .payment-section {
      padding: 80px 20px;
      background: rgba(30, 64, 175, 0.08);
    }

    .payment-container {
      max-width: 800px;
      margin: 0 auto;
      text-align: center;
    }

    .payment-container h2 {
      font-size: 48px;
      margin-bottom: 20px;
      font-family: 'Montserrat', sans-serif;
      animation: slideInRight 0.7s ease-out;
    }

    .payment-container p {
      color: var(--muted);
      font-size: 18px;
      margin-bottom: 40px;
      font-family: 'Roboto', sans-serif;
      animation: fadeInUp 0.7s ease-out 0.2s backwards;
    }

    .wave-btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 15px;
      padding: 20px 50px;
      background: linear-gradient(135deg, #0066cc, #0052a3);
      color: white;
      border: none;
      border-radius: 50px;
      font-size: 18px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s;
      font-family: 'Poppins', sans-serif;
      box-shadow: 0 10px 30px rgba(0, 102, 204, 0.3);
      animation: bounceIn 0.6s ease-out;
    }

    .wave-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 15px 40px rgba(0, 102, 204, 0.4);
    }

    .wave-btn img {
      width: 32px;
      height: 32px;
    }

    .wave-modal {
      display: none;
      position: fixed;
      z-index: 10000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.7);
      animation: fadeIn 0.3s;
    }

    .wave-modal-content {
      background: linear-gradient(135deg, #0f172a, #1a2744);
      margin: 10% auto;
      padding: 40px;
      border: 1px solid var(--border);
      border-radius: 20px;
      width: 90%;
      max-width: 600px;
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
      animation: slideIn 0.3s;
    }

    .wave-modal-content h2 {
      color: var(--accent);
      margin-bottom: 30px;
      font-family: 'Montserrat', sans-serif;
    }

    .price-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
      margin-bottom: 30px;
    }

    .price-item {
      background: rgba(30, 64, 175, 0.2);
      border: 2px solid var(--border);
      border-radius: 15px;
      padding: 20px;
      cursor: pointer;
      transition: all 0.3s;
      text-align: center;
    }

    .price-item:hover {
      border-color: var(--accent);
      background: rgba(96, 165, 250, 0.15);
      transform: translateY(-5px);
    }

    .price-item h3 {
      font-size: 24px;
      color: var(--accent);
      margin-bottom: 10px;
      font-family: 'Poppins', sans-serif;
    }

    .price-item p {
      color: var(--text);
      font-size: 14px;
    }

    .wave-send-btn {
      width: 100%;
      padding: 15px;
      background: linear-gradient(135deg, #0066cc, #0052a3);
      color: white;
      border: none;
      border-radius: 10px;
      font-weight: 600;
      font-size: 16px;
      cursor: pointer;
      transition: all 0.3s;
      font-family: 'Poppins', sans-serif;
    }

    .wave-send-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(0, 102, 204, 0.3);
    }

    .close-wave-btn {
      color: var(--muted);
      float: right;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
      transition: color 0.3s;
    }

    .close-wave-btn:hover {
      color: var(--text);
    }

    .modal h2 {
      margin-bottom: 20px;
      color: var(--accent);
      margin-top: 10px;
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
      margin-bottom: 8px;
      color: var(--text);
      font-weight: 600;
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      width: 100%;
      padding: 12px;
      background: rgba(30, 64, 175, 0.15);
      border: 1px solid var(--border);
      border-radius: 10px;
      color: var(--text);
      font-family: inherit;
      transition: all 0.3s;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: var(--accent);
      background: rgba(60, 130, 246, 0.2);
    }

    .form-group textarea {
      resize: vertical;
      min-height: 100px;
    }

    .form-btn {
      width: 100%;
      padding: 12px;
      background: linear-gradient(135deg, #3b82f6, #1e40af);
      color: white;
      border: none;
      border-radius: 10px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s;
      margin-top: 10px;
    }

    .form-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(59, 130, 246, 0.3);
    }

    @media (max-width: 600px) {
      .modal-content {
        width: 95%;
        margin: 50% auto;
        padding: 25px;
      }

      .floating-btn {
        width: 55px;
        height: 55px;
        bottom: 20px;
        right: 20px;
      }

      .software-icons {
        display: none;
      }

      nav ul {
        gap: 15px;
      }
    }
  </style>
</head>
<body>
  <!-- Navigation -->
  <nav>
    <div class="container">
      <div class="logo">VP Studio</div>
      <div style="display: flex; align-items: center; gap: 40px;">
        <ul>
          <li><a href="#services">Services</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="software-icons">
          <div class="software-icon" title="Adobe Photoshop">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Adobe_Photoshop_CC_icon.svg/120px-Adobe_Photoshop_CC_icon.svg.png" alt="Photoshop" style="width: 24px; height: 24px;">
          </div>
          <div class="software-icon" title="Adobe Illustrator">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Adobe_Illustrator_CC_icon.svg/120px-Adobe_Illustrator_CC_icon.svg.png" alt="Illustrator" style="width: 24px; height: 24px;">
          </div>
          <div class="software-icon" title="Adobe Premiere Pro">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/40/Adobe_Premiere_Pro_CC_icon.svg/120px-Adobe_Premiere_Pro_CC_icon.svg.png" alt="Premiere Pro" style="width: 24px; height: 24px;">
          </div>
        </div>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <div class="container">
      <h1>Vision Pixel Studio</h1>
      <p>Créons ensemble votre identité visuelle unique. Affiches, cartes de visite, sites web et vidéographie professionnelle.</p>
      <div class="btn-group">
        <button class="btn btn-primary" onclick="openModal()">Commencer un projet</button>
        <button class="btn btn-secondary" onclick="document.getElementById('portfolio').scrollIntoView({behavior: 'smooth'})">Voir nos réalisations</button>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="services-section">
    <div class="container">
      <div class="section-title">
        <h2>Nos Services</h2>
        <p>Solutions complètes pour votre communication visuelle</p>
      </div>
      <div class="services-grid">
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=200&fit=crop')"></div>
          <h3>Design Graphique</h3>
          <p>Création d'affiches percutantes, cartes de visite élégantes et supports visuels adaptés à votre marque pour captiver votre audience.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=500&h=200&fit=crop')"></div>
          <h3>Création de Sites Web</h3>
          <p>Sites modernes et responsifs optimisés pour tous les appareils. Design professionnel et performances garanties pour votre succès en ligne.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1492684223066-81342ee5ff30?w=500&h=200&fit=crop')"></div>
          <h3>Vidéographie</h3>
          <p>Productions vidéo de qualité professionnelle pour événements, promotions et contenus marketing. Du concept à la post-production.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=200&fit=crop')"></div>
          <h3>Identité Visuelle</h3>
          <p>Création complète de votre identité : logo, palette de couleurs, charte graphique. Une cohérence visuelle pour toutes vos communications.</p>
          <div class="color-palette">
            <div class="color-swatch" style="background: #FF6B6B;" title="Rouge Vibrant"></div>
            <div class="color-swatch" style="background: #4ECDC4;" title="Turquoise"></div>
            <div class="color-swatch" style="background: #FFE66D;" title="Or"></div>
            <div class="color-swatch" style="background: #95E1D3;" title="Menthe"></div>
            <div class="color-swatch" style="background: #6C5CE7;" title="Violet"></div>
          </div>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=200&fit=crop')"></div>
          <h3>Design UI/UX</h3>
          <p>Interfaces utilisateur intuitives et expériences numériques exceptionnelles. Conception pensée pour l'utilisateur avant tout.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=200&fit=crop')"></div>
          <h3>Branding Complet</h3>
          <p>De la conception à la mise en œuvre, nous créons une marque cohérente et mémorable qui se distingue de la concurrence.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1502920917128-1aa500764cbd?w=500&h=200&fit=crop')"></div>
          <h3>Photographie</h3>
          <p>Photographie professionnelle pour vos événements, produits et portraits. Captures d'images de qualité qui racontent votre histoire et mettent en valeur votre marque.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=200&fit=crop')"></div>
          <h3>Création de Logo</h3>
          <p>Conception de logos uniques et mémorables qui représentent l'essence de votre marque. Designs personnalisés avec impact visuel et reconnaissance instantanée.</p>
        </div>
        <div class="service-card">
          <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1552664730-d307ca884978?w=500&h=200&fit=crop')"></div>
          <h3>Flyer</h3>
          <p>Création de flyers accrocheurs pour promouvoir vos événements, produits ou services. Designs modernes et impactants pour une communication efficace et mémorable.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section id="portfolio" class="portfolio-section">
    <div class="container">
      <div class="section-title">
        <h2>Nos Réalisations</h2>
        <p>Découvrez nos meilleures créations</p>
      </div>
      <div class="portfolio-grid">
        <div class="portfolio-item" style="background-image: url('https://images.unsplash.com/photo-1611162616305-c69b3fa7fbe0?w=500&h=500&fit=crop');">
          <h4>Affiches Créatives</h4>
        </div>
        <div class="portfolio-item" style="background-image: url('https://images.unsplash.com/photo-1611634194278-4bf0b518df5b?w=500&h=500&fit=crop');">
          <h4>Cartes de Visite</h4>
        </div>
        <div class="portfolio-item" style="background-image: url('https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=500&h=500&fit=crop');">
          <h4>Sites Web</h4>
        </div>
        <div class="portfolio-item" style="background-image: url('https://images.unsplash.com/photo-1492684223066-81342ee5ff30?w=500&h=500&fit=crop');">
          <h4>Vidéographie</h4>
        </div>
        <div class="portfolio-item" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=500&fit=crop');">
          <h4>Branding</h4>
        </div>
        <div class="portfolio-item" style="background-image: url('https://images.unsplash.com/photo-1561070791-2526d30994b5?w=500&h=500&fit=crop');">
          <h4>Design UI/UX</h4>
        </div>
      </div>
    </div>
  </section>

  <!-- Stats Section -->
  <section class="stats-section">
    <div class="container">
      <div class="stats-grid">
        <div class="stat">
          <div class="stat-number">150+</div>
          <div class="stat-label">Projets réalisés</div>
        </div>
        <div class="stat">
          <div class="stat-number">50+</div>
          <div class="stat-label">Clients satisfaits</div>
        </div>
        <div class="stat">
          <div class="stat-number">5+</div>
          <div class="stat-label">Années d'expérience</div>
        </div>
        <div class="stat">
          <div class="stat-number">100%</div>
          <div class="stat-label">Satisfaction client</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact-section" style="background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%); padding: 100px 20px;">
    <div class="container">
      <div class="contact-content">
        <h2 style="color: #1e3a8a; font-size: 48px; font-weight: 800; margin-bottom: 15px;">Prêt à démarrer ?</h2>
        <p style="color: #6b7280; font-size: 18px; margin-bottom: 60px;">Contactez-nous pour discuter de votre projet et découvrez comment Vision Pixel Studio peut transformer votre vision en réalité.</p>
        
        <div class="contact-info" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; max-width: 1000px; margin: 0 auto;">
          <div class="info-box" style="background: white; border: 2px solid #e5e7eb; border-radius: 12px; padding: 40px; text-align: center; box-shadow: 0 2px 8px rgba(0,0,0,0.05);">
            <div style="font-size: 40px; margin-bottom: 15px; color: #3b82f6;">✉️</div>
            <h3 style="color: #1e3a8a; font-size: 20px; margin-bottom: 10px; font-weight: 700;">Email</h3>
            <p style="color: #1f2937; font-weight: 600;">contact@visionpixelstudio.com</p>
          </div>
          <div class="info-box" style="background: white; border: 2px solid #e5e7eb; border-radius: 12px; padding: 40px; text-align: center; box-shadow: 0 2px 8px rgba(0,0,0,0.05);">
            <div style="font-size: 40px; margin-bottom: 15px; color: #3b82f6;">📱</div>
            <h3 style="color: #1e3a8a; font-size: 20px; margin-bottom: 10px; font-weight: 700;">Téléphone</h3>
            <p style="color: #1f2937; font-weight: 600;">+221764970398</p>
          </div>
          <div class="info-box" style="background: white; border: 2px solid #e5e7eb; border-radius: 12px; padding: 40px; text-align: center; box-shadow: 0 2px 8px rgba(0,0,0,0.05);">
            <div style="font-size: 40px; margin-bottom: 15px; color: #3b82f6;">⏰</div>
            <h3 style="color: #1e3a8a; font-size: 20px; margin-bottom: 10px; font-weight: 700;">Disponibilité</h3>
            <p style="color: #1f2937; font-weight: 600;">Lun-Ven 09:00 - 18:00</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Payment Section -->
  <section class="payment-section">
    <div class="container">
      <div class="payment-container">
        <h2>Paiement Sécurisé</h2>
        <p>Payez facilement et sécurément vos services via Wave. Cliquez sur le bouton ci-dessous pour voir les options de paiement.</p>
        <button class="wave-btn" onclick="openWaveModal()">
          <img src="https://www.wave.com/en/img/wave-logo.png" alt="Wave">
          Payer via Wave
        </button>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="social-links">
        <a href="#" title="Facebook">f</a>
        <a href="#" title="Instagram">📷</a>
        <a href="#" title="LinkedIn">in</a>
        <a href="#" title="Twitter">𝕏</a>
      </div>
      <p>&copy; 2026 Vision Pixel Studio. Tous droits réservés.</p>
      <p>Agence de design graphique, création web et vidéographie professionnelle</p>
    </div>
  </footer>

  <!-- Floating Button -->
  <button class="floating-btn" onclick="openModal()">💬</button>

  <!-- Wave Payment Modal -->
  <div id="waveModal" class="wave-modal">
    <div class="wave-modal-content">
      <span class="close-wave-btn" onclick="closeWaveModal()">&times;</span>
      <h2>💳 Options de Paiement Wave</h2>
      <div class="price-list">
        <div class="price-item" onclick="selectPrice('10000')">
          <h3>10 000 FCFA</h3>
          <p>Package Basique</p>
        </div>
        <div class="price-item" onclick="selectPrice('25000')">
          <h3>25 000 FCFA</h3>
          <p>Package Standard</p>
        </div>
        <div class="price-item" onclick="selectPrice('50000')">
          <h3>50 000 FCFA</h3>
          <p>Package Premium</p>
        </div>
        <div class="price-item" onclick="selectPrice('100000')">
          <h3>100 000 FCFA</h3>
          <p>Package Pro</p>
        </div>
        <div class="price-item" onclick="selectPrice('250000')">
          <h3>250 000 FCFA</h3>
          <p>Package Entreprise</p>
        </div>
        <div class="price-item" onclick="selectPrice('500000')">
          <h3>500 000 FCFA</h3>
          <p>Package Prestige</p>
        </div>
      </div>
      <p style="color: var(--muted); margin-top: 20px; font-style: italic;">💡 Cliquez sur le montant désiré pour effectuer le paiement directement via Wave</p>
    </div>
  </div>

  <div id="contactModal" class="modal">
    <div class="modal-content">
      <span class="close-btn" onclick="closeModal()">&times;</span>
      <h2>Demander un Devis</h2>
      <form onsubmit="sendMessage(event)">
        <div class="form-group">
          <label for="name">Votre Nom</label>
          <input type="text" id="name" name="name" required>
        </div>

        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" name="email" required>
        </div>

        <div class="form-group">
          <label for="service">Service demandé</label>
          <select id="service" name="service" required>
            <option value="">-- Choisir un service --</option>
            <option value="Design Graphique">Design Graphique</option>
            <option value="Création de Sites Web">Création de Sites Web</option>
            <option value="Vidéographie">Vidéographie</option>
            <option value="Identité Visuelle">Identité Visuelle</option>
            <option value="Design UI/UX">Design UI/UX</option>
            <option value="Branding Complet">Branding Complet</option>
            <option value="Photographie">Photographie</option>
            <option value="Création de Logo">Création de Logo</option>
            <option value="Flyer">Flyer</option>
          </select>
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" name="message" placeholder="Décrivez votre projet..." required></textarea>
        </div>

        <button type="submit" class="form-btn">Envoyer via WhatsApp</button>
      </form>
    </div>
  </div>

  <script>
    // Contact Modal Functions
    const modal = document.getElementById("contactModal");
    const waveModal = document.getElementById("waveModal");

    function openModal() {
      modal.style.display = "block";
    }

    function closeModal() {
      modal.style.display = "none";
    }

    // Wave Modal Functions
    function openWaveModal() {
      waveModal.style.display = "block";
    }

    function closeWaveModal() {
      waveModal.style.display = "none";
    }

    function selectPrice(amount) {
      // Redirection directe vers Wave pour le paiement
      const phoneNumber = "+221764970398";
      const waveUrl = `https://app.wave.com/send/?to=${phoneNumber.replace(/[^0-9]/g, '')}&amount=${amount}`;
      window.open(waveUrl, "_blank");
      closeWaveModal();
    }

    // Close modal when clicking outside
    window.onclick = function(event) {
      if (event.target == modal) {
        modal.style.display = "none";
      }
      if (event.target == waveModal) {
        waveModal.style.display = "none";
      }
    }

    // Send Message via WhatsApp
    function sendMessage(event) {
      event.preventDefault();
      
      const name = document.getElementById("name").value;
      const email = document.getElementById("email").value;
      const service = document.getElementById("service").value;
      const message = document.getElementById("message").value;
      
      const phoneNumber = "+221764970398";
      const text = `Bonjour Vision Pixel Studio,%0AJe suis ${name}%0AEmail: ${email}%0A%0AService demandé: ${service}%0A%0AMessage:%0A${message}`;
      
      const whatsappUrl = `https://wa.me/${phoneNumber.replace(/[^0-9]/g, '')}?text=${text}`;
      
      window.open(whatsappUrl, "_blank");
      
      // Reset form and close modal
      document.querySelector("form").reset();
      closeModal();
    }

    // Animation au scroll
    const elements = document.querySelectorAll(".service-card, .portfolio-item");
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = "1";
          entry.target.style.transform = "translateY(0)";
        }
      });
    }, { threshold: 0.1 });

    elements.forEach(el => {
      el.style.opacity = "0";
      el.style.transform = "translateY(20px)";
      el.style.transition = "opacity 0.6s, transform 0.6s";
      observer.observe(el);
    });
  </script>
</body>
</html>
