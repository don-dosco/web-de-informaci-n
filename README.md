<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Viñedos Don Dosco</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
        }

        header {
            background-color: #800000; /* Bordó */
            color: white;
            padding: 20px;
            text-align: center;
        }

        h1 {
            margin: 0;
            font-size: 2.5em;
        }

        nav {
            margin-top: 10px;
        }

        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }

        .container {
            padding: 20px;
            max-width: 800px;
            margin: auto;
        }

        .section {
            margin-bottom: 40px;
        }

        h2 {
            color: #800000; /* Bordó */
            font-size: 2em;
            margin-bottom: 10px;
        }

        .image-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }

        .image-container img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .text {
            font-size: 1.1em;
            line-height: 1.6;
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: #800000; /* Bordó */
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }

        /* Estilo para el formulario de contacto */
        #contactForm {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        #contactForm input,
        #contactForm textarea {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        #contactForm button {
            background-color: #800000; /* Bordó */
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }

        #contactForm button:hover {
            background-color: #600000; /* Un tono más oscuro */
        }

        @media (max-width: 600px) {
            h1 {
                font-size: 2em;
            }

            h2 {
                font-size: 1.5em;
            }

            .text {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Viñedos Don Dosco</h1>
        <nav>
            <a href="#introduccion">Introducción</a>
            <a href="#produccion">Producción</a>
            <a href="#envasado">Envasado</a>
            <a href="#calidad">Control de Calidad</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <div class="container">
        <section id="introduccion" class="section">
            <h2>Introducción</h2>
            <div class="image-container">
                <img src="fo/1.jpeg" alt="Viñedo en la Cordillera de los Andes">
            </div>
            <p class="text">
                Viñedos Don Dosco está ubicado en la hermosa Cordillera de los Andes, donde las condiciones climáticas son ideales para el cultivo de uvas de alta calidad. Nuestra pasión por el vino se refleja en cada botella que producimos, utilizando técnicas tradicionales y modernas para ofrecer un producto excepcional.
            </p>
        </section>

        <section id="produccion" class="section">
            <h2>Proceso de Producción</h2>
            <div class="image-container">
                <img src="fo/1de2.jpeg" alt="Proceso de producción de vino tinto">
                <img src="fo/2de2.jpeg" alt="Proceso de producción de vino tinto">
                <img src="fo/3de2.jpg" alt="Proceso de producción de vino tinto">
            </div>
            <p class="text">
                El proceso de producción comienza con la cosecha manual de uvas, seguida de la fermentación en tanques de acero inoxidable. Cada etapa es supervisada cuidadosamente para garantizar la calidad del vino.
            </p>
        </section>

        <section id="envasado" class="section">
            <h2>Envasado y Distribución</h2>
            <div class="image-container">
                <img src="fo/3.jpg" alt="Envasado de vino en tetrabrik">
            </div>
            <p class="text">
                El vino se envasa en cajas tipo tetrabrik, manteniendo la frescura y calidad del producto. Esta elección de envasado es práctica y sostenible, facilitando su distribución.
            </p>
        </section>

        <section id="calidad" class="section">
            <h2>Control de Calidad</h2>
            <div class="image-container">
                <img src="fo/4.jpg" alt="Laboratorio de control de calidad">
            </div>
            <p class="text">
                En nuestro laboratorio, cada lote de vino es sometido a pruebas rigurosas de calidad. Nos aseguramos de que cada botella cumpla con los estándares más altos.
            </p>
        </section>

        <section id="contacto" class="section">
            <h2>Contacto</h2>
            <div class="image-container">
                <img src="fo/5.jpg" alt="Botella de vino con fondo de viñedos">
            </div>
            <p class="text">
                Para más información, preguntas o pedidos, no dudes en contactarnos a través del siguiente formulario:
            </p>
            <form id="contactForm">
                <input type="text" id="name" placeholder="Tu nombre" required>
                <input type="email" id="email" placeholder="Tu correo" required>
                <textarea id="message" rows="5" placeholder="Tu mensaje" required></textarea>
                <button type="submit">Enviar</button>
            </form>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 Viñedos Don Dosco. Todos los derechos reservados.</p>
    </footer>

    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/emailjs-com@2/dist/email.min.js"></script>
    <script type="text/javascript">
        (function() {
            emailjs.init("TU_USER_ID");  // Debes obtener TU_USER_ID desde tu cuenta en EmailJS
        })();

        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();

            emailjs.send("tu_service_id", "tu_template_id", {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                message: document.getElementById('message').value
            }).then(function(response) {
                alert('Mensaje enviado exitosamente!');
                document.getElementById('contactForm').reset();  // Limpiar el formulario
            }, function(error) {
                alert('Error al enviar el mensaje. Inténtalo nuevamente.');
            });
        });
    </script>
</body>
</html>
