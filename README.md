<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>⛔SE PUEDE TODO XXX⛔</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    body {
      background-color: #23232b;
      color: #e0e0e0;
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
    }
    header {
      display: flex;
      align-items: center;
      background-color: #2c3e50;
      padding: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.4);
    }
    header img {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      margin-right: 12px;
    }
    .group-name {
      font-size: 17px;
      font-weight: bold;
    }
    .members-info {
      font-size: 13px;
      color: #ccc;
    }
    .chat-area {
      display: none;
      flex-direction: column;
      padding: 15px;
      height: calc(100vh - 160px);
      overflow-y: auto;
    }
    .user {
      display: flex;
      align-items: flex-start;
      margin-bottom: 14px;
    }
    .avatar {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      margin-right: 10px;
    }
    .bubble {
      background-color: #2e3a48;
      padding: 10px 14px;
      border-radius: 12px;
      max-width: 78%;
      font-size: 13px;
      line-height: 1.4;
      word-break: break-word;
      box-shadow: 0 1px 3px rgba(0,0,0,0.2);
    }
    .bubble img {
      max-width: 100%;
      border-radius: 10px;
      margin-top: 8px;
    }
    .footer {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: #1f1f26;
      text-align: center;
      padding: 10px 15px;
    }
    .share-btn, .join-btn {
      background: #00a884;
      border: none;
      padding: 10px 20px;
      border-radius: 30px;
      font-size: 14px;
      color: white;
      cursor: pointer;
      margin-top: 8px;
    }
    .join-btn {
      background: #28a745;
      position: relative;
      animation: pulse 2s infinite;
    }
    .join-btn:before {
      content: '😈';
      position: absolute;
      top: -8px;
      right: -10px;
      font-size: 18px;
      animation: float 1.5s infinite;
    }
    #lockedMsg {
      color: #ff4b4b;
      font-weight: bold;
    }
    #counter {
      color: #ffffff;
      margin-top: 5px;
      font-size: 13px;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
      100% { transform: translateY(0); }
    }
    @keyframes pulse {
      0% { box-shadow: 0 0 0 0 rgba(40,167,69, 0.4); }
      70% { box-shadow: 0 0 0 10px rgba(40,167,69, 0); }
      100% { box-shadow: 0 0 0 0 rgba(40,167,69, 0); }
    }
  </style>
</head>
<body>
  <header>
    <img src="https://imageshack.com/i/pnxFDE3hj" alt="Grupo">
    <div>
      <div class="group-name">⛔SE PUEDE TODO XXX⛔</div>
      <div class="members-info"><span id="membersCount">180,000</span> miembros, 3,000 en línea</div>
    </div>
  </header>

  <div class="chat-area" id="chatArea">
    <div class="user">
      <img class="avatar" src="https://imageshack.com/i/poyZNOzgj" alt="Laura">
      <div class="bubble"><strong>🥵Laura Hot😈:</strong> Este grupo es el mejor 🔥</div>
    </div>
    <div class="user">
      <img class="avatar" src="https://imageshack.com/i/pm0n7zg4j" alt="Dimitri">
      <div class="bubble"><strong>Dimitri:</strong> Sí funciona 100% 😎</div>
    </div>
    <div class="user">
      <img class="avatar" src="https://imageshack.com/i/pooBesOfj" alt="Verónica">
      <div class="bubble"><strong>Verónica 💜🇨🇴:</strong> ¡Gracias por aceptarme! 😍</div>
    </div>
    <div class="user">
      <img class="avatar" src="https://imageshack.com/i/pn3HqqM4j" alt="Marco">
      <div class="bubble"><strong>Marco:</strong> Miren esta foto 🔥<br><img src="https://imageshack.com/i/pnOY7cT8j" alt="Aporte"></div>
    </div>
    <div class="user">
      <img class="avatar" src="https://imageshack.com/i/poQzsm34j" alt="Eliza">
      <div class="bubble"><strong>Eliza:</strong> Mi aporte 😈<br><img src="https://imageshack.com/i/poYsPz8Pj" alt="Mi aporte"></div>
    </div>
    <div class="user">
      <img class="avatar" src="https://randomuser.me/api/portraits/women/21.jpg" alt="Sandra">
      <div class="bubble"><strong>Sandra🔥:</strong> ¿Alguien más pudo desbloquear?</div>
    </div>
    <div class="user">
      <img class="avatar" src="https://randomuser.me/api/portraits/men/15.jpg" alt="Andrés">
      <div class="bubble"><strong>Andrés🔥:</strong> Video nuevo aquí 🔥<br>
        <img src="https://imageshack.com/i/pmHsQ23rj" alt="video" style="position:relative;">
        <div style="font-size:12px; color:#ccc; margin-top:4px;"><i class="fa fa-download"></i> 25.4 MB - 1:28</div>
      </div>
    </div>
  </div>

  <div class="footer">
    <div id="lockedMsg">Chat bloqueado - debes compartir 3 veces para desbloquear</div>
    <div id="counter">Compartido: <span id="sharedCount">0</span>/3</div>
    <button id="shareBtn" class="share-btn">Compartir en Telegram</button>
    <button id="joinBtn" class="join-btn" style="display: none;" onclick="window.location.href='https://t.me/addlist/Pk5dafooIwE0NDAx'">Unirme al grupo</button>
  </div>

  <script>
    let shared = 0;
    const shareBtn = document.getElementById('shareBtn');
    const joinBtn = document.getElementById('joinBtn');
    const chatArea = document.getElementById('chatArea');
    const membersEl = document.getElementById('membersCount');
    const counter = document.getElementById('sharedCount');
    let members = 180000;

    shareBtn.onclick = () => {
      shared++;
      window.open("https://t.me/share/url?url=🔞 Chats Ocultos Por Telegram no te quedes sin ver👉 http://t.me/TPacksBot/Chat", '_blank');
      counter.textContent = shared;
      if (shared >= 3) {
        document.getElementById('lockedMsg').style.display = 'none';
        document.getElementById('counter').style.display = 'none';
        shareBtn.style.display = 'none';
        joinBtn.style.display = 'inline-block';
        chatArea.style.display = 'flex';
      }
    };

    setInterval(() => {
      members += 5;
      membersEl.textContent = members.toLocaleString();
    }, 3000);
  </script>
</body>
</html>
