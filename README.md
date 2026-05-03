<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MUU Steak House - Experiencia Carnicería Premium</title>
    <style>
        :root {
            --primary-red: #d32f2f;
            --dark-bg: #111111;
            --card-bg: #1a1a1a;
            --light-text: #ffffff;
            --gold-accent: #d4af37;
            --whatsapp-green: #25d366;
        }

        body {
            font-family: 'Playfair Display', serif, 'Segoe UI', Arial;
            background-color: var(--dark-bg);
            color: var(--light-text);
            margin: 0;
            padding: 0;
            line-height: 1.8;
        }

        /* Banner de Descuento */
        .promo-banner {
            background-color: var(--primary-red);
            color: white;
            padding: 15px 0;
            text-align: center;
            font-weight: bold;
            font-size: 1.4rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            position: relative;
            z-index: 10;
        }

        /* Video Banner Header con Logo */
        .video-header {
            position: relative;
            width: 100%;
            height: 85vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            border-bottom: 6px solid var(--primary-red);
        }

        .video-header iframe {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100vw;
            height: 56.25vw;
            min-height: 85vh;
            min-width: 151vh;
            transform: translate(-50%, -50%);
            pointer-events: none;
        }

        .video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            z-index: 2;
            padding: 20px;
        }

        .logo-header {
            max-width: 250px;
            height: auto;
            margin-bottom: 20px;
            filter: drop-shadow(0 4px 10px rgba(0,0,0,0.8));
        }

        .video-overlay p {
            font-size: 1.6rem;
            max-width: 800px
            
