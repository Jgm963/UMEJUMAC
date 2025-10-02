<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UMEJUMAC - Soluciones Digitales y Asesoría</title>
    
    <style>
        /* Estilos base para una mejor visualización */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        header {
            background-color: #003366; /* Azul Oscuro */
            color: white;
            padding: 15px 0;
            text-align: center;
        }
        header .logo-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        .main-nav {
            background-color: #0056b3; /* Azul Medio */
            padding: 10px 0;
        }
        .main-nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
            gap: 30px;
        }
        .main-nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 5px 10px;
            transition: background-color 0.3s;
        }
        .main-nav a:hover {
            background-color: #ffcc00; /* Amarillo/Naranja */
            color: #003366;
            border-radius: 4px;
        }
        .content-section {
            background-color: white;
            padding: 40px;
            margin-top: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .section-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 20px;
            justify-content: center;
        }
        .section-card {
            flex: 1 1 300px; /* Responsive: 300px min width */
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            transition: border-color 0.3s;
        }
        .section-card:hover {
            border-color: #0056b3;
        }
    </style>
</head>
<body>

    <header>
        <div class="container logo-container">
            <img src="ruta/al/logo-pequeno.png" alt="Logo UMEJUMAC" style="width: 60px; height: 60px; background-color: white; border-radius: 50%;">
            <h1>UMEJUMAC</h1>
        </div>
    </header>

    <nav class="main-nav">
        <div class="container">
            <ul>
                <li><a href="#asesoria">Asesoría</a></li>
                <li><a href="#bienesyservicios">Bienes y Servicios</a></li>
                <li><a href="#ventas">Ventas</a></li>
                <li><a href="portafolio.html">Portafolio</a></li>
                <li><a href="blog.html">Blog</a></li>
            </ul>
        </div>
    </nav>

    <main class="container">
        <section class="content-section" style="text-align: center;">
            <h2>Impulsando el Bienestar y la Productividad</h2>
            <p>Conozca nuestras soluciones integrales en salud colectiva, bienes, servicios y tecnología.</p>
        </section>

        <div class="section-grid">
            
            <section id="asesoria" class="section-card">
                <h3>1. Asesoría en Salud Colectiva</h3>
                <p>Ofrecemos consultoría especializada para optimizar la gestión de riesgos de salud en comunidades y empresas. Enfocados en prevención y políticas públicas.</p>
                <a href="#" style="color: #0056b3;">Ver Servicios de Asesoría →</a>
            </section>

            <section id="bienesyservicios" class="section-card">
                <h3>2. Bienes y Servicios</h3>
                <p>Suministro de equipos, materiales y servicios esenciales para el sector público y privado. Calidad y eficiencia en logística y distribución.</p>
                <a href="#" style="color: #0056b3;">Explorar Bienes y Servicios →</a>
            </section>

            <section id="ventas" class="section-card">
                <h3>3. Ventas (Soluciones Tecnológicas)</h3>
                <p>Venta de soluciones digitales a medida, incluyendo desarrollo web, software de gestión y plataformas de e-commerce. La tecnología al servicio de tu negocio.</p>
                <a href="#" style="color: #0056b3;">Ver Soluciones en Venta →</a>
            </section>

        </div>
        
    </main>

    <footer style="background-color: #333; color: white; padding: 20px 0; margin-top: 40px; text-align: center;">
        <div class="container">
            <p style="margin: 0;">Contacto: info@umejumac.com</p>
            <p style="margin: 5px 0 0;">&copy; 2024 UMEJUMAC. Todos los derechos reservados.</p>
        </div>
    </footer>

</body>
</html>
