<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maravillas Naturales del Mundo | José Carlos</title>
    <style>
        /* ==================================== */
        /* === ESTILOS GLOBALES Y PERSONALIZACIÓN === */
        /* ==================================== */
        :root {
            --color-fondo-principal: #2c3e50; /* Fondo Oscuro */
            --color-fondo-secundario: #ecf0f1; /* Fondo Claro de la sección */
            --color-texto-principal: #34495e; /* Texto Oscuro */
            --color-texto-claro: white; /* Texto para fondo oscuro */
            --color-acento: #3498db; /* Azul vibrante para enlaces */
        }

        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--color-fondo-secundario);
            color: var(--color-texto-principal);
        }
        
        /* ==================================== */
        /* === MENÚ DE NAVEGACIÓN (NAV) === */
        /* ==================================== */
        .navbar {
            background-color: var(--color-fondo-principal);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        .nav-list {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
        }
        .nav-list li {
            margin: 0 25px;
        }
        .nav-list a {
            color: var(--color-texto-claro);
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1em;
            transition: color 0.3s ease;
        }
        .nav-list a:hover {
            color: var(--color-acento);
        }
        
        /* ==================================== */
        /* === ENCABEZADO Y CONTENIDO GENERAL === */
        /* ==================================== */
        header {
            background-color: var(--color-acento);
            color: var(--color-texto-claro);
            padding: 40px 0;
            text-align: center;
        }
        h1 {
            margin: 0;
            font-size: 3em;
        }
        section {
            padding: 50px 0;
            text-align: center;
        }

        /* ==================================== */
        /* === GALERÍA (TIPOS) ESTILOS BASE === */
        /* ==================================== */
        #galeria h2, #tipos h2 {
            font-size: 2.2em;
            margin-bottom: 40px;
            color: var(--color-fondo-principal);
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
        }
        .card {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            width: 350px; /* Ancho base para desktop */
            transition: transform 0.4s ease;
            text-align: left;
        }
        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        .card img {
            width: 100%;
            height: 450px;
            object-fit: cover;
            display: block;
        }
        .card-content {
            padding: 20px;
        }
        .card-content h3 {
            color: var(--color-acento);
            font-size: 1.5em;
        }
        .card-content a {
            display: block;
            background-color: var(--color-fondo-principal);
            color: var(--color-texto-claro);
            padding: 10px 15px;
            margin-top: 15px;
            border-radius: 5px;
            text-decoration: none;
            text-align: center;
            transition: background-color 0.3s;
        }

        /* ==================================== */
        /* === SECCIÓN CONTACTO Y FOOTER === */
        /* ==================================== */
        #contacto {
            background-color: var(--color-fondo-principal);
            color: var(--color-texto-claro);
        }
        #contacto h2 {
            color: var(--color-texto-claro);
        }
        .contact-info {
            max-width: 600px;
            margin: 0 auto;
            text-align: left;
        }
        .contact-info strong {
            color: var(--color-acento);
            display: inline-block;
            width: 100px;
        }
        /* Estilos del botón de Contacto (Para que se vea bien desde el inicio) */
        #colorButton {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            margin-bottom: 20px; /* Añadido un pequeño margen inferior */
            transition: all 0.3s ease;
            background-color: #34495e; /* Color inicial (Gris Oscuro) */
            color: white;
            font-weight: bold;
        }
        
        footer {
            text-align: center;
            padding: 20px 0;
            background-color: #34495e;
            color: white;
        }

        /* ==================================== */
        /* === MEDIA QUERIES PARA RESPONSIVIDAD === */
        /* ==================================== */

        /* Estilos para pantallas más pequeñas (tabletas y móviles, hasta 768px) */
        @media (max-width: 768px) {
            
            /* Ajuste del menú de navegación */
            .nav-list {
                flex-direction: column; /* Apila los elementos verticalmente */
                gap: 10px; /* Espacio entre los elementos apilados */
            }
            .nav-list li {
                margin: 0; /* Elimina márgenes horizontales */
            }

            /* Ajuste del Encabezado */
            header {
                padding: 30px 10px;
            }
            h1 {
                font-size: 2em; /* Reduce el tamaño del título principal */
            }
            
            /* Ajuste de Contenedores y Tarjetas */
            .container {
                width: 95%; /* Usa casi todo el ancho disponible */
            }
            .card {
                width: 100%; /* Las tarjetas ocupan todo el ancho del contenedor */
                max-width: 400px; /* Límite de ancho para evitar que sean demasiado grandes */
                margin-bottom: 20px;
            }
            .card img {
                height: 300px; /* Reduce la altura de las imágenes en móvil */
            }
            .card-content h3 {
                font-size: 1.3em;
            }

            /* Ajuste de Contacto */
            .contact-info {
                padding: 0 20px;
            }
        }

        /* Estilos para pantallas muy pequeñas (móviles, hasta 480px) */
        @media (max-width: 480px) {
            h1 {
                font-size: 1.5em; /* Reducción adicional del título */
            }
            #galeria h2, #tipos h2 {
                font-size: 1.8em;
            }
            .card img {
                height: 250px; 
            }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <ul class="nav-list">
            <li><a href="#inicio">🏠 Inicio</a></li>
            <li><a href="#galeria">📸 Galería</a></li>
            <li><a href="#tipos">🏔️ Tipos</a></li>
            <li><a href="#contacto">📞 Contacto</a></li>
        </ul>
    </nav>

    <header id="inicio">
        <h1>MARAVILLAS NATURALES DEL MUNDO</h1>
        <p>Un recorrido visual por los paisajes más impresionantes de nuestro planeta.</p>
    </header>

    <section id="galeria">
        <h2>📸 Galería de Paisajes Únicos</h2>
        <div class="container">
            
            <div class="card">
                <img src="1000008597.jpg" alt="Arrecife de Coral">
                <div class="card-content">
                    <h3>El Vibrante Mundo Submarino 🐠</h3>
                    <p>
                        **Tipo:** Ecosistema Marino. **Descripción:** Este paisaje muestra un arrecife de coral lleno de vida. La tortuga marina, junto con peces de colores y estrellas de mar, nadan bajo los rayos de sol que penetran el agua cristalina. Los arrecifes son vitales para la biodiversidad oceánica.
                    </p>
                    <a href="https://pin.it/zPCkuCiFv" target="_blank">Ver Enlace Original</a>
                </div>
            </div>

            <div class="card">
                <img src="1000008598.jpg" alt="Cataratas de Iguazú con Arcoíris">
                <div class="card-content">
                    <h3>Grandes Cataratas con Arcoíris 🌈</h3>
                    <p>
                        **Tipo:** Hidrografía y Bioma Húmedo. **Descripción:** Las grandes cortinas de agua demuestran la fuerza del agua cayendo. La niebla que se levanta crea un espectacular arcoíris, un fenómeno óptico que acompaña a este popular destino turístico.
                    </p>
                    <a href="https://pin.it/7fuQM9Zq1" target="_blank">Ver Enlace Original</a>
                </div>
            </div>

            <div class="card">
                <img src="1000008600.jpg" alt="Dunas de Arena en el Desierto">
                <div class="card-content">
                    <h3>Siluetas del Desierto al Atardecer 🏜️</h3>
                    <p>
                        **Tipo:** Ecosistema Desértico. **Descripción:** Las dunas de arena, moldeadas por el viento a lo largo del tiempo, capturan la luz cálida del atardecer. La textura de la arena y las curvas suaves de las dunas definen este vasto y árido paisaje.
                    </p>
                    <a href="https://pin.it/3RULsXGAw" target="_blank">Ver Enlace Original</a>
                </div>
            </div>

            <div class="card">
                <img src="1000008596.jpg" alt="Volcán activo en medio de la selva">
                <div class="card-content">
                    <h3>Fuego y Vida: El Volcán Tropical 🌋</h3>
                    <p>
                        **Tipo:** Geografía Volcánica y Selva. **Descripción:** El contraste entre la cumbre humeante de un volcán y la densa vegetación tropical. Los ríos y cascadas fluyen a través de la base, enriqueciendo el suelo con minerales volcánicos.
                    </p>
                    <a href="https://pin.it/NhxJHxFQ5" target="_blank">Ver Enlace Original</a>
                </div>
            </div>

            <div class="card">
                <img src="1000008601.jpg" alt="Amanecer en las montañas con pinos">
                <div class="card-content">
                    <h3>Cumbres en la Luz del Alba 🌄</h3>
                    <p>
                        **Tipo:** Cordillera y Bosque de Coníferas. **Descripción:** Una vista panorámica del amanecer en la montaña. Los rayos de sol atraviesan el horizonte, iluminando los picos sucesivos y las siluetas de los pinos.
                    </p>
                    <a href="https://pin.it/3CeynkLjo" target="_blank">Ver Enlace Original</a>
                </div>
            </div>

            <div class="card">
                <img src="1000008595.jpg" alt="Glaciar de Hielo con Aurora Boreal">
                <div class="card-content">
                    <h3>Río de Hielo con Aurora Boreal 🧊</h3>
                    <p>
                        **Tipo:** Glaciar y Fenómeno Atmosférico. **Descripción:** Un río de deshielo fluye a través de un cañón tallado en bloques de hielo azul turquesa. En el cielo oscuro, la Aurora Boreal añade un toque de luces verdes y mágicas.
                    </p>
                    <a href="https://pin.it/5RHw6uLgR" target="_blank">Ver Enlace Original</a>
                </div>
            </div>

            <div class="card">
                <img src="1000008568.jpg" alt="Valle de Montaña con Río Azul">
                <div class="card-content">
                    <h3>Valle Alpino: El Pulmón Verde 🌲</h3>
                    <p>
                        **Tipo:** Valle Fluvial y Ecosistema Boreal. **Descripción:** Un río turquesa serpentea a través de un extenso valle cubierto de densos bosques. Las montañas con picos nevados en el fondo crean un paisaje de inmensa escala y pureza.
                    </p>
                    <a href="https://pin.it/3rTG4nlNP" target="_blank">Ver Enlace Original</a>
                </div>
            </div>
            
        </div>
    </section>

    <hr>

    <section id="tipos">
        <h2>🏔️ Clasificación de Paisajes</h2>
        <div class="container">
            <div class="card" style="width: 350px;">
                <div class="card-content">
                    <h3>Tipos de Terrestres</h3>
                    <p>Incluye **Montañas** (Amanecer, Valle), **Bosques** (Valle, Volcán), y **Desiertos** (Dunas). Caracterizados por la diversidad de relieves y vegetación adaptada al clima.</p>
                </div>
            </div>
            <div class="card" style="width: 350px;">
                <div class="card-content">
                    <h3>Tipos de Hídricos</h3>
                    <p>Incluye **Cataratas** (Grandes Cascada) y **Glaciares** (Cañón Ártico). Son paisajes dominados por masas de agua líquida o congelada que moldean la geografía.</p>
                </div>
            </div>
            <div class="card" style="width: 350px;">
                <div class="card-content">
                    <h3>Tipos de Mixtos/Especiales</h3>
                    <p>Incluye **Volcánicos** (Volcán Tropical) y **Marinos** (Arrecife de Coral). Estos combinan elementos terrestres y acuáticos o presentan fenómenos geológicos únicos.</p>
                </div>
            </div>
        </div>
    </section>

    <hr>

    <section id="contacto">
        <h2>📞 Contáctame</h2>
        <p>Si tienes preguntas o quieres explorar más paisajes, no dudes en contactarme.</p>
        
        <button id="colorButton" 
                onmouseover="cambiarColor('over')" 
                onmouseout="cambiarColor('out')">
            ¡Pasa el Ratón Aquí!
        </button>

        <div class="contact-info">
            <div><strong>Nombre:</strong> José Carlos</div>
            <div><strong>Email:</strong> jcarlossitio@ejemplo.com</div>
            <div><strong>Teléfono:</strong> +57 123 456 7890</div>
            <div><strong>Ubicación:</strong> Colombia</div>
        </div>
    </section>

    <footer>
        <p>Página de Galería de Paisajes Naturales.</p>
        <p>Diseñado y recopilado por: **José Carlos**</p>
    </footer>

    <script>
        /**
         * Función para cambiar el color de fondo y el texto del botón al pasar o retirar el ratón.
         * @param {string} estado - 'over' para mouseover, 'out' para mouseout.
         */
        function cambiarColor(estado) {
            const boton = document.getElementById('colorButton');
            
            // Usamos las variables CSS para mantener la coherencia de los colores
            const colorAcento = getComputedStyle(document.documentElement).getPropertyValue('--color-acento').trim();
            const colorTextoPrincipal = getComputedStyle(document.documentElement).getPropertyValue('--color-texto-principal').trim();

            if (estado === 'over') {
                // Al pasar el ratón: Usa el color de acento
                boton.style.backgroundColor = colorAcento || '#3498db'; 
                boton.style.color = colorTextoPrincipal || 'black';
                boton.innerText = "¡Gracias por el Interés! 😊";
            } else if (estado === 'out') {
                // Al retirar el ratón: Vuelve al color original del footer/navbar
                boton.style.backgroundColor = '#34495e'; 
                boton.style.color = 'white';
                boton.innerText = "¡Pasa el Ratón Aquí!";
            }
        }
    </script>

</body>
</html>

![1000008573](https://github.com/user-attachments/assets/8d80f80d-5a4a-4de1-bde7-97873eecc46b)
![1000008571](https://github.com/user-attachments/assets/1e4b4775-510e-4da2-b2cf-898f78594afe)
![1000008570](https://github.com/user-attachments/assets/891fae61-5c47-49d2-ac1f-2a4ed1e00b88)
![1000008565](https://github.com/user-attachments/assets/c9a5c918-6db2-4cc2-b21f-75e0711a7f5f)
![1000008572](https://github.com/user-attachments/assets/4376c018-77b3-4502-ba4a-81f0d2d06c83)
![1000008568](https://github.com/user-attachments/assets/9dbdd0b4-608a-4c7f-8d05-2cf3b5dec7da)
![1000008569](https://github.com/user-attachments/assets/a773366f-2113-4551-8db6-9dcfbd921591)
