
### Set it up

1. Create a folder on your computer named `Arewa Website`.
2. Save your logo image in that folder as **`arewa-logo.png`**.
3. Copy the code below into a text editor and save it in the same folder as **`index.html`**.
4. Open `index.html` to view your website.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="AREWA GLOBAL INVESTMENT LTD — general trading, shops, POS and financial agent businesses, fashion, import and export, and more.">
  <title>AREWA GLOBAL INVESTMENT LTD</title>

  <style>
    :root {
      --green: #063b24;
      --green-dark: #032719;
      --gold: #d7aa20;
      --cream: #f7f6f0;
      --text: #263129;
      --muted: #626c65;
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      color: var(--text);
      background: var(--cream);
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.6;
    }

    a { color: inherit; text-decoration: none; }

    .container {
      width: min(1100px, calc(100% - 36px));
      margin: 0 auto;
    }

    header {
      position: absolute;
      z-index: 2;
      top: 0;
      width: 100%;
      color: white;
    }

    nav {
      display: flex;
      min-height: 80px;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid rgba(255,255,255,.2);
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 14px;
      font-weight: bold;
      letter-spacing: 1px;
    }

    .brand img {
      width: 48px;
      height: 48px;
      border-radius: 50%;
      object-fit: cover;
      background: white;
    }

    .brand small {
      display: block;
      font-size: 10px;
      font-weight: normal;
      letter-spacing: 2px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 24px;
      font-size: 14px;
    }

    .nav-links a:hover { color: var(--gold); }

    .button {
      display: inline-block;
      padding: 13px 20px;
      border: 0;
      background: var(--gold);
      color: #172517;
      font-weight: bold;
      cursor: pointer;
    }

    .hero {
      display: flex;
      min-height: 650px;
      align-items: center;
      background: linear-gradient(120deg, var(--green-dark), var(--green));
      color: white;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr .9fr;
      align-items: center;
      gap: 35px;
      padding-top: 100px;
    }

    .eyebrow {
      color: var(--gold);
      font-size: 12px;
      font-weight: bold;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    h1, h2, h3 {
      font-family: Georgia, "Times New Roman", serif;
      line-height: 1.15;
    }

    h1 {
      margin: 16px 0;
      font-size: clamp(42px, 7vw, 76px);
      font-weight: normal;
    }

    h1 span { color: var(--gold); }

    .hero p {
      max-width: 560px;
      color: rgba(255,255,255,.8);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 26px;
    }

    .outline-button {
      display: inline-block;
      padding: 12px 19px;
      border: 1px solid white;
      color: white;
    }

    .logo-display { text-align: center; }

    .logo-display img {
      width: min(100%, 390px);
      border-radius: 50%;
      background: white;
    }

    .slogan {
      padding: 17px;
      background: var(--gold);
      color: var(--green-dark);
      text-align: center;
      font-family: Georgia, "Times New Roman", serif;
      font-size: 20px;
    }

    section { padding: 75px 0; }

    .section-title {
      max-width: 680px;
      margin-bottom: 32px;
    }

    h2 {
      margin: 10px 0;
      color: var(--green);
      font-size: clamp(32px, 5vw, 48px);
      font-weight: normal;
    }

    .section-title p, .about p { color: var(--muted); }

    .about-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      align-items: center;
      gap: 50px;
    }

    .about-logo {
      padding: 24px;
      background: #e4e9df;
      text-align: center;
    }

    .about-logo img {
      width: min(100%, 280px);
      border-radius: 50%;
      background: white;
    }

    .activities { background: #eeede5; }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }

    .card {
      min-height: 180px;
      padding: 23px;
      background: white;
      border: 1px solid #e1e4dc;
    }

    .card-number {
      color: #98740c;
      font-size: 13px;
      font-weight: bold;
    }

    .card h3 {
      margin: 18px 0 8px;
      color: var(--green);
      font-size: 22px;
      font-weight: normal;
    }

    .card p { margin: 0; color: var(--muted); font-size: 14px; }

    .contact {
      background: var(--green);
      color: white;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
    }

    .contact h2 { color: white; }

    .contact-info {
      display: grid;
      gap: 18px;
      margin-top: 26px;
    }

    .contact-info strong {
      display: block;
      margin-bottom: 3px;
      color: var(--gold);
      font-size: 12px;
      letter-spacing: 1px;
      text-transform: uppercase;
    }

    .contact-info a:hover { color: var(--gold); }

    form {
      display: grid;
      gap: 14px;
      padding: 24px;
      background: white;
      color: var(--text);
    }

    label {
      display: grid;
      gap: 6px;
      font-size: 14px;
      font-weight: bold;
    }

    input, textarea {
      width: 100%;
      padding: 12px;
      border: 1px solid #d8ddd8;
      font: inherit;
    }

    textarea { min-height: 110px; resize: vertical; }

    footer {
      padding: 22px 0;
      background: var(--green-dark);
      color: white;
      font-size: 13px;
    }

    @media (max-width: 700px) {
      .nav-links { gap: 12px; font-size: 12px; }
      .nav-links .button { padding: 10px; }
      .hero-grid, .about-grid, .contact-grid { grid-template-columns: 1fr; }
      .hero-grid { padding-top: 125px; }
      .logo-display img { width: min(75%, 280px); }
      .cards { grid-template-columns: 1fr 1fr; }
    }

    @media (max-width: 480px) {
      .nav-links a:not(.button) { display: none; }
      .cards { grid-template-columns: 1fr; }
    }
  </style>
</head>

<body>
  <header>
    <div class="container">
      <nav>
        <a class="brand" href="#home">
          <img src="arewa-logo.png" alt="AREWA GLOBAL INVESTMENT LTD logo">
          <span>AREWA GLOBAL<small>INVESTMENT LTD</small></span>
        </a>

        <div class="nav-links">
          <a href="#about">About</a>
          <a href="#activities">Activities</a>
          <a href="#contact">Contact</a>
          <a class="button" href="#contact">Get in Touch</a>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="home">
      <div class="container hero-grid">
        <div>
          <span class="eyebrow">Trade • Business • Opportunity</span>
          <h1>Invest Today.<br><span>Build Tomorrow.</span></h1>
          <p>
            AREWA GLOBAL INVESTMENT LTD is involved in multiple business
            activities, including general trading, shops, POS and financial
            agent businesses, fashion, and import and export.
          </p>
          <div class="hero-actions">
            <a class="button" href="#activities">Our Business Activities</a>
            <a class="outline-button" href="#contact">Contact Us</a>
          </div>
        </div>

        <div class="logo-display">
          <img src="arewa-logo.png" alt="AREWA GLOBAL INVESTMENT LTD — Invest Today, Build Tomorrow">
        </div>
      </div>
    </section>

    <div class="slogan">Invest Today • Build Tomorrow</div>

    <section id="about">
      <div class="container about-grid">
        <div class="about-logo">
          <img src="arewa-logo.png" alt="AREWA GLOBAL INVESTMENT LTD logo">
        </div>
        <div class="about">
          <span class="eyebrow">About Us</span>
          <h2>Many business activities. One company.</h2>
          <p>
            AREWA GLOBAL INVESTMENT LTD is engaged in a range of business
            activities. Our activities include general trading, shops,
            POS and financial agent businesses, fashion, import and export,
            and other business activities.
          </p>
          <p>
            Please contact us by phone or email for enquiries about our
            business, products, and services.
          </p>
        </div>
      </div>
    </section>

    <section class="activities" id="activities">
      <div class="container">
        <div class="section-title">
          <span class="eyebrow">What We Do</span>
          <h2>Our Business Activities</h2>
          <p>Our company is involved in multiple business activities.</p>
        </div>

        <div class="cards">
          <article class="card">
            <span class="card-number">01 / TRADING</span>
            <h3>General Trading</h3>
            <p>General trading activities across a range of goods and products.</p>
          </article>

          <article class="card">
            <span class="card-number">02 / RETAIL</span>
            <h3>Shops</h3>
            <p>Retail and shop-based business activities.</p>
          </article>

          <article class="card">
            <span class="card-number">03 / AGENT SERVICES</span>
            <h3>POS &amp; Financial Agent Businesses</h3>
            <p>POS and financial agent business activities.</p>
          </article>

          <article class="card">
            <span class="card-number">04 / FASHION</span>
            <h3>Fashion Businesses</h3>
            <p>Fashion-related business activities.</p>
          </article>

          <article class="card">
            <span class="card-number">05 / INTERNATIONAL TRADE</span>
            <h3>Import &amp; Export</h3>
            <p>Import and export business activities.</p>
          </article>

          <article class="card">
            <span class="card-number">06 / OTHER ACTIVITIES</span>
            <h3>Multiple Business Activities</h3>
            <p>Other business activities and opportunities.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="container contact-grid">
        <div>
          <span class="eyebrow">Contact Us</span>
          <h2>Let’s talk business.</h2>
          <p>Contact AREWA GLOBAL INVESTMENT LTD for business enquiries.</p>

          <div class="contact-info">
            <div>
              <strong>Email</strong>
              <a href="mailto:arewaglobalinvestmentltd@gmail.com">
                arewaglobalinvestmentltd@gmail.com
              </a>
            </div>

            <div>
              <strong>Phone / WhatsApp</strong>
              <a href="tel:+2348080175461">08080175461</a>
              &nbsp;|&nbsp;
              <a href="https://wa.me/2348080175461" target="_blank" rel="noopener">
                WhatsApp us
              </a>
            </div>

            <div>
              <strong>Locations</strong>
              <div>Maiduguri, Borno State</div>
              <div>Abuja Sheraton Hadiza Memorial School Street</div>
            </div>
          </div>
        </div>

        <form id="contact-form">
          <label>
            Your name
            <input name="name" required>
          </label>

          <label>
            Your email
            <input name="email" type="email" required>
          </label>

          <label>
            Your message
            <textarea name="message" required></textarea>
          </label>

          <button class="button" type="submit">Send an Enquiry</button>
        </form>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      © <span id="year"></span> AREWA GLOBAL INVESTMENT LTD
    </div>
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();

    document.getElementById("contact-form").addEventListener("submit", function(event) {
      event.preventDefault();

      const name = this.elements.name.value.trim();
      const email = this.elements.email.value.trim();
      const message = this.elements.message.value.trim();

      const subject = encodeURIComponent("Website enquiry from " + name);
      const body = encodeURIComponent(
        "Name: " + name + "\nEmail: " + email + "\n\nMessage:\n" + message
      );

      window.location.href =
        "mailto:arewaglobalinvestmentltd@gmail.com?subject=" + subject + "&body=" + body;
    });
  </script>
</body>
</html>
```

`index.html` 
