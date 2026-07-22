GitHub Pages Web Page Template

This is a clean, modern single-page template tailored for GitHub Pages. It uses plain HTML5, modern CSS3 (with CSS variables for easy styling and responsive design), and zero external frameworks.1. File Structure

To host this on GitHub Pages, set up your repository layout like this:
my-github-pages-site/  
├── index.html  
├── style.css  
└── README.md
2. Template Filesindex.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Personal portfolio and project showcase hosted on GitHub Pages." />
  <title>Project or Personal Name | Portfolio</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- Header / Navigation -->
  <header>
    <div class="container nav-container">
      <a href="#" class="logo">Project Title</a>
      <nav>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#features">Features</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <div class="container">
      <h1>Welcome to My Project</h1>
      <p>A fast, lightweight template designed to deploy effortlessly on GitHub Pages.</p>
      <div class="hero-buttons">
        <a href="https://github.com/your-username/your-repo" class="btn primary-btn" target="_blank" rel="noopener">View on GitHub</a>
        <a href="#about" class="btn secondary-btn">Learn More</a>
      </div>
    </div>
  </section>

  <!-- Main Content -->
  <main class="container">

    <!-- About Section -->
    <section id="about" class="section">
      <h2>About the Project</h2>
      <p>
        Provide a concise overview of your repository, documentation, or background. This static layout is built with standard semantic HTML5 elements and requires no build pipeline or node modules.
      </p>
    </section>

    <!-- Features Grid Section -->
    <section id="features" class="section">
      <h2>Key Features</h2>
      <div class="grid">
        <div class="card">
          <h3>Zero Dependencies</h3>
          <p>Built with vanilla HTML and CSS, ensuring maximum stability, security, and quick load speeds.</p>
        </div>
        <div class="card">
          <h3>Fully Responsive</h3>
          <p>Layouts automatically adjust across mobile, tablet, and desktop viewports using CSS Grid and Flexbox.</p>
        </div>
        <div class="card">
          <h3>GitHub Pages Ready</h3>
          <p>Drop these files straight into your repository root or <code>/docs</code> folder to go live immediately.</p>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
      <h2>Projects & Documentation</h2>
      <div class="grid">
        <div class="card">
          <h3>Module Alpha</h3>
          <p>Brief description of a specific sub-project, documentation page, or tool in your ecosystem.</p>
          <a href="#" class="card-link">Read Docs →</a>
        </div>
        <div class="card">
          <h3>Module Beta</h3>
          <p>Another area to highlight source repositories, research notes, or interactive sandboxes.</p>
          <a href="#" class="card-link">View Source →</a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
      <h2>Get in Touch</h2>
      <p>Feel free to reach out via issues, pull requests, or standard channels:</p>
      <ul class="contact-list">
        <li><strong>GitHub:</strong> <a href="https://github.com/your-username" target="_blank" rel="noopener">github.com/your-username</a></li>
        <li><strong>Email:</strong> <a href="mailto:your.email@example.com">your.email@example.com</a></li>
      </ul>
    </section>

  </main>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>© 2026 Your Name. Hosted open-source on <a href="https://pages.github.com/" target="_blank" rel="noopener">GitHub Pages</a>.</p>
    </div>
  </footer>

</body>
</html>
style.css
/* CSS Variables for simplified theme management */
:root {
  --bg-color: #0d1117;
  --card-bg: #161b22;
  --border-color: #30363d;
  --text-main: #c9d1d9;
  --text-heading: #f0f6fc;
  --accent-color: #58a6ff;
  --accent-hover: #1f6feb;
  --font-stack: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  --max-width: 900px;
}

/* Base Reset */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: var(--bg-color);
  color: var(--text-main);
  font-family: var(--font-stack);
  line-height: 1.6;
}

/* Layout Container */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 1.5rem;
}

/* Navigation Bar */
header {
  background-color: var(--card-bg);
  border-bottom: 1px solid var(--border-color);
  position: sticky;
  top: 0;
  z-index: 100;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
}

.logo {
  color: var(--text-heading);
  font-weight: 700;
  font-size: 1.1rem;
  text-decoration: none;
}

nav ul {
  display: flex;
  list-style: none;
  gap: 1.25rem;
}

nav a {
  color: var(--text-main);
  text-decoration: none;
  font-size: 0.95rem;
  transition: color 0.2s ease;
}

nav a:hover {
  color: var(--accent-color);
}

/* Hero Section */
.hero {
  padding: 4rem 0 3rem 0;
  text-align: center;
  border-bottom: 1px solid var(--border-color);
}

.hero h1 {
  color: var(--text-heading);
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.hero p {
  font-size: 1.15rem;
  max-width: 600px;
  margin: 0 auto 1.75rem auto;
}

.hero-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.btn {
  display: inline-block;
  padding: 0.6rem 1.2rem;
  border-radius: 6px;
  font-size: 0.95rem;
  font-weight: 600;
  text-decoration: none;
  transition: background-color 0.2s ease;
}

.primary-btn {
  background-color: var(--accent-hover);
  color: #ffffff;
}

.primary-btn:hover {
  background-color: var(--accent-color);
}

.secondary-btn {
  background-color: var(--card-bg);
  color: var(--text-heading);
  border: 1px solid var(--border-color);
}

.secondary-btn:hover {
  border-color: var(--accent-color);
}

/* Sections */
.section {
  padding: 3rem 0;
  border-bottom: 1px solid var(--border-color);
}

.section h2 {
  color: var(--text-heading);
  font-size: 1.75rem;
  margin-bottom: 1rem;
}

/* Responsive Grid */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}

.card {
  background-color: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: 6px;
  padding: 1.5rem;
}

.card h3 {
  color: var(--text-heading);
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
}

.card-link {
  display: inline-block;
  margin-top: 1rem;
  color: var(--accent-color);
  text-decoration: none;
  font-weight: 500;
}

.card-link:hover {
  text-decoration: underline;
}

code {
  background-color: rgba(110, 118, 129, 0.4);
  padding: 0.2em 0.4em;
  border-radius: 6px;
  font-size: 85%;
}

.contact-list {
  list-style: none;
  margin-top: 1rem;
}

.contact-list li {
  margin-bottom: 0.5rem;
}

.contact-list a {
  color: var(--accent-color);
  text-decoration: none;
}

.contact-list a:hover {
  text-decoration: underline;
}

/* Footer */
footer {
  padding: 2rem 0;
  text-align: center;
  font-size: 0.85rem;
}

footer a {
  color: var(--accent-color);
  text-decoration: none;
}

/* Mobile Responsiveness */
@media (max-width: 600px) {
  .nav-container {
    flex-direction: column;
    height: auto;
    padding: 1rem;
    gap: 0.75rem;
  }

  .hero h1 {
    font-size: 1.8rem;
  }
}
3. How to Enable GitHub Pages
Push Code to GitHub: Commit index.html and style.css to the root directory of your GitHub repository and push to the default branch (usually main or master).
Open Settings: In your GitHub repository, navigate to Settings → Pages (under the "Code and automation" section on the left menu).
Configure Deployment Source: Under Build and deployment, set Source to "Deploy from a branch." Select branch main (or master) and keep folder as / (root).
Save and Deploy: Click Save. GitHub Actions will run automatically to build and deploy your site. Your site URL will display at the top of the page once published (typically `https://<username>.github.io/<repository-name>/`).
