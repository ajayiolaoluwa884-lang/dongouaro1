<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>DONGOUARO1 | A Digital Gold Affair</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #050505;
      color: #ffffff;
      line-height: 1.6;
    }

    /* NAVIGATION */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 7%;
      background: rgba(5, 5, 5, 0.88);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(212, 175, 55, 0.2);
    }

    .logo {
      color: #d4af37;
      font-size: 21px;
      font-weight: 900;
      letter-spacing: 2px;
    }

    nav a {
      color: #ddd;
      text-decoration: none;
      margin-left: 20px;
      font-size: 14px;
      transition: 0.3s;
    }

    nav a:hover {
      color: #d4af37;
    }

    /* HERO */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 120px 7% 80px;
      position: relative;
      overflow: hidden;
      background:
        radial-gradient(circle at 50% 30%, rgba(212,175,55,0.16), transparent 35%),
        #050505;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 420px;
      height: 420px;
      border: 1px solid rgba(212,175,55,0.18);
      border-radius: 50%;
      animation: pulse 4s infinite alternate;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 850px;
    }

    .small-title {
      color: #d4af37;
      letter-spacing: 5px;
      font-size: 12px;
      margin-bottom: 18px;
      text-transform: uppercase;
    }

    h1 {
      font-size: clamp(45px, 12vw, 100px);
      line-height: 0.95;
      letter-spacing: -3px;
      margin-bottom: 22px;
    }

    .gold {
      color: #d4af37;
      text-shadow: 0 0 25px rgba(212,175,55,0.25);
    }

    .tagline {
      color: #d7d7d7;
      font-size: clamp(18px, 4vw, 27px);
      margin-bottom: 12px;
    }

    .description {
      color: #888;
      max-width: 600px;
      margin: 0 auto 35px;
      font-size: 15px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 14px 27px;
      border-radius: 5px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    .primary {
      background: #d4af37;
      color: #050505;
    }

    .primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 25px rgba(212,175,55,0.35);
    }

    .secondary {
      border: 1px solid #d4af37;
      color: #d4af37;
    }

    .secondary:hover {
      background: #d4af37;
      color: #050505;
    }

    /* SECTIONS */
    section {
      padding: 90px 7%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 50px;
    }

    .section-title span {
      color: #d4af37;
      font-size: 12px;
      letter-spacing: 4px;
      text-transform: uppercase;
    }

    .section-title h2 {
      font-size: 38px;
      margin-top: 8px;
    }

    /* CATEGORIES */
    .categories {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
      max-width: 1100px;
      margin: auto;
    }

    .card {
      position: relative;
      padding: 35px 25px;
      min-height: 260px;
      border: 1px solid rgba(212,175,55,0.18);
      border-radius: 14px;
      background: linear-gradient(
        145deg,
        #111111,
        #080808
      );
      overflow: hidden;
      transition: 0.35s;
    }

    .card::after {
      content: "";
      position: absolute;
      width: 100px;
      height: 100px;
      right: -40px;
      bottom: -40px;
      background: #d4af37;
      filter: blur(70px);
      opacity: 0.12;
    }

    .card:hover {
      transform: translateY(-8px);
      border-color: #d4af37;
      box-shadow: 0 10px 40px rgba(0,0,0,0.5);
    }

    .icon {
      font-size: 45px;
      margin-bottom: 20px;
    }

    .card h3 {
      color: #d4af37;
      font-size: 24px;
      margin-bottom: 10px;
    }

    .card p {
      color: #999;
      font-size: 14px;
    }

    /* ABOUT */
    .about {
      max-width: 850px;
      margin: auto;
      text-align: center;
    }

    .about p {
      color: #999;
      margin-top: 15px;
    }

    /* CONTACT */
    .contact-box {
      max-width: 700px;
      margin: auto;
      text-align: center;
      padding: 45px 25px;
      border: 1px solid rgba(212,175,55,0.2);
      border-radius: 15px;
      background: #0b0b0b;
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 35px 20px;
      border-top: 1px solid rgba(212,175,55,0.15);
      color: #666;
      font-size: 13px;
    }

    footer strong {
      color: #d4af37;
    }

    @keyframes pulse {
      from {
        transform: scale(0.85);
        opacity: 0.3;
      }
      to {
        transform: scale(1.15);
        opacity: 0.7;
      }
    }

    /* PHONE */
    @media (max-width: 700px) {

      nav {
        padding: 16px 5%;
      }

      nav a {
        display: none;
      }

      .hero {
        min-height: 90vh;
      }

      .categories {
        grid-template-columns: 1fr;
      }

      section {
        padding: 70px 5%;
      }

      .section-title h2 {
        font-size: 30px;
      }

      h1 {
        letter-spacing: -2px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <div class="logo">DONGOUARO1</div>

    <div>
      <a href="#home">Home</a>
      <a href="#services">Services</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero" id="home">

    <div class="hero-content">

      <div class="small-title">
        Welcome to DONGOUARO1
      </div>

      <h1>
        DONGOUARO<span class="gold">1</span>
      </h1>

      <div class="tagline">
        A Digital Gold Affair.
      </div>

      <p class="description">
        Gaming, software and graphics brought together
        in one premium digital experience.
      </p>

      <div class="buttons">
        <a href="#services" class="btn primary">
          EXPLORE NOW
        </a>

        <a href="#contact" class="btn secondary">
          CONTACT US
        </a>
      </div>

    </div>
  </section>


  <!-- SERVICES -->
  <section id="services">

    <div class="section-title">
      <span>Explore</span>
      <h2>What We Offer</h2>
    </div>

    <div class="categories">

      <div class="card">
        <div class="icon">🎮</div>
        <h3>Gaming</h3>
        <p>
          Discover gaming resources, services and
          digital experiences built for gamers.
        </p>
      </div>

      <div class="card">
        <div class="icon">💻</div>
        <h3>Software</h3>
        <p>
          Explore useful digital software and tools
          designed to make your digital life easier.
        </p>
      </div>

      <div class="card">
        <div class="icon">🎨</div>
        <h3>Graphics</h3>
        <p>
          Creative graphics, visual resources and
          digital designs for your projects.
        </p>
      </div>

    </div>
  </section>


  <!-- ABOUT -->
  <section id="about">

    <div class="section-title">
      <span>About Us</span>
      <h2>The Digital Gold Affair</h2>
    </div>

    <div class="about">

      <p>
        DONGOUARO1 is a digital hub focused on gaming,
        software and graphics.
      </p>

      <p>
        Our goal is to create a modern place where
        digital creativity meets technology.
      </p>

    </div>
  </section>


  <!-- CONTACT -->
  <section id="contact">

    <div class="section-title">
      <span>Get In Touch</span>
      <h2>Let's Connect</h2>
    </div>

    <div class="contact-box">

      <p>
        Interested in our gaming, software or graphics
        services? Contact DONGOUARO1.
      </p>

      <br>

      <a href="https://wa.me/" class="btn primary">
        CONTACT ON WHATSAPP
      </a>

    </div>

  </section>


  <!-- FOOTER -->
  <footer>

    <p>
      © 2026 <strong>DONGOUARO1</strong>
    </p>

    <p>
      A Digital Gold Affair.
    </p>

  </footer>

</body>
</html> dongouaro1
