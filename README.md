<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para a Laís, com carinho</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;1,9..144,500;1,9..144,600&family=Caveat:wght@500;600;700&family=Work+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#FAF6EE;
    --paper-2:#F2EADC;
    --ink:#3A2C36;
    --ink-soft:#6E5D67;
    --rose:#C67B87;
    --rose-deep:#A85C6C;
    --sage:#7E9680;
    --sage-deep:#5F7862;
    --gold:#CFA045;
    --line:#E3D6C5;
    --shadow: 0 8px 24px rgba(58,44,54,0.08);
  }

  *{box-sizing:border-box;}

  body{
    margin:0;
    background:
      radial-gradient(ellipse at top left, rgba(198,123,135,0.07), transparent 45%),
      radial-gradient(ellipse at bottom right, rgba(126,150,128,0.07), transparent 45%),
      var(--paper);
    color:var(--ink);
    font-family:'Work Sans', sans-serif;
    min-height:100vh;
    padding:32px 16px 80px;
    -webkit-font-smoothing:antialiased;
  }

  .wrap{
    max-width:640px;
    margin:0 auto;
  }

  /* ---------- HEADER ---------- */
  header.top{
    text-align:center;
    margin-bottom:28px;
  }
  .eyebrow{
    font-family:'Caveat', cursive;
    font-size:1.35rem;
    color:var(--rose-deep);
    margin:0 0 2px;
    transform:rotate(-1.5deg);
    display:inline-block;
  }
  h1.title{
    font-family:'Fraunces', serif;
    font-style:italic;
    font-weight:600;
    font-size:clamp(1.9rem, 6vw, 2.6rem);
    margin:0 0 6px;
    color:var(--ink);
  }
  .subtitle{
    font-size:0.92rem;
    color:var(--ink-soft);
    margin:0;
  }

  /* ---------- DAY TABS ---------- */
  .tabs{
    display:flex;
    gap:6px;
    overflow-x:auto;
    padding:6px 2px 14px;
    margin-bottom:6px;
    scrollbar-width:thin;
  }
  .tab{
    flex:0 0 auto;
    font-family:'Work Sans', sans-serif;
    font-weight:600;
    font-size:0.82rem;
    padding:9px 14px;
    border-radius:999px;
    border:1px solid var(--line);
    background:#fff;
    color:var(--ink-soft);
    cursor:pointer;
    transition:all .2s ease;
    white-space:nowrap;
    position:relative;
  }
  .tab:hover{ border-color:var(--rose); color:var(--rose-deep); }
  .tab.active{
    background:var(--ink);
    border-color:var(--ink);
    color:var(--paper);
  }
  .tab .dot{
    display:inline-block;
    width:6px;height:6px;border-radius:50%;
    background:var(--sage);
    margin-left:6px;
    vertical-align:middle;
  }
  .tab.active .dot{ background:var(--gold); }

  /* ---------- PROTEIN BADGE ---------- */
  .meta-row{
    display:flex;
    justify-content:center;
    margin:6px 0 22px;
  }
  .protein-pill{
    display:inline-flex;
    align-items:center;
    gap:6px;
    background:var(--paper-2);
    border:1px solid var(--line);
    padding:7px 14px;
    border-radius:999px;
    font-size:0.78rem;
    color:var(--ink-soft);
  }
  .protein-pill b{ color:var(--ink); font-weight:600; }

  /* ---------- PROGRESS CARD ---------- */
  .progress-card{
    background:#fff;
    border:1px solid var(--line);
    border-radius:20px;
    padding:22px 22px 20px;
    box-shadow:var(--shadow);
    margin-bottom:18px;
  }
  .progress-top{
    display:flex;
    justify-content:space-between;
    align-items:baseline;
    margin-bottom:10px;
  }
  .progress-label{
    font-size:0.85rem;
    color:var(--ink-soft);
    font-weight:500;
  }
  .progress-count{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.05rem;
    color:var(--ink);
  }
  .progress-pct{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.9rem;
    color:var(--rose-deep);
  }
  .bar-track{
    width:100%;
    height:14px;
    background:var(--paper-2);
    border-radius:999px;
    overflow:hidden;
    position:relative;
    border:1px solid var(--line);
  }
  .bar-fill{
    height:100%;
    border-radius:999px;
    background:linear-gradient(90deg, var(--sage), var(--sage-deep));
    width:0%;
    transition:width .5s cubic-bezier(.4,0,.2,1);
  }
  .bar-fill.full{
    background:linear-gradient(90deg, var(--gold), #E0B360);
  }

  /* ---------- MESSAGE NOTE ---------- */
  .note{
    font-family:'Caveat', cursive;
    font-size:1.5rem;
    line-height:1.35;
    background:#fff;
    border:1px solid var(--line);
    border-radius:4px 16px 16px 16px;
    padding:16px 20px;
    color:var(--rose-deep);
    box-shadow:var(--shadow);
    transform:rotate(-0.6deg);
    margin-bottom:24px;
    position:relative;
  }
  .note::before{
    content:'';
    position:absolute;
    top:-9px; left:26px;
    width:46px; height:16px;
    background:rgba(207,160,69,0.35);
    transform:rotate(-3deg);
    border-radius:2px;
  }

  /* ---------- MEAL CARDS ---------- */
  .meals{
    display:flex;
    flex-direction:column;
    gap:12px;
  }
  .meal{
    background:#fff;
    border:1px solid var(--line);
    border-radius:16px;
    padding:16px 16px 16px 14px;
    display:flex;
    gap:14px;
    align-items:flex-start;
    transition:border-color .2s ease, box-shadow .2s ease, opacity .2s ease;
  }
  .meal.done{
    border-color:var(--sage);
    background:linear-gradient(180deg, rgba(126,150,128,0.06), rgba(126,150,128,0.02));
  }
  .check-btn{
    flex:0 0 auto;
    width:34px; height:34px;
    border-radius:50%;
    border:2px solid var(--line);
    background:#fff;
    cursor:pointer;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:1.05rem;
    color:transparent;
    transition:all .25s cubic-bezier(.4,0,.2,1);
    margin-top:2px;
  }
  .check-btn:hover{ border-color:var(--rose); transform:scale(1.06); }
  .meal.done .check-btn{
    background:var(--sage);
    border-color:var(--sage);
    color:#fff;
    transform:scale(1.0);
  }
  .meal-body{ flex:1; min-width:0; }
  .meal-top{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:8px;
    margin-bottom:4px;
  }
  .meal-name{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.05rem;
    color:var(--ink);
    display:flex;
    align-items:center;
    gap:8px;
  }
  .meal-icon{ font-size:1.1rem; }
  .meal-protein{
    font-size:0.72rem;
    font-weight:600;
    color:var(--sage-deep);
    background:rgba(126,150,128,0.12);
    padding:3px 9px;
    border-radius:999px;
    white-space:nowrap;
  }
  .meal-foods{
    margin:0;
    padding:0;
    list-style:none;
    font-size:0.87rem;
    color:var(--ink-soft);
    line-height:1.65;
  }
  .meal-foods li::before{
    content:'· ';
    color:var(--rose);
    font-weight:700;
  }
  .meal.done .meal-name{ color:var(--sage-deep); }

  /* ---------- WEEK SUMMARY ---------- */
  .week-card{
    margin-top:26px;
    background:var(--paper-2);
    border:1px solid var(--line);
    border-radius:18px;
    padding:18px 20px;
  }
  .week-title{
    font-family:'Fraunces', serif;
    font-style:italic;
    font-size:1.05rem;
    margin:0 0 10px;
    color:var(--ink);
  }
  .week-dots{
    display:flex;
    justify-content:space-between;
    margin-bottom:10px;
  }
  .week-dot{
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:6px;
    font-size:0.68rem;
    color:var(--ink-soft);
  }
  .week-dot .circle{
    width:26px; height:26px;
    border-radius:50%;
    border:2px solid var(--line);
    background:#fff;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:0.65rem;
    font-weight:700;
    color:var(--ink-soft);
  }
  .week-dot.complete .circle{
    background:var(--gold);
    border-color:var(--gold);
    color:#fff;
  }
  .week-dot.partial .circle{
    background:rgba(126,150,128,0.25);
    border-color:var(--sage);
    color:var(--sage-deep);
  }
  .week-summary-text{
    font-size:0.8rem;
    color:var(--ink-soft);
    text-align:center;
  }
  .week-summary-text b{ color:var(--ink); }

  /* ---------- SUBSTITUTIONS ---------- */
  .subs{
    margin-top:16px;
  }
  .subs summary{
    cursor:pointer;
    font-size:0.82rem;
    color:var(--ink-soft);
    font-weight:600;
    padding:6px 0;
  }
  .subs-grid{
    display:grid;
    grid-template-columns:1fr;
    gap:6px;
    margin-top:8px;
    font-size:0.8rem;
    color:var(--ink-soft);
  }
  .subs-grid .cat{ font-weight:700; color:var(--ink); margin-top:6px; }

  /* ---------- CELEBRATION OVERLAY ---------- */
  .celebrate{
    position:fixed;
    inset:0;
    background:rgba(58,44,54,0.55);
    display:none;
    align-items:center;
    justify-content:center;
    z-index:50;
    padding:20px;
  }
  .celebrate.show{ display:flex; }
  .celebrate-card{
    background:var(--paper);
    border-radius:22px;
    padding:36px 30px;
    max-width:380px;
    text-align:center;
    box-shadow:0 20px 60px rgba(0,0,0,0.3);
    position:relative;
    overflow:hidden;
  }
  .celebrate-emoji{ font-size:2.6rem; margin-bottom:8px; }
  .celebrate-title{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-style:italic;
    font-size:1.5rem;
    color:var(--rose-deep);
    margin:0 0 10px;
  }
  .celebrate-msg{
    font-family:'Caveat', cursive;
    font-size:1.4rem;
    color:var(--ink);
    margin:0 0 20px;
    line-height:1.3;
  }
  .celebrate-close{
    background:var(--ink);
    color:var(--paper);
    border:none;
    padding:10px 22px;
    border-radius:999px;
    font-family:'Work Sans', sans-serif;
    font-weight:600;
    font-size:0.85rem;
    cursor:pointer;
  }
  .heart{
    position:absolute;
    top:-20px;
    font-size:1.2rem;
    animation:fall linear forwards;
    opacity:0.85;
  }
  @keyframes fall{
    to{ transform:translateY(340px) rotate(180deg); opacity:0; }
  }

  footer.credit{
    text-align:center;
    margin-top:34px;
    font-family:'Caveat', cursive;
    font-size:1.1rem;
    color:var(--ink-soft);
  }

  @media (prefers-reduced-motion: reduce){
    .bar-fill, .meal, .check-btn, .heart{ transition:none !important; animation:none !important; }
  }
</style>
</head>
<body>

<div class="wrap">

  <header class="top">
    <p class="eyebrow">feito especialmente para você</p>
    <h1 class="title">Oi, minha farma ❤️</h1>
    <p class="subtitle">Seu acompanhamento da semana — vai no seu ritmo.</p>
  </header>

  <nav class="tabs" id="tabs"></nav>

  <div class="meta-row">
    <span class="protein-pill">🍳 Meta do dia: <b>~85g</b> de proteína — não precisa ser exato, viu?</span>
  </div>

  <section class="progress-card">
    <div class="progress-top">
      <div>
        <div class="progress-label" id="dayLabel">Segunda-feira</div>
        <div class="progress-count" id="countLabel">0 de 4 refeições concluídas</div>
      </div>
      <div class="progress-pct" id="pctLabel">0%</div>
    </div>
    <div class="bar-track"><div class="bar-fill" id="barFill"></div></div>
  </section>

  <div class="note" id="noteMsg">Vamos, minha farma ❤️</div>

  <section class="meals" id="meals"></section>

  <section class="week-card">
    <p class="week-title">Semana da Laís</p>
    <div class="week-dots" id="weekDots"></div>
    <p class="week-summary-text" id="weekSummary">0 de 28 refeições essa semana</p>
  </section>

  <details class="subs">
    <summary>Trocas permitidas, se precisar variar</summary>
    <div class="subs-grid">
      <div class="cat">Proteínas</div>
      <div>80g frango ↔ 80g carne moída · 80g carne ↔ peixe · frango desfiado ↔ carne moída · ovos + queijo ↔ frango/carne</div>
      <div class="cat">Carboidratos</div>
      <div>arroz ↔ macarrão · arroz ↔ batata · arroz ↔ mandioca · pão ↔ tapioca</div>
      <div class="cat">Frutas</div>
      <div>banana ↔ mamão · banana ↔ manga · laranja ↔ maçã · uva ↔ outras frutas</div>
    </div>
  </details>

  <footer class="credit">
    com carinho, torcendo sempre por você.<br>
    <span style="font-family:'Work Sans',sans-serif;font-size:.68rem;opacity:.65;">
      seu progresso é salvo automaticamente neste dispositivo.
    </span>
  </footer>

</div>

<div class="celebrate" id="celebrateOverlay">
  <div class="celebrate-card" id="celebrateCard">
    <div class="celebrate-emoji">❤️</div>
    <p class="celebrate-title">Você conseguiu, minha farma!</p>
    <p class="celebrate-msg" id="celebrateMsg">4 de 4! Missão cumprida. Tenho muito orgulho de você.</p>
    <button class="celebrate-close" onclick="closeCelebration()">Fechar</button>
  </div>
</div>

<script>
/* ================= DADOS DO PLANO (equivalentes ao XML) ================= */
const PLANO = [
  { id:"segunda", nome:"Segunda-feira", proteinaDia:"~85 g", refeicoes:[
    { id:"segunda-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["2 pães","2 ovos mexidos","1 fatia de queijo","banana"] },
    { id:"segunda-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["4-5 colheres de arroz","½-1 concha de feijão","80g de frango","salada","azeite","laranja"] },
    { id:"segunda-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["1 pão","2 ovos","1 fatia de queijo","banana"] },
    { id:"segunda-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["arroz","feijão","80g de carne moída","cenoura e tomate","fruta"] }
  ]},
  { id:"terca", nome:"Terça-feira", proteinaDia:"~85 g", refeicoes:[
    { id:"terca-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["2 pães","2 ovos","1 fatia de queijo","mamão"] },
    { id:"terca-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["arroz","feijão","80g de carne bovina","salada","azeite","banana"] },
    { id:"terca-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["tapioca média","2 ovos","1 fatia de queijo","maçã"] },
    { id:"terca-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["arroz","feijão","80g de frango desfiado","legumes","fruta"] }
  ]},
  { id:"quarta", nome:"Quarta-feira", proteinaDia:"~85-90 g", refeicoes:[
    { id:"quarta-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["2 fatias de pão","2 ovos mexidos","1 fatia de queijo","banana"] },
    { id:"quarta-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["arroz","feijão","80g de frango assado","salada","azeite","manga"] },
    { id:"quarta-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["1 pão","50g de frango desfiado","1 fatia de queijo","fruta"] },
    { id:"quarta-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["macarrão","80g de carne moída","legumes/salada","fruta"] }
  ]},
  { id:"quinta", nome:"Quinta-feira", proteinaDia:"~85 g", refeicoes:[
    { id:"quinta-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["tapioca","2 ovos","1 fatia de queijo","banana"] },
    { id:"quinta-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["arroz","feijão","80g de carne moída","salada","azeite","laranja"] },
    { id:"quinta-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["1 pão","2 ovos","1 fatia de queijo","mamão"] },
    { id:"quinta-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["arroz","feijão","80g de frango grelhado","salada","fruta"] }
  ]},
  { id:"sexta", nome:"Sexta-feira", proteinaDia:"~85-90 g", refeicoes:[
    { id:"sexta-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["2 pães","omelete de 2 ovos com 1 fatia de queijo","banana"] },
    { id:"sexta-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["arroz","feijão","80g de carne bovina","legumes","azeite","fruta"] },
    { id:"sexta-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["tapioca","2 ovos mexidos","1 fatia de queijo","banana"] },
    { id:"sexta-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["arroz","feijão","80g de frango desfiado","salada","fruta"] }
  ]},
  { id:"sabado", nome:"Sábado", proteinaDia:"~85 g", refeicoes:[
    { id:"sabado-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["2 pães","2 ovos mexidos","1 fatia de queijo","mamão"] },
    { id:"sabado-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["arroz","feijão","80g de frango","salada","azeite","manga"] },
    { id:"sabado-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["sanduíche com pão","50g de carne moída","1 fatia de queijo","fruta"] },
    { id:"sabado-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["macarrão","80g de carne moída","salada","fruta"] }
  ]},
  { id:"domingo", nome:"Domingo", proteinaDia:"~80-90 g", refeicoes:[
    { id:"domingo-cafe", nome:"Café da manhã", icon:"☀️", proteina:"18-20g", alimentos:["2 pães","2 ovos","1 fatia de queijo","banana"] },
    { id:"domingo-almoco", nome:"Almoço", icon:"🍚", proteina:"25g", alimentos:["arroz","feijão","80-100g de carne/frango assado","batata","salada","fruta"] },
    { id:"domingo-lanche", nome:"Lanche da tarde", icon:"🥪", proteina:"15-18g", alimentos:["tapioca","1 fatia de queijo","2 ovos","banana"] },
    { id:"domingo-jantar", nome:"Jantar", icon:"🌙", proteina:"25g", alimentos:["arroz","feijão","omelete de 2 ovos com queijo","salada"] }
  ]}
];

const MENSAGENS = {
  "0-24": ["Vamos, minha farma ❤️","Um dia de cada vez. Tô com você.","Respira, vai com calma e faz o seu melhor. Confio em você.","Minha farma tá on! ❤️"],
  "25-49": ["Mais uma refeição concluída. Tô orgulhoso de você ❤️","Vai no seu ritmo, minha farma. O importante é continuar.","Você consegue. Um pouquinho todos os dias.","Bora, minha farma! Você tá indo bem ❤️"],
  "50-74": ["Metade do dia já é sua. Continua assim ❤️","Olha você cumprindo mais uma meta. Sabia que você conseguia.","Não precisa ser perfeito, só precisa continuar.","Eu sei que você consegue."],
  "75-99": ["Só falta mais uma! Tô aqui torcendo por você ❤️","Cuida de você, tá? Eu me importo muito com você.","Reta final do dia. Confio em você, minha farma.","Tá quase lá. Um pouquinho mais 💪"],
  "100": ["VOCÊ CONSEGUIU, MINHA FARMA! ❤️","4 de 4! Missão cumprida. Tenho muito orgulho de você.","Hoje você cuidou de você. E isso me deixa muito feliz. ❤️","Meta do dia concluída! Sabia que você conseguia."]
};

/* ================= ESTADO PERSISTENTE =================
   O progresso é salvo automaticamente no navegador usando localStorage.
   Cada dia possui seu próprio estado e é separado pela data.
*/
const STORAGE_KEY = "plano_lais_progresso_v1";

function hojeKey() {
  const d = new Date();
  const y = d.getFullYear();
  const m = String(d.getMonth() + 1).padStart(2, "0");
  const day = String(d.getDate()).padStart(2, "0");
  return `${y}-${m}-${day}`;
}

function estadoInicial() {
  const estado = {};
  PLANO.forEach(dia => dia.refeicoes.forEach(r => estado[r.id] = false));
  return estado;
}

function carregarEstado() {
  try {
    const salvo = JSON.parse(localStorage.getItem(STORAGE_KEY) || "{}");
    const dia = hojeKey();
    return salvo[dia] || estadoInicial();
  } catch (e) {
    console.warn("Não foi possível carregar o progresso salvo:", e);
    return estadoInicial();
  }
}

function salvarEstado() {
  try {
    const salvo = JSON.parse(localStorage.getItem(STORAGE_KEY) || "{}");
    salvo[hojeKey()] = status;
    localStorage.setItem(STORAGE_KEY, JSON.stringify(salvo));
  } catch (e) {
    console.warn("Não foi possível salvar o progresso:", e);
  }
}

let status = carregarEstado();

// dia atual: tenta detectar o dia da semana real; senão cai em Segunda
const weekdayMap = [6,0,1,2,3,4,5]; // JS getDay(): 0=Dom -> index 6 no nosso array (Domingo é o último)
let currentDayIndex = weekdayMap[new Date().getDay()];
let messageIndex = { "0-24":0, "25-49":0, "50-74":0, "75-99":0, "100":0 };
let celebratedToday = {};

/* ================= RENDER ================= */
const tabsEl = document.getElementById('tabs');
const mealsEl = document.getElementById('meals');
const weekDotsEl = document.getElementById('weekDots');

function dayProgress(dia){
  const total = dia.refeicoes.length;
  const done = dia.refeicoes.filter(r => status[r.id]).length;
  const pct = Math.round((done/total)*100);
  return { done, total, pct };
}

function faixaFor(pct){
  if(pct >= 100) return "100";
  if(pct >= 75) return "75-99";
  if(pct >= 50) return "50-74";
  if(pct >= 25) return "25-49";
  return "0-24";
}

function nextMessage(faixa){
  const arr = MENSAGENS[faixa];
  const i = messageIndex[faixa] % arr.length;
  messageIndex[faixa] = i + 1;
  return arr[i];
}

function renderTabs(){
  tabsEl.innerHTML = "";
  PLANO.forEach((dia, idx) => {
    const { done, total } = dayProgress(dia);
    const btn = document.createElement('button');
    btn.className = 'tab' + (idx === currentDayIndex ? ' active' : '');
    btn.innerHTML = dia.nome.replace('-feira','') + (done>0 ? `<span class="dot"></span>` : '');
    btn.onclick = () => { currentDayIndex = idx; renderAll(false); };
    tabsEl.appendChild(btn);
  });
}

function renderMeals(dia){
  mealsEl.innerHTML = "";
  dia.refeicoes.forEach(r => {
    const done = status[r.id];
    const card = document.createElement('div');
    card.className = 'meal' + (done ? ' done' : '');
    card.innerHTML = `
      <button class="check-btn" aria-label="Marcar ${r.nome} como concluída">${done ? '✓' : ''}</button>
      <div class="meal-body">
        <div class="meal-top">
          <span class="meal-name"><span class="meal-icon">${r.icon}</span>${r.nome}</span>
          <span class="meal-protein">~${r.proteina} proteína</span>
        </div>
        <ul class="meal-foods">${r.alimentos.map(a => `<li>${a}</li>`).join('')}</ul>
      </div>
    `;
    card.querySelector('.check-btn').onclick = () => {
      status[r.id] = !status[r.id];
      salvarEstado();
      renderAll(true);
    };
    mealsEl.appendChild(card);
  });
}

function renderProgress(dia){
  const { done, total, pct } = dayProgress(dia);
  document.getElementById('dayLabel').textContent = dia.nome;
  document.getElementById('countLabel').textContent = `${done} de ${total} refeições concluídas`;
  document.getElementById('pctLabel').textContent = `${pct}%`;
  const fill = document.getElementById('barFill');
  fill.style.width = pct + '%';
  fill.classList.toggle('full', pct >= 100);

  const faixa = faixaFor(pct);
  document.getElementById('noteMsg').textContent = nextMessage(faixa) === undefined
    ? MENSAGENS[faixa][0]
    : (function(){ messageIndex[faixa]--; return MENSAGENS[faixa][messageIndex[faixa] % MENSAGENS[faixa].length]; })();
}

function renderWeek(){
  weekDotsEl.innerHTML = "";
  let totalDone = 0, totalAll = 0, diasCompletos = 0;
  const shortNames = ["Seg","Ter","Qua","Qui","Sex","Sáb","Dom"];
  PLANO.forEach((dia, idx) => {
    const { done, total } = dayProgress(dia);
    totalDone += done; totalAll += total;
    if(done === total) diasCompletos++;
    const wrap = document.createElement('div');
    const cls = done === total ? 'week-dot complete' : (done > 0 ? 'week-dot partial' : 'week-dot');
    wrap.className = cls;
    wrap.innerHTML = `<div class="circle">${done === total ? '★' : done}</div><span>${shortNames[idx]}</span>`;
    weekDotsEl.appendChild(wrap);
  });
  document.getElementById('weekSummary').innerHTML = `<b>${totalDone} de ${totalAll}</b> refeições essa semana · <b>${diasCompletos}</b> dia(s) 100% completo(s)`;
}

function maybeCelebrate(dia, wasToggled){
  const { done, total, pct } = dayProgress(dia);
  if(wasToggled && pct >= 100 && !celebratedToday[dia.id]){
    celebratedToday[dia.id] = true;
    showCelebration();
  }
  if(pct < 100){
    celebratedToday[dia.id] = false;
  }
}

function showCelebration(){
  const arr = MENSAGENS["100"];
  document.getElementById('celebrateMsg').textContent = arr[Math.floor(Math.random()*arr.length)];
  const overlay = document.getElementById('celebrateOverlay');
  overlay.classList.add('show');
  spawnHearts();
}
function closeCelebration(){
  document.getElementById('celebrateOverlay').classList.remove('show');
}
function spawnHearts(){
  const card = document.getElementById('celebrateCard');
  const emojis = ['❤️','💪','🥹','✨'];
  for(let i=0;i<14;i++){
    const h = document.createElement('span');
    h.className = 'heart';
    h.textContent = emojis[Math.floor(Math.random()*emojis.length)];
    h.style.left = Math.random()*90 + '%';
    h.style.animationDuration = (1.6 + Math.random()*1.2) + 's';
    h.style.animationDelay = (Math.random()*0.6) + 's';
    card.appendChild(h);
    setTimeout(() => h.remove(), 3200);
  }
}

function renderAll(wasToggled){
  const dia = PLANO[currentDayIndex];
  renderTabs();
  renderMeals(dia);
  renderProgress(dia);
  renderWeek();
  maybeCelebrate(dia, wasToggled);
}

renderAll(false);
</script>

</body>
</html>
