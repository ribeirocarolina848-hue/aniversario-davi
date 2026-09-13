<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aniversário do Davi!</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@700&display=swap');
  body { margin:0; font-family:'Fredoka', sans-serif; background: linear-gradient(135deg,#a855f7,#ec4899,#f59e0b); min-height:100vh; display:flex; justify-content:center; align-items:center; overflow:hidden; }
  .card { background:white; width:90%; max-width:420px; border-radius:30px; padding:30px; text-align:center; position:relative; box-shadow:0 20px 60px rgba(0,0,0,0.3); animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{transform:scale(1)} 50%{transform:scale(1.03)} }
  h1 { color:#7c3aed; font-size:22px; margin:0; }
  .nome { font-size:70px; background: linear-gradient(90deg,#06b6d4,#f43f5e,#f59e0b,#22c55e); -webkit-background-clip:text; -webkit-text-fill-color:transparent; margin:10px 0; line-height:1; animation: rainbow 3s linear infinite; background-size:400%; }
  @keyframes rainbow { to { background-position:400% } }
  .sub { font-size:20px; color:#334155; }
  .bolo { font-size:80px; animation: bounce 1s infinite; }
  @keyframes bounce { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-10px)} }
  .info { background:#f1f5f9; border-radius:20px; padding:15px; margin-top:20px; color:#1e293b; text-align:left; }
  .info p { margin:8px 0; font-size:18px; }
  .btn { display:block; width:100%; background:#22c55e; color:white; padding:15px; border-radius:15px; text-decoration:none; font-size:20px; margin-top:20px; }
  .balao { position:absolute; font-size:30px; animation: subir 4s linear infinite; }
  @keyframes subir { 0%{transform:translateY(100vh)} 100%{transform:translateY(-100vh)} }
  .confete { position:fixed; width:10px; height:10px; top:-10px; animation: cair 3s linear infinite; }
  @keyframes cair { to { transform:translateY(110vh) rotate(720deg); } }
</style>
</head>
<body>

<div class="card">
  <div class="bolo">🎂</div>
  <h1>CONVITE DE ANIVERSÁRIO</h1>
  <div class="nome">DAVI</div>
  <div class="sub">VEM COMEMORAR COMIGO!</div>

  <div class="info">
    <p>📅 <b>Dia 28 de fevereiro - 14h</b></p>
    <p>📍 Salão Kids Fest - Rua da Alegria, 123</p>
    <p>🎈 Traga muita animação!</p>
  </div>

  <a class="btn" href="https://wa.me/5511999999999?text=Confirmo%20presença%20no%20aniversário%20do%20Davi!" target="_blank">✅ CONFIRMAR PRESENÇA</a>
  <p style="font-size:12px; color:#94a3b8; margin-top:10px;">Clique para confirmar no WhatsApp</p>
</div>

<script>
// BALÕES VOANDO
for(let i=0;i<15;i++){
  let b = document.createElement('div');
  b.className='balao';
  b.innerHTML='🎈';
  b.style.left=Math.random()*100+'vw';
  b.style.animationDelay=Math.random()*4+'s';
  b.style.fontSize=(20+Math.random()*30)+'px';
  document.body.appendChild(b);
}
// CONFETE
let cores=['#f43f5e','#22c55e','#3b82f6','#f59e0b','#a855f7'];
for(let i=0;i<50;i++){
  let c = document.createElement('div');
  c.className='confete';
  c.style.left=Math.random()*100+'vw';
  c.style.background=cores[Math.floor(Math.random()*cores.length)];
  c.style.animationDelay=Math.random()*3+'s';
  c.style.animationDuration=(2+Math.random()*3)+'s';
  document.body.appendChild(c);
}
</script>
</body>
</html>
