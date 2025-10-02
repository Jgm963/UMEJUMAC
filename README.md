<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Umejumac - Soluciones Digitales</title>
    
    <style>
        /* --- VARIABLES DE COLOR (AÑADIDAS PARA CONSISTENCIA) --- */
        :root {
            /* Usando los colores primarios de tu nuevo CSS: Azul oscuro y Amarillo/Naranja */
            --color-principal: #003366; 
            --color-acento: #ffcc00;   
            --color-fondo: #f4f4f9;
        }

        /* --- ESTILOS GENERALES (REVISADO Y CORREGIDO) --- */
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: var(--color-fondo);
            color: #333;
            scroll-behavior: smooth; 
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* ====================================
            ESTILOS GENERALES Y DE NAVEGACIÓN (TU CSS)
            ==================================== */

        .fade-in { animation: fadeIn 0.5s ease-in-out; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* Dejamos .view en display: block para que el contenido sea visible */
        .view { display: block; }
        
        .placeholder-img {
            background-color: #003366;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.25rem;
            font-weight: 700;
        }

        .cover-placeholder {
            height: 180px; 
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 1rem; 
            text-align: center;
        }
        
        .cover-placeholder span {
            font-size: 1.25rem;
            line-height: 1.4;
            display: block;
            max-height: 100%;
            overflow: hidden;
            word-break: break-word;
        }
        
        .cover-image {
            height: 180px;
            width: 100%;
            object-fit: cover; 
        }

        /* ENCABEZADO CON TU NUEVO ESTILO */
        .header-nav {
            background-color: var(--color-principal); /* #003366 */
            color: white;
            position: sticky;
            top: 0;
            z-index: 20;
            box-shadow: 0 2px 4px 0 rgba(0,0,0,0.1);
            /* Añadimos Flexbox para alinear el título y el logo */
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 30px; 
        }

        /* Logo como área clicable (Ajustado para el encabezado) */
        .logo-click-area {
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
            transition: all 0.2s;
            padding: 0.25rem; 
            border-radius: 0.5rem;
            text-decoration: none; /* Asegura que no tenga subrayado */
            color: white; /* Color del texto del logo */
        }
        .logo-click-area:hover {
            background-color: rgba(255, 255, 255, 0.1); 
        }

        /* LOGO: Si usas una imagen, la clase #logo-image no es adecuada,
           pero si usas el logo de texto, este estilo lo define. */
        #logo-image {
            background-color: var(--color-acento); /* #ffcc00 */
            border: 2px solid var(--color-acento); 
            border-radius: 0.5rem; 
            padding: 4px; 
            transition: all 0.2s ease-in-out;
            box-shadow: 0 0 8px rgba(255, 204, 0, 0.7); 
            width: 40px; /* Tamaño fijo para imagen o texto */
            height: 40px;
        }
        .logo-click-area:hover #logo-image {
            transform: scale(1.05); 
            box-shadow: 0 0 12px rgba(255, 204, 0, 1);
        }
        
        .book-card {
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s, box-shadow 0.2s;
            overflow: hidden; 
        }
        .book-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
        }

        .main-section-card {
            background-color: #f7f9fc;
            border-left: 5px solid var(--color-principal); 
            transition: all 0.3s;
            cursor: pointer; 
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 4px;
        }
        .main-section-card:hover {
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            transform: translateY(-5px);
            border-left: 5px solid var(--color-acento); 
        }
        
        /* ====================================
            ESTILOS DEL LOGO PERSONALIZADO (Modal, adaptado)
            ==================================== */
        .custom-logo-container {
            width: 100%;
            max-width: 250px;
            margin: 0 auto;
            background-color: white; 
            border: 2px solid var(--color-principal); 
            text-align: center;
            padding: 20px;
        }
        .logo-m {
            font-size: 7rem;
            line-height: 1;
            font-weight: 900;
            color: #000000; 
            text-shadow: none; 
        }
        .logo-acronym {
            font-size: 1rem;
            font-weight: 500;
            color: #444;
            margin-top: -5px; 
        }
        .acronym-highlight {
            font-weight: 900;
            color: var(--color-principal); 
            font-size: 1.1rem;
            padding: 0 2px;
        }
        .autonomy-concept {
            font-size: 1.2rem; 
            font-weight: 900;
            color: #000000; 
            margin-top: 10px; 
            border-top: 2px solid var(--color-principal); 
            padding-top: 8px;
            width: 90%; 
            margin-left: auto;
            margin-right: auto;
        }
        .etae-concept {
            font-size: 0.8rem;
            font-weight: 700;
            color: #dc2626; 
            margin-top: 5px; 
            padding-bottom: 5px;
            width: 90%;
            border-bottom: 1px solid #e5e7eb; 
            margin-left: auto;
            margin-right: auto;
        }

    </style>
</head>
<body>

    <header class="header-nav">
        <h1>Umejumac</h1>
        
        <a href="#about-logo" class="logo-click-area">
            <img id="logo-image" src="ruta/al/logo-pequeno.png" alt="Logo Umejumac">
        </a>
    </header>

    <main class="container view fade-in">
        
        <section style="text-align: center; padding: 50px 0 30px;">
            <h2>Bienvenido a Umejumac</h2>
            <p style="font-size: 1.2em; color: #555;">Especialistas en soluciones digitales y desarrollo web, impulsando tu negocio al siguiente nivel.</p>
        </section>

        <section style="display: flex; gap: 20px; margin-bottom: 40px;">
            <div class="main-section-card" style="flex: 1;">
                <h3>Servicios de Desarrollo</h3>
                <p>Webs, Apps, Integraciones.</p>
            </div>
            <div class="main-section-card" style="flex: 1;">
                <h3>Proyectos Destacados</h3>
                <p>Mira nuestro portafolio.</p>
            </div>
            <div class="main-section-card" style="flex: 1;">
                <h3>Contacto</h3>
                <p>Inicia tu proyecto hoy.</p>
            </div>
        </section>

        <section id="about-logo" style="padding: 60px 0; text-align: center; background-color: #ffffff; border-top: 1px solid #eee;">
            <h2>Identidad de Umejumac (Concepto de Logo)</h2>
            
            <div class="custom-logo-container">
                <div class="logo-m">M</div>
                <div class="logo-acronym">
                    <span class="acronym-highlight">U</span>tilidad, <span class="acronym-highlight">M</span>ovilidad, <span class="acronym-highlight">E</span>ficiencia, <span class="acronym-highlight">J</span>uicio, <span class="acronym-highlight">U</span>nidad, <span class="acronym-highlight">M</span>aestría, <span class="acronym-highlight">A</span>gilidad, <span class="acronym-highlight">C</span>reatividad.
                </div>
                <div class="autonomy-concept">AUTONOMY & CONECTIVITY</div>
                <div class="etae-concept">Efficiency, Transparency, Agility, Excellence</div>
            </div>
            
            <p style="margin-top: 20px; max-width: 800px; margin-left: auto; margin-right: auto; color: #555;">Este diseño utiliza la tipografía y el acrónimo para representar nuestros valores fundamentales en soluciones digitales.</p>
        </section>
    </main>

    <footer style="background-color: #333; color: white; padding: 30px 0; text-align: center; margin-top: 60px;">
        <div class="container">
            <h2>Contacto</h2>
            <p style="margin-top: 20px; font-size: 0.9em; color: #bbb;">&copy; 2024 Umejumac. Todos los derechos reservados.</p>
        </div>
    </footer>

</body>
</html>
