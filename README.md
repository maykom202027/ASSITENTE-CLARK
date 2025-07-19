<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <title>FORTAL INVESTIMENTOS</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
      integrity="sha512-yH05R9QnW+e3yIOMVpDQYONN6ADf3F5hBeaFo4eK7mOfyBjKbOMJ1OZPB6xG4HDqzZCkqew5vVef6Z1kkZz1DA=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <style>
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: Arial, sans-serif;
        color: white;
        background-image: url('https://static.vecteezy.com/ti/vetor-gratis/p3/15187163-fundo-de-site-moderno-futurista-de-conexao-de-mapa-do-mundo-ou-de-pagina-de-capa-para-conceito-de-tecnologia-e-financas-e-empresa-futura-de-educacao-vetor.jpg');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
      }

      header {
        background-color: rgba(0, 0, 0, 0.8);
        padding: 10px 20px;
        display: flex;
        align-items: center;
        justify-content: space-between;
      }

      header img {
        height: 40px;
        border-radius: 50%;
      }

      nav a {
        color: white;
        margin-left: 15px;
        text-decoration: none;
        font-weight: bold;
      }

      .alert-bar {
        background-color: #ff5722;
        text-align: center;
        padding: 10px;
        font-weight: bold;
        animation: slideDown 1s ease;
      }

      @keyframes slideDown {
        from {
          transform: translateY(-100%);
        }
        to {
          transform: translateY(0);
        }
      }

      main {
        flex: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 20px;
      }

      .container {
        background-color: rgba(0, 0, 0, 0.7);
        padding: 30px;
        border-radius: 15px;
        max-width: 700px;
        text-align: center;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.6);
        animation: fadeIn 1.2s ease;
      }

      @keyframes fadeIn {
        from {
          opacity: 0;
          transform: scale(0.95);
        }
        to {
          opacity: 1;
          transform: scale(1);
        }
      }

      h1 {
        margin-bottom: 20px;
      }

      p {
        font-size: 18px;
        margin-bottom: 20px;
      }

      button {
        padding: 12px 24px;
        font-size: 16px;
        background-color: #25d366;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        display: inline-flex;
        align-items: center;
        gap: 8px;
        transition: background-color 0.3s ease;
      }

      button:hover {
        background-color: #128c7e;
      }

      button img {
        height: 20px;
        border-radius: 50%;
      }

      form {
        margin-top: 30px;
        display: flex;
        flex-direction: column;
        gap: 15px;
        text-align: left;
      }

      input,
      textarea {
        padding: 10px;
        border: none;
        border-radius: 5px;
        width: 100%;
        font-size: 16px;
      }

      footer {
        background-color: rgba(0, 0, 0, 0.85);
        text-align: center;
        padding: 15px;
        font-size: 14px;
      }

      .socials i {
        margin: 0 8px;
        color: white;
        font-size: 18px;
      }
    </style>
  </head>
  <body>
    <header>
      <img src="URL_DA_SUA_IMAGEM" alt="Logo Fortal" />
      <nav>
        <a href="#">Início</a>
        <a href="#">Serviços</a>
        <a href="#">Contato</a>
      </nav>
    </header>

    <div class="alert-bar">🎉 Feirão de imóveis e automóveis por tempo limitado!</div>

    <main>
      <div class="container">
        <h1>Olá! Me chame Maycon. Sou seu assistente virtual.</h1>
        <p>
          Estou aqui para agendar seu atendimento. Neste momento, estamos com um
          feirão incrível de imóveis e automóveis! Vamos marcar?
        </p>
        <button onclick="window.location.href='https://wa.me/558592835198?text=Olá%2C+quero+agendar+meu+atendimento'">
          <img src="URL_DA_SUA_IMAGEM" alt="WhatsApp" />
          <i class="fab fa-whatsapp"></i> Agendar pelo WhatsApp
        </button>

        <form onsubmit="sendToWhatsApp(); return false;">
          <h2>Contato Rápido</h2>
          <input type="text" id="nome" placeholder="Seu nome" required />
          <input type="tel" id="telefone" placeholder="Telefone / WhatsApp" required />
          <textarea id="mensagem" placeholder="Mensagem" rows="4" required></textarea>
          <button type="submit"><i class="fas fa-paper-plane"></i> Enviar</button>
        </form>
      </div>
    </main>

    <footer>
      <div class="socials">
        <a href="https://wa.me/558592835198" target="_blank"><i class="fab fa-whatsapp"></i></a>
        <a href="https://instagram.com" target="_blank"><i class="fab fa-instagram"></i></a>
        <a href="https://facebook.com" target="_blank"><i class="fab fa-facebook-f"></i></a>
      </div>
      <p>&copy; 2025 Fortal Investimentos. com Mais de 38 mil cotas contempladas

Mais de R$ 360 milhões em créditos entregues

Atuação nacional com +20 anos de mercado .</p>
    </footer>

    <script>
      function sendToWhatsApp() {
        const nome = document.getElementById("nome").value;
        const telefone = document.getElementById("telefone").value;
        const mensagem = document.getElementById("mensagem").value;

        const texto = `Olá! Me chamo ${nome}, meu telefone é ${telefone}. Mensagem: ${mensagem}`;
        const url = `https://wa.me/558592835198?text=${encodeURIComponent(texto)}`;

        window.open(url, '_blank');
      }
    </script>
  </body>
</html>
