HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coders Club - Responsive Flexbox Landing Page</title>
    <meta name="description" content="Join Coders Club at Invertis University. Learn web development, participate in hackathons, and build projects.">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- 1. Navigation Bar -->
    <header class="site-header">
        <div class="nav-container">
            <div class="logo">
                <a href="#">CodersClub</a>
            </div>
            <nav class="nav-menu">
                <ul class="nav-links">
                    <li><a href="#hero" class="active">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#cta">Join Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="header-action">
                <a href="#cta" class="btn btn-primary">Get Started</a>
            </div>
        </div>
    </header>

    <main class="main-content">
        <!-- 2. Hero Section -->
        <section id="hero" class="hero-section">
            <div class="hero-container">
                <div class="hero-text">
                    <span class="badge">Invertis University</span>
                    <h1>Build Your Future with Code & Collaboration</h1>
                    <p>Empowering Computer Science students through hands-on workshops, real-world projects, and competitive programming sessions.</p>
                    <div class="hero-buttons">
                        <a href="#cta" class="btn btn-primary btn-lg">Join the Club</a>
                        <a href="#features" class="btn btn-outline btn-lg">Explore Features</a>
                    </div>
                </div>
                <div class="hero-image-wrapper">
                    <img src="images/hero-illustration.jpg" alt="Students collaborating on programming and web development projects" class="hero-img">
                </div>
            </div>
        </section>

        <!-- 3. Feature Cards Section -->
        <section id="features" class="features-section">
            <div class="section-header">
                <h2>Why Join Coders Club?</h2>
                <p>Everything you need to accelerate your software engineering journey.</p>
            </div>
            <div class="features-grid">
                <!-- Feature 1 -->
                <div class="feature-card">
                    <div class="feature-icon">💻</div>
                    <h3>Hands-On Workshops</h3>
                    <p>Learn semantic HTML, responsive CSS, modern JavaScript frameworks, and Java backend development through guided lab sessions.</p>
                </div>
                <!-- Feature 2 -->
                <div class="feature-card">
                    <div class="feature-icon">🚀</div>
                    <h3>Hackathons & Contests</h3>
                    <p>Test your problem-solving skills in coding competitions, hackathons, and collaborative team-based project builds.</p>
                </div>
                <!-- Feature 3 -->
                <div class="feature-card">
                    <div class="feature-icon">🤝</div>
                    <h3>Peer Mentorship</h3>
                    <p>Connect with senior developers, share resources, build open-source portfolios, and prepare for technical interviews.</p>
                </div>
            </div>
        </section>

        <!-- 4. Call-to-Action Section -->
        <section id="cta" class="cta-section">
            <div class="cta-container">
                <h2>Ready to Start Your Coding Journey?</h2>
                <p>Register for our upcoming workshops and become part of Bareilly's most active student developer community.</p>
                <a href="registration.html" class="btn btn-light btn-lg">Register for Membership</a>
            </div>
        </section>
    </main>

    <!-- 5. Footer -->
    <footer id="contact" class="site-footer">
        <div class="footer-container">
            <div class="footer-info">
                <h3>Coders Club</h3>
                <p>Department of Computer Science Engineering, Invertis University, Bareilly, UP</p>
            </div>
            <ul class="footer-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="https://github.com/falak siddiqui" target="_blank" rel="noopener">GitHub</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 falak siddiqui. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
CSS
/* style.css */
:root {
    --primary-color: #0284c7;
    --primary-hover: #0369a1;
    --secondary-color: #0f172a;
    --bg-color: #f8fafc;
    --surface-color: #ffffff;
    --text-color: #334155;
    --text-muted: #64748b;
    --border-color: #e2e8f0;

    --space-sm: 8px;
    --space-md: 16px;
    --space-lg: 24px;
    --space-xl: 40px;

    --radius-md: 8px;
    --radius-lg: 12px;
    --shadow-sm: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    --shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    line-height: 1.6;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

/* 1. Navigation Bar */
.site-header {
    background-color: var(--secondary-color);
    color: var(--surface-color);
    padding: var(--space-md) var(--space-xl);
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--space-md);
}

.logo a {
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--surface-color);
    text-decoration: none;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: var(--space-lg);
}

.nav-links a {
    color: #94a3b8;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.2s ease;
}

.nav-links a:hover,
.nav-links a.active {
    color: #38bdf8;
}

/* 2. Hero Section */
.hero-section {
    padding: 5rem var(--space-xl);
    background-color: var(--surface-color);
    border-bottom: 1px solid var(--border-color);
}

.hero-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 3rem;
    flex-wrap: wrap;
}

