<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gailesh Chaudhary</title>
  <style>
    /* =========================================================
   Theme: Classic Editorial with Neo-Futuristic Accents
   ========================================================= */

:root {
  /* Classic Warm Editorial Dark Palette */
  --bg-primary: #0a0c10;
  --bg-secondary: #12161f;
  --bg-card: rgba(18, 22, 31, 0.75);
  
  /* Futuristic Neon & Plasma Accents */
  --accent-cyan: #00f2fe;
  --accent-amber: #ffb703;
  --accent-glow: rgba(0, 242, 254, 0.18);
  --border-subtle: rgba(255, 255, 255, 0.08);
  --border-neon: rgba(0, 242, 254, 0.35);

  /* Typography Colors */
  --text-main: #e6edf3;
  --text-muted: #8b949e;
  --text-gold: #e2c08d;

  /* Classic Serif & Futuristic Mono Fonts */
  --font-serif: "Playfair Display", "Cinzel", "Georgia", "Times New Roman", serif;
  --font-sans: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  --font-mono: "JetBrains Mono", "SF Mono", "Fira Code", monospace;

  --transition-smooth: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
}

/* Base Styles */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: var(--bg-primary);
  background-image: 
    radial-gradient(circle at 15% 15%, rgba(0, 242, 254, 0.04) 0%, transparent 40%),
    radial-gradient(circle at 85% 85%, rgba(255, 183, 3, 0.03) 0%, transparent 40%),
    linear-gradient(rgba(255, 255, 255, 0.015) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.015) 1px, transparent 1px);
  background-size: 100% 100%, 100% 100%, 40px 40px, 40px 40px;
  color: var(--text-main);
  font-family: var(--font-sans);
  line-height: 1.65;
  padding: 3rem 1rem;
}

.container {
  max-width: 960px;
  margin: 0 auto;
}

/* Header Section */
header {
  text-align: center;
  margin-bottom: 4rem;
  position: relative;
  padding: 2.5rem 1.5rem;
  border: 1px solid var(--border-subtle);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
  border-radius: 4px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
}

header::before {
  content: "";
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 120px;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent-cyan), transparent);
  box-shadow: 0 0 12px var(--accent-cyan);
}

.user-name {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  color: #fff;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}

.user-headline {
  font-family: var(--font-mono);
  font-size: 0.95rem;
  color: var(--accent-cyan);
  text-transform: uppercase;
  letter-spacing: 0.15em;
  margin-bottom: 1.25rem;
}

.user-summary {
  max-width: 680px;
  margin: 0 auto 1.5rem auto;
  color: var(--text-muted);
  font-size: 1rem;
}

/* Contact Links */
.contact-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.25rem;
  font-family: var(--font-mono);
  font-size: 0.85rem;
}

.contact-list a, .contact-item {
  color: var(--text-gold);
  text-decoration: none;
  transition: var(--transition-smooth);
}

.contact-list a:hover {
  color: var(--accent-cyan);
  text-shadow: 0 0 8px var(--accent-cyan);
}

/* Section Containers & Headers */
.card-section {
  margin-bottom: 3.5rem;
}

.section-title {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: var(--text-gold);
  margin-bottom: 1.5rem;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.section-title::after {
  content: "";
  flex: 1;
  height: 1px;
  background: linear-gradient(90deg, var(--border-neon), transparent);
}

/* Interactive Grid & Cards */
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}

.card {
  background: var(--bg-card);
  backdrop-filter: blur(8px);
  border: 1px solid var(--border-subtle);
  border-radius: 4px;
  padding: 1.5rem;
  position: relative;
  transition: var(--transition-smooth);
  overflow: hidden;
}

.card:hover {
  border-color: var(--border-neon);
  transform: translateY(-3px);
  box-shadow: 0 10px 25px var(--accent-glow);
}

.card-title {
  font-family: var(--font-serif);
  font-size: 1.2rem;
  color: #fff;
  margin-bottom: 0.25rem;
}

.card-subtitle {
  font-family: var(--font-mono);
  font-size: 0.85rem;
  color: var(--accent-cyan);
  margin-bottom: 0.75rem;
}

.card-meta {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--text-muted);
  margin-bottom: 0.75rem;
}

.card-body {
  font-size: 0.92rem;
  color: var(--text-muted);
}

/* Skills Badges */
.skills-wrapper {
  display: flex;
  flex-wrap: wrap;
  gap: 0.65rem;
}

.skill-tag {
  font-family: var(--font-mono);
  font-size: 0.8rem;
  padding: 0.4rem 0.85rem;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid var(--border-subtle);
  border-radius: 2px;
  color: var(--text-main);
  letter-spacing: 0.03em;
  transition: var(--transition-smooth);
}

.skill-tag:hover {
  border-color: var(--accent-cyan);
  color: var(--accent-cyan);
  background: rgba(0, 242, 254, 0.05);
}

/* Bullet Points */
ul {
  padding-left: 1.2rem;
}

li {
  color: var(--text-muted);
  margin-bottom: 0.4rem;
  font-size: 0.9rem;
}

li::marker {
  color: var(--accent-cyan);
}

/* Responsive */
@media (max-width: 600px) {
  .user-name {
    font-size: 2rem;
  }
  body {
    padding: 1.5rem 0.75rem;
  }
}


.profile-container {
  text-align: center;
  margin-top: 20px;
}

.profile-img {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  border: 3px solid #333;
  object-fit: cover;
}

  </style>
