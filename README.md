<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ableads</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #6a0dad;
      --text: #000000;
      --bg: #ffffff;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      font-family: 'Inter', sans-serif;
      background-color: var(--bg);
      color: var(--text);
      height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 40px 20px;
      text-align: center;
    }

    header {
      font-weight: 700;
      font-size: 1.5rem;
      margin-bottom: 2rem;
    }

    h1 {
      font-size: 2.75rem;
      font-weight: 700;
      margin-bottom: 1.2rem;
      max-width: 700px;
    }

    p {
      font-size: 1.2rem;
      font-weight: 400;
      color: #333;
      max-width: 600px;
      margin-bottom: 2.5rem;
      line-height: 1.6;
    }

    .cta-button {
      background-color: var(--primary);
      color: #fff;
      border: none;
      padding: 1rem 2.5rem;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .cta-button:hover {
      background-color: #550d99;
    }

    .modal {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      background-color: rgba(0,0,0,0.6);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .modal-content {
      position: relative;
      width: 90%;
      max-width: 800px;
      height: 90%;
      background: #fff;
      border-radius: 12px;
      overflow: hidden;
    }

    .close {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 2rem;
      font-weight: 600;
      color: #333;
      cursor: pointer;
      z-index: 10;
    }

    iframe {
      width: 100%;
      height: 100%;
      border: none;
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 2rem;
      }
      p {
        font-size: 1rem;
      }
      .cta-button {
        padding: 0.9rem 2rem;
        font-size: 0.95rem;
      }
    }
  </style>
</head>
<body>

  <header>Ableads</header>

  <h1>Consigue clientes todos los días con Meta Ads.</h1>
  <p>Hacemos campañas en Meta Ads para negocios que venden servicios de ticket alto. Si no conseguimos resultados, no cobramos.</p>

  <button class="cta-button" onclick="document.getElementById('modal').style.display='flex'">
    Agenda una llamada
  </button>

  <div id="modal" class="modal" onclick="event.target === this && (this.style.display='none')">
    <div class="modal-content">
      <div class="close" onclick="document.getElementById('modal').style.display='none'">×</div>
      <iframe src="https://calendly.com/ableads/30min"></iframe>
    </div>
  </div>

</body>
</html>
