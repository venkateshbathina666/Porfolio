<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Venkatesh Bathena - Cyber Athlete Portfolio</title>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700;900&amp;family=Poppins:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
        body {
            box-sizing: border-box;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: #000000;
            color: #ffffff;
            overflow-x: hidden;
            line-height: 1.6;
        }

        .cyber-grid {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 255, 65, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 65, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -1;
            animation: gridPulse 4s ease-in-out infinite;
        }

        @keyframes gridPulse {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.6; }
        }

        @keyframes avatarRotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .neon-glow {
            box-shadow: 0 0 20px rgba(0, 255, 65, 0.5);
        }

        .hero-section {
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            padding: 2rem;
            background: radial-gradient(circle at center, rgba(0, 255, 65, 0.1) 0%, transparent 70%);
        }

        .athlete-card {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.9) 0%, rgba(0, 255, 65, 0.1) 100%);
            border: 2px solid #00ff41;
            border-radius: 20px;
            padding: 3rem;
            margin-bottom: 2rem;
            position: relative;
            overflow: hidden;
        }

        .athlete-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #00ff41, transparent, #00ff41);
            border-radius: 20px;
            z-index: -1;
            animation: borderGlow 2s linear infinite;
        }

        @keyframes borderGlow {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .athlete-name {
            font-size: 4rem;
            font-weight: 900;
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(45deg, #ffffff, #00ff41);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .athlete-title {
            font-size: 1.5rem;
            color: #00ff41;
            font-weight: 600;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .hero-tagline {
            font-size: 1.2rem;
            color: #cccccc;
            font-style: italic;
            font-weight: 300;
        }

        .stats-board {
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid #00ff41;
            border-radius: 15px;
            padding: 2rem;
            margin: 2rem 0;
            backdrop-filter: blur(10px);
        }

        .stats-title {
            font-size: 2rem;
            font-weight: 700;
            color: #00ff41;
            text-align: center;
            margin-bottom: 2rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .stat-item {
            background: linear-gradient(135deg, rgba(0, 255, 65, 0.1) 0%, rgba(0, 0, 0, 0.5) 100%);
            border: 1px solid rgba(0, 255, 65, 0.3);
            border-radius: 10px;
            padding: 1.5rem;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 255, 65, 0.3);
            border-color: #00ff41;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #cccccc;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: #00ff41;
            font-family: 'Poppins', sans-serif;
        }

        .achievements-section {
            padding: 3rem 2rem;
            background: linear-gradient(180deg, rgba(0, 0, 0, 0.9) 0%, rgba(0, 255, 65, 0.05) 100%);
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            color: #ffffff;
            text-align: center;
            margin-bottom: 3rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #00ff41, transparent);
        }

        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .achievement-badge {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.8) 0%, rgba(0, 255, 65, 0.1) 100%);
            border: 2px solid rgba(0, 255, 65, 0.3);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .achievement-badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 65, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .achievement-badge:hover::before {
            left: 100%;
        }

        .achievement-badge:hover {
            transform: translateY(-10px);
            border-color: #00ff41;
            box-shadow: 0 15px 40px rgba(0, 255, 65, 0.3);
        }

        .achievement-icon {
            font-size: 3rem;
            color: #00ff41;
            margin-bottom: 1rem;
        }

        .achievement-title {
            font-size: 1.2rem;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 0.5rem;
        }

        .achievement-desc {
            font-size: 0.9rem;
            color: #cccccc;
        }

        .projects-section {
            padding: 3rem 2rem;
            background: rgba(0, 0, 0, 0.95);
        }

        .match-card {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.9) 0%, rgba(0, 255, 65, 0.1) 100%);
            border: 1px solid rgba(0, 255, 65, 0.3);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
        }

        .match-card:hover {
            border-color: #00ff41;
            transform: translateX(10px);
            box-shadow: 0 5px 25px rgba(0, 255, 65, 0.2);
        }

        .match-info {
            flex: 1;
        }

        .match-title {
            font-size: 1.3rem;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 0.5rem;
        }

        .match-desc {
            font-size: 0.9rem;
            color: #cccccc;
        }

        .match-result {
            font-size: 2rem;
            color: #00ff41;
            font-weight: 700;
        }

        .mindset-section {
            padding: 3rem 2rem;
            background: linear-gradient(45deg, rgba(0, 0, 0, 0.9) 0%, rgba(0, 255, 65, 0.1) 100%);
            text-align: center;
        }

        .quote {
            font-size: 2rem;
            font-weight: 300;
            color: #ffffff;
            font-style: italic;
            margin-bottom: 2rem;
            position: relative;
        }

        .quote::before,
        .quote::after {
            content: '"';
            font-size: 3rem;
            color: #00ff41;
            font-weight: 700;
        }

        .mindset-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .mindset-item {
            background: rgba(0, 255, 65, 0.1);
            border: 1px solid rgba(0, 255, 65, 0.3);
            border-radius: 10px;
            padding: 1.5rem;
            font-weight: 600;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
        }

        .mindset-item:hover {
            background: rgba(0, 255, 65, 0.2);
            transform: scale(1.05);
        }

        .hud-overlay {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid #00ff41;
            border-radius: 10px;
            padding: 1rem;
            font-family: 'Courier New', monospace;
            font-size: 0.8rem;
            color: #00ff41;
            z-index: 1000;
        }

        .energy-trail {
            position: absolute;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, #00ff41, transparent);
            animation: energyFlow 3s linear infinite;
        }

        @keyframes energyFlow {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        @media (max-width: 768px) {
            .athlete-name {
                font-size: 2.5rem;
            }
            
            .athlete-card {
                padding: 2rem;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .quote {
                font-size: 1.5rem;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="cyber-grid"></div>
  <div class="hud-overlay">
   <div>
    STATUS: LEARNING
   </div>
   <div>
    SECURITY: ACTIVE
   </div>
   <div>
    PROGRESS: ADVANCING
   </div>
  </div>
  <main><!-- Hero Section -->
   <section class="hero-section">
    <div class="athlete-card neon-glow">
     <div class="energy-trail"></div>
     <h1 class="athlete-name" id="athlete-name">VENKATESH BATHENA</h1>
     <p class="athlete-title" id="athlete-title">Cyber Security Student | Future Analyst | Digital Defender</p>
     <p class="hero-tagline" id="hero-tagline">Learning to defend the digital world, one skill at a time.</p>
    </div><!-- Stats Board -->
    <div class="stats-board">
     <h2 class="stats-title">Performance Dashboard</h2>
     <div class="stats-grid">
      <div class="stat-item">
       <div class="stat-label">
        Cyber Skills Score
       </div>
       <div class="stat-value" id="cyber-skills-score">
        ⭐⭐⭐⭐
       </div>
      </div>
      <div class="stat-item">
       <div class="stat-label">
        CTF Battles Won
       </div>
       <div class="stat-value" id="ctf-battles">
        8
       </div>
      </div>
      <div class="stat-item">
       <div class="stat-label">
        Projects Completed
       </div>
       <div class="stat-value" id="projects-completed">
        12
       </div>
      </div>
      <div class="stat-item">
       <div class="stat-label">
        Lab Sessions
       </div>
       <div class="stat-value" id="lab-sessions">
        25
       </div>
      </div>
      <div class="stat-item">
       <div class="stat-label">
        Tools Learning
       </div>
       <div class="stat-value" id="tools-learning">
        8
       </div>
      </div>
     </div>
    </div>
   </section><!-- About Me Section -->
   <section class="achievements-section">
    <h2 class="section-title">Mission Profile</h2>
    <div style="max-width: 1000px; margin: 0 auto; text-align: center; margin-bottom: 4rem;">
     <div style="position: relative; display: inline-block; margin-bottom: 2rem;">
      <div style="width: 120px; height: 120px; border: 3px solid #00ff41; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 4rem; margin: 0 auto; animation: avatarRotate 8s linear infinite; background: linear-gradient(135deg, rgba(0, 0, 0, 0.8) 0%, rgba(0, 255, 65, 0.1) 100%);">
       🔥
      </div>
     </div>
     <h3 id="about-title" style="font-size: 2.5rem; color: #00ff41; margin-bottom: 1rem; font-weight: 700;">Rising Cyber Warrior</h3>
     <p id="about-subtitle" style="font-size: 1.3rem; color: #ffffff; margin-bottom: 2rem; font-weight: 600;">Building Skills Through Dedication &amp; Discipline</p>
     <p id="about-description" style="font-size: 1.1rem; color: #cccccc; line-height: 1.8; max-width: 800px; margin: 0 auto;">I'm a passionate cybersecurity student who approaches learning like an elite athlete approaches training. Every lab session, every CTF challenge, and every certification is a step toward mastering the art of digital defense. My goal is to become a guardian of the digital realm, protecting organizations and individuals from cyber threats.</p>
    </div>
    <div class="mindset-grid" style="margin-top: 3rem;">
     <div class="mindset-item">
      Continuous Learning
     </div>
     <div class="mindset-item">
      Hands-On Practice
     </div>
     <div class="mindset-item">
      Ethical Mindset
     </div>
     <div class="mindset-item">
      Team Collaboration
     </div>
    </div>
   </section><!-- Technical Achievements -->
   <section class="achievements-section">
    <h2 class="section-title">Technical Arsenal</h2>
    <div class="achievements-grid">
     <div class="achievement-badge">
      <div class="achievement-icon">
       🛡️
      </div>
      <div class="achievement-title">
       Network Security
      </div>
      <div class="achievement-desc">
       Firewall Configuration &amp; Monitoring
      </div>
     </div>
     <div class="achievement-badge">
      <div class="achievement-icon">
       🔍
      </div>
      <div class="achievement-title">
       Vulnerability Assessment
      </div>
      <div class="achievement-desc">
       Scanning &amp; Analysis Tools
      </div>
     </div>
     <div class="achievement-badge">
      <div class="achievement-icon">
       🐧
      </div>
      <div class="achievement-title">
       Linux Fundamentals
      </div>
      <div class="achievement-desc">
       Command Line &amp; System Admin
      </div>
     </div>
     <div class="achievement-badge">
      <div class="achievement-icon">
       🐍
      </div>
      <div class="achievement-title">
       Python Scripting
      </div>
      <div class="achievement-desc">
       Security Automation Basics
      </div>
     </div>
     <div class="achievement-badge">
      <div class="achievement-icon">
       📊
      </div>
      <div class="achievement-title">
       Wireshark Analysis
      </div>
      <div class="achievement-desc">
       Network Traffic Investigation
      </div>
     </div>
     <div class="achievement-badge">
      <div class="achievement-icon">
       ⚔️
      </div>
      <div class="achievement-title">
       Ethical Hacking
      </div>
      <div class="achievement-desc">
       Penetration Testing Basics
      </div>
     </div>
    </div>
   </section><!-- Certificates Section -->
   <section class="achievements-section">
    <h2 class="section-title">Championship Trophies</h2>
    <div class="achievements-grid">
     <div class="achievement-badge" style="border-color: #FFD700;">
      <div class="achievement-icon">
       🏆
      </div>
      <div class="achievement-title" id="cert1-name">
       Cisco CyberOps Associate
      </div>
      <div class="achievement-desc">
       <div id="cert1-issuer">
        Cisco Systems
       </div>
       <div style="color: #00ff41; font-weight: 600; margin-top: 0.5rem;" id="cert1-date">
        2024
       </div>
       <div style="margin-top: 0.5rem;"><span style="background: rgba(255, 215, 0, 0.2); color: #FFD700; padding: 0.2rem 0.5rem; border-radius: 5px; font-size: 0.8rem;">SOC Operations</span>
       </div>
      </div>
     </div>
     <div class="achievement-badge" style="border-color: #C0C0C0;">
      <div class="achievement-icon">
       🥈
      </div>
      <div class="achievement-title" id="cert2-name">
       CompTIA Security+
      </div>
      <div class="achievement-desc">
       <div id="cert2-issuer">
        CompTIA
       </div>
       <div style="color: #00ff41; font-weight: 600; margin-top: 0.5rem;" id="cert2-date">
        2024
       </div>
       <div style="margin-top: 0.5rem;"><span style="background: rgba(192, 192, 192, 0.2); color: #C0C0C0; padding: 0.2rem 0.5rem; border-radius: 5px; font-size: 0.8rem;">Security Fundamentals</span>
       </div>
      </div>
     </div>
     <div class="achievement-badge" style="border-color: #CD7F32;">
      <div class="achievement-icon">
       🥉
      </div>
      <div class="achievement-title" id="cert3-name">
       Ethical Hacking Basics
      </div>
      <div class="achievement-desc">
       <div id="cert3-issuer">
        Coursera
       </div>
       <div style="color: #00ff41; font-weight: 600; margin-top: 0.5rem;" id="cert3-date">
        2023
       </div>
       <div style="margin-top: 0.5rem;"><span style="background: rgba(205, 127, 50, 0.2); color: #CD7F32; padding: 0.2rem 0.5rem; border-radius: 5px; font-size: 0.8rem;">Penetration Testing</span>
       </div>
      </div>
     </div>
     <div class="achievement-badge" style="border-color: #00ff41;">
      <div class="achievement-icon">
       ⭐
      </div>
      <div class="achievement-title" id="cert4-name">
       Python for Security
      </div>
      <div class="achievement-desc">
       <div id="cert4-issuer">
        Udemy
       </div>
       <div style="color: #00ff41; font-weight: 600; margin-top: 0.5rem;" id="cert4-date">
        2023
       </div>
       <div style="margin-top: 0.5rem;"><span style="background: rgba(0, 255, 65, 0.2); color: #00ff41; padding: 0.2rem 0.5rem; border-radius: 5px; font-size: 0.8rem;">Automation</span>
       </div>
      </div>
     </div>
    </div>
   </section><!-- Projects as Learning Experiences -->
   <section class="projects-section">
    <h2 class="section-title">Learning Battles</h2>
    <div class="match-card">
     <div class="match-info">
      <div class="match-title">
       Home Network Security Lab
      </div>
      <div class="match-desc">
       Built secure home network with firewall configuration
      </div>
     </div>
     <div class="match-result">
      ✅ SECURED
     </div>
    </div>
    <div class="match-card">
     <div class="match-info">
      <div class="match-title">
       Vulnerability Scanner Project
      </div>
      <div class="match-desc">
       Created Python script for basic network scanning
      </div>
     </div>
     <div class="match-result">
      ✅ CODED
     </div>
    </div>
    <div class="match-card">
     <div class="match-info">
      <div class="match-title">
       CTF Team Participation
      </div>
      <div class="match-desc">
       Competed in university cybersecurity challenges
      </div>
     </div>
     <div class="match-result">
      ✅ 8 WINS
     </div>
    </div>
    <div class="match-card">
     <div class="match-info">
      <div class="match-title">
       Security Awareness Presentation
      </div>
      <div class="match-desc">
       Educated classmates on phishing prevention
      </div>
     </div>
     <div class="match-result">
      ✅ SHARED
     </div>
    </div>
   </section><!-- Contact Section -->
   <section class="achievements-section">
    <h2 class="section-title">Connect to the Network</h2><!-- Contact Info -->
    <div style="max-width: 800px; margin: 0 auto 4rem auto;">
     <h3 style="color: #00ff41; font-size: 1.5rem; margin-bottom: 2rem; text-align: center;">Direct Communication Channels</h3>
     <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.5rem;">
      <div class="stat-item" style="cursor: pointer;" onclick="window.open('mailto:venkatesh.bathena@email.com', '_blank')">
       <div style="font-size: 2rem; margin-bottom: 0.5rem;">
        📧
       </div>
       <div class="stat-label">
        Email
       </div>
       <div class="stat-value" id="email" style="font-size: 1rem;">
        venkatesh.bathena@email.com
       </div>
      </div>
      <div class="stat-item">
       <div style="font-size: 2rem; margin-bottom: 0.5rem;">
        📱
       </div>
       <div class="stat-label">
        Phone
       </div>
       <div class="stat-value" id="phone" style="font-size: 1rem;">
        +91 98765 43210
       </div>
      </div>
      <div class="stat-item">
       <div style="font-size: 2rem; margin-bottom: 0.5rem;">
        📍
       </div>
       <div class="stat-label">
        Location
       </div>
       <div class="stat-value" id="location" style="font-size: 1rem;">
        Hyderabad, India
       </div>
      </div>
     </div>
    </div><!-- Social Media -->
    <div style="max-width: 1000px; margin: 0 auto;">
     <h3 style="color: #00ff41; font-size: 1.5rem; margin-bottom: 2rem; text-align: center;">Social Networks</h3>
     <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1.5rem;">
      <div class="achievement-badge" style="cursor: pointer; position: relative;" onclick="window.open('https://linkedin.com/in/venkateshbathena', '_blank', 'noopener,noreferrer')">
       <div class="energy-trail"></div>
       <div style="font-size: 2.5rem; margin-bottom: 1rem;">
        💼
       </div>
       <div class="achievement-title">
        LinkedIn
       </div>
       <div class="achievement-desc" id="linkedin-handle">
        @venkateshbathena
       </div>
      </div>
      <div class="achievement-badge" style="cursor: pointer; position: relative;" onclick="window.open('https://github.com/venkateshbathena', '_blank', 'noopener,noreferrer')">
       <div class="energy-trail"></div>
       <div style="font-size: 2.5rem; margin-bottom: 1rem;">
        💻
       </div>
       <div class="achievement-title">
        GitHub
       </div>
       <div class="achievement-desc" id="github-handle">
        @venkateshbathena
       </div>
      </div>
      <div class="achievement-badge" style="cursor: pointer; position: relative;" onclick="window.open('https://twitter.com/venkatesh_sec', '_blank', 'noopener,noreferrer')">
       <div class="energy-trail"></div>
       <div style="font-size: 2.5rem; margin-bottom: 1rem;">
        🐦
       </div>
       <div class="achievement-title">
        Twitter
       </div>
       <div class="achievement-desc" id="twitter-handle">
        @venkatesh_sec
       </div>
      </div>
      <div class="achievement-badge" style="cursor: pointer; position: relative;">
       <div class="energy-trail"></div>
       <div style="font-size: 2.5rem; margin-bottom: 1rem;">
        🎮
       </div>
       <div class="achievement-title">
        Discord
       </div>
       <div class="achievement-desc" id="discord-handle">
        VenkateshB#2024
       </div>
      </div>
      <div class="achievement-badge" style="cursor: pointer; position: relative;" onclick="window.open('https://medium.com/@venkateshbathena', '_blank', 'noopener,noreferrer')">
       <div class="energy-trail"></div>
       <div style="font-size: 2.5rem; margin-bottom: 1rem;">
        📝
       </div>
       <div class="achievement-title">
        Medium
       </div>
       <div class="achievement-desc" id="medium-handle">
        @venkateshbathena
       </div>
      </div>
      <div class="achievement-badge" style="cursor: pointer; position: relative;" onclick="window.open('https://youtube.com/@VenkateshCyber', '_blank', 'noopener,noreferrer')">
       <div class="energy-trail"></div>
       <div style="font-size: 2.5rem; margin-bottom: 1rem;">
        📺
       </div>
       <div class="achievement-title">
        YouTube
       </div>
       <div class="achievement-desc" id="youtube-handle">
        VenkateshCyber
       </div>
      </div>
     </div>
    </div>
   </section><!-- Mindset Section -->
   <section class="mindset-section">
    <div class="quote" id="main-quote">
     Every challenge is a chance to level up
    </div>
    <p style="color: #cccccc; font-size: 1.1rem; margin-bottom: 2rem;">Learning cybersecurity with the heart of a champion</p>
    <div class="mindset-grid">
     <div class="mindset-item">
      Curiosity
     </div>
     <div class="mindset-item">
      Persistence
     </div>
     <div class="mindset-item">
      Ethics
     </div>
     <div class="mindset-item">
      Growth
     </div>
    </div>
   </section>
  </main>
  <script>
        // Initialize Element SDK
        const defaultConfig = {
            athlete_name: "VENKATESH BATHENA",
            athlete_title: "Cyber Security Student | Future Analyst | Digital Defender",
            hero_tagline: "Learning to defend the digital world, one skill at a time.",
            cyber_skills_score: "⭐⭐⭐⭐",
            ctf_battles: "8",
            projects_completed: "12",
            lab_sessions: "25",
            tools_learning: "8",
            about_title: "Rising Cyber Warrior",
            about_subtitle: "Building Skills Through Dedication & Discipline",
            about_description: "I'm a passionate cybersecurity student who approaches learning like an elite athlete approaches training. Every lab session, every CTF challenge, and every certification is a step toward mastering the art of digital defense. My goal is to become a guardian of the digital realm, protecting organizations and individuals from cyber threats.",
            cert1_name: "Cisco CyberOps Associate",
            cert1_issuer: "Cisco Systems",
            cert1_date: "2024",
            cert2_name: "CompTIA Security+",
            cert2_issuer: "CompTIA",
            cert2_date: "2024",
            cert3_name: "Ethical Hacking Basics",
            cert3_issuer: "Coursera",
            cert3_date: "2023",
            cert4_name: "Python for Security",
            cert4_issuer: "Udemy",
            cert4_date: "2023",
            email: "venkatesh.bathena@email.com",
            phone: "+91 98765 43210",
            location: "Hyderabad, India",
            linkedin_handle: "@venkateshbathena",
            github_handle: "@venkateshbathena",
            twitter_handle: "@venkatesh_sec",
            discord_handle: "VenkateshB#2024",
            medium_handle: "@venkateshbathena",
            youtube_handle: "VenkateshCyber"
        };

        async function onConfigChange(config) {
            // Update hero section
            document.getElementById('athlete-name').textContent = config.athlete_name || defaultConfig.athlete_name;
            document.getElementById('athlete-title').textContent = config.athlete_title || defaultConfig.athlete_title;
            document.getElementById('hero-tagline').textContent = config.hero_tagline || defaultConfig.hero_tagline;
            
            // Update stats
            document.getElementById('cyber-skills-score').textContent = config.cyber_skills_score || defaultConfig.cyber_skills_score;
            document.getElementById('ctf-battles').textContent = config.ctf_battles || defaultConfig.ctf_battles;
            document.getElementById('projects-completed').textContent = config.projects_completed || defaultConfig.projects_completed;
            document.getElementById('lab-sessions').textContent = config.lab_sessions || defaultConfig.lab_sessions;
            document.getElementById('tools-learning').textContent = config.tools_learning || defaultConfig.tools_learning;

            // Update about section
            document.getElementById('about-title').textContent = config.about_title || defaultConfig.about_title;
            document.getElementById('about-subtitle').textContent = config.about_subtitle || defaultConfig.about_subtitle;
            document.getElementById('about-description').textContent = config.about_description || defaultConfig.about_description;

            // Update certificates
            document.getElementById('cert1-name').textContent = config.cert1_name || defaultConfig.cert1_name;
            document.getElementById('cert1-issuer').textContent = config.cert1_issuer || defaultConfig.cert1_issuer;
            document.getElementById('cert1-date').textContent = config.cert1_date || defaultConfig.cert1_date;
            document.getElementById('cert2-name').textContent = config.cert2_name || defaultConfig.cert2_name;
            document.getElementById('cert2-issuer').textContent = config.cert2_issuer || defaultConfig.cert2_issuer;
            document.getElementById('cert2-date').textContent = config.cert2_date || defaultConfig.cert2_date;
            document.getElementById('cert3-name').textContent = config.cert3_name || defaultConfig.cert3_name;
            document.getElementById('cert3-issuer').textContent = config.cert3_issuer || defaultConfig.cert3_issuer;
            document.getElementById('cert3-date').textContent = config.cert3_date || defaultConfig.cert3_date;
            document.getElementById('cert4-name').textContent = config.cert4_name || defaultConfig.cert4_name;
            document.getElementById('cert4-issuer').textContent = config.cert4_issuer || defaultConfig.cert4_issuer;
            document.getElementById('cert4-date').textContent = config.cert4_date || defaultConfig.cert4_date;

            // Update contact info
            document.getElementById('email').textContent = config.email || defaultConfig.email;
            document.getElementById('phone').textContent = config.phone || defaultConfig.phone;
            document.getElementById('location').textContent = config.location || defaultConfig.location;

            // Update social handles
            document.getElementById('linkedin-handle').textContent = config.linkedin_handle || defaultConfig.linkedin_handle;
            document.getElementById('github-handle').textContent = config.github_handle || defaultConfig.github_handle;
            document.getElementById('twitter-handle').textContent = config.twitter_handle || defaultConfig.twitter_handle;
            document.getElementById('discord-handle').textContent = config.discord_handle || defaultConfig.discord_handle;
            document.getElementById('medium-handle').textContent = config.medium_handle || defaultConfig.medium_handle;
            document.getElementById('youtube-handle').textContent = config.youtube_handle || defaultConfig.youtube_handle;
        }

        function mapToCapabilities(config) {
            return {
                recolorables: [],
                borderables: [],
                fontEditable: undefined,
                fontSizeable: undefined
            };
        }

        function mapToEditPanelValues(config) {
            return new Map([
                ["athlete_name", config.athlete_name || defaultConfig.athlete_name],
                ["athlete_title", config.athlete_title || defaultConfig.athlete_title],
                ["hero_tagline", config.hero_tagline || defaultConfig.hero_tagline],
                ["cyber_skills_score", config.cyber_skills_score || defaultConfig.cyber_skills_score],
                ["ctf_battles", config.ctf_battles || defaultConfig.ctf_battles],
                ["projects_completed", config.projects_completed || defaultConfig.projects_completed],
                ["lab_sessions", config.lab_sessions || defaultConfig.lab_sessions],
                ["tools_learning", config.tools_learning || defaultConfig.tools_learning],
                ["about_title", config.about_title || defaultConfig.about_title],
                ["about_subtitle", config.about_subtitle || defaultConfig.about_subtitle],
                ["about_description", config.about_description || defaultConfig.about_description],
                ["cert1_name", config.cert1_name || defaultConfig.cert1_name],
                ["cert1_issuer", config.cert1_issuer || defaultConfig.cert1_issuer],
                ["cert1_date", config.cert1_date || defaultConfig.cert1_date],
                ["cert2_name", config.cert2_name || defaultConfig.cert2_name],
                ["cert2_issuer", config.cert2_issuer || defaultConfig.cert2_issuer],
                ["cert2_date", config.cert2_date || defaultConfig.cert2_date],
                ["cert3_name", config.cert3_name || defaultConfig.cert3_name],
                ["cert3_issuer", config.cert3_issuer || defaultConfig.cert3_issuer],
                ["cert3_date", config.cert3_date || defaultConfig.cert3_date],
                ["cert4_name", config.cert4_name || defaultConfig.cert4_name],
                ["cert4_issuer", config.cert4_issuer || defaultConfig.cert4_issuer],
                ["cert4_date", config.cert4_date || defaultConfig.cert4_date],
                ["email", config.email || defaultConfig.email],
                ["phone", config.phone || defaultConfig.phone],
                ["location", config.location || defaultConfig.location],
                ["linkedin_handle", config.linkedin_handle || defaultConfig.linkedin_handle],
                ["github_handle", config.github_handle || defaultConfig.github_handle],
                ["twitter_handle", config.twitter_handle || defaultConfig.twitter_handle],
                ["discord_handle", config.discord_handle || defaultConfig.discord_handle],
                ["medium_handle", config.medium_handle || defaultConfig.medium_handle],
                ["youtube_handle", config.youtube_handle || defaultConfig.youtube_handle]
            ]);
        }

        // Initialize SDK when available
        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange,
                mapToCapabilities,
                mapToEditPanelValues
            });
        }

        // Add dynamic effects
        document.addEventListener('DOMContentLoaded', function() {
            // Animate stats on scroll
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'fadeInUp 0.6s ease forwards';
                    }
                });
            }, observerOptions);

            // Observe all animated elements
            document.querySelectorAll('.stat-item, .achievement-badge, .match-card').forEach(el => {
                observer.observe(el);
            });

            // Add glitch effect to name on hover
            const athleteName = document.getElementById('athlete-name');
            athleteName.addEventListener('mouseenter', function() {
                this.style.animation = 'glitch 0.3s ease';
            });

            athleteName.addEventListener('animationend', function() {
                this.style.animation = '';
            });
        });

        // Add glitch animation
        const style = document.createElement('style');
        style.textContent = `
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

            @keyframes glitch {
                0% { transform: translate(0); }
                20% { transform: translate(-2px, 2px); }
                40% { transform: translate(-2px, -2px); }
                60% { transform: translate(2px, 2px); }
                80% { transform: translate(2px, -2px); }
                100% { transform: translate(0); }
            }
        `;
        document.head.appendChild(style);
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'998c8fcbf1a74013',t:'MTc2MjE4MDE0NC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
