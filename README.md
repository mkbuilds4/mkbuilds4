<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed - MK Builds</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
            color: #e0e0e0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 20px;
        }

        .hero {
            text-align: center;
            margin-bottom: 80px;
            position: relative;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: fadeInDown 1s ease;
        }

        .hero .subtitle {
            font-size: 1.4rem;
            color: #a0a0a0;
            max-width: 700px;
            margin: 0 auto 30px;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .philosophy {
            font-size: 1.1rem;
            color: #70A5FD;
            font-style: italic;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .stats-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 60px;
            backdrop-filter: blur(10px);
            animation: fadeIn 1s ease 0.6s both;
        }

        .stats-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .stats-header h2 {
            font-size: 2rem;
            color: #bf91f3;
            margin-bottom: 10px;
        }

        .contribution-count {
            font-size: 3rem;
            font-weight: 800;
            background: linear-gradient(135deg, #38bdae 0%, #70A5FD 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .contribution-label {
            color: #a0a0a0;
            font-size: 1.1rem;
        }

        .github-embed {
            width: 100%;
            text-align: center;
            margin-top: 30px;
        }

        .github-embed img {
            max-width: 100%;
            border-radius: 10px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .tech-stack {
            margin-bottom: 60px;
        }

        .tech-stack h2 {
            font-size: 2rem;
            color: #bf91f3;
            margin-bottom: 30px;
            text-align: center;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .tech-category {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            transform: translateY(-5px);
            border-color: #70A5FD;
            box-shadow: 0 10px 30px rgba(112, 165, 253, 0.2);
        }

        .tech-category h3 {
            color: #70A5FD;
            font-size: 1.2rem;
            margin-bottom: 15px;
        }

        .tech-category ul {
            list-style: none;
        }

        .tech-category li {
            color: #c0c0c0;
            padding: 5px 0;
            font-size: 0.95rem;
        }

        .projects {
            margin-bottom: 60px;
        }

        .projects h2 {
            font-size: 2rem;
            color: #bf91f3;
            margin-bottom: 40px;
            text-align: center;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #667eea 0%, #764ba2 100%);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .project-card:hover::before {
            transform: scaleX(1);
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        .project-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 15px;
        }

        .project-icon {
            font-size: 2rem;
        }

        .project-title {
            font-size: 1.8rem;
            color: #fff;
        }

        .project-description {
            color: #b0b0b0;
            margin-bottom: 20px;
            font-size: 1.05rem;
        }

        .project-link {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            text-decoration: none;
            border-radius: 25px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.4);
        }

        .learning-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 60px;
        }

        .learning-section h2 {
            font-size: 2rem;
            color: #bf91f3;
            margin-bottom: 30px;
            text-align: center;
        }

        .learning-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .learning-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
        }

        .learning-card h3 {
            color: #70A5FD;
            margin-bottom: 15px;
        }

        .learning-card ul {
            list-style: none;
        }

        .learning-card li {
            color: #c0c0c0;
            padding: 8px 0;
            padding-left: 20px;
            position: relative;
        }

        .learning-card li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: #38bdae;
        }

        .connect {
            text-align: center;
            padding: 60px 20px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .connect h2 {
            font-size: 2rem;
            color: #bf91f3;
            margin-bottom: 20px;
        }

        .connect p {
            color: #b0b0b0;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        .social-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 12px 30px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 25px;
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-color: transparent;
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

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

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .subtitle {
                font-size: 1.1rem;
            }

            .contribution-count {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hero">
            <h1>Hi there, I'm Mohamed 👋</h1>
            <p class="subtitle">
                A builder, developer, and storyteller focused on creating tools that help people grow. 
                I work across mobile apps, backend systems, and AI-driven features, currently building 
                <strong>Deen n' Dunya</strong>, <strong>Sanad+</strong>, and a suite of productivity and 
                community-centered tools under <strong>MK Builds</strong>.
            </p>
            <p class="philosophy">
                "Build with purpose, ship quickly, and constantly refine using data, design, and first-principles thinking."
            </p>
        </div>

        <div class="stats-section">
            <div class="stats-header">
                <h2>🔥 GitHub Activity</h2>
                <div class="contribution-count">390</div>
                <div class="contribution-label">contributions in the last year</div>
            </div>
            <div class="github-embed">
                <img src="https://ghchart.rshah.org/667eea/mkbuilds4" alt="GitHub Contribution Chart" />
            </div>
        </div>

        <div class="tech-stack">
            <h2>💻 Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h3>Mobile & Frontend</h3>
                    <ul>
                        <li>Flutter / Dart</li>
                        <li>iOS & Android</li>
                        <li>Figma</li>
                    </ul>
                </div>
                <div class="tech-category">
                    <h3>Backend & Database</h3>
                    <ul>
                        <li>Supabase / PostgreSQL</li>
                        <li>Firebase / Firestore</li>
                        <li>Edge Functions</li>
                    </ul>
                </div>
                <div class="tech-category">
                    <h3>Tools & Platform</h3>
                    <ul>
                        <li>Cursor / VS Code</li>
                        <li>Vercel / Notion</li>
                        <li>Mixpanel / OneSignal</li>
                    </ul>
                </div>
                <div class="tech-category">
                    <h3>Specialization</h3>
                    <ul>
                        <li>Mobile-first systems</li>
                        <li>AI-assisted experiences</li>
                        <li>Gamification</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="projects">
            <h2>📱 Featured Projects</h2>
            
            <div class="project-card">
                <div class="project-header">
                    <span class="project-icon">🌙</span>
                    <h3 class="project-title">Deen n' Dunya</h3>
                </div>
                <p class="project-description">
                    A personal-growth system designed to help people build consistency in faith and life through 
                    streaks, daily habits, tokens, and long-term challenges. Features a full token economy, 
                    challenges system, shop, streak logic, and cross-platform architecture.
                </p>
                <a href="https://deenndunya.org" class="project-link" target="_blank">Visit Project →</a>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <span class="project-icon">🕌</span>
                    <h3 class="project-title">Sanad+</h3>
                </div>
                <p class="project-description">
                    A spiritual support companion focused on Salah — reminders, reflections, and khushoo-building 
                    tools wrapped in a minimal and modern design.
                </p>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <span class="project-icon">📚</span>
                    <h3 class="project-title">Manara</h3>
                </div>
                <p class="project-description">
                    An education and CRM platform built for local programs to manage attendance, communication, 
                    teacher tools, finances, and community operations in one place.
                </p>
                <a href="https://manara.mkbuilds.dev" class="project-link" target="_blank">Visit Project →</a>
            </div>
        </div>

        <div class="learning-section">
            <h2>🌱 Growth & Learning</h2>
            <div class="learning-grid">
                <div class="learning-card">
                    <h3>Currently Exploring</h3>
                    <ul>
                        <li>Deeper Islamic studies</li>
                        <li>Advanced backend patterns</li>
                        <li>Scalable infrastructure</li>
                        <li>Platform-level growth strategies</li>
                    </ul>
                </div>
                <div class="learning-card">
                    <h3>What's Next</h3>
                    <ul>
                        <li>AI coaching inside apps</li>
                        <li>Intelligent user-insight systems</li>
                        <li>Mini-app ecosystem inside DnD</li>
                        <li>On-device AI & agent workflows</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="connect">
            <h2>🤝 Let's Connect</h2>
            <p>
                Open to selective collaborations, especially projects that combine tech, personal growth, 
                and community impact. I love conversations about app building, entrepreneurship, personal 
                growth, Islamic education, and community systems.
            </p>
            <div class="social-links">
                <a href="https://mkbuilds.dev" class="social-link" target="_blank">
                    🌐 Portfolio
                </a>
                <a href="https://instagram.com/YOUR_HANDLE" class="social-link" target="_blank">
                    📸 Instagram
                </a>
                <a href="mailto:YOUR_EMAIL" class="social-link" target="_blank">
                    ✉️ Email
                </a>
            </div>
        </div>
    </div>
</body>
</html>
