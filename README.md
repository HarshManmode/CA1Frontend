<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Reference Layout Site</title>

  <!-- Script-style font -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet" />

  <link rel="stylesheet" href="index.css" />
</head>

<body>
  <div class="page">
    <header class="bar header" role="banner">
      <div class="title">My Retro Site</div>
    </header>

    <nav class="bar nav" role="navigation">
      <button class="menu-toggle" aria-label="Toggle menu" aria-expanded="false">☰</button>
      <ul class="nav-list">
        <li><a href="#">Home</a></li>
        <li><a href="#">Features</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>

    <main class="content" role="main">
      <section class="side left">
        <div>
          <h2>Content</h2>
          <p>secondary info.</p>
        </div>
      </section>

      <section class="main">
        <div>
          <h1>Main Content</h1>
          <p>Hello There</p>
        </div>
      </section>

      <section class="side right">
        <div>
          <h2>Content</h2>
          <p>supplemental content.</p>
        </div>
      </section>
    </main>

    <footer class="bar footer" role="contentinfo">
      <div>© 2025 Retro site. All rights reserved.</div>
    </footer>
  </div>

  <script src="script.js"></script>
</body>

</html>......




/* reset + base */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  min-height: 100vh;
  background: linear-gradient(135deg, #0f1f3f 0%, #0b142a 80%);
  padding: 30px;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
  color: #111;
  line-height: 1.2;
}

/* container */
.page {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

/* pill bars */
.bar {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: clamp(10px, 1.2vw, 18px) clamp(20px, 4vw, 40px);
  border: 4px solid #000;
  border-radius: 999px;
  font-family: 'Great Vibes', cursive;
  font-size: clamp(1.5rem, 2.2vw, 2.4rem);
  letter-spacing: .5px;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.25);
  box-shadow: 0 8px 24px -4px rgba(0, 0, 0, 0.5);
  position: relative;
  background-clip: padding-box;
}

/* specific bar colors */
.header {
  background: #ffdaab;
}

.nav {
  background: #d7ff8f;
  position: relative;
}

.footer {
  background: #aee7ff;
}

/* nav list */
.nav-list {
  list-style: none;
  display: flex;
  gap: 1rem;
  margin-left: 10px;
  flex-wrap: wrap;
  align-items: center;
  padding: 0;
}

.nav-list li a {
  text-decoration: none;
  font-size: 1rem;
  color: #111;
  padding: 6px 12px;
  border-radius: 8px;
  transition: background .2s;
}

.nav-list li a:hover {
  background: rgba(0, 0, 0, 0.1);
}

/* hamburger for small */
.menu-toggle {
  display: none;
  background: transparent;
  border: none;
  font-size: 1.6rem;
  cursor: pointer;
  margin-right: 8px;
}

/* main content row */
.content {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  align-items: stretch;
}

/* panels */
.side,
.main {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 4px solid #000;
  border-radius: 25px;
  padding: 25px;
  font-family: 'Great Vibes', cursive;
  min-height: 220px;
  text-align: center;
  flex: 1;
  position: relative;
  background-clip: padding-box;
  box-shadow: 0 12px 32px -6px rgba(0, 0, 0, 0.45);
}

/* side panels */
.side {
  background: #fface0;
  font-size: clamp(1.2rem, 1.6vw, 1.8rem);
  min-width: 140px;
}

/* main panel bigger */
.main {
  background: #e8c3ff;
  font-size: clamp(1.8rem, 2.5vw, 2.8rem);
  flex: 2;
  min-width: 260px;
}

/* responsive adjustments */
@media (max-width: 1000px) {
  .bar {
    font-size: clamp(1.2rem, 2vw, 1.9rem);
    padding: clamp(8px, 1.5vw, 14px) clamp(16px, 3vw, 30px);
  }

  .content {
    flex-direction: column;
  }

  .side,
  .main {
    flex: 1 1 100%;
    min-width: auto;
  }

  /* nav becomes toggleable */
  .nav-list {
    display: none;
    flex-direction: column;
    gap: 8px;
    margin-top: 10px;
    width: 100%;
    background: rgba(255, 255, 255, 0.08);
    padding: 10px 16px;
    border-radius: 16px;
  }

  .nav-list.open {
    display: flex;
  }

  .menu-toggle {
    display: inline-block;
    background: rgba(0, 0, 0, 0.05);
    border-radius: 8px;
    padding: 4px 8px;
  }
}
