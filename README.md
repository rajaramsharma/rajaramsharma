<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rajaram Sharma - Full Stack Developer</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      min-height: 100vh;
      font-family: 'Fira Code', monospace;
      color: #fff;
      overflow-x: hidden;
    }

    .stars {
      position: fixed;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: 1;
      pointer-events: none;
    }

    .star {
      position: absolute;
      width: 2px;
      height: 2px;
      background: white;
      border-radius: 50%;
      animation: twinkle 3s infinite;
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 1; }
    }

    .container {
      position: relative;
      z-index: 2;
      max-width: 1200px;
      margin: 0 auto;
      padding: 40px 20px;
    }

    .header {
      text-align: center;
      margin-bottom: 60px;
      animation: slideDown 0.8s ease-out;
    }

    @keyframes slideDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    h1 {
      font-size: 3.5rem;
      margin-bottom: 20px;
      background: linear-gradient(45deg, #00ff87, #60efff, #ff006e);
      background-size: 300% 300%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: gradientShift 3s ease infinite, pulse 2s ease-in-out infinite;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.02); }
    }

    .subtitle {
      font-size: 1.3rem;
      color: #00ff87;
      margin-bottom: 30px;
      animation: fadeInUp 0.8s ease-out 0.2s both;
      text-shadow: 0 0 10px rgba(0, 255, 135, 0.5);
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      margin-bottom: 60px;
      animation: fadeInUp 0.8s ease-out 0.4s both;
    }

    .social-link {
      display: inline-block;
      padding: 12px 24px;
      background: rgba(255, 255, 255, 0.1);
      border: 2px solid #00ff87;
      border-radius: 50px;
      color: #fff;
      text-decoration: none;
      transition: all 0.3s ease;
      backdrop-filter: blur(10px);
      animation: float 3s ease-in-out infinite;
    }

    .social-link:nth-child(1) { animation-delay: 0s; }
    .social-link:nth-child(2) { animation-delay: 0.1s; }
    .social-link:nth-child(3) { animation-delay: 0.2s; }
    .social-link:nth-child(4) { animation-delay: 0.3s; }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }

    .social-link:hover {
      background: #00ff87;
      color: #667eea;
      transform: scale(1.05);
      box-shadow: 0 0 20px rgba(0, 255, 135, 0.6);
    }

    .section {
      margin-bottom: 50px;
      animation: fadeInUp 0.8s ease-out both;
    }

    .section:nth-of-type(1) { animation-delay: 0.5s; }
    .section:nth-of-type(2) { animation-delay: 0.6s; }
    .section:nth-of-type(3) { animation-delay: 0.7s; }
    .section:nth-of-type(4) { animation-delay: 0.8s; }

    h2 {
      font-size: 2rem;
      margin-bottom: 30px;
      color: #60efff;
      padding-bottom: 10px;
      border-bottom: 3px solid #00ff87;
      display: inline-block;
      animation: glow 2s ease-in-out infinite;
    }

    @keyframes glow {
      0%, 100% { text-shadow: 0 0 10px rgba(96, 239, 255, 0.5); }
      50% { text-shadow: 0 0 20px rgba(96, 239, 255, 0.8), 0 0 30px rgba(0, 255, 135, 0.4); }
    }

    .tech-stack {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-bottom: 30px;
    }

    .tech-category {
      background: rgba(255, 255, 255, 0.05);
      padding: 25px;
      border-radius: 15px;
      border: 2px solid rgba(0, 255, 135, 0.3);
      backdrop-filter: blur(10px);
      transition: all 0.3s ease;
    }

    .tech-category:hover {
      background: rgba(0, 255, 135, 0.1);
      border-color: #00ff87;
      transform: translateY(-10px);
      box-shadow: 0 10px 30px rgba(0, 255, 135, 0.3);
    }

    .tech-category h3 {
      color: #00ff87;
      margin-bottom: 15px;
      font-size: 1.2rem;
    }

    .tech-list {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .tech-item {
      padding: 8px 12px;
      background: rgba(96, 239, 255, 0.1);
      border-left: 3px solid #60efff;
      border-radius: 5px;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .tech-item:hover {
      background: rgba(96, 239, 255, 0.2);
      transform: translateX(10px);
      color: #60efff;
    }

    .analytics {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      margin: 40px 0;
    }

    .stats-card {
      background: rgba(255, 255, 255, 0.05);
      padding: 30px;
      border-radius: 15px;
      border: 2px solid rgba(0, 255, 135, 0.3);
      backdrop-filter: blur(10px);
      text-align: center;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .stats-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(0, 255, 135, 0.3), transparent);
      transition: left 0.5s ease;
    }

    .stats-card:hover::before {
      left: 100%;
    }

    .stats-card:hover {
      border-color: #00ff87;
      transform: scale(1.05);
      box-shadow: 0 15px 40px rgba(0, 255, 135, 0.4);
    }

    .stats-label {
      color: #60efff;
      font-size: 0.9rem;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: 2px;
    }

    .counter {
      font-size: 2.5rem;
      color: #00ff87;
      font-weight: bold;
      animation: countUp 2s ease-out;
    }

    @keyframes countUp {
      from {
        opacity: 0;
        transform: scale(0.5);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    .footer {
      text-align: center;
      margin-top: 80px;
      padding-top: 40px;
      border-top: 2px solid rgba(0, 255, 135, 0.3);
      color: #60efff;
      animation: fadeInUp 0.8s ease-out 1s both;
    }

    .visitor-badge {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 20px;
      background: rgba(0, 255, 135, 0.1);
      border: 2px solid #00ff87;
      border-radius: 25px;
      animation: bounce 2s infinite;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }

    @media (max-width: 768px) {
      h1 {
        font-size: 2rem;
      }

      h2 {
        font-size: 1.5rem;
      }

      .tech-stack {
        grid-template-columns: 1fr;
      }

      .analytics {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <div class="stars" id="stars"></div>

  <div class="container">
    <div class="header">
      <h1>🚀 RAJARAM SHARMA</h1>
      <p class="subtitle">Full Stack Developer | Next.js Enthusiast | Open Source Contributor</p>

      <div class="social-links">
        <a href="https://www.linkedin.com/in/rajaram-sharma-425a8a2a1/" target="_blank" class="social-link">💼 LinkedIn</a>
        <a href="https://www.instagram.com/rajaram_sharma_01/?hl=en" target="_blank" class="social-link">📸 Instagram</a>
        <a href="https://www.youtube.com/@rajaramsharmanepal" target="_blank" class="social-link">🎥 YouTube</a>
        <a href="mailto:sharmarajaram18000@gmail.com" class="social-link">📧 Email</a>
      </div>
    </div>

    <section class="section">
      <h2>⚡ Frontend & Frameworks</h2>
      <div class="tech-stack">
        <div class="tech-category">
          <h3>Core Technologies</h3>
          <div class="tech-list">
            <div class="tech-item">Next.js 🎯</div>
            <div class="tech-item">React ⚛️</div>
            <div class="tech-item">TypeScript 📘</div>
            <div class="tech-item">JavaScript 🟨</div>
          </div>
        </div>
        <div class="tech-category">
          <h3>Styling & Markup</h3>
          <div class="tech-list">
            <div class="tech-item">HTML5 🏗️</div>
            <div class="tech-item">CSS3 🎨</div>
            <div class="tech-item">Tailwind CSS 🌊</div>
            <div class="tech-item">Responsive Design 📱</div>
          </div>
        </div>
      </div>
    </section>

    <section class="section">
      <h2>🛠️ Backend & Database</h2>
      <div class="tech-stack">
        <div class="tech-category">
          <h3>Server & APIs</h3>
          <div class="tech-list">
            <div class="tech-item">Node.js 🟢</div>
            <div class="tech-item">Express.js ⚙️</div>
            <div class="tech-item">REST APIs 🌐</div>
            <div class="tech-item">GraphQL 📊</div>
          </div>
        </div>
        <div class="tech-category">
          <h3>Databases</h3>
          <div class="tech-list">
            <div class="tech-item">MongoDB 🍃</div>
            <div class="tech-item">MySQL 🗄️</div>
            <div class="tech-item">Firebase 🔥</div>
            <div class="tech-item">PostgreSQL 🐘</div>
          </div>
        </div>
      </div>
    </section>

    <section class="section">
      <h2>📊 GitHub Analytics</h2>
      <div class="analytics">
        <div class="stats-card">
          <div class="stats-label">Total Repositories</div>
          <div class="counter">25+</div>
        </div>
        <div class="stats-card">
          <div class="stats-label">Open Source Contributions</div>
          <div class="counter">42+</div>
        </div>
        <div class="stats-card">
          <div class="stats-label">Projects Completed</div>
          <div class="counter">18+</div>
        </div>
      </div>
    </section>

    <section class="section">
      <h2>🎨 Coding Activity</h2>
      <div style="background: rgba(255, 255, 255, 0.05); padding: 30px; border-radius: 15px; border: 2px solid rgba(0, 255, 135, 0.3); text-align: center;">
        <p style="color: #60efff; margin-bottom: 15px;">Year-round development & open source contributions</p>
        <div style="height: 100px; background: linear-gradient(90deg, transparent, #00ff87, transparent); border-radius: 10px; animation: slideRight 3s ease-in-out infinite;"></div>
      </div>
    </section>

    <div class="footer">
      <p>💡 Always learning, always building, always improving</p>
      <div class="visitor-badge">👁️ PROFILE VIEWS COUNTER</div>
    </div>
  </div>

  <script>
    // Create stars
    const starsContainer = document.getElementById('stars');
    for (let i = 0; i < 50; i++) {
      const star = document.createElement('div');
      star.className = 'star';
      star.style.left = Math.random() * 100 + '%';
      star.style.top = Math.random() * 100 + '%';
      star.style.animationDelay = Math.random() * 3 + 's';
      starsContainer.appendChild(star);
    }

    // Counter animation
    const counters = document.querySelectorAll('.counter');
    const targets = ['25', '42', '18'];
    let currentCounts = [0, 0, 0];

    const animateCounters = () => {
      counters.forEach((counter, index) => {
        const interval = setInterval(() => {
          if (currentCounts[index] < parseInt(targets[index])) {
            currentCounts[index] += Math.ceil(parseInt(targets[index]) / 30);
            counter.textContent = Math.min(currentCounts[index], parseInt(targets[index])) + '+';
          } else {
            clearInterval(interval);
          }
        }, 30);
      });
    };

    // Trigger animation on scroll
    window.addEventListener('load', () => {
      setTimeout(animateCounters, 500);
    });

    // Smooth scroll
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth' });
        }
      });
    });
  </script>
</body>
</html>
