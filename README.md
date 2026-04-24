<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galería Dinámica Pro</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #1a1a1a;
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 0;
            padding: 20px;
        }

        h1 { margin-bottom: 30px; color: #f0f0f0; }

        /* Contenedor de los 3 cuadros */
        .gallery-container {
            display: flex;
            gap: 20px;
            width: 90%;
            max-width: 1000px;
            justify-content: center;
        }

        .photo-box {
            flex: 1;
            height: 300px;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.5);
            border: 2px solid #333;
            background: #000;
            transition: all 0.5s ease-in-out;
        }

        .photo-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.5s ease;
        }

        /* Estilo para los botones de control */
        .controls { margin-top: 30px; }
        button {
            padding: 10px 20px;
            cursor: pointer;
            background: #e67e22;
            border: none;
            color: white;
            border-radius: 5px;
            font-weight: bold;
            transition: 0.3s;
        }
        button:hover { background: #d35400; }
    </style>
</head>
<body>

    <h1>Catálogo en Movimiento</h1>

    <div class="gallery-container">
        <div class="photo-box" id="box1"></div>
        <div class="photo-box" id="box2"></div>
        <div class="photo-box" id="box3"></div>
    </div>

    <div class="controls">
        <button onclick="rotateGallery()">Rotar Manualmente</button>
    </div>

    <script>
        // Array con los enlaces directos de tus fotos de ImgBB
        const images = [
            "https://i.ibb.co/9mWr3ZkT/IMG-20260424-WA0063.jpg",
            "https://i.ibb.co/G4yT7zJS/IMG-20260424-WA0062.jpg",
            "https://i.ibb.co/0R8JGDS3/IMG-20260424-WA0061.jpg",
            "https://i.ibb.co/Wj1dpJc/IMG-20260424-WA0060.jpg",
            "https://i.ibb.co/bRDv80QL/IMG-20260424-WA0058.jpg",
            "https://i.ibb.co/nMXG041N/IMG-20260424-WA0059.jpg",
            "https://i.ibb.co/Rp9zWcHT/IMG-20260424-WA0054.jpg",
            "https://i.ibb.co/chF3j7Gk/IMG-20260424-WA0057.jpg",
            "https://i.ibb.co/LdBY1RVB/IMG-20260424-WA0053.jpg",
            "https://i.ibb.co/99xWhPdw/IMG-20260424-WA0047.jpg"
        ];

        let currentIndex = 0;

        function updateGallery() {
            // Calculamos los índices de las 3 fotos a mostrar
            const idx1 = currentIndex % images.length;
            const idx2 = (currentIndex + 1) % images.length;
            const idx3 = (currentIndex + 2) % images.length;

            // Insertamos las imágenes en los cuadros
            document.getElementById('box1').innerHTML = `<img src="${images[idx1]}">`;
            document.getElementById('box2').innerHTML = `<img src="${images[idx2]}">`;
            document.getElementById('box3').innerHTML = `<img src="${images[idx3]}">`;
        }

        function rotateGallery() {
            currentIndex++;
            updateGallery();
        }

        // Iniciar la galería
        updateGallery();

        // Configurar rotación automática cada 3 segundos
        setInterval(rotateGallery, 3000);
    </script>
</body>
</html>
