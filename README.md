# WORLD-HISTORY-BY-AL
An explanation of world history that I made for education. 
index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>World History Archive</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  font-family: Georgia, serif;
  background: #f4f1ec;
  color: #2b2b2b;
}
header {
  background: #2c2a26;
  color: #f0e6c8;
  padding: 30px;
  text-align: center;
}
section {
  padding: 30px;
}
h2 {
  border-bottom: 2px solid #bfa76f;
  padding-bottom: 6px;
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 15px;
  margin-top: 20px;
}
.card {
  background: #ffffff;
  padding: 15px;
  border-left: 5px solid #bfa76f;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
.card h3 {
  margin-top: 0;
}
.card small {
  color: #666;
}
footer {
  background: #e0d6b8;
  text-align: center;
  padding: 20px;
  font-size: 14px;
}
</style>
</head>

<body>

<header>
  <h1>World History Archive</h1>
  <p>Empires, Wars, Plagues & Golden Ages</p>
</header>

<section>
  <h2>World War I</h2>
  <div id="ww1" class="grid"></div>
</section>

<section>
  <h2>World War II</h2>
  <div id="ww2" class="grid"></div>
</section>

<section>
  <h2>The Crusades</h2>
  <div id="crusades" class="grid"></div>
</section>

<section>
  <h2>Golden Age of Islam</h2>
  <div id="islamic" class="grid"></div>
</section>

<section>
  <h2>Imperial Courts & Palaces</h2>
  <div id="empires" class="grid"></div>
</section>

<section>
  <h2>Global Plagues & Diseases</h2>
  <div id="plagues" class="grid"></div>
</section>

<footer>
  <p>Static Educational Website • Secure • Lightweight</p>
</footer>

<script>
const ww1 = [
  { name:"Archduke Franz Ferdinand", role:"Austro-Hungarian Heir", desc:"His assassination in 1914 triggered World War I." },
  { name:"Kaiser Wilhelm II", role:"German Emperor", desc:"Militarism and diplomacy escalated European tensions." }
];

const ww2 = [
  { name:"Winston Churchill", role:"British Prime Minister", desc:"Led Britain through World War II with resilience." },
  { name:"Adolf Hitler", role:"Leader of Nazi Germany", desc:"Instigator of World War II and the Holocaust." },
  { name:"Joseph Stalin", role:"Leader of the USSR", desc:"Central figure in the defeat of Nazi Germany." }
];

const crusades = [
  { name:"Saladin (Salah ad-Din)", role:"Muslim Leader", desc:"Recaptured Jerusalem in 1187." },
  { name:"Richard the Lionheart", role:"King of England", desc:"Major Crusader leader during the Third Crusade." }
];

const islamicGoldenAge = [
  { name:"Al-Khwarizmi", role:"Mathematician", desc:"Founder of algebra and algorithms." },
  { name:"Ibn Sina (Avicenna)", role:"Physician", desc:"Author of The Canon of Medicine." },
  { name:"Ibn Al-Haytham", role:"Scientist", desc:"Pioneer of optics and scientific method." }
];

const empires = [
  { name:"Palace of Versailles", role:"France", desc:"Symbol of absolute monarchy." },
  { name:"Topkapi Palace", role:"Ottoman Empire", desc:"Political center of the Ottoman state." }
];

const plagues = [
  { name:"Black Death", role:"14th Century", desc:"Killed nearly one-third of Europe." },
  { name:"Spanish Flu", role:"1918 Pandemic", desc:"One of the deadliest pandemics in history." }
];

function render(data, id) {
  const el = document.getElementById(id)
  data.forEach(item => {
    const card = document.createElement("div")
    card.className = "card"
    card.innerHTML = `
      <h3>${item.name}</h3>
      <small>${item.role}</small>
      <p>${item.desc}</p>
    `
    el.appendChild(card)
  })
}

render(ww1,"ww1")
render(ww2,"ww2")
render(crusades,"crusades")
render(islamicGoldenAge,"islamic")
render(empires,"empires")
render(plagues,"plagues")
</script>

</body>
</html>
