<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FuturFit | Entrenamiento Personalizado de Vanguardia</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --space-black: #0A0A12;
            --cyber-white: #F0F0F0;
            --neon-blue: #00F0FF;
            --neon-purple: #B026FF;
            --tech-gray: #1E1E2E;
            --hologram-effect: linear-gradient(45deg, rgba(0, 240, 255, 0.1), rgba(176, 38, 255, 0.1));
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Rajdhani', sans-serif;
            background-color: var(--space-black);
            color: var(--cyber-white);
            line-height: 1.7;
            overflow-x: hidden;
        }

        /* Futuristic Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: var(--tech-gray);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--neon-blue);
            border-radius: 4px;
        }

        /* Header */
        header {
            background-color: rgba(10, 10, 18, 0.9);
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--neon-blue);
        }

        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-decoration: none;
            letter-spacing: 2px;
            position: relative;
        }

        .logo::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .logo:hover::after {
            transform: scaleX(1);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
            position: relative;
        }

        nav ul li a {
            color: var(--cyber-white);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
        }

        nav ul li a:hover {
            color: var(--neon-blue);
        }

        nav ul li a::before {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            transition: width 0.3s ease;
        }

        nav ul li a:hover::before {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
            padding: 0 10%;
            position: relative;
            overflow: hidden;
            margin-top: 80px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            opacity: 0.3;
            z-index: -1;
        }

        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--hologram-effect);
            z-index: -1;
        }

        .hero h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            text-shadow: 0 0 15px rgba(0, 240, 255, 0.3);
            letter-spacing: 2px;
        }

        .hero p {
            font-size: 1.5rem;
            max-width: 600px;
            margin-bottom: 2.5rem;
            font-weight: 500;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            color: var(--space-black);
            padding: 15px 35px;
            border: none;
            border-radius: 50px;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.5);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, var(--neon-purple), var(--neon-blue));
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: -1;
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 25px rgba(0, 240, 255, 0.8);
        }

        .btn:hover::before {
            opacity: 1;
        }

        /* Grid Section */
        .grid-section {
            padding: 5rem 10%;
            background-color: var(--tech-gray);
            position: relative;
        }

        .grid-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            opacity: 0.05;
            z-index: 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 2px;
            position: relative;
            z-index: 1;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            position: relative;
            z-index: 1;
        }

        .grid-item {
            background: rgba(30, 30, 46, 0.7);
            padding: 2.5rem;
            border-radius: 10px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(0, 240, 255, 0.2);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .grid-item::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-purple));
            z-index: -1;
            border-radius: 12px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .grid-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0, 240, 255, 0.1);
            border-color: transparent;
        }

        .grid-item:hover::before {
            opacity: 1;
        }

        .grid-item i {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .grid-item h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--neon-blue);
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
        }

        .grid-item p {
            margin-bottom: 1.5rem;
            color: var(--cyber-white);
            opacity: 0.9;
        }

        .grid-item ul {
            margin-bottom: 1.5rem;
            padding-left: 1.5rem;
        }

        .grid-item ul li {
            margin-bottom: 0.5rem;
        }

        /* About Section */
        .about {
            display: flex;
            align-items: center;
            padding: 5rem 10%;
            background-color: var(--space-black);
            position: relative;
            overflow: hidden;
        }

        .about::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1517836357463-d25dfeac3438?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            opacity: 0.1;
            z-index: 0;
        }

        .about-img {
            flex: 1;
            padding-right: 3rem;
            position: relative;
            z-index: 1;
        }

        .about-img img {
            width: 100%;
            max-width: 500px;
            border-radius: 10px;
            box-shadow: 0 0 30px rgba(0, 240, 255, 0.2);
            transition: transform 0.5s ease;
        }

        .about-img:hover img {
            transform: scale(1.02);
        }

        .about-content {
            flex: 1;
            position: relative;
            z-index: 1;
        }

        .about-content h2 {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 1.5rem;
            letter-spacing: 1px;
        }

        .about-content p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Projects Section */
        .projects {
            padding: 5rem 10%;
            background-color: var(--tech-gray);
            position: relative;
        }

        .projects::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1571902943202-507ec2618e8f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1075&q=80') no-repeat center center/cover;
            opacity: 0.05;
            z-index: 0;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            position: relative;
            z-index: 1;
        }

        .project-card {
            background: rgba(30, 30, 46, 0.7);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: all 0.4s ease;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(0, 240, 255, 0.1);
            position: relative;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-purple));
            z-index: -1;
            border-radius: 12px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 240, 255, 0.2);
            border-color: transparent;
        }

        .project-card:hover::before {
            opacity: 0.5;
        }

        .project-img {
            height: 250px;
            overflow: hidden;
            position: relative;
        }

        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-img img {
            transform: scale(1.1);
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--neon-blue);
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
        }

        .project-info p {
            margin-bottom: 1rem;
            color: var(--cyber-white);
            opacity: 0.9;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            color: var(--neon-blue);
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s ease;
        }

        .project-link i {
            margin-left: 5px;
            transition: transform 0.3s ease;
        }

        .project-link:hover {
            color: var(--neon-purple);
        }

        .project-link:hover i {
            transform: translateX(5px);
        }

        .projects-cta {
            text-align: center;
            margin-top: 3rem;
            position: relative;
            z-index: 1;
        }

        /* Footer */
        footer {
            background-color: var(--space-black);
            padding: 4rem 10% 2rem;
            position: relative;
            border-top: 1px solid rgba(0, 240, 255, 0.2);
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .footer-logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 2rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 1.5rem;
            display: inline-block;
            letter-spacing: 2px;
        }

        .footer-text {
            max-width: 600px;
            margin: 0 auto 2rem;
            text-align: center;
            font-size: 1.1rem;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 2rem;
        }

        .footer-links a {
            color: var(--cyber-white);
            text-decoration: none;
            margin: 0 1rem;
            font-weight: 500;
            transition: color 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.9rem;
        }

        .footer-links a:hover {
            color: var(--neon-blue);
        }

        .social-icons {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            margin: 0 0.5rem;
            background: rgba(0, 240, 255, 0.1);
            color: var(--neon-blue);
            font-size: 1.2rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 240, 255, 0.3);
        }

        .social-icons a:hover {
            background: var(--neon-blue);
            color: var(--space-black);
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 240, 255, 0.4);
        }

        .footer-bottom {
            margin-top: 2rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            font-size: 0.9rem;
            color: rgba(240, 240, 240, 0.7);
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .about {
                flex-direction: column;
            }
            
            .about-img {
                padding-right: 0;
                margin-bottom: 3rem;
            }
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 1rem 5%;
            }
            
            .logo {
                margin-bottom: 1rem;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero {
                align-items: center;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }
            
            .grid-container {
                grid-template-columns: 1fr;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-links a {
                margin: 0.5rem;
            }
        }

        /* Futuristic Animations */
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(0, 240, 255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(0, 240, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 240, 255, 0); }
        }

        .pulse-effect {
            animation: pulse 2s infinite;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <a href="#" class="logo">FUTURFIT</a>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#quien-soy">Quién Soy</a></li>
                <li><a href="#experiencia">Experiencia</a></li>
                <li><a href="#proyectos">Proyectos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <h1>ENTRENAMIENTO PERSONALIZADO Y MEJORA DEPORTIVA</h1>
        <p>Potencia tu rendimiento con tecnología de vanguardia y métodos científicos avanzados</p>
        <a href="#contacto" class="btn pulse-effect">CONTÁCTAME</a>
    </section>

    <!-- Grid Section -->
    <section class="grid-section" id="quien-soy">
        <h2 class="section-title">MI PERFIL</h2>
        <div class="grid-container">
            <!-- Quién Soy -->
            <div class="grid-item">
                <i class="fas fa-user-astronaut"></i>
                <h3>Quién Soy</h3>
                <p>Entrenador especializado en tecnología deportiva con más de 10 años transformando el rendimiento de atletas de élite.</p>
                <a href="#" class="btn">Leer más</a>
            </div>
            
            <!-- Experiencia & Certificados -->
            <div class="grid-item">
                <i class="fas fa-medal"></i>
                <h3>Experiencia & Certificados</h3>
                <ul>
                    <li>Certificado en Biomecánica Avanzada</li>
                    <li>Especialista en Wearable Tech</li>
                    <li>Entrenador de Atletas Olímpicos</li>
                </ul>
                <a href="#" class="btn">Ver logros</a>
            </div>
            
            <!-- Lenguajes -->
            <div class="grid-item">
                <i class="fas fa-globe-americas"></i>
                <h3>Lenguajes</h3>
                <ul>
                    <li>Español (Nativo)</li>
                    <li>Inglés (C2)</li>
                    <li>Alemán (B2)</li>
                </ul>
                <a href="#" class="btn">Saber más</a>
            </div>
            
            <!-- Redes Sociales -->
            <div class="grid-item">
                <i class="fas fa-satellite-dish"></i>
                <h3>Redes Sociales</h3>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
                <p>contacto@futurfit.tech</p>
                <a href="#contacto" class="btn">Contactar</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="experiencia">
        <div class="about-img">
            <img src="https://images.unsplash.com/photo-1601422407692-ec4eeec1d9b3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=725&q=80" alt="Entrenador Futurista">
        </div>
        <div class="about-content">
            <h2>MI EXPERIENCIA FUTURISTA</h2>
            <p>Pionero en la integración de tecnología avanzada en el entrenamiento deportivo. Utilizo wearables, análisis de datos en tiempo real y realidad aumentada para optimizar cada aspecto del rendimiento atlético.</p>
            <p>Mi metodología combina inteligencia artificial, biomecánica y neurociencia para crear programas personalizados que maximizan resultados en tiempo récord.</p>
            <p>He trabajado con equipos profesionales y atletas olímpicos, desarrollando sistemas de entrenamiento que marcan la diferencia en competiciones de alto nivel.</p>
            <a href="#" class="btn">Ver tecnología</a>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="proyectos">
        <h2 class="section-title">PROYECTOS RECIENTES</h2>
        <div class="projects-grid">
            <!-- Proyecto 1 -->
            <div class="project-card">
                <div class="project-img">
                    <img src="https://images.unsplash.com/photo-1538805060514-97d9cc17730c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" alt="Proyecto 1">
                </div>
                <div class="project-info">
                    <h3>Sistema de Fuerza 4.0</h3>
                    <p>Programa de fuerza con sensores IoT para optimizar cada repetición y prevenir lesiones.</p>
                    <a href="#" class="project-link">Ver detalles <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            
            <!-- Proyecto 2 -->
            <div class="project-card">
                <div class="project-img">
                    <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Proyecto 2">
                </div>
                <div class="project-info">
                    <h3>AR Training Suite</h3>
                    <p>Entrenamiento con realidad aumentada para mejorar técnica y rendimiento en tiempo real.</p>
                    <a href="#" class="project-link">Ver detalles <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            
            <!-- Proyecto 3 -->
            <div class="project-card">
                <div class="project-img">
                    <img src="https://images.unsplash.com/photo-1545205597-3d9d02c29597?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Proyecto 3">
                </div>
                <div class="project-info">
                    <h3>Neuro Performance</h3>
                    <p>Programa que combina entrenamiento físico con estimulación cognitiva para máximo rendimiento.</p>
                    <a href="#" class="project-link">Ver detalles <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </div>
        <div class="projects-cta">
            <a href="#" class="btn pulse-effect">VER MÁS PROYECTOS</a>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contacto">
        <div class="footer-content">
            <a href="#" class="footer-logo">FUTURFIT</a>
            <p class="footer-text">Especializado en entrenamiento personalizado con tecnología de vanguardia y 10+ años de experiencia en alto rendimiento.</p>
            
            <div class="footer-links">
                <a href="#inicio">Inicio</a>
                <a href="#quien-soy">Quién Soy</a>
                <a href="#experiencia">Experiencia</a>
                <a href="#proyectos">Proyectos</a>
                <a href="#contacto">Contacto</a>
            </div>
            
            <div class="social-icons">
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
                <a href="#"><i class="fab fa-tiktok"></i></a>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 FuturFit. Todos los derechos reservados. | Diseño futurista para el alto rendimiento</p>
            </div>
        </div>
    </footer>
</body>
</html>
