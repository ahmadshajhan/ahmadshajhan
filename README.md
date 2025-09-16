<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mr Code | AI Developer & Full Stack Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Roboto+Mono:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #ff4d7c;
            --secondary: #4d5eff;
            --accent: #4dffea;
            --dark: #1a1a2e;
            --darker: #16213e;
            --light: #f0f0f0;
            --lighter: #ffffff;
            --gradient-start: #ff4d7c;
            --gradient-end: #4d5eff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            background-attachment: fixed;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background: rgba(26, 26, 46, 0.8);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            z-index: 1000;
            padding: 15px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 28px;
            font-weight: 800;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-right: 10px;
            font-size: 32px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            max-width: 650px;
            z-index: 1;
        }

        .hero h1 {
            font-size: 60px;
            font-weight: 800;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero h1 span {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            color: rgba(255, 255, 255, 0.8);
        }

        .btn {
            display: inline-block;
            padding: 15px 30px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 18px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 5px 15px rgba(255, 77, 124, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 77, 124, 0.4);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            margin-left: 15px;
        }

        .btn-secondary:hover {
            background: rgba(255, 77, 124, 0.1);
        }

        .hero-image {
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 50%;
            max-width: 600px;
            z-index: 0;
            opacity: 0.8;
        }

        /* Animated Background Elements */
        .circle {
            position: absolute;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            opacity: 0.1;
            animation: float 8s infinite ease-in-out;
        }

        .circle:nth-child(1) {
            width: 300px;
            height: 300px;
            top: 10%;
            left: 5%;
            animation-delay: 0s;
        }

        .circle:nth-child(2) {
            width: 200px;
            height: 200px;
            top: 60%;
            left: 10%;
            animation-delay: 1s;
        }

        .circle:nth-child(3) {
            width: 250px;
            height: 250px;
            top: 30%;
            right: 10%;
            animation-delay: 2s;
        }

        .circle:nth-child(4) {
            width: 150px;
            height: 150px;
            bottom: 10%;
            right: 20%;
            animation-delay: 3s;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0) scale(1);
            }
            50% {
                transform: translateY(-20px) scale(1.05);
            }
        }

        /* Sections */
        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 40px;
            font-weight: 700;
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 70px;
            height: 4px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
            padding-right: 40px;
        }

        .about-text h3 {
            font-size: 30px;
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 15px;
            font-size: 18px;
            color: rgba(255, 255, 255, 0.8);
        }

        .skills {
            flex: 1;
            min-width: 300px;
        }

        .skill {
            margin-bottom: 25px;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .skill-bar {
            height: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            overflow: hidden;
        }

        .skill-level {
            height: 100%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            border-radius: 5px;
            position: relative;
            width: 0;
            transition: width 1.5s ease-in-out;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .project-img {
            width: 100%;
            height: 200px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 40px;
        }

        .project-content {
            padding: 20px;
        }

        .project-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }

        .project-content p {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 15px;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .project-link i {
            margin-left: 5px;
            transition: transform 0.3s;
        }

        .project-link:hover {
            color: var(--secondary);
        }

        .project-link:hover i {
            transform: translateX(5px);
        }

        /* Contact Section */
        .contact-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .contact-info {
            flex: 1;
            min-width: 300px;
        }

        .contact-info h3 {
            font-size: 26px;
            margin-bottom: 20px;
        }

        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .contact-info i {
            margin-right: 15px;
            color: var(--primary);
            font-size: 20px;
            width: 24px;
        }

        .social-links {
            display: flex;
            margin-top: 30px;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            font-size: 20px;
            margin-right: 15px;
            text-decoration: none;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .social-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(255, 77, 124, 0.3);
        }

        .contact-form {
            flex: 1;
            min-width: 300px;
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            color: white;
            font-family: 'Poppins', sans-serif;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: var(--darker);
            padding: 40px 0;
            text-align: center;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .footer-logo {
            font-size: 24px;
            font-weight: 800;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .footer-links {
            display: flex;
            list-style: none;
        }

        .footer-links li {
            margin-left: 20px;
        }

        .footer-links a {
            color: var(--light);
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .copyright {
            margin-top: 30px;
            color: rgba(255, 255, 255, 0.6);
        }

        /* Animations */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate {
            opacity: 0;
            animation: fadeIn 1s forwards;
        }

        .delay-1 {
            animation-delay: 0.2s;
        }

        .delay-2 {
            animation-delay: 0.4s;
        }

        .delay-3 {
            animation-delay: 0.6s;
        }

        .delay-4 {
            animation-delay: 0.8s;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 48px;
            }
            
            .hero-image {
                width: 45%;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero {
                text-align: center;
            }
            
            .hero-content {
                margin: 0 auto;
            }
            
            .hero-image {
                display: none;
            }
            
            .about-text {
                padding-right: 0;
                margin-bottom: 40px;
            }
            
            .contact-info {
                margin-bottom: 40px;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .btn {
                padding: 12px 25px;
                font-size: 16px;
            }
            
            .section-title h2 {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
    <!-- Animated Background Elements -->
    <div class="circle"></div>
    <div class="circle"></div>
    <div class="circle"></div>
    <div class="circle"></div>

    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fas fa-code"></i>
                    Mr Code
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1 class="animate">Hi, I'm <span>Ahmad Shajahan</span></h1>
                <p class="animate delay-1">AI Developer & Full Stack Engineer with expertise in Java, Python, and modern web technologies. I create innovative solutions that blend cutting-edge technology with stunning design.</p>
                <div class="animate delay-2">
                    <a href="#contact" class="btn">Get In Touch</a>
                    <a href="#projects" class="btn btn-secondary">View My Work</a>
                </div>
            </div>
        </div>
        <div class="hero-image">
            <!-- This would be an image or SVG in a real implementation -->
            <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <path fill="#FF4D7C" d="M44.7,-76.3C58.1,-70.2,69.1,-58.1,77.2,-43.5C85.3,-28.9,90.5,-11.9,89.8,4.6C89.1,21.1,82.5,37.1,71.8,49.2C61.1,61.3,46.4,69.5,30.7,74.8C15,80.1,-1.8,82.5,-17.3,79.2C-32.8,75.9,-47.1,66.9,-58.2,54.7C-69.3,42.5,-77.2,27.1,-80.1,10.7C-83,-5.7,-81,-22.9,-74.1,-37.3C-67.2,-51.6,-55.5,-63.1,-42.1,-69.2C-28.7,-75.3,-14.3,-75.9,0.5,-76.6C15.3,-77.4,30.6,-78.3,44.7,-76.3Z" transform="translate(100 100)" />
            </svg>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2 class="animate">About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text animate delay-1">
                    <h3>Innovative Developer with a Passion for Technology</h3>
                    <p>I'm a versatile developer specializing in AI, web development, and software engineering. With expertise in multiple programming languages and frameworks, I create solutions that are both technically robust and visually stunning.</p>
                    <p>My journey in technology started at a young age, and I've since developed a diverse skill set that allows me to tackle projects from concept to deployment.</p>
                    <p>When I'm not coding, I enjoy exploring new technologies, contributing to open source projects, and sharing knowledge with the developer community.</p>
                </div>
                <div class="skills animate delay-2">
                    <div class="skill">
                        <div class="skill-name">
                            <span>Java Development</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 95%"></div>
                        </div>
                    </div>
                    <div class="skill">
                        <div class="skill-name">
                            <span>Python & AI</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill">
                        <div class="skill-name">
                            <span>Web Development</span>
                            <span>92%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 92%"></div>
                        </div>
                    </div>
                    <div class="skill">
                        <div class="skill-name">
                            <span>UI/UX Design</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 85%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <div class="section-title">
                <h2 class="animate">My Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card animate delay-1">
                    <div class="project-img">
                        <i class="fas fa-robot"></i>
                    </div>
                    <div class="project-content">
                        <h3>AI Assistant</h3>
                        <p>An intelligent virtual assistant built with Python and machine learning algorithms.</p>
                        <a href="https://mrcode-ai.netlify.app/" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="project-card animate delay-2">
                    <div class="project-img">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <div class="project-content">
                        <h3>Developer Portfolio</h3>
                        <p>A modern, responsive portfolio website showcasing my projects and skills.</p>
                        <a href="https://mrcode11.netlify.app/" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="project-card animate delay-3">
                    <div class="project-img">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="project-content">
                        <h3>E-commerce Platform</h3>
                        <p>A full-stack e-commerce solution with Java Spring Boot and React.</p>
                        <a href="https://www.nexsou.com/" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="project-card animate delay-4">
                    <div class="project-img">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <div class="project-content">
                        <h3>PyGame Applications</h3>
                        <p>Interactive games and simulations built with Python PyGame library.</p>
                        <a href="https://mrcode11.netlify.app/python" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2 class="animate">Get In Touch</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info animate delay-1">
                    <h3>Let's Talk About Your Project</h3>
                    <p><i class="fas fa-envelope"></i> ahmadshajahan2000@gmail.com</p>
                    <p><i class="fas fa-phone"></i> +91 8089021973</p>
                    <p><i class="fas fa-map-marker-alt"></i> India</p>
                    
                    <div class="social-links">
                        <a href="https://github.com/ahmadshajhan" class="social-link"><i class="fab fa-github"></i></a>
                        <a href="https://www.linkedin.com/in/mr-code-9567b333b" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                        <a href="https://x.com/MrCode59636" class="social-link"><i class="fab fa-twitter"></i></a>
                        <a href="https://www.instagram.com/mr_code_ahmad" class="social-link"><i class="fab fa-instagram"></i></a>
                        <a href="https://www.facebook.com/share/15wggD8y3b/" class="social-link"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
                <div class="contact-form animate delay-2">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Your Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">Mr Code</div>
                <ul class="footer-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Mr Code. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Animation on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.animate');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animationPlayState = 'running';
                        observer.unobserve(entry.target);
                    }
                });
            }, {
                threshold: 0.1
            });
            
            animatedElements.forEach(element => {
                observer.observe(element);
            });
            
            // Skill bars animation
            const skillBars = document.querySelectorAll('.skill-level');
            const skillsSection = document.querySelector('.skills');
            
            const skillsObserver = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        skillBars.forEach(bar => {
                            const width = bar.style.width;
                            bar.style.width = '0';
                            setTimeout(() => {
                                bar.style.width = width;
                            }, 200);
                        });
                        skillsObserver.unobserve(entry.target);
                    }
                });
            }, {
                threshold: 0.5
            });
            
            skillsObserver.observe(skillsSection);
            
            // Form submission
            const contactForm = document.getElementById('contactForm');
            if (contactForm) {
                contactForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    alert('Thank you for your message! I will get back to you soon.');
                    contactForm.reset();
                });
            }
        });
    </script>
</body>
</html>
