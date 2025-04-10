# Practica4marisolcarreolagithub.io
Marisol Carreola Davila
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canserbero - Vida y Legado</title>
    <style>
        :root {
            --dark: #121212;
            --darker: #0a0a0a;
            --accent: #e63946;
            --light: #f1faee;
            --text: #e2e2e2;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--dark);
            color: var(--text);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://i.ytimg.com/vi/3tmd9pF5yho/maxresdefault.jpg');
            background-size: cover;
            background-position: center;
            height: 70vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }
        
        h1 {
            font-size: 4rem;
            margin: 0;
            color: var(--accent);
            text-shadow: 3px 3px 5px rgba(0,0,0,0.7);
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-top: 20px;
            max-width: 800px;
        }
        
        nav {
            background-color: var(--darker);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }
        
        .nav-container {
            display: flex;
            justify-content: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .nav-link {
            color: var(--text);
            text-decoration: none;
            margin: 0 1.5rem;
            font-weight: bold;
            font-size: 1.1rem;
            transition: color 0.3s;
        }
        
        .nav-link:hover {
            color: var(--accent);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        section {
            margin-bottom: 3rem;
        }
        
        h2 {
            color: var(--accent);
            font-size: 2.2rem;
            border-bottom: 2px solid var(--accent);
            padding-bottom: 0.5rem;
            margin-top: 0;
        }
        
        .bio-section {
            display: flex;
            gap: 2rem;
            align-items: center;
            margin-bottom: 3rem;
        }
        
        .bio-text {
            flex: 2;
        }
        
        .bio-image {
            flex: 1;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .bio-image img {
            width: 100%;
            display: block;
        }
        
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 4px;
            background-color: var(--accent);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: var(--light);
            border: 4px solid var(--accent);
            border-radius: 50%;
            top: 15px;
            z-index: 1;
        }
        
        .left {
            left: 0;
            text-align: right;
        }
        
        .right {
            left: 50%;
            text-align: left;
        }
        
        .left::after {
            right: -12px;
        }
        
        .right::after {
            left: -12px;
        }
        
        .content {
            padding: 20px;
            background-color: var(--darker);
            border-radius: 8px;
            box-shadow: 0 3px 5px rgba(0,0,0,0.2);
        }
        
        .discography {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .album {
            background-color: var(--darker);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }
        
        .album:hover {
            transform: translateY(-5px);
        }
        
        .album-cover {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        
        .album-info {
            padding: 1rem;
        }
        
        .album-title {
            font-weight: bold;
            margin: 0 0 0.5rem 0;
            color: var(--accent);
        }
        
        .album-year {
            color: #999;
            font-size: 0.9rem;
        }
        
        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            margin: 2rem 0;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        
        footer {
            background-color: var(--darker);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: var(--text);
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent);
        }
        
        @media (max-width: 768px) {
            .bio-section {
                flex-direction: column;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item::after {
                left: 21px;
            }
            
            .left::after, .right::after {
                left: 21px;
            }
            
            .right {
                left: 0;
                text-align: left;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <h1>CANSERBERO</h1>
        <p class="subtitle">Tyrone José Gonzalez Orama · 1988-2015 · El filósofo del rap en español</p>
    </header>
    
    <nav>
        <div class="nav-container">
            <a href="#biografia" class="nav-link">Biografía</a>
            <a href="#carrera" class="nav-link">Carrera Musical</a>
            <a href="#discografia" class="nav-link">Discografía</a>
            <a href="#legado" class="nav-link">Legado</a>
            <a href="#documental" class="nav-link">Documental</a>
        </div>
    </nav>
    
    <div class="container">
        <section id="biografia">
            <h2>Biografía</h2>
            <div class="bio-section">
                <div class="bio-text">
                    <p>Tirso José Romero Orama, conocido artísticamente como Canserbero, fue un rapero, compositor y activista social venezolano, considerado uno de los más importantes exponentes del rap en español. Nació el 11 de marzo de 1988 en Caracas, Venezuela.</p>
                    <p>Criado en la ciudad de Maracay, desde joven mostró interés por la música y la escritura. Su nombre artístico proviene de la combinación de "Cáncer" (por el signo zodiacal) y "Cerbero" (el guardián del inframundo en la mitología griega).</p>
                    <p>Su música se caracterizó por letras profundas que abordaban temas sociales, políticos, filosóficos y personales, convirtiéndose en la voz de una generación.</p>
                </div>
                <div class="bio-image">
                    <img src="https://www.lahiguera.net/musicalia/artistas/canserbero/fotos/32274/canserbero_1-portada.jpg" alt="Canserbero en concierto">
                </div>
            </div>
        </section>
        
        <section id="carrera">
            <h2>Carrera Musical</h2>
            <div class="timeline">
                <div class="timeline-item left">
                    <div class="content">
                        <h3>2004-2006: Inicios</h3>
                        <p>Forma parte del grupo "Códigos de Barrio" junto a su primo Lil Supa. Graban maquetas y participan en batallas de rap.</p>
                    </div>
                </div>
                <div class="timeline-item right">
                    <div class="content">
                        <h3>2008: Primer álbum</h3>
                        <p>Lanza "Vida", su primer trabajo solista, con temas como "Pensando en ti" y "Es épico".</p>
                    </div>
                </div>
                <div class="timeline-item left">
                    <div class="content">
                        <h3>2010: Can+Zoo Indigos</h3>
                        <p>Forma el dúo Can+Zoo Indigos con Apache. Publican el álbum "Indigo" con temas contestatarios.</p>
                    </div>
                </div>
                <div class="timeline-item right">
                    <div class="content">
                        <h3>2012: Muerte</h3>
                        <p>Lanza su álbum conceptual "Muerte", considerado su obra maestra, con canciones como "Jeremías 17-5" y "C'est la mort".</p>
                    </div>
                </div>
                <div class="timeline-item left">
                    <div class="content">
                        <h3>2015: Fallecimiento</h3>
                        <p>El 20 de enero de 2015, Canserbero fallece en circunstancias no completamente aclaradas en su apartamento en Maracay.</p>
                    </div>
                </div>
                <div class="timeline-item right">
                    <div class="content">
                        <h3>Post Mortem</h3>
                        <p>Su música cobra aún más relevancia después de su muerte, convirtiéndose en un ícono cultural latinoamericano.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="discografia">
            <h2>Discografía</h2>
            <div class="discography">
                <div class="album">
                    <img src="https://images.genius.com/9c0a4c6c0a0c0c5c5c0c0c5c0c0c5c0.1000x1000x1.jpg" alt="Álbum Vida" class="album-cover">
                    <div class="album-info">
                        <h3 class="album-title">Vida (2008)</h3>
                        <p class="album-year">2008</p>
                        <p>Primer álbum solista con 15 tracks</p>
                    </div>
                </div>
                <div class="album">
                    <img src="https://images.genius.com/9c0a4c6c0a0c0c5c5c0c0c5c0c0c5c0.1000x1000x1.jpg" alt="Álbum Indigo" class="album-cover">
                    <div class="album-info">
                        <h3 class="album-title">Indigo (2010)</h3>
                        <p class="album-year">2010</p>
                        <p>Como parte de Can+Zoo Indigos</p>
                    </div>
                </div>
                <div class="album">
                    <img src="https://images.genius.com/9c0a4c6c0a0c0c5c5c0c0c5c0c0c5c0.1000x1000x1.jpg" alt="Álbum Muerte" class="album-cover">
                    <div class="album-info">
                        <h3 class="album-title">Muerte (2012)</h3>
                        <p class="album-year">2012</p>
                        <p>Álbum conceptual de 12 canciones</p>
                    </div>
                </div>
                <div class="album">
                    <img src="https://images.genius.com/9c0a4c6c0a0c0c5c5c0c0c5c0c0c5c0.1000x1000x1.jpg" alt="Álbum póstumo" class="album-cover">
                    <div class="album-info">
                        <h3 class="album-title">Nuestra Doctrina No Es un Dogma... (2019)</h3>
                        <p class="album-year">2019</p>
                        <p>Recopilación póstuma de temas inéditos</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="legado">
            <h2>Legado</h2>
            <p>Canserbero se ha convertido en un símbolo del rap en español y la conciencia social. Sus letras, llenas de crítica social, reflexión filosófica y mensajes de superación, continúan inspirando a nuevas generaciones.</p>
            <p>Algunos de sus temas más influyentes incluyen:</p>
            <ul>
                <li>"Pensando en ti" - Un homenaje a su madre fallecida</li>
                <li>"Jeremías 17-5" - Crítica al sistema político y social</li>
                <li>"Es épico" - Sobre la importancia de perseguir los sueños</li>
                <li>"C'est la mort" - Reflexión sobre la muerte</li>
            </ul>
            <p>Su influencia trasciende la música, siendo estudiado en universidades y citado en movimientos sociales.</p>
        </section>
        
        <section id="documental">
            <h2>Documental</h2>
            <p>En 2023 se estrenó el documental "Canserbero: La Verdadera Historia", que explora su vida, carrera y las circunstancias de su muerte.</p>
            <div class="video-container">
                <iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
            <p style="text-align: center;"><em>Reemplaza "VIDEO_ID" con el ID del tráiler/documental oficial</em></p>
        </section>
    </div>
    
    <footer>
        <p>© 2023 Tributo a Canserbero - Todos los derechos reservados</p>
        <p>"El conocimiento nos hace libres, la ignorancia nos esclaviza" - Canserbero</p>
        <div class="social-links">
            <a href="#"><i class="fab fa-youtube"></i></a>
            <a href="#"><i class="fab fa-spotify"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
        </div>
    </footer>
</body>
</html>