.hero-text {
    flex: 1 1 320px;
    max-width: 560px;
}

.badge {
    display: inline-block;
    background-color: #e0f2fe;
    color: var(--primary-color);
    font-size: 0.75rem;
    font-weight: bold;
    padding: 4px 12px;
    border-radius: 20px;
    text-transform: uppercase;
    margin-bottom: var(--space-md);
}

.hero-text h1 {
    font-size: 2.75rem;
    color: var(--secondary-color);
    line-height: 1.2;
    margin-bottom: var(--space-md);
}

.hero-text p {
    font-size: 1.125rem;
    color: var(--text-muted);
    margin-bottom: var(--space-lg);
}

.hero-buttons {
    display: flex;
    gap: var(--space-md);
    flex-wrap: wrap;
}

.hero-image-wrapper {
    flex: 1 1 320px;
    max-width: 520px;
    background-color: var(--border-color);
    border-radius: var(--radius-lg);
    overflow: hidden;
    box-shadow: var(--shadow-md);
}

.hero-img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
}

/* 3. Feature Cards Section */
.features-section {
    max-width: 1200px;
    margin: 4rem auto;
    padding: 0 var(--space-xl);
    width: 100%;
}

.section-header {
    text-align: center;
    margin-bottom: 3rem;
}

.section-header h2 {
    font-size: 2rem;
    color: var(--secondary-color);
    margin-bottom: 0.5rem;
}

.section-header p {
    color: var(--text-muted);
    font-size: 1.1rem;
}

.features-grid {
    display: flex;
    justify-content: center;
    align-items: stretch;
    gap: 2rem;
    flex-wrap: wrap;
}

.feature-card {
    flex: 1 1 280px;
    max-width: 360px;
    background-color: var(--surface-color);
    border: 1px solid var(--border-color);
    border-radius: var(--radius-lg);
    padding: 2.5rem 2rem;
    box-shadow: var(--shadow-sm);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-md);
}

.feature-icon {
    font-size: 2.5rem;
    margin-bottom: var(--space-md);
}

.feature-card h3 {
    font-size: 1.25rem;
    color: var(--secondary-color);
    margin-bottom: var(--space-sm);
}

.feature-card p {
    color: var(--text-muted);
    font-size: 0.95rem;
}

/* 4. Call-to-Action Section */
.cta-section {
    background-color: var(--primary-color);
    color: var(--surface-color);
    padding: 4rem var(--space-xl);
    text-align: center;
}

.cta-container {
    max-width: 800px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: var(--space-md);
}

.cta-container h2 {
    font-size: 2.25rem;
    color: var(--surface-color);
}

.cta-container p {
    font-size: 1.1rem;
    color: #e0f2fe;
    max-width: 600px;
    margin-bottom: var(--space-sm);
}

/* 5. Footer */
.site-footer {
    background-color: var(--secondary-color);
    color: var(--surface-color);
    padding: 3rem var(--space-xl) 1.5rem var(--space-xl);
    margin-top: auto;
    border-top: 1px solid var(--border-color);
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--space-lg);
    padding-bottom: 2rem;
    border-bottom: 1px solid #1e293b;
}

.footer-info h3 {
    font-size: 1.25rem;
    margin-bottom: 4px;
}

.footer-info p {
    color: var(--text-muted);
    font-size: 0.875rem;
}

.footer-links {
    list-style: none;
    display: flex;
    gap: var(--space-lg);
}

.footer-links a {
    color: var(--text-muted);
    text-decoration: none;
    font-size: 0.95rem;
    transition: color 0.2s ease;
}

.footer-links a:hover {
    color: var(--surface-color);
}

.footer-bottom {
    max-width: 1200px;
    margin: 1.5rem auto 0 auto;
    text-align: center;
    color: var(--text-muted);
    font-size: 0.875rem;
}

/* Buttons */
.btn {
    padding: 0.6rem 1.25rem;
    font-size: 0.95rem;
    font-weight: bold;
    border-radius: var(--radius-md);
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.2s ease, transform 0.1s ease;
    display: inline-block;
    text-align: center;
    border: none;
}

.btn-primary {
    background-color: var(--primary-color);
    color: var(--surface-color);
}

.btn-primary:hover {
    background-color: var(--primary-hover);
}

.btn-outline {
    background-color: transparent;
    border: 1px solid var(--border-color);
    color: var(--secondary-color);
}

.btn-outline:hover {
    background-color: #f1f5f9;
    border-color: var(--text-muted);
}

.btn-light {
    background-color: var(--surface-color);
    color: var(--primary-color);
}

.btn-light:hover {
    background-color: #f8fafc;
}

.btn-lg {
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
}
