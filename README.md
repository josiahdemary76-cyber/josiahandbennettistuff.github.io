my-website/
│
├── index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>My Website</title>

  <link rel="stylesheet" href="style.css">
</head>

<body>

  <!-- Navigation -->
  <header class="navbar">
    <div class="logo">MyWebsite</div>

    <nav>
      <a href="#home">Home</a>
      <a href="#features">Features</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>

    <button class="menu-btn" onclick="toggleMenu()">☰</button>
  </header>


  <!-- Hero -->
  <section id="home" class="hero">

    <div class="hero-content">
      <p class="eyebrow">WELCOME TO MY WEBSITE</p>

      <h1>
        Build something
        <span>awesome.</span>
      </h1>

      <p class="hero-text">
        A simple, modern website layout that you can customize
        and host for free with GitHub Pages.
      </p>

      <div class="hero-buttons">
        <a href="#features" class="btn primary">Get Started</a>
        <a href="#about" class="btn secondary">Learn More</a>
      </div>
    </div>

  </section>


  <!-- Features -->
  <section id="features" class="section">

    <div class="section-heading">
      <p class="eyebrow">FEATURES</p>
      <h2>Everything you need</h2>
      <p>
        A simple layout designed to be easy to edit and expand.
      </p>
    </div>

    <div class="cards">

      <div class="card">
        <div class="icon">⚡</div>
        <h3>Fast</h3>
        <p>
          Lightweight HTML and CSS means your website loads quickly.
        </p>
      </div>

      <div class="card">
        <div class="icon">🎨</div>
        <h3>Modern</h3>
        <p>
          Clean spacing, rounded corners, and a modern visual style.
        </p>
      </div>

      <div class="card">
        <div class="icon">📱</div>
        <h3>Responsive</h3>
        <p>
          The layout automatically adjusts for phones, tablets, and desktops.
        </p>
      </div>

    </div>

  </section>


  <!-- About -->
  <section id="about" class="about">

    <div class="about-content">

      <div>
        <p class="eyebrow">ABOUT</p>

        <h2>A website made for you.</h2>

        <p>
          Replace this text with information about yourself,
          your project, your business, or whatever you're building.
        </p>

        <a href="#contact" class="btn primary">
          Contact Me
        </a>
      </div>

      <div class="about-box">
        <div class="about-number">01</div>
        <h3>Your Project</h3>
        <p>
          Add your own images, projects, links, and content here.
        </p>
      </div>

    </div>

  </section>


  <!-- Contact -->
  <section id="contact" class="section contact">

    <p class="eyebrow">CONTACT</p>

    <h2>Let's build something.</h2>

    <p>
      Have a project in mind? Get in touch.
    </p>

    <a href="mailto:you@example.com" class="btn primary">
      Email Me
    </a>

  </section>


  <!-- Footer -->
  <footer>
    <p>© 2026 MyWebsite. All rights reserved.</p>
  </footer>


  <script src="script.js"></script>

</body>
</html>
├── style.css
/* =========================
   RESET
========================= */

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
  background: #0b0b0f;
  color: #ffffff;
  line-height: 1.6;
}


/* =========================
   NAVBAR
========================= */

.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;

  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 20px 7%;

  background: rgba(11, 11, 15, 0.85);
  backdrop-filter: blur(12px);

  border-bottom: 1px solid rgba(255, 255, 255, 0.08);

  z-index: 1000;
}

.logo {
  font-size: 22px;
  font-weight: 800;
}

.navbar nav {
  display: flex;
  gap: 30px;
}

.navbar nav a {
  color: #aaa;
  text-decoration: none;
  font-size: 15px;
  transition: 0.3s;
}

.navbar nav a:hover {
  color: white;
}

.menu-btn {
  display: none;

  background: none;
  border: none;
  color: white;

  font-size: 25px;
  cursor: pointer;
}


/* =========================
   HERO
========================= */

.hero {
  min-height: 100vh;

  display: flex;
  align-items: center;
  justify-content: center;

  text-align: center;

  padding: 120px 7% 80px;

  background:
    radial-gradient(
      circle at 50% 20%,
      rgba(90, 70, 255, 0.25),
      transparent 40%
    ),
    #0b0b0f;
}

.hero-content {
  max-width: 850px;
}

