
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SmileCare Dental Clinic | Expert Dental Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* CSS Variables for Easy Theme Change */
        :root {
            --primary: #0ea5e9; /* Medical Blue */
            --secondary: #0284c7;
            --dark: #0f172a;
            --light: #f8fafc;
            --text: #334155;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; scroll-behavior: smooth; }
        body { background-color: #ffffff; color: var(--text); overflow-x: hidden; }

        /* --- NAVIGATION --- */
        header { background: white; box-shadow: 0 2px 10px rgba(0,0,0,0.05); position: fixed; width: 100%; top: 0; z-index: 1000; display: flex; justify-content: space-between; align-items: center; padding: 15px 5%; }
        .logo { font-size: 1.8rem; font-weight: 800; color: var(--primary); display: flex; align-items: center; gap: 8px; }
        .nav-links { display: flex; gap: 20px; }
        .nav-links a { text-decoration: none; color: var(--dark); font-weight: 500; transition: 0.3s; }
        .nav-links a:hover { color: var(--primary); }
        .btn { padding: 10px 25px; background: var(--primary); color: white !important; border-radius: 50px; text-decoration: none; font-weight: bold; transition: 0.3s; display: inline-block; border: none; cursor: pointer; }
        .btn:hover { background: var(--secondary); transform: translateY(-2px); box-shadow: 0 5px 15px rgba(14, 165, 233, 0.3); }
        .menu-btn { display: none; font-size: 1.5rem; color: var(--dark); cursor: pointer; }

        /* --- HERO SECTION --- */
        .hero { margin-top: 70px; height: 85vh; background: linear-gradient(rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.9)), url('https://images.unsplash.com/photo-1606811841689-23dfddce3e95?auto=format&fit=crop&w=1920&q=80') center/cover; display: flex; flex-direction: column; justify-content: center; padding: 0 5%; }
        .hero h1 { font-size: 3.5rem; color: var(--dark); margin-bottom: 15px; line-height: 1.2; }
        .hero h1 span { color: var(--primary); }
        .hero p { font-size: 1.2rem; margin-bottom: 30px; max-width: 600px; color: #475569; }
        .hero-buttons { display: flex; gap: 15px; }
        .btn-outline { background: transparent; border: 2px solid var(--primary); color: var(--primary) !important; }

        /* --- SERVICES SECTION --- */
        .section-title { text-align: center; margin-bottom: 40px; font-size: 2.2rem; color: var(--dark); }
        .services { padding: 80px 5%; background: var(--light); }
        .service-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
        .service-card { background: white; padding: 30px; border-radius: 15px; text-align: center; box-shadow: 0 5px 20px rgba(0,0,0,0.03); transition: 0.3s; }
        .service-card:hover { transform: translateY(-10px); box-shadow: 0 10px 30px rgba(0,0,0,0.08); }
        .service-icon { font-size: 3rem; color: var(--primary); margin-bottom: 20px; }
        .service-card h3 { color: var(--dark); margin-bottom: 10px; font-size: 1.3rem; }

        /* --- ABOUT CLINIC --- */
        .about { padding: 80px 5%; display: flex; align-items: center; gap: 50px; flex-wrap: wrap; }
        .about-img { flex: 1; min-width: 300px; border-radius: 20px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.1); }
        .about-img img { width: 100%; height: auto; display: block; }
        .about-text { flex: 1; min-width: 300px; }
        .about-text h2 { font-size: 2.2rem; color: var(--dark); margin-bottom: 20px; }
        .about-text p { margin-bottom: 15px; line-height: 1.6; }
        .check-list { list-style: none; margin-top: 20px; margin-bottom: 30px; }
        .check-list li { margin-bottom: 10px; display: flex; align-items: center; gap: 10px; font-weight: 500; }
        .check-list i { color: #10b981; }

        /* --- FOOTER & CONTACT --- */
        .contact-cta { background: var(--primary); padding: 60px 5%; text-align: center; color: white; }
        .contact-cta h2 { font-size: 2.5rem; margin-bottom: 20px; }
        footer { background: var(--dark); color: white; padding: 50px 5% 20px; display: flex; flex-wrap: wrap; gap: 40px; justify-content: space-between; }
        .footer-col h3 { font-size: 1.2rem; margin-bottom: 20px; color: var(--primary); }
        .footer-col p { margin-bottom: 10px; display: flex; align-items: center; gap: 10px; color: #cbd5e1; }
        .bottom-bar { text-align: center; padding-top: 20px; margin-top: 40px; border-top: 1px solid rgba(255,255,255,0.1); color: #94a3b8; font-size: 0.9rem; width: 100%; }

        /* --- MOBILE RESPONSIVE --- */
        @media (max-width: 768px) {
            .nav-links { display: none; flex-direction: column; position: absolute; top: 70px; left: 0; width: 100%; background: white; padding: 20px; text-align: center; box-shadow: 0 10px 10px rgba(0,0,0,0.05); }
            .nav-links.active { display: flex; }
            .menu-btn { display: block; }
            .hero h1 { font-size: 2.5rem; }
            .hero-buttons { flex-direction: column; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo"><i class="fa-solid fa-tooth"></i> SmileCare</div>
        <i class="fa-solid fa-bars menu-btn" onclick="toggleMenu()"></i>
        <nav class="nav-links" id="navLinks">
            <a href="#home">Home</a>
            <a href="#services">Services</a>
            <a href="#about">About Dr.</a>
            <a href="#contact" class="btn">Book Appointment</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <h1>Your Smile, <br><span>Our Priority.</span></h1>
        <p>Experience world-class dental care with painless treatments, advanced technology, and a team that genuinely cares about your oral health.</p>
        <div class="hero-buttons">
            <a href="#contact" class="btn">Book a Free Consultation</a>
            <a href="tel:+919876543210" class="btn btn-outline"><i class="fa-solid fa-phone"></i> +91 98765 43210</a>
        </div>
    </section>

    <section class="services" id="services">
        <h2 class="section-title">Our Dental Services</h2>
        <div class="service-grid">
            <div class="service-card">
                <i class="fa-solid fa-teeth-open service-icon"></i>
                <h3>Teeth Whitening</h3>
                <p>Get a brighter, more confident smile in just one session with our advanced laser whitening.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-syringe service-icon"></i>
                <h3>Root Canal Treatment</h3>
                <p>Painless and fast root canal procedures to save your natural teeth and relieve severe pain.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-face-smile service-icon"></i>
                <h3>Dental Implants</h3>
                <p>Permanent and natural-looking tooth replacements that restore your full chewing ability.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-child service-icon"></i>
                <h3>Pediatric Dentistry</h3>
                <p>Gentle and friendly dental care specialized for children to ensure healthy growing teeth.</p>
            </div>
        </div>
    </section>

    <section class="about" id="about">
        <div class="about-img">
            <img src="https://images.unsplash.com/photo-1598256989800-ef61ed5ba4aa?auto=format&fit=crop&w=800&q=80" alt="Dr. working">
        </div>
        <div class="about-text">
            <h2>Meet Your Expert Dentist</h2>
            <p>At SmileCare Clinic, we believe that a healthy smile is the foundation of a healthy life. Led by highly experienced specialists, our clinic uses the latest state-of-the-art equipment to ensure precise diagnostics and painless treatments.</p>
            <ul class="check-list">
                <li><i class="fa-solid fa-circle-check"></i> 10+ Years of Medical Experience</li>
                <li><i class="fa-solid fa-circle-check"></i> Painless & Modern Technologies</li>
                <li><i class="fa-solid fa-circle-check"></i> 100% Sterilized Environment</li>
                <li><i class="fa-solid fa-circle-check"></i> Affordable & Transparent Pricing</li>
            </ul>
            <a href="#contact" class="btn">Contact Us Today</a>
        </div>
    </section>

    <section class="contact-cta">
        <h2>Ready for a healthier smile?</h2>
        <p style="margin-bottom: 30px; font-size: 1.2rem;">Don't let dental pain hold you back. Schedule your visit today.</p>
        <a href="https://wa.me/917740834806" class="btn" style="background: white; color: var(--primary) !important; font-size: 1.2rem; padding: 15px 30px;"><i class="fa-brands fa-whatsapp"></i> Chat on WhatsApp</a>
    </section>

    <footer id="contact">
        <div class="footer-col">
            <div class="logo" style="color: white; margin-bottom: 20px;"><i class="fa-solid fa-tooth"></i> SmileCare</div>
            <p>Providing the best dental care with advanced technology and a gentle touch.</p>
        </div>
        <div class="footer-col">
            <h3>Clinic Address</h3>
            <p><i class="fa-solid fa-location-dot"></i> 123, Malviya Nagar Main Road, Jaipur, Rajasthan</p>
            <p><i class="fa-solid fa-clock"></i> Mon - Sat: 9:00 AM - 8:00 PM</p>
            <p><i class="fa-solid fa-clock"></i> Sunday: Closed</p>
        </div>
        <div class="footer-col">
            <h3>Contact Us</h3>
            <p><i class="fa-solid fa-phone"></i> +91 77408 34806</p>
            <p><i class="fa-solid fa-envelope"></i> khushalmourya3@gmail.com</p>
        </div>
        <div class="bottom-bar">
            &copy; 2026 SmileCare Dental Clinic. Developed by Expert Web Solutions.
        </div>
    </footer>

    <script>
        function toggleMenu() {
            document.getElementById('navLinks').classList.toggle('active');
        }
    </script>
</body>
</html>