</head>
<body>
  <div class="container">

    <!-- Header Section -->
    <header>
      
      <h1 class="user-name">Gailesh Chaudhary</h1>
      

      
      <p class="user-headline">AIML Undergraduate & Full-Stack Developer</p>
      

      
      <p class="user-summary">Motivated 2nd-year B.Tech Artificial Intelligence and Machine Learning student with a strong foundation in software engineering and web development. Proficient in Python, Java, React, and modern frontend technologies. Passionate about developing intelligent applications, integrating machine learning pipelines with responsive web interfaces, and solving algorithmic challenges.</p>
      

      
      <div class="contact-list">
        
        <a href="mailto:gailesh.chaudhary_cs.aiml25@gla.ac.in" class="contact-item">✉ gailesh.chaudhary_cs.aiml25@gla.ac.in</a>
        
        
        <span class="contact-item">📞 +91 8439256725</span>
        
        
        <span class="contact-item">📍 Mathura, Uttar Pradesh, India</span>
        
        
        <a href="https://linkedin.com/in/gailesh-chaudhary" target="_blank" rel="noopener noreferrer" class="contact-item">LinkedIn</a>
        
        
        <a href="https://github.com/gailesh-codes" target="_blank" rel="noopener noreferrer" class="contact-item">GitHub</a>
        
        
        <a href="https://gaileshchaudhary.dev" target="_blank" rel="noopener noreferrer" class="contact-item">Website</a>
        
      </div>
      
    </header>

    <!-- Skills Section -->
    
    <section class="card-section">
      <h2 class="section-title">Skills & Expertise</h2>
      <div class="skills-wrapper">
        
        <span class="skill-tag">Python</span>
        
        <span class="skill-tag">Java</span>
        
        <span class="skill-tag">C</span>
        
        <span class="skill-tag">JavaScript</span>
        
        <span class="skill-tag">SQL</span>
        
        <span class="skill-tag">React.js</span>
        
        <span class="skill-tag">HTML5</span>
        
        <span class="skill-tag">CSS3</span>
        
        <span class="skill-tag">JavaScript (ES6+)</span>
        
        <span class="skill-tag">Pandas</span>
        
        <span class="skill-tag">NumPy</span>
        
        <span class="skill-tag">Scikit-Learn</span>
        
        <span class="skill-tag">OpenCV</span>
        
        <span class="skill-tag">Matplotlib</span>
        
        <span class="skill-tag">Git</span>
        
        <span class="skill-tag">GitHub</span>
        
        <span class="skill-tag">VS Code</span>
        
        <span class="skill-tag">Linux</span>
        
        <span class="skill-tag">Postman</span>
        
        <span class="skill-tag">Data Structures & Algorithms (DSA)</span>
        
        <span class="skill-tag">Object-Oriented Programming (OOP)</span>
        
        <span class="skill-tag">REST APIs</span>
        
      </div>
    </section>
    

    <!-- Experience Section -->
    

    <!-- Projects Section -->
    
    <section class="card-section">
      <h2 class="section-title">Featured Projects</h2>
      <div class="grid-container">
        
        <div class="card">
          <h3 class="card-title">Number Guessing / Console Calculator (Python)</h3>
          
          <p class="card-body">Built a small command-line application to practice control flow, functions, and error handling.</p>
          
          
          <div class="skills-wrapper" style="margin-top: 0.75rem;">
            
            <span class="skill-tag">Python</span>
            
          </div>
          
          
        </div>
        
        <div class="card">
          <h3 class="card-title">Beginner Data Analysis Mini-Project</h3>
          
          <p class="card-body">Explored a public dataset (e.g., Titanic/Iris) to practice data cleaning and basic visualization.</p>
          
          
          <div class="skills-wrapper" style="margin-top: 0.75rem;">
            
            <span class="skill-tag">Pandas</span>
            
            <span class="skill-tag">NumPy</span>
            
          </div>
          
          
        </div>
        
        <div class="card">
          <h3 class="card-title">Personal Portfolio Webpage</h3>
          
          <p class="card-body">Designed and built a static one-page site showcasing academic background and interests.</p>
          
          
          <div class="skills-wrapper" style="margin-top: 0.75rem;">
            
            <span class="skill-tag">HTML</span>
            
            <span class="skill-tag">CSS</span>
            
          </div>
          
          
          <div style="margin-top: 1rem;">
            <a href="https://github.com/gailesh-codes/ai-resume-analyzer" target="_blank" rel="noopener noreferrer" class="contact-item" style="font-size: 0.85rem;">View Project →</a>
          </div>
          
        </div>
        
      </div>
    </section>
    

    <!-- Education Section -->
    
    <section class="card-section">
      <h2 class="section-title">Education</h2>
      <div class="grid-container">
        
        <div class="card">
          <h3 class="card-title">Bachelor of Technology in Artificial Intelligence and Machine Learning (B.Tech AIML)</h3>
          <p class="card-subtitle">GLA university</p>
          
          <p class="card-meta">Expected Graduation: June 2029</p>
          
          
          <p class="card-body">Current Year: 2nd Year (Semester III) - Relevant Coursework: Data Structures, Object-Oriented Programming in Java, Database Management Systems, Discrete Mathematics, AI Fundamentals</p>
          
        </div>
        
      </div>
    </section>
    

    <!-- Achievements Section -->
    
    <section class="card-section">
      <h2 class="section-title">Achievements & Certifications</h2>
      <div class="grid-container">
        
        <div class="card">
          <h3 class="card-title">Python for Everybody</h3>
          
          <p class="card-body">Coursera</p>
          
          
        </div>
        
        <div class="card">
          <h3 class="card-title">Problem Solving (Basic)</h3>
          
          <p class="card-body">leetcode</p>
          
          
        </div>
        
      </div>
    </section>
    

  </div>
</body>
</html>

