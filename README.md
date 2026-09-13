<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aniversário Do Davi - Homem Aranha!</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Bangers&display=swap');
  body { margin:0; font-family:'Bangers', cursive; background:#0f172a; min-height:100vh; display:flex; justify-content:center; align-items:center; overflow:hidden; }

  /* FUNDO COM TEIAS */
  body::before { content:"🕸️"; position:fixed; font-size:200px; top:-20px; left:-20px; opacity:0.3; }
  body::after { content:"🕸️"; position:fixed; font-size:200px; bottom:-20px; right:-20px; opacity:0.3; transform:scaleX(-1); }

  .card { background:white; width:90%; max-width:430px; border-radius:25px; padding:0; overflow:hidden; text-align:center; border:8px solid #dc2626; box-shadow:0 0 0 6px #1d4ed8, 0 20px 60px rgba(0,0,0,0.5); position:relative; z-index:2; }

  .topo { background: linear-gradient(180deg,#dc2626 0%, #991b1b 100%); padding:20px; position:relative; }
  .teia-topo { position:absolute; top:0; left:0; right:0; font-size:30px; letter-spacing:15px; opacity:0.7; }
  .topo h1 { color:white; margin:0; font-size:28px; letter-spacing:2px; text-shadow:3px 3px 0 #1e3a8a; }

  .nome { font-size:85px; color:#1d4ed8; margin:10px 0 0 0; line-height:1; text-shadow: 4px 4px 0 #fbbf24, 7px 7px 0 #dc2626; letter-spacing:3px; animation: balanca 1s infinite alternate; }
  @keyframes balanca { from{transform:rotate(-2deg)} to{transform:rotate(2deg)} }

  .sub { background:#fbbf24; display:inline-block; padding:5px 15px; border-radius:50px; font-size:20px; color:#991b1b; margin-top:5px; }

  .conteudo { padding:25px; }
  .aranha { font-size:70px; animation: pula 0.8s infinite; display:inline-block; }
  @keyframes pula { 0%,100%{transform:translateY(0) rotate(0)} 50%{transform:translateY(-12px) rotate(10deg)} }

  .info { background:#eff6ff; border:3px dashed #1d4ed8; border-radius:20px; padding:15px; margin-top:15px; text-align:left; font-family: Arial, sans-serif; font-weight:bold; }
  .info p { margin:10px 0; font-size:18px; color:#1e293b; }
  .info span { color:#dc2626; }

  .btn { display:block; width:100%; background:#dc2626; color:white; padding:16px; border-radius:15px; text-decoration:none; font-size:26px; margin-top:18px; letter-spacing:2px; box-shadow:0 6px 0 #991b1b; transition:0.1s; }
  .btn:active { transform:translateY(6px); box-shadow:0 0 0 #991b1b; }

  /* TEIAS CAINDO */
  .teia { position:fixed; top:-50px; animation: cair linear infinite; z-index:1; pointer-events:none; }
  @keyframes cair { to { transform:translateY(110vh) rotate(360deg); } }
</style>
</head>
<body>

<div class="card">
  <div class="topo">
    <div class="teia-topo">🕸️🕸️🕸️</div>
    <h1>CONVITE SUPER ESPECIAL</h1>
  </div>

  <div class="conteudo">
    <div class="aranha">🕷️</div>
    <div class="nome">DAVI</div>
    <div class="sub">VAI FAZER ANIVERSÁRIO!</div>

    <div style="font-size:40px; margin:10px 0;">🕸️💥🕸️</div>

    <div class="info">
      <p>🕷️ <span>Idade:</span> 1 Aninhos</p>
      <p>📅 <span>Quando:</span> 28 de Fvereiro - 13h</p>
      <p>📍 <span>Onde:</span> Salão Kids Fest</p>
      <p>🕸️ <span>Traje:</span> Venha de Homem-Aranha!</p>
    </div>

    <a class="btn" href="https://wa.me/5511999999999?text=Confirmo%20presença%20no%20aniversário%20do%20Davi%20Homem-Aranha!🕷️" target="_blank">CONFIRMAR 🕸️</a>
    <p style="font-family:Arial; font-size:11px; color:#94a3b8; margin-top:8px;">Clique no botão para confirmar no Zap da mamãe</p>
  </div>
</div>

<script>
// CHUVA DE TEIAS E ARANHAS
let emojis = ['🕸️','🕷️','💥','⭐'];
for(let i=0;i<35;i++){
  let el = document.createElement('div');
  el.className='teia';
  el.innerHTML=emojis[Math.floor(Math.random()*emojis.length)];
  el.style.left=Math.random()*100+'vw';
  el.style.fontSize=(15+Math.random()*25)+'px';
  el.style.animationDuration=(3+Math.random()*4)+'s';
  el.style.animationDelay=Math.random()*5+'s';
  document.body.appendChild(el);
}
</script>
</body>
</html>