.eyebrow {
  color: #8d7cff;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 3px;
  margin-bottom: 15px;
}

.hero h1 {
  font-size: clamp(50px, 8vw, 100px);
  line-height: 1;
  letter-spacing: -4px;
  margin-bottom: 30px;
}

.hero h1 span {
  color: #8d7cff;
}

.hero-text {
  max-width: 650px;
  margin: auto;

  color: #aaa;
  font-size: 18px;
}

.hero-buttons {
  margin-top: 35px;

  display: flex;
  justify-content: center;
  gap: 15px;
}


/* =========================
   BUTTONS
========================= */

.btn {
  display: inline-block;

  padding: 14px 25px;

  border-radius: 10px;

  text-decoration: none;

  font-weight: 700;

  transition: 0.3s;
}

.primary {
  background: #8d7cff;
  color: white;
}

.primary:hover {
  transform: translateY(-3px);
  background: #7865ff;
}

.secondary {
  border: 1px solid #333;
  color: white;
}

.secondary:hover {
  background: #18181f;
}


/* =========================
   SECTIONS
========================= */

.section {
  padding: 120px 7%;
  max-width: 1300px;
  margin: auto;
}

.section-heading {
  text-align: center;
  max-width: 650px;
  margin: auto;
}

.section-heading h2,
.about h2,
.contact h2 {
  font-size: clamp(35px, 5vw, 60px);
  line-height: 1.1;
  margin-bottom: 20px;
}

.section-heading p:last-child,
.contact p {
  color: #999;
}


/* =========================
   CARDS
========================= */

.cards {
  margin-top: 60px;

  display: grid;
  grid-template-columns: repeat(3, 1fr);

  gap: 20px;
}

.card {
  padding: 35px;

  background: #121218;

  border: 1px solid #24242d;
  border-radius: 18px;

  transition: 0.3s;
}

.card:hover {
  transform: translateY(-8px);
  border-color: #8d7cff;
}

.icon {
  font-size: 35px;
  margin-bottom: 20px;
}

.card h3 {
  font-size: 22px;
  margin-bottom: 10px;
}

.card p {
  color: #999;
}


/* =========================
   ABOUT
========================= */

.about {
  padding: 120px 7%;

  background: #101016;
}

.about-content {
  max-width: 1100px;
  margin: auto;

  display: grid;
  grid-template-columns: 1fr 1fr;

  gap: 70px;

  align-items: center;
}

.about-content > div:first-child p {
  color: #999;
  margin-bottom: 25px;
}

.about-box {
  padding: 50px;

  background: #171720;

  border-radius: 20px;

  border: 1px solid #292934;
}

.about-number {
  font-size: 60px;
  font-weight: 900;
  color: #8d7cff;

  margin-bottom: 20px;
}

.about-box h3 {
  font-size: 28px;
  margin-bottom: 10px;
}

.about-box p {
  color: #999;
}


/* =========================
   CONTACT
========================= */

.contact {
  text-align: center;
}

.contact p {
  margin-bottom: 30px;
}


/* =========================
   FOOTER
========================= */

footer {
  padding: 30px 7%;

  text-align: center;

  border-top: 1px solid #222;

  color: #777;

  font-size: 14px;
}


/* =========================
   MOBILE
========================= */

@media (max-width: 768px) {

  .navbar nav {
    display: none;

    position: absolute;

    top: 70px;
    left: 0;

    width: 100%;

    flex-direction: column;

    padding: 25px;

    background: #101016;

    text-align: center;
  }

  .navbar nav.active {
    display: flex;
  }

  .menu-btn {
    display: block;
  }

  .hero h1 {
    letter-spacing: -2px;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .hero-buttons .btn {
    width: 100%;
  }

  .cards {
    grid-template-columns: 1fr;
  }

  .about-content {
    grid-template-columns: 1fr;
  }

  .about-box {
    padding: 30px;
  }

}
└── script.js
function toggleMenu() {
  const nav = document.querySelector(".navbar nav");

  nav.classList.toggle("active");
}


// Close mobile menu when clicking a link

document.querySelectorAll(".navbar nav a").forEach(link => {
  link.addEventListener("click", () => {
    document.querySelector(".navbar nav").classList.remove("active");
  });
});
