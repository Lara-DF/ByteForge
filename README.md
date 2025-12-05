# ByteForge
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>ByteForge - Inovação e Tecnologia</title>
<style>
  body { 
    margin:0;
    font-family: Arial, sans-serif;
    background:#f2f2f2;
  }

  header {
    background:#111827;
    color:white;
    padding:20px 40px;
    display:flex;
    justify-content:space-between;
    align-items:center;
  }

  header h1 {
    margin:0;
    font-size:28px;
  }

  nav a {
    color:white;
    margin-left:20px;
    text-decoration:none;
    font-weight:bold;
  }

  .hero {
    text-align:center;
    padding:40px;
    background:white;
  }

  .hero h2 {
    font-size:32px;
    margin-bottom:10px;
  }

  .carousel {
    width: 80%;
    max-width:800px;
    height:400px;
    margin:40px auto;
    position: relative;
    overflow: hidden;
    border-radius: 12px;
    background: #ddd;
  }

  .carousel img { 
    width:100%; 
    height:100%;
    object-fit: cover;  
    display:none; 
  }

  .carousel img.active { 
    display:block; 
  }

  button {
    position:absolute; 
    top:50%; 
    transform:translateY(-50%);
    background:#0008; 
    color:white; 
    border:none; 
    padding:10px 15px;
    font-size:24px; 
    cursor:pointer; 
    border-radius:5px;
  }

  #prev { left:10px; }
  #next { right:10px; }

  footer {
    background:#111827;
    color:white;
    padding:20px;
    text-align:center;
    margin-top:40px;
  }
</style>
</head>

<body>

<header>
  <h1>ByteForge</h1>
  <nav>
    <a href="#">Home</a>
    <a href="#">Projetos</a>
    <a href="#">Sobre</a>
    <a href="#">Contato</a>
  </nav>
</header>

<section class="hero">
  <h2>Bem-vindo à ByteForge</h2>
  <p>Inovação, criatividade e tecnologia em um só lugar.</p>
</section>

<div class="carousel">
  <img src="imagem1.jpg" class="active">
  <img src="imagem2.jpg">
  <img src="imagem3.jpg">

  <button id="prev">❮</button>
  <button id="next">❯</button>
</div>

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
