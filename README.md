[RV.html](https://github.com/user-attachments/files/24412459/RV.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RINCONCITO VERDE | 2026</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&family=Playfair+Display:ital,wght@0,600;1,400&display=swap" rel="stylesheet">
    <style>
        :root {
            --verde-principal: #2E7D32;
            --verde-oscuro: #122113;
            --amarillo-mango: #FFB300;
            --crema: #FFFDF5;
            --blanco: #ffffff;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Montserrat', sans-serif; background: var(--crema); color: #333; line-height: 1.6; overflow-x: hidden; scroll-behavior: smooth; }
        
        /* --- 1. HEADER E INSTITUCIONAL --- */
        header {
            background: var(--blanco);
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
        }
        .logo { font-family: 'Playfair Display', serif; font-size: 1.8rem; font-weight: bold; color: var(--verde-principal); letter-spacing: -1px; text-decoration: none; }

        .nav-container { display: flex; align-items: center; gap: 30px; }
        nav ul { list-style: none; display: flex; gap: 20px; }
        nav a { text-decoration: none; color: #444; font-weight: 600; font-size: 0.85rem; transition: 0.3s; }
        nav a:hover { color: var(--verde-principal); border-bottom: 2px solid var(--amarillo-mango); }

        .search-section { display: flex; align-items: center; background: #f0f0f0; padding: 8px 15px; border-radius: 20px; }
        .search-section input { border: none; background: none; outline: none; padding-left: 10px; font-size: 0.8rem; width: 150px; }

        /* --- 2. PORTADA DINÁMICA (HERO) --- */
        .hero {
            height: 90vh;
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
        }
        .hero-bg {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
                        url( 'https://sl.bing.net/ijEE8tdUhci');
            background-size: cover;
            background-position: center;
            animation: zoomDynamic 20s infinite alternate;
            z-index: -1;
        }
        @keyframes zoomDynamic {
            from { transform: scale(1); }
            to { transform: scale(1.1); }
        }
        .hero-content h1 { font-family: 'Playfair Display', serif; font-size: 5rem; margin-bottom: 10px; text-shadow: 2px 2px 15px rgba(0,0,0,0.5); }
        .hero-content p { font-size: 1.4rem; font-weight: 300; letter-spacing: 4px; text-transform: uppercase; }

        /* --- 3. NOSOTROS (PRESENTACIÓN INSTITUCIONAL) --- */
        .nosotros { padding: 100px 10%; text-align: center; background: var(--blanco); }
        .info-content { max-width: 850px; margin: 0 auto; }
        .ceo-statement { 
            padding: 40px; 
            border-radius: 20px; 
            background: var(--crema); 
            border-left: 8px solid var(--amarillo-mango);
            margin-bottom: 50px;
            text-align: left;
        }
        .mvv-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; margin-top: 40px; }
        .mvv-card { padding: 30px; background: white; border: 1px solid #eee; border-radius: 15px; transition: 0.3s; }
        .mvv-card:hover { box-shadow: 0 10px 30px rgba(0,0,0,0.05); }

        /* --- 4. CATÁLOGO (ESTILO DARK) --- */
        .catalog { background: var(--verde-oscuro); color: white; padding: 100px 8%; text-align: center; }
        .catalog-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 40px; margin-top: 60px; }
        .card { 
            background: rgba(255,255,255,0.03); 
            border-radius: 25px; 
            padding: 20px; 
            border: 1px solid rgba(255,255,255,0.1); 
            transition: 0.4s ease-in-out;
            position: relative;
        }
        .card:hover { transform: translateY(-15px); border-color: var(--amarillo-mango); background: rgba(255,255,255,0.06); }
        .card img { width: 100%; height: 320px; object-fit: cover; border-radius: 20px; background: #fff; }
        .price-tag { color: var(--amarillo-mango); font-size: 1.6rem; font-weight: bold; margin-top: 15px; display: block; }

        /* --- 5. CONTACTO Y REDES --- */
        .contacto { padding: 100px 10%; display: grid; grid-template-columns: 1fr 1fr; gap: 80px; background: var(--crema); }
        .contact-details h2 { font-family: 'Playfair Display', serif; font-size: 3rem; margin-bottom: 25px; color: var(--verde-principal); }
        .social-box { display: flex; gap: 15px; margin-top: 35px; }
        .social-box a { 
            background: var(--verde-principal); 
            color: white; 
            width: 50px; height: 50px; 
            display: flex; align-items: center; justify-content: center; 
            border-radius: 50%; text-decoration: none; transition: 0.3s; font-weight: bold;
        }
        .social-box a:hover { background: var(--amarillo-mango); transform: translateY(-5px); }

        .form-container input, .form-container textarea { 
            width: 100%; padding: 15px; margin-bottom: 20px; 
            border: none; border-bottom: 2px solid #ccc; background: transparent; outline: none;
            font-family: inherit; transition: 0.3s;
        }
        .form-container input:focus { border-bottom-color: var(--verde-principal); }
        .btn-action { 
            background: var(--verde-principal); color: white; border: none; 
            padding: 18px 50px; border-radius: 35px; font-weight: bold; cursor: pointer; transition: 0.3s;
        }
        .btn-action:hover { background: var(--amarillo-mango); color: var(--verde-oscuro); }

        /* --- 6. CHATBOT E INTERFAZ --- */
        #chatbot-btn { position: fixed; bottom: 30px; right: 30px; background: var(--amarillo-mango); width: 65px; height: 65px; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; box-shadow: 0 10px 25px rgba(0,0,0,0.2); font-size: 1.8rem; z-index: 2000; transition: 0.3s; }
        #chatbot-btn:hover { transform: scale(1.1); }

        footer { background: var(--verde-oscuro); color: white; padding: 60px 5% 30px; text-align: center; }
        .footer-links { margin-bottom: 30px; display: flex; justify-content: center; gap: 30px; font-size: 0.8rem; opacity: 0.7; }
        .footer-links a { color: white; text-decoration: none; }

        @media (max-width: 768px) { .contacto, .mvv-grid { grid-template-columns: 1fr; } .hero-content h1 { font-size: 3rem; } .nav-container { display: none; } }
    </style>
</head>
<body>

    <header>
        <a href="#inicio" class="logo">RINCONCITO VERDE</a>
        <div class="nav-container">
            <div class="search-section">
                <span>🔍</span>
                <input type="text" placeholder="Buscar especie...">
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#catalogo">Catálogo</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="inicio" class="hero">
          <div class=>
                <img src="c:\Users\Usuario\Downloads\descarga (14).jpg"
        <div class="hero-bg"></div>
        <div class="hero-content">
            <h1>RINCONCITO VERDE</h1>
            <p>Donde la naturaleza florece contigo</p>
        </div>
    </section>

    <section id="nosotros" class="nosotros">
        <div class="info-content">
            <div class="ceo-statement">
                <h3 style="color: var(--verde-principal); margin-bottom: 15px;">Mensaje de nuestra CEO</h3>
                <p>Bajo la dirección estratégica de Edith Mercedes Barrios Cruz, Rinconcito Verde trasciende el concepto de vivero tradicional. En este 2026, reafirmamos nuestro compromiso con la educación ambiental y la sostenibilidad, cultivando no solo plantas, sino conciencia ecológica en nuestra comunidad.</p>
            </div>
            
            <div class="mvv-grid">
                <div class="mvv-card">
                    <h4 style="color: var(--verde-principal); margin-bottom: 10px;">Misión</h4>
                    <p style="font-size: 0.9rem;">Proveer experiencias y ejemplares botánicos que impulsen prácticas sostenibles y embellezcan cada entorno con vida consciente.</p>
                </div>
                <div class="mvv-card" style="border-top: 4px solid var(--amarillo-mango);">
                    <h4 style="color: var(--verde-principal); margin-bottom: 10px;">Visión</h4>
                    <p style="font-size: 0.9rem;">Ser el referente regional líder en cultura verde, reconocido por nuestra calidad botánica y compromiso con el futuro del planeta.</p>
                </div>
                <div class="mvv-card">
                    <h4 style="color: var(--verde-principal); margin-bottom: 10px;">Valores</h4>
                    <p style="font-size: 0.9rem;">Honestidad, Respeto por la Tierra, Sostenibilidad y Excelencia en el Cuidado.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="catalogo" class="catalog">
        <h2 style="font-family: 'Playfair Display'; font-size: 3.5rem; margin-bottom: 10px;">Catálogo 2026</h2>
        <p style="color: var(--amarillo-mango); letter-spacing: 3px;">EDICIONES LIMITADAS Y SUCULENTAS</p>

        <div class="catalog-grid">
            <div class="card">
                <img src="https://www.decorgreenchile.cl/wp-content/uploads/2024/03/cactus-san-pedro.jpg" alt="Cactus San Pedro (Echinopsis Pachanoi)">
                <h3 style="margin-top:20px; font-family: 'Playfair Display';">San Pedro</h3>
                <p style="font-size: 0.8rem; opacity: 0.7; margin-top:10px;">*Echinopsis pachanoi*: Ejemplar columnar majestuoso, seleccionado bajo estrictos estándares de calidad botánica.</p>
                <span class="price-tag">S/ 65.00</span>
            </div>

            <div class="card">
                <img src="https://images.unsplash.com/photo-1509423350716-97f9360b4e09?q=80&w=600&auto=format&fit=crop" alt="Echeveria Elegans">
                <h3 style="margin-top:20px; font-family: 'Playfair Display';">Rosé</h3>
                <p style="font-size: 0.8rem; opacity: 0.7; margin-top:10px;">Suculenta de roseta perfecta, ideal para colecciones de interior iluminado.</p>
                <span class="price-tag">S/ 15.00</span>
            </div>

            <div class="card">
                <img src="https://images.unsplash.com/photo-1614594975525-e45190c55d0b?q=80&w=600&auto=format&fit=crop" alt="Haworthia Fasciata">
                <h3 style="margin-top:20px; font-family: 'Playfair Display';">Haworthia Zebra</h3>
                <p style="font-size: 0.8rem; opacity: 0.7; margin-top:10px;">Planta exótica y altamente resistente con patrones únicos en relieve.</p>
                <span class="price-tag">S/ 12.00</span>
            </div>

            <div class="card">
                <img src="\Users\Usuario\Downloads\Echeveria 'Blue Sky' _ Echeveria, Succulents, Plants.jpg " alt="Haworthia Fasciata">
                <h3 style="margin-top:20px; font-family: 'Playfair Display';">Echeberia Bicolor</h3>
                <p style="font-size: 0.8rem; opacity: 0.7; margin-top:10px;">Planta exótica y altamente resistente con patrones únicos en relieve.</p>
                <span class="price-tag">S/ 12.00</span>
            </div>
            
            <div class="card">
                <img src="c:\Users\Usuario\Downloads\descarga (12).jpg" alt="Haworthia Fasciata">
                <h3 style="margin-top:20px; font-family: 'Playfair Display';">Echeberia - Nébula verde</h3>
                <p style="font-size: 0.8rem; opacity: 0.7; margin-top:10px;">Planta exótica y altamente resistente con patrones únicos en relieve.</p>
                <span class="price-tag">S/ 15.00</span>
            </div>

                <div class="card">
                <img src="c:\Users\Usuario\Downloads\Rare Succulents.jpg " alt="Haworthia Fasciata">
                <h3 style="margin-top:20px; font-family: 'Playfair Display';">Echeberia -  Rosa de alabastro </h3>
                <p style="font-size: 0.8rem; opacity: 0.7; margin-top:10px;">Planta exótica y altamente resistente con patrones únicos en relieve.</p>
                <span class="price-tag">S/ 12.00</span>
            </div>
        </div>
    </section>

    <section id="contacto" class="contacto">
        <div class="contact-details">
            <h2>Hablemos.</h2>
            <p style="margin-bottom: 30px;">Nuestro equipo de expertos y la dirección de Edith Barrios están listos para asesorarte.</p>
            <p><strong>📍 Sede Central:</strong> Valle Sagrado, Arequipa - Perú</p>
            <p><strong>📞 WhatsApp:</strong> +51 987 654 321</p>
            <p><strong>✉️ Email:</strong> institucional@rinconcitoverde.com</p>
            
            <div class="social-box">
                <a href="https://facebook.com/rinconcitoverde" target="_blank" title="Facebook">FB</a>
                <a href="https://instagram.com/rinconcitoverde" target="_blank" title="Instagram">IG</a>
                <a href="https://tiktok.com/@rinconcitoverde" target="_blank" title="TikTok">TK</a>
                <a href="https://linkedin.com/company/rinconcitoverde" target="_blank" title="LinkedIn">IN</a>
            </div>
        </div>
        <div class="form-container">
            <form action="#">
                <input type="text" placeholder="Nombre y Apellidos" required>
                <input type="email" placeholder="Correo Corporativo" required>
                <textarea rows="5" placeholder="¿En qué podemos asesorarte hoy?" required></textarea>
                <button type="submit" class="btn-action">ENVIAR CONSULTA INSTITUCIONAL</button>
            </form>
        </div>
    </section>

    <div id="chatbot-btn" onclick="alert('Asistente Virtual Rinconcito Verde 2026: ¿Deseas información sobre el cuidado del Cactus San Pedro?')">💬</div>

    <footer>
        <div class="footer-links">
            <a href="#">Políticas de Privacidad</a>
            <a href="#">Sostenibilidad</a>
            <a href="#">Trabaja con nosotros</a>
            <a href="#">Preguntas Frecuentes</a>
        </div>
        <p style="opacity: 0.6; font-size: 0.75rem;">© 2026 RINCONCITO VERDE. Gestión Estratégica: Edith Mercedes Barrios Cruz.</p>
    </footer>

</body>
</html>
