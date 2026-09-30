<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>SaifizAI | Technology. Intelligence. Innovation.</title>

  <style>
    :root {
      --blue: #0754d9;
      --deep-blue: #062d91;
      --cyan: #00cfff;
      --green: #7ee000;
      --orange: #ff9d00;
      --red: #ff3515;
      --dark: #02050d;
      --dark2: #071329;
      --white: #ffffff;
      --text: #b9c8e8;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: var(--dark);
      color: var(--white);
      overflow-x: hidden;
    }

    /* Background glow */
    body::before {
      content: "";
      position: fixed;
      width: 600px;
      height: 600px;
      top: -250px;
      left: -250px;
      background: var(--blue);
      filter: blur(180px);
      opacity: .18;
      z-index: -1;
    }

    body::after {
      content: "";
      position: fixed;
      width: 500px;
      height: 500px;
      right: -200px;
      bottom: -200px;
      background: var(--cyan);
      filter: blur(180px);
      opacity: .12;
      z-index: -1;
    }

    /* NAVBAR */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      padding: 18px 7%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      background: rgba(2, 5, 13, .85);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(0, 207, 255, .15);
      z-index: 1000;
    }

    .nav-logo {
      height: 55px;
      width: auto;
    }

    .nav-links {
      display: flex;
      gap: 32px;
      list-style: none;
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      font-size: 15px;
      transition: .3s;
    }

    .nav-links a:hover {
      color: var(--cyan);
    }

    .nav-btn {
      padding: 12px 22px;
      border-radius: 30px;
      color: white !important;
      background: linear-gradient(90deg, var(--blue), var(--cyan));
      box-shadow: 0 0 20px rgba(0,207,255,.25);
    }

    /* HERO */
    .hero {
      min-height: 100vh;
      padding: 150px 7% 80px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 60px;
    }

    .hero-content {
      max-width: 700px;
    }

    .badge {
      display: inline-block;
      padding: 9px 18px;
      border: 1px solid rgba(0,207,255,.4);
      border-radius: 50px;
      color: var(--cyan);
      background: rgba(0,207,255,.06);
      margin-bottom: 25px;
      font-size: 14px;
    }

    .hero h1 {
      font-size: clamp(50px, 7vw, 90px);
      line-height: 1;
      margin-bottom: 25px;
      background: linear-gradient(
        90deg,
        #0876ff,
        #00d9ff,
        #79e500,
        #ff9c00,
        #ff3215
      );
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero h2 {
      font-size: 28px;
      margin-bottom: 20px;
      color: white;
    }

    .hero p {
      color: var(--text);
      font-size: 18px;
      line-height: 1.8;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 15px 28px;
      border-radius: 8px;
      text-decoration: none;
      color: white;
      font-weight: bold;
      transition: .3s;
    }

    .btn-primary {
      background: linear-gradient(90deg, var(--blue), #008cff);
      box-shadow: 0 8px 30px rgba(0,100,255,.3);
    }

    .btn-secondary {
      border: 1px solid var(--cyan);
      color: var(--cyan);
    }

    .btn:hover {
      transform: translateY(-4px);
    }

    .hero-logo {
      width: min(420px, 90%);
      filter: drop-shadow(0 0 35px rgba(0,140,255,.25));
      animation: float 5s ease-in-out infinite;
    }

    @keyframes float {
      0%,100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }

    /* SECTIONS */
    section {
      padding: 100px 7%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 55px;
    }

    .section-title span {
      color: var(--cyan);
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 3px;
    }

    .section-title h2 {
      font-size: 42px;
      margin-top: 12px;
    }

    .section-title p {
      max-width: 650px;
      margin: 15px auto;
      color: var(--text);
      line-height: 1.7;
    }

    /* SERVICES */
    .services {
      background: linear-gradient(
        180deg,
        transparent,
        rgba(7,45,145,.12),
        transparent
      );
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 22px;
    }

    .card {
      position: relative;
      padding: 35px 25px;
      background: linear-gradient(
        145deg,
        rgba(8,50,130,.32),
        rgba(2,10,25,.8)
      );
      border: 1px solid rgba(0,207,255,.15);
      border-radius: 18px;
      transition: .4s;
      overflow: hidden;
    }

    .card::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(
        90deg,
        var(--blue),
        var(--cyan),
        var(--green),
        var(--orange),
        var(--red)
      );
    }

    .card:hover {
      transform: translateY(-10px);
      border-color: rgba(0,207,255,.5);
      box-shadow: 0 15px 50px rgba(0,80,255,.15);
    }

    .icon {
      font-size: 45px;
      margin-bottom: 22px;
    }

    .card h3 {
      font-size: 21px;
      margin-bottom: 15px;
    }

    .card p {
      color: var(--text);
      line-height: 1.7;
      font-size: 15px;
    }

    /* ABOUT */
    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 70px;
      align-items: center;
    }

    .about h2 {
      font-size: 44px;
      margin-bottom: 20px;
    }

    .about h2 span {
      color: var(--cyan);
    }

    .about p {
      color: var(--text);
      line-height: 1.9;
      margin-bottom: 18px;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .stat {
      padding: 35px;
      text-align: center;
      border-radius: 15px;
      background: var(--dark2);
      border: 1px solid rgba(0,207,255,.15);
    }

    .stat strong {
      display: block;
      font-size: 40px;
      color: var(--cyan);
      margin-bottom: 8px;
    }

    .stat span {
      color: var(--text);
    }

    /* TECHNOLOGY */
    .tech-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .tech {
      padding: 25px;
      background: rgba(5,25,60,.6);
      border-left: 3px solid var(--blue);
      border-radius: 10px;
    }

    .tech h3 {
      margin-bottom: 10px;
    }

    .tech p {
      color: var(--text);
      line-height: 1.6;
    }

    /* CTA */
    .cta {
      text-align: center;
      margin: 60px 7%;
      padding: 80px 30px;
      border-radius: 30px;
      background:
        radial-gradient(circle at 20% 20%, rgba(0,207,255,.2), transparent 35%),
        radial-gradient(circle at 80% 80%, rgba(126,224,0,.15), transparent 35%),
        linear-gradient(135deg, #061b55, #020914);
      border: 1px solid rgba(0,207,255,.25);
    }

    .cta h2 {
      font-size: 45px;
      margin-bottom: 18px;
    }

    .cta p {
      color: var(--text);
      margin-bottom: 30px;
    }

    /* CONTACT */
    .contact {
      max-width: 900px;
      margin: auto;
    }

    .contact-form {
      display: grid;
      gap: 18px;
    }

    .contact-form input,
    .contact-form textarea {
      width: 100%;
      padding: 17px;
      background: #050d1d;
      border: 1px solid rgba(0,207,255,.2);
      border-radius: 8px;
      color: white;
      outline: none;
    }

    .contact-form input:focus,
    .contact-form textarea:focus {
      border-color: var(--cyan);
    }

    .contact-form textarea {
      min-height: 150px;
      resize: vertical;
    }

    /* FOOTER */
    footer {
      padding: 50px 7%;
      border-top: 1px solid rgba(0,207,255,.12);
      text-align: center;
    }

    footer img {
      width: 220px;
      margin-bottom: 20px;
    }

    footer p {
      color: var(--text);
    }

    .footer-line {
      width: 120px;
      height: 3px;
      margin: 20px auto;
      background: linear-gradient(
        90deg,
        var(--blue),
        var(--cyan),
        var(--green),
        var(--orange),
        var(--red)
      );
    }

    /* MOBILE */
    @media (max-width: 900px) {
      .nav-links {
        display: none;
      }

      .hero {
        flex-direction: column;
        text-align: center;
        padding-top: 140px;
      }

      .buttons {
        justify-content: center;
      }

      .service-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .about {
        grid-template-columns: 1fr;
      }

      .tech-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 600px) {
      .service-grid {
        grid-template-columns: 1fr;
      }

      .stats {
        grid-template-columns: 1fr;
      }

      .hero h1 {
        font-size: 55px;
      }

      .section-title h2,
      .about h2,
      .cta h2 {
        font-size: 32px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <a href="#home">
      <img src="logo.png" class="nav-logo" alt="SaifizAI">
    </a>

    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#technology">Technology</a></li>
      <li><a href="#contact" class="nav-btn">Contact Us</a></li>
    </ul>
  </nav>


  <!-- HERO -->
  <section class="hero" id="home">

    <div class="hero-content">

      <div class="badge">
        🚀 Technology • Intelligence • Innovation
      </div>

      <h1>SaifizAI</h1>

      <h2>Building Intelligent Digital Solutions</h2>

      <p>
        We combine Artificial Intelligence, Cloud Technology,
        Automation and Digital Innovation to help businesses
        transform ideas into powerful solutions.
      </p>

      <div class="buttons">
        <a href="#services" class="btn btn-primary">
          Explore Services
        </a>

        <a href="#contact" class="btn btn-secondary">
          Get In Touch
        </a>
      </div>

    </div>

    <img src="logo.png" class="hero-logo" alt="SaifizAI Logo">

  </section>


  <!-- SERVICES -->
  <section class="services" id="services">

    <div class="section-title">
      <span>What We Do</span>
      <h2>Our Services</h2>
      <p>
        Innovative technology solutions designed to simplify,
        automate and accelerate modern businesses.
      </p>
    </div>

    <div class="service-grid">

      <div class="card">
        <div class="icon">🤖</div>
        <h3>AI Solutions</h3>
        <p>
          Intelligent AI systems, machine learning, AI assistants,
          predictive analytics and custom automation.
        </p>
      </div>

      <div class="card">
        <div class="icon">☁️</div>
        <h3>Cloud & Digital</h3>
        <p>
          Modern cloud infrastructure, digital platforms,
          application development and scalable solutions.
        </p>
      </div>

      <div class="card">
        <div class="icon">⚙️</div>
        <h3>Automation</h3>
        <p>
          Automate repetitive processes and improve productivity
          with intelligent business workflows.
        </p>
      </div>

      <div class="card">
        <div class="icon">📈</div>
        <h3>Business Growth</h3>
        <p>
          Technology-driven solutions that help organizations
          improve efficiency, customer experience and growth.
        </p>
      </div>

    </div>

  </section>


  <!-- ABOUT -->
  <section id="about">

    <div class="about">

      <div>
        <h2>
          Technology for a
          <span>Smarter Future.</span>
        </h2>

        <p>
          SaifizAI is focused on creating practical technology
          solutions that solve real business problems.
        </p>

        <p>
          From artificial intelligence and automation to cloud
          platforms and digital transformation, we help organizations
          move faster and work smarter.
        </p>

        <a href="#contact" class="btn btn-primary">
          Start a Conversation
        </a>
      </div>

      <div class="stats">

        <div class="stat">
          <strong>AI</strong>
          <span>Intelligent Solutions</span>
        </div>

        <div class="stat">
          <strong>24/7</strong>
          <span>Digital Innovation</span>
        </div>

        <div class="stat">
          <strong>∞</strong>
          <span>Possibilities</span>
        </div>

        <div class="stat">
          <strong>360°</strong>
          <span>Technology Approach</span>
        </div>

      </div>

    </div>

  </section>


  <!-- TECHNOLOGY -->
  <section id="technology">

    <div class="section-title">
      <span>Our Expertise</span>
      <h2>Technology & Innovation</h2>
      <p>
        Combining modern technologies to create scalable,
        secure and intelligent digital experiences.
      </p>
    </div>

    <div class="tech-grid">

      <div class="tech">
        <h3>Artificial Intelligence</h3>
        <p>
          Generative AI, machine learning, intelligent assistants
          and AI-powered applications.
        </p>
      </div>

      <div class="tech">
        <h3>Cloud Computing</h3>
        <p>
          Cloud-native applications, infrastructure and
          scalable digital platforms.
        </p>
      </div>

      <div class="tech">
        <h3>Automation</h3>
        <p>
          Intelligent workflows and process automation
          for improved productivity.
        </p>
      </div>

      <div class="tech">
        <h3>Data & Analytics</h3>
        <p>
          Transforming business data into useful insights
          and intelligent decisions.
        </p>
      </div>

      <div class="tech">
        <h3>Web Development</h3>
        <p>
          Modern, responsive and high-performance websites
          and web applications.
        </p>
      </div>

      <div class="tech">
        <h3>Digital Transformation</h3>
        <p>
          Helping organizations modernize their technology
          and digital operations.
        </p>
      </div>

    </div>

  </section>


  <!-- CTA -->
  <div class="cta">

    <h2>Let's Build Something Intelligent.</h2>

    <p>
      Have an idea, business challenge or technology project?
      Let's turn it into reality.
    </p>

    <a href="#contact" class="btn btn-primary">
      Talk to SaifizAI
    </a>

  </div>


  <!-- CONTACT -->
  <section id="contact">

    <div class="section-title">
      <span>Contact</span>
      <h2>Let's Connect</h2>
      <p>
        Tell us about your project and let's explore
        how technology can help.
      </p>
    </div>

    <div class="contact">

      <form class="contact-form">

        <input
          type="text"
          placeholder="Your Name"
          required
        >

        <input
          type="email"
          placeholder="Email Address"
          required
        >

        <input
          type="text"
          placeholder="Company"
        >

        <textarea
          placeholder="Tell us about your project..."
        ></textarea>

        <button
          type="submit"
          class="btn btn-primary"
          style="border:0; cursor:pointer;"
        >
          Send Message
        </button>

      </form>

    </div>

  </section>


  <!-- FOOTER -->
  <footer>

    <img src="logo.png" alt="SaifizAI">

    <div class="footer-line"></div>

    <p>
      Technology. Intelligence. Innovation.
    </p>

    <p style="margin-top:15px; font-size:13px;">
      © 2026 SaifizAI. All Rights Reserved.
    </p>

  </footer>


  <script>
    document.querySelector(".contact-form").addEventListener("submit", function(e) {
      e.preventDefault();
      alert("Thank you! Your message has been received.");
    });
  </script>

</body>
</html>
