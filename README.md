
<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MOZ AJUDA</title>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f3f7f4;
  color: #173c2b;
}

header {
  background: #075b37;
  color: white;
  padding: 25px;
  text-align: center;
}

nav {
  background: #064529;
  padding: 15px;
  text-align: center;
}

nav a {
  color: white;
  text-decoration: none;
  margin: 8px;
}

main {
  padding: 20px;
  max-width: 800px;
  margin: auto;
}

.hero, .card, .calculadora {
  background: white;
  padding: 20px;
  border-radius: 15px;
  margin-bottom: 18px;
}

.hero { text-align: center; }

.cards {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.card { text-align: center; }

.card h2 { font-size: 30px; }

.calculadora input {
  width: 100%;
  padding: 13px;
  margin: 8px 0 15px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

button {
  width: 100%;
  padding: 14px;
  background: #087b43;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
}

#resultado {
  font-weight: bold;
  font-size: 19px;
}

footer {
  background: #064529;
  color: white;
  text-align: center;
  padding: 20px;
}
</style>
</head>

<body>

<header>
<h1>🇲🇿 MOZ AJUDA</h1>
<p>Ajudamos Moçambique a crescer!</p>
</header>

<nav>
<a href="#inicio">Início</a>
<a href="#servicos">Serviços</a>
<a href="#calculadora">Calculadora</a>
</nav>

<main>

<section class="hero" id="inicio">
<h2>Bem-vindo ao MOZ AJUDA!</h2>
<p>O teu espaço gratuito de educação,
oportunidades e ferramentas digitais.</p>
</section>

<h2 id="servicos">Os nossos serviços</h2>

<div class="cards">

<div class="card">
<h2>📚</h2>
<h3>Educação</h3>
<p>Aprende e prepara-te para exames.</p>
</div>

<div class="card">
<h2>💼</h2>
<h3>Emprego</h3>
<p>Descobre oportunidades e bolsas.</p>
</div>

<div class="card">
<h2>🧮</h2>
<h3>Calculadoras</h3>
<p>Calcula as tuas contas.</p>
</div>

<div class="card">
<h2>📱</h2>
<h3>Serviços digitais</h3>
<p>Ferramentas para o teu dia.</p>
</div>

</div>

<section class="calculadora" id="calculadora">

<h2>🧮 Calculadora de Lucro</h2>

<label>Preço de compra (MT)</label>
<input type="number" id="compra"
placeholder="Ex: 100" min="0">

<label>Preço de venda (MT)</label>
<input type="number" id="venda"
placeholder="Ex: 150" min="0">

<button onclick="calcularLucro()">
Calcular lucro
</button>

<p id="resultado">O resultado aparecerá aqui.</p>

</section>

</main>

<footer>
<h3>MOZ AJUDA 🇲🇿</h3>
<p>Feito para Moçambique.</p>
</footer>

<script>
function calcularLucro() {

let compra = document.getElementById("compra").value;
let venda = document.getElementById("venda").value;

let resultado = document.getElementById("resultado");

if (compra === "" || venda === "" ||
Number(compra) < 0 || Number(venda) < 0) {
resultado.innerText = "Introduza valores válidos!";
return;
}

let lucro = Number(venda) - Number(compra);

resultado.innerText =
"Resultado: " + lucro.toFixed(2) + " MT";
}
</script>

</body>
</html>
