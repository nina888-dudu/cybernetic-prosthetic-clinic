<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>NEXUS MEDICAL | Santo Domingo Prosthetic Transformation</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts: Inter & Space Grotesk for cyber-sleek feel -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #03030C;
            font-family: 'Inter', sans-serif;
            color: #EBECF2;
            line-height: 1.5;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        /* Cyberpunk grid + glowing overlay */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 255, 255, 0.02) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 255, 0.02) 1px, transparent 1px);
            background-size: 40px 40px;
            pointer-events: none;
            z-index: 0;
        }

        /* Glow orbs */
        .bg-glow {
            position: fixed;
            width: 60vw;
            height: 60vw;
            background: radial-gradient(circle, rgba(0, 234, 255, 0.08) 0%, rgba(0, 0, 0, 0) 70%);
            border-radius: 50%;
            top: -20%;
            right: -20%;
            pointer-events: none;
            z-index: 0;
        }
        .bg-glow-2 {
            position: fixed;
            width: 80vh;
            height: 80vh;
            background: radial-gradient(circle, rgba(182, 36, 255, 0.06) 0%, rgba(0,0,0,0) 70%);
            bottom: 0;
            left: -30%;
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 0 30px;
            position: relative;
            z-index: 2;
        }

        /* glass card style */
        .glass-card {
            background: rgba(12, 15, 28, 0.65);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(0, 234, 255, 0.2);
            border-radius: 32px;
            transition: all 0.3s ease;
        }
        .glass-card:hover {
            border-color: rgba(0, 234, 255, 0.6);
            box-shadow: 0 0 18px rgba(0, 234, 255, 0.1);
        }

        /* navigation */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 24px 0;
            flex-wrap: wrap;
            border-bottom: 1px solid rgba(0, 234, 255, 0.25);
            margin-bottom: 20px;
        }
        .logo {
            font-family: 'Space Grotesk', monospace;
            font-size: 1.7rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #FFFFFF, #00EAFF);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        .nav-links {
            display: flex;
            gap: 2rem;
            align-items: center;
            flex-wrap: wrap;
        }
        .nav-links a {
            text-decoration: none;
            color: #D0D5F0;
            font-weight: 500;
            transition: 0.2s;
            font-size: 0.95rem;
            letter-spacing: 0.3px;
        }
        .nav-links a:hover {
            color: #00EAFF;
            text-shadow: 0 0 5px #00EAFF;
        }
        .btn-outline-cyan {
            border: 1.5px solid #00EAFF;
            background: transparent;
            padding: 8px 20px;
            border-radius: 60px;
            color: #00EAFF;
            font-weight: 600;
            transition: 0.25s;
            cursor: pointer;
        }
        .btn-outline-cyan:hover {
            background: #00EAFF20;
            box-shadow: 0 0 12px #00EAFF40;
        }

        /* buttons */
        .btn-primary {
            background: linear-gradient(105deg, #00C9FF, #00EAFF);
            border: none;
            padding: 14px 34px;
            border-radius: 40px;
            font-weight: 700;
            font-size: 1rem;
            color: #03030C;
            cursor: pointer;
            transition: 0.25s;
            box-shadow: 0 0 10px #00EAFF60;
        }
        .btn-primary:hover {
            transform: scale(1.02);
            box-shadow: 0 0 22px #00EAFF;
        }
        .btn-secondary {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(0, 234, 255, 0.6);
            padding: 14px 34px;
            border-radius: 40px;
            font-weight: 600;
            color: #EBECF2;
            cursor: pointer;
            transition: 0.2s;
        }
        .btn-secondary:hover {
            background: rgba(0, 234, 255, 0.15);
            border-color: #00EAFF;
        }

        /* hero */
        .hero {
            padding: 60px 0 80px 0;
        }
        .hero-badge {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            color: #00EAFF;
            background: rgba(0, 234, 255, 0.1);
            display: inline-block;
            padding: 6px 14px;
            border-radius: 40px;
            margin-bottom: 24px;
        }
        h1 {
            font-size: 4.2rem;
            font-weight: 800;
            line-height: 1.2;
            font-family: 'Space Grotesk', monospace;
            background: linear-gradient(135deg, #FFFFFF 30%, #93F9FF 80%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 20px;
        }
        .hero-sub {
            font-size: 1.25rem;
            color: #B0B8E0;
            max-width: 650px;
            margin-bottom: 32px;
        }
        .home-to-hospital {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: rgba(0,0,0,0.5);
            padding: 8px 18px;
            border-radius: 60px;
            border-left: 3px solid #00EAFF;
            font-weight: 500;
            margin-bottom: 30px;
        }

        /* section titles */
        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            font-family: 'Space Grotesk', monospace;
            margin-bottom: 15px;
        }
        .section-sub {
            color: #7F89B0;
            margin-bottom: 48px;
            border-left: 3px solid #00EAFF;
            padding-left: 20px;
        }
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }
        .tech-card {
            background: rgba(8, 12, 25, 0.75);
            backdrop-filter: blur(4px);
            border-radius: 28px;
            padding: 32px 24px;
            border: 1px solid rgba(0, 234, 255, 0.2);
            transition: all 0.3s;
        }
        .tech-card i {
            font-size: 2.5rem;
            color: #00EAFF;
            margin-bottom: 20px;
        }
        .tech-card h3 {
            font-size: 1.7rem;
            font-weight: 600;
            margin-bottom: 12px;
        }
        .tech-card p {
            color: #B7C0E0;
            line-height: 1.5;
        }

        /* advantage 5 pillars grid */
        .pillars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin: 50px 0;
        }
        .pillar {
            background: rgba(0, 0, 0, 0.45);
            backdrop-filter: blur(4px);
            border-radius: 28px;
            padding: 28px 16px;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.08);
            transition: 0.2s;
        }
        .pillar:hover {
            border-color: #00EAFF;
            transform: translateY(-5px);
        }
        .pillar h4 {
            font-size: 2rem;
            font-weight: 800;
            background: linear-gradient(145deg, #FFFFFF, #9beaff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 12px;
        }
        .pillar p {
            font-size: 0.85rem;
            color: #B0BBE5;
        }

        /* logistics + price */
        .load-section {
            background: linear-gradient(135deg, rgba(0, 20, 30, 0.8), rgba(2, 5, 18, 0.9));
            border-radius: 48px;
            padding: 48px 40px;
            margin: 60px 0;
            border: 1px solid rgba(0, 234, 255, 0.3);
            box-shadow: 0 15px 35px rgba(0,0,0,0.5);
        }
        .load-today {
            font-family: 'Space Grotesk', monospace;
            font-size: 2.4rem;
            font-weight: 700;
            letter-spacing: -0.5px;
        }
        .price-badge {
            font-size: 3rem;
            font-weight: 800;
            background: linear-gradient(145deg, #FFF, #00f2ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        .price-footnote {
            color: #8892b0;
            font-size: 0.9rem;
        }
        .scan-area {
            background: rgba(0,0,0,0.6);
            border-radius: 32px;
            padding: 20px;
            text-align: center;
            border: 1px dashed #00EAFF;
            margin-top: 30px;
        }

        footer {
            margin-top: 80px;
            padding: 40px 0 30px;
            border-top: 1px solid rgba(0, 234, 255, 0.2);
            font-size: 0.8rem;
            color: #6F78A0;
        }

        @media (max-width: 780px) {
            h1 { font-size: 2.5rem; }
            .navbar { flex-direction: column; gap: 20px; }
            .nav-links { justify-content: center; gap: 1.2rem; }
            .container { padding: 0 20px; }
            .load-today { font-size: 1.8rem; }
            .price-badge { font-size: 2.2rem; }
            .load-section { padding: 30px 20px; }
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(20px);}
            to { opacity: 1; transform: translateY(0);}
        }
        .animate {
            animation: fadeUp 0.6s ease forwards;
        }
        .glow-text {
            text-shadow: 0 0 6px rgba(0,234,255,0.3);
        }
    </style>
</head>
<body>
<div class="bg-glow"></div>
<div class="bg-glow-2"></div>

<div class="container">
    <!-- Navigation -->
    <nav class="navbar">
        <div class="logo">NEXUS MEDICAL</div>
        <div class="nav-links">
            <a href="#">About Us</a>
            <a href="#">Prosthetics & Cyberware</a>
            <a href="#" style="border-bottom: 2px solid #00EAFF;">The Santo Domingo Plan</a>
            <a href="#">Patient Care</a>
            <button class="btn-outline-cyan"><i class="fas fa-calendar-alt"></i> BOOK CONSULTATION</button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-badge"><i class="fas fa-microchip"></i> NEXT-GEN BIOMECHANICS</div>
        <h1>Reframe Your<br>Evolution.</h1>
        <div class="home-to-hospital">
            <i class="fas fa-car-side"></i> From your home → to hospital → elite recovery
        </div>
        <p class="hero-sub">The Santo Domingo Prosthetic Transformation Plan: seamless integration from your residence to our premium facilities. Experience the future of human augmentation — zero pain, total bio-synchronization.</p>
        <div style="display: flex; gap: 18px; flex-wrap: wrap;">
            <button class="btn-primary"><i class="fas fa-syringe"></i> Begin Your Transformation</button>
            <button class="btn-secondary"><i class="fas fa-chart-line"></i> View Pricing</button>
        </div>
    </section>

    <!-- Core Technologies (species / plug-in / no pain / bio charge / 6 month care) -->
    <section>
        <div class="section-title">Engineered for Perfection</div>
        <div class="section-sub">Breaking the boundaries between biology and technology — zero awareness, bio-electric symbiosis, and total somatic mastery.</div>
        <div class="grid-3">
            <div class="tech-card">
                <i class="fas fa-brain"></i>
                <h3>Zero Sensory Awareness</h3>
                <p>High-tech neural plug-in interface with total pain signal suppression. Once calibrated, the prosthetic feels entirely organic — zero friction, zero discomfort. Pure fusion of mind and machine.</p>
                <div style="margin-top: 12px; font-size:0.8rem; color:#00EAFF;"><i class="fas fa-bolt"></i> no pain • instant reflex</div>
            </div>
            <div class="tech-card">
                <i class="fas fa-charging-station"></i>
                <h3>Bio-Electric Autonomy</h3>
                <p>Self-sustaining power architecture. Forgets charging cables — harvests kinetic & thermal energy from your own bio-electricity. Continuous power, driven by your metabolism.</p>
                <div style="margin-top: 12px; font-size:0.8rem; color:#00EAFF;"><i class="fas fa-database"></i> no need charge • body-powered</div>
            </div>
            <div class="tech-card">
                <i class="fas fa-heartbeat"></i>
                <h3>Total Somatic Synchronization</h3>
                <p>6-month comprehensive post-op care and elite physical reprogramming. Complete cybernetic mastery, enhanced strength, reflexes, and cognitive output — greater than your original body.</p>
                <div style="margin-top: 12px; font-size:0.8rem; color:#00EAFF;"><i class="fas fa-chart-simple"></i> 6 month care • greater your body</div>
            </div>
        </div>
        <p style="text-align: center; font-style: italic; background: rgba(0,0,0,0.3); border-radius: 40px; padding: 8px; max-width: 600px; margin: 0 auto; font-size:0.85rem;"><i class="fas fa-microchip"></i> High-tech plug-in • total body control • neural handshake guaranteed</p>
    </section>

    <!-- The Nexus Advantage (5 pillars) -->
    <section style="margin-top: 60px;">
        <div class="section-title">The Nexus Advantage</div>
        <div class="section-sub">Why the world's elite choose our cyber-surgical network</div>
        <div class="pillars-grid">
            <div class="pillar"><h4>EXPERT</h4><p>Directed by leading neurosurgeons & cyberware engineers. Nobel-awarded research.</p></div>
            <div class="pillar"><h4>PROFESSIONAL</h4><p>Elite, hospital-grade environments. ISO 7 cleanrooms & sterile state-of-the-art tech.</p></div>
            <div class="pillar"><h4>FAST</h4><p>Streamlined outpatient procedure. Ultra-accelerated recovery — ambulatory in hours.</p></div>
            <div class="pillar"><h4>SAFE</h4><p>Triple-certified bio-compatible alloys. Zero rejection rate guarantee.</p></div>
            <div class="pillar"><h4>INCREASE</h4><p>Quantifiable upgrades: +340% tensile strength, +180ms reflex gain, cognitive data stream.</p></div>
        </div>
    </section>

    <!-- Instant Mobilization + Pricing + LOAD TODAY LEAVE TODAY -->
    <section>
        <div class="load-section">
            <div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 20px;">
                <div>
                    <div class="load-today"><i class="fas fa-rocket"></i> LOAD TODAY. LEAVE TODAY.</div>
                    <p style="margin-top: 15px; font-size: 1rem; max-width: 500px;">Our medical response team coordinates your admission and neural prep the very same day — from your doorstep to the operation suite. Zero downtime, maximum precision.</p>
                    <div style="margin-top: 20px;"><i class="fas fa-shuttle-van"></i> 24/7 Biometric Transport Fleet</div>
                </div>
                <div style="text-align: right;">
                    <div class="price-badge">¥114,500</div>
                    <div class="price-footnote">starting from · basic prosthetic hardware<br>neural integration + 6-mo post-op care</div>
                    <button class="btn-primary" style="margin-top: 16px; padding: 12px 28px;"><i class="fas fa-credit-card"></i> Secure Your Slot</button>
                </div>
            </div>
            <div class="scan-area">
                <i class="fas fa-fingerprint" style="font-size: 28px; color: #00EAFF; margin-bottom: 10px; display: block;"></i>
                <p><strong>Scan Biometric ID to Begin</strong><br><span style="font-size: 0.75rem;">(retina / palm-vein / neural imprint ready)</span></p>
                <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent, #00EAFF, transparent); margin: 15px 0;"></div>
                <i class="fas fa-qrcode" style="opacity: 0.7; letter-spacing: 2px;">  SIMULATED NEURAL GATEWAY  </i>
            </div>
        </div>
    </section>

    <!-- Additional seamless integration & features ( home to hospital care timeline ) -->
    <div style="display: flex; flex-wrap: wrap; gap: 30px; justify-content: space-between; margin: 40px 0;">
        <div style="flex:1; min-width: 200px;">
            <i class="fas fa-hospital-user" style="font-size: 2rem; color:#00EAFF;"></i>
            <h3 style="margin: 10px 0 8px;">From your home → Hospital</h3>
            <p style="color:#B0B8E0;">Concierge-level extraction and direct admission. No waiting lists, no bureaucracy.</p>
        </div>
        <div style="flex:1; min-width: 200px;">
            <i class="fas fa-waveform" style="font-size: 2rem; color:#00EAFF;"></i>
            <h3 style="margin: 10px 0 8px;">Neural Synchronization</h3>
            <p style="color:#B0B8E0;">Full body-control integration. Your thoughts become action with zero latency.</p>
        </div>
        <div style="flex:1; min-width: 200px;">
            <i class="fas fa-shield-alt" style="font-size: 2rem; color:#00EAFF;"></i>
            <h3 style="margin: 10px 0 8px;">6-Month Elite Care</h3>
            <p style="color:#B0B8E0;">Monthly recalibration, physio-neural training, and performance analytics dashboard.</p>
        </div>
    </div>

    <!-- pricing and final CTA + footnote about species: control your body statement -->
    <div style="margin: 40px 0 20px; background: rgba(0, 234, 255, 0.03); border-radius: 40px; padding: 28px; text-align: center;">
        <p style="font-size: 1.1rem;"><i class="fas fa-robot"></i> “Total somatic command — your body, amplified. No pain, no external charging, no limits.”</p>
        <p style="margin-top: 14px;">✔ 0 awareness ✔ high-tech plug-in ✔ charge by your own bio-electricity ✔ full motor control ✔ 6 month post-op transformation guarantee</p>
        <div style="margin: 24px auto; width: fit-content;">
            <button class="btn-secondary" style="font-weight: bold;"><i class="fas fa-head-side-medical"></i> Schedule Free Neural Assessment</button>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div style="display: flex; flex-wrap: wrap; justify-content: space-between; gap: 20px;">
            <div>
                <div class="logo" style="font-size: 1.3rem;">NEXUS MEDICAL</div>
                <p style="margin-top: 12px;">Santo Domingo Division — Cyber Prosthetics & Neural Integration<br>© 2026 Nexus Medical Group. All rights reserved.</p>
            </div>
            <div>
                <p><i class="fas fa-flask"></i> Advanced Biomechatronics Lab</p>
                <p><i class="fas fa-shield-heart"></i> ISO 13485 / IEC 60601</p>
                <p><i class="fas fa-globe"></i> Global access program</p>
            </div>
            <div>
                <p><i class="fas fa-envelope"></i> care@nexusmedical.sd</p>
                <p><i class="fas fa-phone-alt"></i> +1 (809) 227-9990</p>
                <p><i class="fab fa-discord"></i> Neural Support 24/7</p>
            </div>
        </div>
        <div style="margin-top: 30px; font-size: 0.7rem; text-align: center; border-top: 1px solid rgba(255,255,255,0.05); padding-top: 20px;">
            Disclaimer: Neural integration requires preliminary biometric screening. Results may vary based on individual bio-electric output. All procedures meet international cyber-medical standards.
        </div>
    </footer>
</div>

<!-- subtle floating interactive addition (just for style) -->
<script>
    // optional simple hover parallax for glass cards
    document.querySelectorAll('.tech-card, .pillar, .load-section').forEach(card => {
        card.addEventListener('mousemove', (e) => {
            const rect = card.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            const xMove = (x / rect.width - 0.5) * 3;
            const yMove = (y / rect.height - 0.5) * 3;
            card.style.transform = `perspective(800px) rotateY(${xMove}deg) rotateX(${-yMove}deg) translateZ(2px)`;
        });
        card.addEventListener('mouseleave', () => {
            card.style.transform = '';
        });
    });
</script>
</body>
</html>
