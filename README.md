
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hossain Islam Hemel - Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* CSS Variables for colors - easily customizable */
        :root {
            --primary-color: #2563eb; /* Vibrant Blue */
            --bg-color: #f8fafc;
            --card-bg: #ffffff;
            --text-main: #1e293b;
            --text-sub: #64748b;
            --transition-speed: 0.3s;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        /* --- Global Styles --- */
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 20px;
        }
        section {
            padding: 80px 0;
        }
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            position: relative;
        }
        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background-color: var(--primary-color);
            margin: 10px auto 0;
            border-radius: 2px;
        }

        /* --- Header / Nav --- */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        nav.container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo { font-size: 1.5rem; font-weight: 600; color: var(--primary-color); }
        .nav-links { display: flex; gap: 30px; }
        .nav-links a:hover { color: var(--primary-color); font-weight: 400; }

        /* --- Hero Section --- */
        #home {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(135deg, #e0f2fe 0%, #f0f9ff 100%);
        }
        #home h1 { font-size: 3.5rem; font-weight: 600; margin-bottom: 10px; }
        #home h2 { font-size: 1.5rem; color: var(--text-sub); font-weight: 300; margin-bottom: 30px; }
        .hero-info p { color: var(--text-sub); margin-bottom: 10px; }
        .hero-btn {
            display: inline-block;
            margin-top: 30px;
            padding: 12px 30px;
            background-color: var(--primary-color);
            color: #fff;
            border-radius: 30px;
            font-weight: 600;
            transition: var(--transition-speed);
        }
        .hero-btn:hover { background-color: #1d4ed8; transform: translateY(-3px); }

        /* --- Cards & Grid Layouts --- */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        .card {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: var(--transition-speed);
        }
        .card:hover { transform: translateY(-5px); box-shadow: 0 10px 15px rgba(0,0,0,0.1); }
        .card-icon {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        .card h3 { margin-bottom: 15px; font-weight: 600; }
        .card p, .card ul { color: var(--text-sub); font-weight: 300; }

        /* --- Experience/Education Details --- */
        .timeline-item {
            position: relative;
            padding-left: 30px;
            margin-bottom: 30px;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 5px;
            width: 12px;
            height: 12px;
            background-color: var(--primary-color);
            border-radius: 50%;
        }
        .timeline-item::after {
            content: '';
            position: absolute;
            left: 5px;
            top: 22px;
            width: 2px;
            height: calc(100% + 10px);
            background-color: #e2e8f0;
        }
        .timeline-item:last-child::after { display: none; }
        .timeline-date { color: var(--primary-color); font-weight: 600; font-size: 0.9rem; }

        /* --- Contact --- */
        .contact-links {
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: center;
        }
        .contact-btn {
            display: flex;
            align-items: center;
            gap: 15px;
            width: 100%;
            max-width: 400px;
            padding: 15px;
            background: var(--card-bg);
            border: 2px solid transparent;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            transition: var(--transition-speed);
        }
        .contact-btn:hover {
            border-color: var(--primary-color);
            transform: translateX(5px);
        }
        .contact-btn span.icon {
            font-size: 1.5rem;
            color: var(--primary-color);
        }

        /* --- Responsive Styles (Tablet and Mobile) --- */
        @media (max-width: 768px) {
            #home h1 { font-size: 2.8rem; }
            .section-title { font-size: 2rem; }
            .nav-links { display: none; } /* Hide on small screens */
        }
    </style>
</head>
<body>

    <header>
        <nav class="container">
            <a href="#home" class="logo">Hossain Islam Hemel</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <div class="container hero-info">
            <h2>Hello, I'm</h2>
            <h1>Hossain Islam Hemel</h1>
            <h2>Research & Tech Enthusiast | Notre Dame College</h2>
            <p>A passionate HSC '26 student focused on exploration.</p>
            <p>From Rajarhat, Kurigram, currently exploring tech in Dhaka.</p>
            <a href="#contact" class="hero-btn">Connect With Me</a>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="grid-3">
                <div class="card">
                    <div class="card-icon">🔍</div>
                    <h3>Research & Tech</h3>
                    <p>I thrive on finding things out and exploring new technologies. My interest in tech is fueled by curiosity.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🤖</div>
                    <h3>Robotics</h3>
                    <p>My journey includes job simulations from Forage and active participation in the Robotics Olympiad.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🏏</div>
                    <h3>Hobbies</h3>
                    <p>When I'm not exploring tech, you can find me enjoying a game of cricket or engaging in lively gossiping sessions.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="education">
        <div class="container">
            <h2 class="section-title">Education</h2>
            <div class="card">
                <div class="timeline-item">
                    <p class="timeline-date">Current</p>
                    <h3>Notre Dame College, Dhaka</h3>
                    <p>HSC, Batch 2026</p>
                    <p>Living in Arambag, Dhaka.</p>
                </div>
                <div class="timeline-item">
                    <p class="timeline-date">SSC</p>
                    <h3>Deutirhat High School, Lalmonirhat</h3>
                    <p>Secondary School Certificate</p>
                    <p>Origin: Rajarhat, Kurigram.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <h2 class="section-title">Experience & Achievements</h2>
            <div class="grid-3">
                <div class="card">
                    <div class="card-icon">🎓</div>
                    <h3>Online Intern - Forage</h3>
                    <p>Participated in Robotics Job Simulations, gaining practical insights into the field.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🏆</div>
                    <h3>Robotics Olympiad</h3>
                    <p>Participated in the national level Robotics Olympiad, showcasing dedication and skill.</p>
                </div>
                <div class="card">
                    <div class="card-icon">💡</div>
                    <h3>Tech Exploration</h3>
                    <p>Continually engaged in self-learning and exploration of new technology trends.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-links card">
                <a href="https://www.facebook.com/hossain.islam.hemel.2025" target="_blank" class="contact-btn">
                    <span class="icon">👥</span>
                    <span>Facebook Profile</span>
                </a>
                <a href="https://www.linkedin.com/in/hossain-islam-hemel-84437b35a" target="_blank" class="contact-btn">
                    <span class="icon">🔗</span>
                    <span>LinkedIn Profile</span>
                </a>
                <a href="mailto:hossainislamhemel@gmail.com" class="contact-btn">
                    <span class="icon">📧</span>
                    <span>hossainislamhemel@gmail.com</span>
                </a>
            </div>
        </div>
    </section>

</body>
</html>
