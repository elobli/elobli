<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Perfil GitHub Mejorado</title>
    <style>
        :root {
            --primary-color: #6e5494;
            --secondary-color: #4078c0;
            --background-color: #0d1117;
            --card-background: #161b22;
            --text-color: #c9d1d9;
            --accent-color: #58a6ff;
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
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 3fr;
            gap: 20px;
        }
        
        header {
            grid-column: 1 / -1;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            border-bottom: 1px solid #30363d;
            margin-bottom: 30px;
        }
        
        .profile-card {
            background-color: var(--card-background);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 20px;
        }
        
        .profile-img {
            width: 100%;
            border-radius: 50%;
            border: 3px solid var(--primary-color);
            margin-bottom: 20px;
        }
        
        .profile-name {
            font-size: 24px;
            margin-bottom: 5px;
            color: white;
        }
        
        .profile-username {
            color: var(--secondary-color);
            margin-bottom: 15px;
            font-size: 18px;
        }
        
        .profile-bio {
            margin-bottom: 20px;
            font-size: 14px;
        }
        
        .profile-stats {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
            font-size: 14px;
        }
        
        .profile-location, .profile-link {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            font-size: 14px;
        }
        
        .icon {
            margin-right: 8px;
            width: 16px;
            height: 16px;
        }
        
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .section {
            background-color: var(--card-background);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .section-title {
            font-size: 20px;
            margin-bottom: 15px;
            color: white;
            border-bottom: 1px solid #30363d;
            padding-bottom: 10px;
        }
        
        .pinned-repos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .repo-card {
            background-color: rgba(22, 27, 34, 0.6);
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 15px;
            transition: transform 0.2s;
        }
        
        .repo-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-color);
        }
        
        .repo-name {
            color: var(--accent-color);
            font-size: 16px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .repo-desc {
            font-size: 14px;
            margin-bottom: 15px;
            color: #8b949e;
        }
        
        .repo-stats {
            display: flex;
            gap: 15px;
            font-size: 12px;
            color: #8b949e;
        }
        
        .repo-lang {
            display: flex;
            align-items: center;
        }
        
        .lang-color {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 5px;
        }
        
        .javascript { background-color: #f1e05a; }
        .python { background-color: #3572A5; }
        .html { background-color: #e34c26; }
        .css { background-color: #563d7c; }
        
        .activity-grid {
            display: grid;
            grid-template-columns: repeat(53, 1fr);
            grid-template-rows: repeat(7, 1fr);
            gap: 3px;
            margin-top: 15px;
        }
        
        .activity-day {
            width: 12px;
            height: 12px;
            background-color: #ebedf0;
            border-radius: 2px;
        }
        
        .activity-day.low { background-color: #9be9a8; }
        .activity-day.medium { background-color: #40c463; }
        .activity-day.high { background-color: #30a14e; }
        .activity-day.very-high { background-color: #216e39; }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-tag {
            background-color: var(--primary-color);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 14px;
        }
        
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
            
            .profile-card {
                position: static;
                margin-bottom: 20px;
            }
            
            .pinned-repos {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Mi Perfil GitHub</h1>
            <nav>
                <!-- Simulación de navegación -->
            </nav>
        </header>
        
        <div class="profile-card">
            <img src="https://via.placeholder.com/260" alt="Avatar" class="profile-img">
            <h2 class="profile-name">Tu Nombre</h2>
            <p class="profile-username">@tuusername</p>
            <p class="profile-bio">Desarrollador apasionado por la tecnología y el código limpio. Amante del open source.</p>
            
            <div class="profile-stats">
                <div><strong>24</strong> seguidores</div>
                <div><strong>12</strong> siguiendo</div>
                <div><strong>8</strong> repositorios</div>
            </div>
            
            <div class="profile-location">
                <svg class="icon" viewBox="0 0 16 16" fill="currentColor">
                    <path fill-rule="evenodd" d="M11.536 3.464a5 5 0 010 7.072L8 14.07l-3.536-3.535a5 5 0 117.072-7.072v.001zM8 8a2 2 0 100-4 2 2 0 000 4z"/>
                </svg>
                Ciudad, País
            </div>
            
            <div class="profile-link">
                <svg class="icon" viewBox="0 0 16 16" fill="currentColor">
                    <path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
                </svg>
                github.com/tuusername
            </div>
        </div>
        
        <div class="main-content">
            <section class="section">
                <h3 class="section-title">Repositorios destacados</h3>
                <div class="pinned-repos">
                    <div class="repo-card">
                        <h4 class="repo-name">
                            <svg viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="margin-right: 8px;">
                                <path fill-rule="evenodd" d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.53.22l2.72 2.72a.75.75 0 01.22.53v8.75a.75.75 0 01-1.5 0V4.5h-8a.75.75 0 00-.75.75v8.75a.75.75 0 01-1.5 0V4.5h-8a.75.75 0 00-.75.75v8.75a.75.75 0 01-1.5 0v-9z"></path>
                                <path fill-rule="evenodd" d="M4.5 3.5a.75.75 0 00-.75.75v8.75a.75.75 0 001.5 0V4.25a.75.75 0 00-.75-.75z"></path>
                            </svg>
                            proyecto-innovador
                        </h4>
                        <p class="repo-desc">Un proyecto innovador que resuelve problemas complejos con soluciones elegantes.</p>
                        <div class="repo-stats">
                            <div class="repo-lang">
                                <span class="lang-color javascript"></span>
                                JavaScript
                            </div>
                            <div>⭐ 128</div>
                            <div>📋 12</div>
                        </div>
                    </div>
                    
                    <div class="repo-card">
                        <h4 class="repo-name">
                            <svg viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="margin-right: 8px;">
                                <path fill-rule="evenodd" d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.53.22l2.72 2.72a.75.75 0 01.22.53v8.75a.75.75 0 01-1.5 0V4.5h-8a.75.75 0 00-.75.75v8.75a.75.75 0 01-1.5 0V4.5h-8a.75.75 0 00-.75.75v8.75a.75.75 0 01-1.5 0v-9z"></path>
                                <path fill-rule="evenodd" d="M4.5 3.5a.75.75 0 00-.75.75v8.75a.75.75 0 001.5 0V4.25a.75.75 0 00-.75-.75z"></path>
                            </svg>
                            web-app
                        </h4>
                        <p class="repo-desc">Aplicación web moderna con React y Node.js con funcionalidades avanzadas.</p>
                        <div class="repo-stats">
                            <div class="repo-lang">
                                <span class="lang-color javascript"></span>
                                JavaScript
                            </div>
                            <div>⭐ 86</div>
                            <div>📋 7</div>
                        </div>
                    </div>
                    
                    <div class="repo-card">
                        <h4 class="repo-name">
                            <svg viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="margin-right: 8px;">
                                <path fill-rule="evenodd" d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.53.22l2.72 2.72a.75.75 0 01.22.53v8.75a.75.75 0 01-1.5 0V4.5h-8a.75.75 0 00-.75.75v8.75a.75.75 0 01-1.5 0V4.5h-8a.75.75 0 00-.75.75v8.75a.75.75 0 01-1.5 0v-9z"></path>
                                <path fill-rule="evenodd" d="M4.5 3.5a.75.75 0 00-.75.75v8.75a.75.75 0 001.5 0V4.25a.75.75 0 00-.75-.75z"></path>
                            </svg>
                            data-analysis
                        </h4>
                        <p class="repo-desc">Herramientas de análisis de datos con Python y visualización interactiva.</p>
                        <div class="repo-stats">
                            <div class="repo-lang">
                                <span class="lang-color python"></span>
                                Python
                            </div>
                            <div>⭐ 54</div>
                            <div>📋 3</div>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="section">
                <h3 class="section-title">Actividad reciente</h3>
                <div class="activity-grid">
                    <!-- Generar 365 días de actividad (53x7 = 371, algunos vacíos) -->
                    <!-- Esto es solo una simulación visual -->
                </div>
            </section>
            
            <section class="section">
                <h3 class="section-title">Habilidades y tecnologías</h3>
                <div class="skills-container">
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">Git</span>
                    <span class="skill-tag">MongoDB</span>
                    <span class="skill-tag">Express</span>
                    <span class="skill-tag">AWS</span>
                    <span class="skill-tag">Docker</span>
                    <span class="skill-tag">CI/CD</span>
                </div>
            </section>
            
            <section class="section">
                <h3 class="section-title">Acerca de mí</h3>
                <p>Soy un desarrollador fullstack con 3 años de experiencia creando aplicaciones web escalables y eficientes. Me apasiona aprender nuevas tecnologías y compartir conocimiento con la comunidad.</p>
                <br>
                <p>🔭 Actualmente trabajando en: Mi startup personal de tecnología</p>
                <p>🌱 Actualmente aprendiendo: Machine Learning y DevOps</p>
                <p>👯 Busco colaborar en: Proyectos open source interesantes</p>
                <p>💬 Pregúntame sobre: React, Node.js y desarrollo web en general</p>
                <p>📫 Cómo contactarme: email@ejemplo.com</p>
                <p>⚡ Dato curioso: Me encanta el ajedrez y la fotografía</p>
            </section>
        </div>
    </div>

    <script>
        // Generar la cuadrícula de actividad
        document.addEventListener('DOMContentLoaded', function() {
            const activityGrid = document.querySelector('.activity-grid');
            const days = 53 * 7; // 53 semanas x 7 días
            
            for (let i = 0; i < days; i++) {
                const day = document.createElement('div');
                day.classList.add('activity-day');
                
                // Aleatoriamente asignar niveles de actividad
                const random = Math.random();
                if (random < 0.6) {
                    // 60% de días sin actividad o baja
                    if (random < 0.3) {
                        day.classList.add('low');
                    }
                    // El resto se queda sin clase (sin actividad)
                } else if (random < 0.8) {
                    day.classList.add('medium');
                } else if (random < 0.95) {
                    day.classList.add('high');
                } else {
                    day.classList.add('very-high');
                }
                
                activityGrid.appendChild(day);
            }
        });
    </script>
</body>
</html>
