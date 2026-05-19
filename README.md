<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARASAKA MEDICAL | Santo Domingo Transformation Plan</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Space+Grotesk:wght@300;400;600&family=Roboto+Mono:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-dark: #050508;
            --panel-dark: #0d0d13;
            --accent-cyan: #00f3ff;
            --accent-red: #ff003c;
            --accent-gold: #ffb700;
            --text-light: #f5f5fa;
            --text-dim: #7e7e8c;
            --border-glow: 0 0 15px rgba(0, 243, 255, 0.25);
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            background-color: var(--bg-dark);
            color: var(--text-light);
            font-family: 'Space Grotesk', sans-serif;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Glitch Effect Elements */
        .glitch-text {
            font-family: 'Orbitron', sans-serif;
            position: relative;
            color: var(--text-light);
        }
        .glitch-text::after {
            content: attr(data-text);
            position: absolute;
            left: 2px; text-shadow: -1px 0 var(--accent-red);
            top: 0; color: var(--text-light); background: var(--bg-dark);
            overflow: hidden; clip: rect(0,900px,0,0); 
            animation: glitch-anim 2s infinite linear alternate-reverse;
        }
        @keyframes glitch-anim {
            0% { clip: rect(15px, 9999px, 66px, 0); }
            100% { clip: rect(34px, 9999px, 55px, 0); }
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 25px 50px;
            border-bottom: 1px solid #1a1a26;
            background: rgba(5, 5, 8, 0.85);
            backdrop-filter: blur(10px);
            position: fixed; width: 100%; top: 0; z-index: 1000;
        }
        .logo-area {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .logo-svg {
            width: 45px; height: 45px;
            fill: var(--text-light);
            filter: drop-shadow(0 0 5px var(--accent-cyan));
        }
        .logo-text {
            font-family: 'Orbitron', sans-serif;
            font-weight: 900; letter-spacing: 4px; font-size: 20px;
        }
        .nav-links { display: flex; gap: 35px; list-style: none; }
        .nav-links a {
            color: var(--text-dim); text-decoration: none;
            font-family: 'Roboto Mono', monospace; font-size: 14px;
            transition: 0.3s; text-transform: uppercase;
        }
        .nav-links a:hover, .nav-links a.active { color: var(--accent-cyan); text-shadow: var(--border-glow); }
        
        .cta-btn {
            background: transparent; border: 1px solid var(--accent-cyan);
            color: var(--accent-cyan); font-family: 'Orbitron', sans-serif;
            padding: 10px 24px; font-weight: bold; cursor: pointer;
            transition: 0.3s; letter-spacing: 1px;
            box-shadow: var(--border-glow);
        }
        .cta-btn:hover {
            background: var(--accent-cyan); color: #000;
            box-shadow: 0 0 25px var(--accent-cyan);
        }

        /* Hero Section */
        section.hero {
            padding-top: 180px; padding-bottom: 100px;
            min-height: 100vh; display: flex; align-items: center;
            position: relative;
        }
        .hero-grid {
            max-width: 1300px; margin: 0 auto; padding: 0 50px;
            display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 60px;
            align-items: center;
        }
        .hero-tag {
            font-family: 'Roboto Mono', monospace; color: var(--accent-red);
            font-size: 14px; letter-spacing: 3px; font-weight: bold; margin-bottom: 20px;
        }
        .hero h1 {
            font-size: 64px; font-weight: 900; line-height: 1.1;
            margin-bottom: 30px; letter-spacing: -1px;
        }
        .hero p { font-size: 18px; color: var(--text-dim); max-width: 600px; margin-bottom: 40px; }
        
        .hero-graphic {
            border: 1px solid #1a1a26; background: var(--panel-dark);
            height: 450px; position: relative; border-radius: 4px;
            display: flex; align-items: center; justify-content: center;
            overflow: hidden; box-shadow: inset 0 0 40px rgba(0,0,0,0.8);
        }
        .grid-bg {
            position: absolute; width: 200%; height: 200%;
            background-image: linear-gradient(rgba(26,26,38,0.15) 1px, transparent 1px), linear-gradient(90deg, rgba(26,26,38,0.15) 1px, transparent 1px);
            background-size: 30px 30px; transform: rotateX(60deg) translateY(-30%);
            animation: grid-move 20s infinite linear; opacity: 0.5;
        }
        @keyframes grid-move { 0% { transform: rotateX(60deg) translateY(0); } 100% { transform: rotateX(60deg) translateY(-50%); } }

        .center-hud {
            z-index: 2; text-align: center; font-family: 'Roboto Mono', monospace;
        }
        .center-hud i { font-size: 70px; color: var(--accent-cyan); animation: pulse 2s infinite; }
        @keyframes pulse { 0% { opacity: 0.4; } 50% { opacity: 1; } 100% { opacity: 0.4; } }

        /* Tech Features Section */
        .section-title {
            text-align: center; font-size: 36px; font-family: 'Orbitron', sans-serif;
            margin-bottom: 60px; letter-spacing: 2px;
        }
        .section-title span { color: var(--accent-cyan); }
        
        .features-section { padding: 100px 50px; max-width: 1300px; margin: 0 auto; }
        .tech-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; }
        .tech-card {
            background: var(--panel-dark); border: 1px solid #1a1a26;
            padding: 40px 30px; border-radius: 4px; position: relative; transition: 0.3s;
        }
        .tech-card:hover {
            border-color: var(--accent-cyan); transform: translateY(-5px);
            box-shadow: var(--border-glow);
        }
        .tech-card .icon-wrap {
            width: 60px; height: 60px; background: rgba(0, 243, 255, 0.05);
            border: 1px solid rgba(0, 243, 255, 0.2); border-radius: 4px;
            display: flex; align-items: center; justify-content: center;
            font-size: 24px; color: var(--accent-cyan); margin-bottom: 30px;
        }
        .tech-card h3 { font-family: 'Orbitron', sans-serif; font-size: 20px; margin-bottom: 15px; letter-spacing: 1px; }
        .tech-card p { color: var(--text-dim); font-size: 15px; }

        /* Core Matrix Pillars Table */
        .matrix-section { padding: 100px 50px; max-width: 1300px; margin: 0 auto; }
        .table-container {
            background: var(--panel-dark); border: 1px solid #1a1a26; border-radius: 4px; overflow: hidden;
        }
        table { width: 100%; border-collapse: collapse; text-align: left; }
        th {
            background: #11111a; padding: 22px 30px; font-family: 'Orbitron', sans-serif;
            font-size: 14px; letter-spacing: 2px; color: var(--accent-cyan); border-bottom: 1px solid #1a1a26;
        }
        td { padding: 22px 30px; border-bottom: 1px solid #12121a; font-size: 16px; }
        tr:last-child td { border-bottom: none; }
        .pillar-tag {
            font-family: 'Roboto Mono', monospace; font-weight: bold;
            background: rgba(255, 0, 60, 0.1); border: 1px solid rgba(255, 0, 60, 0.3);
            color: var(--accent-red); padding: 4px 12px; border-radius: 2px; font-size: 13px;
        }

        /* Pricing & Logistics Section */
        .pricing-section { padding: 100px 50px; max-width: 1300px; margin: 0 auto; text-align: center; }
        .price-box {
            background: radial-gradient(circle at center, #11111a 0%, var(--panel-dark) 100%);
            border: 1px solid #1a1a26; max-width: 700px; margin: 0 auto;
            padding: 60px 40px; border-radius: 4px; position: relative;
        }
        .price-box::before {
            content: 'SANTO DOMINGO EXCLUSIVE'; position: absolute; top: -12px; left: 50%;
            transform: translateX(-50%); background: var(--accent-gold); color: #000;
            font-family: 'Roboto Mono', monospace; font-size: 11px; font-weight: bold;
            padding: 2px 16px; letter-spacing: 2px; border-radius: 2px;
        }
        .price-tag {
            font-family: 'Orbitron', sans-serif; font-size: 84px; font-weight: 900;
            color: var(--accent-gold); margin: 20px 0; line-height: 1;
        }
        .price-desc { font-family: 'Roboto Mono', monospace; color: var(--text-dim); margin-bottom: 40px; font-size: 14px; }
        
        .logistics-grid {
            display: grid; grid-template-columns: 1fr 1fr; gap: 30px; margin-top: 40px; text-align: left;
        }
        .logistics-card {
            border-left: 3px solid var(--accent-cyan); padding-left: 20px;
        }
        .logistics-card h4 { font-family: 'Orbitron', sans-serif; font-size: 16px; margin-bottom: 8px; color: var(--text-light); }
        .logistics-card p { font-size: 14px; color: var(--text-dim); }

        /* Footer */
        footer {
            border-top: 1px solid #1a1a26; padding: 40px 50px; text-align: center;
            font-family: 'Roboto Mono', monospace; font-size: 12px; color: var(--text-dim);
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo-area">
            <svg class="logo-svg" viewBox="0 0 100 100">
                <polygon points="50,15 80,45 65,45 50,30 35,45 20,45"/>
                <polygon points="50,43 85,78 70,78 50,58 30,78 15,78"/>
                <circle cx="50" cy="88" r="4"/>
            </svg>
            <div class="logo-text">ARASAKA</div>
        </div>
        <ul class="nav-links">
            <li><a href="#hero" class="active">Overview</a></li>
            <li><a href="#specs">Specifications</a></li>
            <li><a href="#matrix">Core Pillars</a></li>
            <li><a href="#pricing">Logistics & Price</a></li>
        </ul>
        <button class="cta-btn" onclick="window.location.href='#pricing'">BOOK CLINIC</button>
    </nav>

    <section class="hero" id="hero">
        <div class="hero-grid">
            <div class="hero-info">
                <div class="hero-tag">// SPECIAL MEDICAL PROJECT</div>
                <h1 class="glitch-text" data-text="REFRAME YOUR BIOLOGY.">REFRAME YOUR BIOLOGY.</h1>
                <p>Welcome to the premium Santo Domingo Prosthetic Transformation Plan. Engineered for individuals seeking flawless adaptation, unmatched structural integrity, and deep neural synchronization. From your current localization directly to our elite facility.</p>
                <button class="cta-btn" style="padding: 15px 35px;" onclick="window.location.href='#pricing'">INITIALIZE ADMISSION</button>
            </div>
            <div class="hero-graphic">
                <div class="grid-bg"></div>
                <div class="center-hud">
                    <i class="fa-solid fa-fingerprint"></i>
                    <p style="margin-top:20px; font-size:12px; letter-spacing:2px; color:var(--accent-cyan)">BIOMETRIC SECURE LINK</p>
                </div>
            </div>
        </div>
    </section>

    <section class="features-section" id="specs">
        <h2 class="section-title">ENGINEERED <span>PERFECTION</span></h2>
        <div class="tech-grid">
            <div class="tech-card">
                <div class="icon-wrap"><i class="fa-solid fa-brain"></i></div>
                <h3>0 Awareness</h3>
                <p>Advanced high-tech neural plug-ins bypass biological rejection. Operates seamlessly beneath conscious threshold, offering zero friction and immediate cortical acceptance.</p>
            </div>
            <div class="tech-card">
                <div class="icon-wrap"><i class="fa-solid fa-bolt"></i></div>
                <h3>No Need Charge</h3>
                <p>Equipped with internal bio-electric micro-cells that harvest thermal and kinetic energy directly from human somatic feedback. Absolute energy autonomy.</p>
            </div>
            <div class="tech-card">
                <div class="icon-wrap"><i class="fa-solid fa-shield-halved"></i></div>
                <h3>Total Control</h3>
                <p>Includes a mandatory, elite 6-month post-operative care and synchronization program. Guarantees 100% calibration with muscle-growth and motor reflexes.</p>
            </div>
        </div>
    </section>

    <section class="matrix-section" id="matrix">
        <h2 class="section-title">THE <span>ARASAKA MATRIX</span></h2>
        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>OPERATIONAL PILLAR</th>
                        <th>TECHNICAL STANDARD</th>
                        <th>SYSTEM RETURN EXPECTATION</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><span class="pillar-tag">EXPERT</span></td>
                        <td>Managed by top neurosurgeons and structural cyberware engineers.</td>
                        <td>Zero surgical derivation, micro-millimeter precision placement.</td>
                    </tr>
                    <tr>
                        <td><span class="pillar-tag">PROFESSION</span></td>
                        <td>Hospital-grade sterile execution chambers, Grade-5 Titanium matrix.</td>
                        <td>Absolute elimination of standard tissue contamination risks.</td>
                    </tr>
                    <tr>
                        <td><span class="pillar-tag">FAST</span></td>
                        <td>Streamlined micro-invasive surgical protocols.</td>
                        <td>Accelerated structural recovery. Leave operational within hours.</td>
                    </tr>
                    <tr>
                        <td><span class="pillar-tag">SAFE</span></td>
                        <td>Triple-layered hardware firewalls & bio-compatible plating.</td>
                        <td>Complete insulation from local network breaches and organic rejection.</td>
                    </tr>
                    <tr>
                        <td><span class="pillar-tag">INCREASE</span></td>
                        <td>Integrated neural signal amplifiers.</td>
                        <td>Substantial acceleration in raw cognitive data processing and reflex index.</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>

    <section class="pricing-section" id="pricing">
        <h2 class="section-title">ADMISSION <span>& VALUATION</span></h2>
        <div class="price-box">
            <p style="font-family: 'Roboto Mono', monospace; font-size:14px; letter-spacing:1px;">TOTAL PLAN PACKAGE RETAIL COST</p>
            <div class="price-tag">¥114,500</div>
            <p class="price-desc">INCLUSIVE OF PROSTHETIC HARDWARE, NEURAL COUPLING, AND 6 MONTHS COMPREHENSIVE RECOVERY MONITORING.</p>
            
            <div style="border-top: 1px solid #1a1a26; padding-top: 30px;">
                <h3 style="font-family:'Orbitron'; font-size:20px; color:var(--accent-cyan); letter-spacing:1px;">LOAD TODAY, LEAVE TODAY</h3>
                <p style="font-size:14px; color:var(--text-dim); margin-top:10px;">Frictionless process. Same-day transport mobilization, surgical execution, and neural sync authorization.</p>
            </div>

            <div class="logistics-grid">
                <div class="logistics-card">
                    <h4>Direct Deployment</h4>
                    <p>Secured medical transport unit deploys to your home coordinate instantly upon transaction authentication.</p>
                </div>
                <div class="logistics-card">
                    <h4>Instant Adaptability</h4>
                    <p>Neural circuits settle immediately, ensuring full legal mobile capacity the moment you exit the operating table.</p>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <p>© 2026 ARASAKA MEDICAL CORP. / SANTO DOMINGO ADMISSION NODE. ALL RIGHTS SECURITY ENFORCED.</p>
        <p style="color: #333; margin-top: 5px;">RESTRICTED UNDER CYBER-REGULATORY EXECUTIVE ORDER 77-B</p>
    </footer>

    <script>
        // Smooth scrolling active links indicator
        window.addEventListener('scroll', () => {
            let scrollDistance = window.scrollY;
            document.querySelectorAll('section').forEach((el, i) => {
                if (el.offsetTop - 200 <= scrollDistance) {
                    document.querySelectorAll('.nav-links a').forEach((el) => {
                        if (el.classList.contains('active')) el.classList.remove('active');
                    });
                    document.querySelectorAll('.nav-links li')[i].querySelector('a').classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
