<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tu Perfil GitHub</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #6e5494;
            --secondary-color: #4078c0;
            --accent-color: #58a6ff;
            --background-color: #0d1117;
            --card-background: #161b22;
            --text-color: #c9d1d9;
            --header-color: #ffffff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            margin-bottom: 30px;
            border-bottom: 1px solid #30363d;
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 4px solid var(--primary-color);
            margin: 0 auto 20px;
            background: linear-gradient(45deg, #6e5494, #4078c0);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            color: white;
        }
        
        h1 {
            color: var(--header-color);
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .tagline {
            color: var(--accent-color);
            font-size: 1.2rem;
            margin-bottom: 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-links a {
            color: var(--text-color);
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent-color);
        }
        
        .section {
            background-color: var(--card-background);
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--header-color);
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title i {
            color: var(--accent-color);
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 15px;
        }
        
        .skill-tag {
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .project-card {
            background-color: rgba(22, 27, 34, 0.6);
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 20px;
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-color);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .project-title {
            color: var(--accent-color);
            font-size: 1.2rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .project-desc {
            font-size: 0.95rem;
            margin-bottom: 15px;
            color: #8b949e;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }
        
        .tech-tag {
            background-color: rgba(88, 166, 255, 0.15);
            color: var(--accent-color);
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .stat-card {
            background-color: rgba(22, 27, 34, 0.6);
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--accent-color);
            margin-bottom: 5px;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: #8b949e;
        }
        
        .two-columns {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        
        @media (max-width: 768px) {
            .two-columns {
                grid-template-columns: 1fr;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                grid-template-columns: 1fr 1fr;
            }
        }
        
        .quote {
            font-style: italic;
            text-align: center;
            padding: 20px;
            border-left: 3px solid var(--primary-color);
            background-color: rgba(110, 84, 148, 0.1);
            border-radius: 5px;
            margin: 20px 0;
        }
        
        .highlight {
            color: var(--accent-color);
            font-weight: bold;
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            border-top: 1px solid #30363d;
            color: #8b949e;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <header>
        <div class="profile-img">
            <i class="fas fa-code"></i>
        </div>
        <h1>Luis Oblitas</h1>
        <p class="tagline">Desarrollador Full Stack | React | Node.js | Python</p>
        <p>Apasionado por crear soluciones innovadoras y aprender nuevas tecnologías</p>
        
        <div class="social-links">
            <a href="#" title="GitHub"><i class="fab fa-github"></i></a>
            <a href="#" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="#" title="Twitter"><i class="fab fa-twitter"></i></a>
            <a href="#" title="Portafolio"><i class="fas fa-briefcase"></i></a>
        </div>
    </header>
    
    <div class="two-columns">
        <div class="section">
            <h2 class="section-title"><i class="fas fa-user"></i> Acerca de mí</h2>
            <p>Soy un desarrollador full stack con experiencia en la creación de aplicaciones web y móviles. Me encanta enfrentar nuevos desafíos y aprender tecnologías emergentes.</p>
            <p>Mi objetivo es crear software de alta calidad que brinde valor a los usuarios y solucione problemas reales.</p>
            
            <div class="quote">
                "La tecnología es mejor cuando une a las personas." - Matt Mullenweg
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title"><i class="fas fa-globe"></i> Dónde encontrarme</h2>
            <p><i class="fas fa-map-marker-alt"></i> <span class="highlight">Ubicación:</span> Perú</p>
            <p><i class="fas fa-envelope"></i> <span class="highlight">Email:</span> luis@example.com</p>
            <p><i class="fas fa-link"></i> <span class="highlight">Portafolio:</span> portafolio-oblitas.vercel.app</p>
            <p><i class="fab fa-linkedin"></i> <span class="highlight">LinkedIn:</span> linkedin.com/in/tuperfil</p>
            
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">15+</div>
                    <div class="stat-label">Proyectos</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">3+</div>
                    <div class="stat-label">Años de experiencia</div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title"><i class="fas fa-laptop-code"></i> Tecnologías y Herramientas</h2>
        <div class="skills-container">
            <div class="skill-tag"><i class="fab fa-react"></i> React</div>
            <div class="skill-tag"><i class="fab fa-node-js"></i> Node.js</div>
            <div class="skill-tag"><i class="fab fa-python"></i> Python</div>
            <div class="skill-tag"><i class="fab fa-js"></i> JavaScript</div>
            <div class="skill-tag"><i class="fab fa-html5"></i> HTML5</div>
            <div class="skill-tag"><i class="fab fa-css3-alt"></i> CSS3</div>
            <div class="skill-tag"><i class="fab fa-git-alt"></i> Git</div>
            <div class="skill-tag"><i class="fas fa-database"></i> MongoDB</div>
            <div class="skill-tag"><i class="fas fa-database"></i> MySQL</div>
            <div class="skill-tag"><i class="fab fa-docker"></i> Docker</div>
            <div class="skill-tag"><i class="fab fa-aws"></i> AWS</div>
            <div class="skill-tag"><i class="fas fa-server"></i> Express</div>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title"><i class="fas fa-project-diagram"></i> Proyectos Destacados</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3 class="project-title"><i class="fas fa-shopping-cart"></i> E-commerce App</h3>
                <p class="project-desc">Plataforma de comercio electrónico completa con carrito de compras, pasarela de pago y panel de administración.</p>
                <div class="project-tech">
                    <span class="tech-tag">React</span>
                    <span class="tech-tag">Node.js</span>
                    <span class="tech-tag">MongoDB</span>
                </div>
            </div>
            
            <div class="project-card">
                <h3 class="project-title"><i class="fas fa-tasks"></i> Task Management System</h3>
                <p class="project-desc">Sistema de gestión de tareas con funciones de colaboración en tiempo real y seguimiento de progreso.</p>
                <div class="project-tech">
                    <span class="tech-tag">Vue.js</span>
                    <span class="tech-tag">Express</span>
                    <span class="tech-tag">MySQL</span>
                </div>
            </div>
            
            <div class="project-card">
                <h3 class="project-title"><i class="fas fa-chart-line"></i> Data Analytics Dashboard</h3>
                <p class="project-desc">Panel de control interactivo para visualización y análisis de datos con gráficos personalizables.</p>
                <div class="project-tech">
                    <span class="tech-tag">React</span>
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">D3.js</span>
                </div>
            </div>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Educación y Certificaciones</h2>
        <p><span class="highlight">Ingeniería de Sistemas</span> - Universidad Nacional de Ingeniería (2015-2020)</p>
        <p><span class="highlight">AWS Certified Developer Associate</span> - Amazon Web Services (2021)</p>
        <p><span class="highlight">Scrum Master Certification</span> - Scrum.org (2022)</p>
    </div>
    
    <div class="footer">
        <p>¡No dudes en contactarme para colaborar en proyectos interesantes!</p>
        <p>Última actualización: Agosto 2023</p>
    </div>

    <script>
        // Efecto de escritura para el tagline
        document.addEventListener('DOMContentLoaded', function() {
            const tagline = document.querySelector('.tagline');
            const originalText = tagline.textContent;
            tagline.textContent = '';
            let i = 0;
            
            function typeWriter() {
                if (i < originalText.length) {
                    tagline.textContent += originalText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 100);
                }
            }
            
            setTimeout(typeWriter, 1000);
        });
    </script>
</body>
</html>
