# assistante-administrative[assistant.html](https://github.com/user-attachments/files/22265241/assistant.html)
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Géraldine Ragon - Assistante Administrative & Comptable</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Animations */
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

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            opacity: 0.3;
        }

        .hero-content {
            max-width: 800px;
            padding: 0 2rem;
            animation: fadeInUp 1s ease;
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.3);
            backdrop-filter: blur(10px);
        }

        .cta-button:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .floating-icons {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .floating-icon {
            position: absolute;
            font-size: 2rem;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        .floating-icon:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .floating-icon:nth-child(2) { top: 70%; left: 80%; animation-delay: 2s; }
        .floating-icon:nth-child(3) { top: 30%; left: 75%; animation-delay: 4s; }
        .floating-icon:nth-child(4) { top: 80%; left: 20%; animation-delay: 1s; }

        /* Sections */
        section {
            padding: 80px 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #333;
        }

        /* About */
        .about {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text {
            animation: fadeInUp 1s ease;
        }

        .about-text h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #333;
        }

        .about-text p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            color: #666;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        .about-image {
            text-align: center;
        }

        .profile-placeholder {
            width: 300px;
            height: 300px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: white;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.2);
        }

        /* Contact */
        .contact {
            background: #1a1a2e;
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            color: #667eea;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .contact-item i {
            font-size: 1.5rem;
            margin-right: 1rem;
            color: #667eea;
            width: 30px;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #667eea;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1rem;
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        .submit-btn {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        /* Footer */
        footer {
            background: #0f0f23;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .profile-placeholder {
                width: 200px;
                height: 200px;
                font-size: 3rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">Géraldine Ragon</div>
            <ul class="nav-links">
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#a-propos">À propos</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="accueil" class="hero">
        <div class="floating-icons">
            <div class="floating-icon">📊</div>
            <div class="floating-icon">📋</div>
            <div class="floating-icon">💼</div>
            <div class="floating-icon">📈</div>
        </div>
        <div class="hero-content">
            <h1>Assistante Administrative & Comptable</h1>
            <p>Simplifiez votre gestion administrative et comptable avec une expertise professionnelle et personnalisée</p>
            <a href="#contact" class="cta-button">Demander un devis gratuit</a>
        </div>
    </section>

    <!-- Services -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Mes Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📊</div>
                    <h3>Comptabilité</h3>
                    <p>Tenue de livres, saisie comptable, rapprochements bancaires, déclarations TVA et fiscales. Une gestion comptable rigoureuse pour votre tranquillité d'esprit.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📋</div>
                    <h3>Administration</h3>
                    <p>Gestion du courrier, classement, rédaction de documents, suivi des échéances, organisation administrative complète de votre activité.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">💰</div>
                    <h3>Paie & Social</h3>
                    <p>Établissement des bulletins de paie, déclarations sociales, gestion des congés et absences, suivi des obligations sociales.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📈</div>
                    <h3>Tableau de Bord</h3>
                    <p>Création de tableaux de bord personnalisés, suivi des KPIs, analyse financière pour piloter votre activité en toute sérénité.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📞</div>
                    <h3>Secrétariat</h3>
                    <p>Accueil téléphonique, prise de rendez-vous, gestion de planning, correspondance professionnelle et relation client.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🎯</div>
                    <h3>Optimisation & Organisation</h3>
                    <p>Analyse de vos processus administratifs, recommandations d'optimisation, mise en place de procédures efficaces.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="a-propos" class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>À propos de moi</h2>
                    <p>Forte de plus de 10 ans d'expérience dans l'administration et la comptabilité, je vous accompagne dans la gestion quotidienne de votre entreprise.</p>
                    <p>Diplômée en comptabilité et gestion, je maîtrise les outils modernes et les réglementations en vigueur pour vous offrir un service de qualité, adapté à vos besoins spécifiques.</p>
                    <p>Mon objectif : vous libérer du temps pour vous concentrer sur le développement de votre activité.</p>
                    <div class="skills">
                        <span class="skill-tag">Odoo</span>
                        <span class="skill-tag">Excel Avancé</span>
                        <span class="skill-tag">WinBooks</span>
                        <span class="skill-tag">ERP</span>
                        <span class="skill-tag">Pack Office</span>
                        <span class="skill-tag">Législation sociale</span>
                        <span class="skill-tag">Fiscalité</span>
                    </div>
                </div>
                <div class="about-image">
                    <div class="profile-placeholder">👩‍💼</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Contact</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Parlons de votre projet</h3>
                    <div class="contact-item">
                        <i>📞</i>
                        <div>
                            <strong>Téléphone</strong><br>
                            +32 494.41.05.20
                        </div>
                    </div>
                    <div class="contact-item">
                        <i>📧</i>
                        <div>
                            <strong>Email</strong><br>
                            geraldine.ragon@gmx.com
                        </div>
                    </div>
                    <div class="contact-item">
                        <i>📍</i>
                        <div>
                            <strong>Localisation</strong><br>
                            Binche Hainaut<br>
                            Déplacements possibles
                        </div>
                    </div>
                    <div class="contact-item">
                        <i>⏰</i>
                        <div>
                            <strong>Horaires</strong><br>
                            Lun-Ven : 9h00-18h00<br>
                            Réponse sous 24h
                        </div>
                    </div>
                </div>
                <form class="contact-form" onsubmit="handleSubmit(event)">
                    <div class="form-group">
                        <label for="name">Nom complet</label>
                        <input type="text" id="name" name="name" placeholder="Votre nom" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" placeholder="votre@email.com" required>
                    </div>
                    <div class="form-group">
                        <label for="company">Entreprise</label>
                        <input type="text" id="company" name="company" placeholder="Nom de votre entreprise">
                    </div>
                    <div class="form-group">
                        <label for="service">Service souhaité</label>
                        <select id="service" name="service" style="width: 100%; padding: 1rem; border: none; border-radius: 10px; background: rgba(255, 255, 255, 0.1); color: white; font-size: 1rem;">
                            <option value="" style="background: #333; color: white;">Sélectionnez un service</option>
                            <option value="comptabilite" style="background: #333; color: white;">Comptabilité</option>
                            <option value="administration" style="background: #333; color: white;">Administration</option>
                            <option value="paie" style="background: #333; color: white;">Paie & Social</option>
                            <option value="tableau-bord" style="background: #333; color: white;">Tableau de Bord</option>
                            <option value="secretariat" style="background: #333; color: white;">Secrétariat</option>
                            <option value="odoo" style="background: #333; color: white;">Implémentation Odoo</option>
                            <option value="odoo" style="background: #333; color: white;">Optimisation & Organisation</option>
                           
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" rows="4" placeholder="Décrivez vos besoins..." required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Envoyer ma demande</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 Géraldine Ragon - Assistante Administrative & Comptable. Tous droits réservés.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Header background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
            }
        });

        // Form submission
        function handleSubmit(event) {
            event.preventDefault();
            const form = event.target;
            const formData = new FormData(form);
            
            // Simulate form submission
            const submitBtn = form.querySelector('.submit-btn');
            const originalText = submitBtn.textContent;
            
            submitBtn.textContent = 'Envoi en cours...';
            submitBtn.disabled = true;
            
            setTimeout(() => {
                alert('Merci pour votre message ! Je vous répondrai dans les plus brefs délais.');
                form.reset();
                submitBtn.textContent = originalText;
                submitBtn.disabled = false;
            }, 1500);
        }

        // Animate elements on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 1s ease forwards';
                }
            });
        }, observerOptions);

        // Observe service cards
        document.querySelectorAll('.service-card').forEach(card => {
            observer.observe(card);
        });

        // Add some interactive hover effects
        document.querySelectorAll('.service-card').forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.transform = 'translateY(-10px) scale(1.02)';
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'translateY(0) scale(1)';
            });
        });
    </script>
</body>
</html>
