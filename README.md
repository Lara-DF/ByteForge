<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>ByteForge - Inovação e Tecnologia</title>
<style>
  body { margin:0; font-family: Arial, sans-serif; background:#f2f2f2; }
  header { background:#111827; color:white; padding:20px 40px; display:flex; justify-content:space-between; align-items:center; position:sticky; top:0; }
  header h1 { margin:0; font-size:28px; }
  nav a { color:white; margin-left:20px; text-decoration:none; font-weight:bold; }
  section { padding:60px 40px; }
  .hero { text-align:center; background:white; }
  .hero h2 { font-size:32px; margin-bottom:10px; }

  /* CARROSSEL */
  .carousel { width: 80%; max-width:800px; height:400px; margin:40px auto; position: relative; overflow: hidden; border-radius: 12px; background: #ddd; }
  .carousel img { width:100%; height:100%; object-fit: cover; display:none; }
  .carousel img.active { display:block; }
  button { position:absolute; top:50%; transform:translateY(-50%); background:#0008; color:white; border:none; padding:10px 15px; font-size:24px; cursor:pointer; border-radius:5px; }
  #prev { left:10px; } #next { right:10px; }

  /* PROJETOS */
  .projetos-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; }
  .card { background:white; padding:20px; border-radius:10px; box-shadow:0 2px 5px #00000020; }

  /* SOBRE */
  .sobre-box { max-width:700px; margin:auto; background:white; padding:30px; border-radius:10px; box-shadow:0 2px 5px #00000020; }

  /* CONTATO */
  form { max-width:600px; margin:auto; display:flex; flex-direction:column; gap:15px; }
  input, textarea { padding:12px; border-radius:8px; border:1px solid #ccc; }
  button.enviar { background:#111827; color:white; padding:12px; border:none; border-radius:8px; cursor:pointer; font-size:18px; }

  footer { background:#111827; color:white; padding:20px; text-align:center; margin-top:40px; }
</style>
</head>
<body>

<header>
  <h1>ByteForge</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#projetos">Projetos</a>
    <a href="#sobre">Sobre</a>
    <a href="#contato">Contato</a>
  </nav>
</header>

<section id="home" class="hero">
  <h2>Bem-vindo à ByteForge</h2>
  <p>Inovação, criatividade e tecnologia em um só lugar.</p>
</section>

<div class="carousel">
  <img src="imagem1.jpg" class="active">
  <img src="imagem2.jpg">
  <button id="prev">❮</button>
  <button id="next">❯</button>
</div>

<section id="projetos">
  <h2>Projetos</h2>
  <div class="projetos-grid">
    <div class="card"><h3>Projeto 1</h3><p>Descrição do projeto 1...</p></div>
    <div class="card"><h3>Projeto 2</h3><p>Descrição do projeto 2...</p></div>
    <div class="card"><h3>Projeto 3</h3><p>Descrição do projeto 3...</p></div>
  </div>
</section>

<section id="sobre">
  <h2>Sobre a ByteForge</h2>
  <div class="sobre-box">
    <p>A ByteForge é um grupo dedicado a desenvolver soluções digitais criativas e eficientes. Nossa missão é transformar ideias em projetos reais e impactantes.</p>
  </div>
</section>

<section id="contato">
  <h2>Contato</h2>
  <form>
    <input type="text" placeholder="Seu nome">
    <input type="email" placeholder="Seu email">
    <textarea rows="5" placeholder="Sua mensagem"></textarea>
    <button class="enviar">Enviar</button>
  </form>
</section>

<footer>
  © 2025 ByteForge — Desenvolvido por vocês 🚀
</footer>

<script>
  const images = document.querySelectorAll('.carousel img');
  let index = 0;
  document.getElementById('next').onclick = () => {
    images[index].classList.remove('active');
    index = (index + 1) % images.length;
    images[index].classList.add('active');
  };
  document.getElementById('prev').onclick = () => {
    images[index].classList.remove('active');
    index = (index - 1 + images.length) % images.length;
    images[index].classList.add('active');
  };
</script>

</body>
</html>
