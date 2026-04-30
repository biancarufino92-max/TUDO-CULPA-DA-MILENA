<!doctype html>
<html lang="pt-BR" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>O Mistério de Milena</title>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Special+Elite&amp;family=Cormorant+Garamond:wght@400;600;700&amp;display=swap" rel="stylesheet">
  <style>
  body {
    font-family: 'Cormorant Garamond', serif;
    background-color: #1a1410;
    background-image:
      radial-gradient(circle at 20% 30%, rgba(139, 69, 19, 0.15) 0%, transparent 50%),
      radial-gradient(circle at 80% 70%, rgba(101, 67, 33, 0.2) 0%, transparent 50%),
      url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='100' viewBox='0 0 100 100'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3CfeColorMatrix values='0 0 0 0 0.1 0 0 0 0 0.08 0 0 0 0 0.06 0 0 0 0.3 0'/%3E%3C/filter%3E%3Crect width='100' height='100' filter='url(%23noise)' opacity='0.4'/%3E%3C/svg%3E");
  }
  .typewriter { font-family: 'Special Elite', cursive; }
  .paper {
    background: #f4e8d0;
    background-image:
      linear-gradient(rgba(139, 90, 43, 0.05) 1px, transparent 1px),
      radial-gradient(circle at 10% 20%, rgba(101, 67, 33, 0.08) 0%, transparent 40%),
      radial-gradient(circle at 90% 80%, rgba(101, 67, 33, 0.1) 0%, transparent 40%);
    background-size: 100% 28px, 100%, 100%;
    box-shadow:
      0 20px 40px rgba(0,0,0,0.6),
      0 0 0 1px rgba(139, 90, 43, 0.2),
      inset 0 0 60px rgba(139, 90, 43, 0.1);
  }
  .stamp {
    border: 3px solid #8b0000;
    color: #8b0000;
    transform: rotate(-12deg);
    font-family: 'Special Elite', cursive;
    opacity: 0.85;
  }
  .suspect-card {
    transition: all 0.3s ease;
    background: #2a1f17;
    border: 1px solid rgba(212, 175, 115, 0.3);
  }
  .suspect-card:hover {
    transform: translateY(-4px);
    border-color: #d4af73;
    box-shadow: 0 10px 30px rgba(212, 175, 115, 0.2);
  }
  .suspect-card.selected {
    border-color: #d4af73;
    box-shadow: 0 0 0 2px #d4af73, 0 10px 30px rgba(212, 175, 115, 0.3);
  }
  .evidence-item {
    background: rgba(244, 232, 208, 0.05);
    border-left: 3px solid #d4af73;
    transition: all 0.2s ease;
  }
  .evidence-item:hover {
    background: rgba(244, 232, 208, 0.1);
    transform: translateX(4px);
  }
  .evidence-item.examined {
    background: rgba(212, 175, 115, 0.15);
    border-left-color: #f4e8d0;
  }
  @keyframes flicker {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.85; }
  }
  .lamp-glow { animation: flicker 3s ease-in-out infinite; }
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .fade-in { animation: fadeInUp 0.6s ease forwards; }
  @keyframes stamp-in {
    0% { transform: rotate(-12deg) scale(3); opacity: 0; }
    60% { transform: rotate(-12deg) scale(0.9); opacity: 1; }
    100% { transform: rotate(-12deg) scale(1); opacity: 0.85; }
  }
  .stamp-animate { animation: stamp-in 0.8s ease-out forwards; }
  .title-font { font-family: 'Special Elite', cursive; letter-spacing: 0.05em; }
  .btn-primary {
    background: #d4af73;
    color: #1a1410;
    font-family: 'Special Elite', cursive;
    transition: all 0.2s ease;
  }
  .btn-primary:hover:not(:disabled) {
    background: #e8c896;
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(212, 175, 115, 0.4);
  }
  .btn-primary:disabled { opacity: 0.4; cursor: not-allowed; }
  .btn-secondary {
    background: transparent;
    color: #d4af73;
    border: 1px solid #d4af73;
    font-family: 'Special Elite', cursive;
    transition: all 0.2s ease;
  }
  .btn-secondary:hover { background: rgba(212, 175, 115, 0.1); }
  .case-badge {
    background: linear-gradient(135deg, #8b0000, #5a0000);
    color: #f4e8d0;
    font-family: 'Special Elite', cursive;
  }
  .smoke {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 60px;
    background: linear-gradient(to top, rgba(212, 175, 115, 0.08), transparent);
    pointer-events: none;
  }
</style>
  <style>body { box-sizing: border-box; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full w-full overflow-auto text-amber-50">
  <div class="w-full min-h-full relative">
   <div class="smoke"></div><!-- HEADER -->
   <header class="w-full border-b border-amber-900/40 bg-black/30 backdrop-blur-sm sticky top-0 z-20">
    <div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
     <div class="flex items-center gap-3">
      <div class="lamp-glow text-4xl">
       🔎
      </div>
      <div>
       <h1 id="gameTitle" class="title-font text-xl md:text-2xl text-amber-100">O Mistério de Milena</h1>
       <p id="gameSubtitle" class="text-xs md:text-sm text-amber-200/60 italic">Arquivos Confidenciais — Delegacia Central</p>
      </div>
     </div>
     <div class="flex items-center gap-4">
      <div class="text-right">
       <div class="text-xs text-amber-200/50 uppercase tracking-wider">
        Caso
       </div>
       <div id="caseCounter" class="title-font text-amber-100">
        01 / 05
       </div>
      </div>
      <div class="text-right">
       <div class="text-xs text-amber-200/50 uppercase tracking-wider">
        Resolvidos
       </div>
       <div id="scoreCounter" class="title-font text-amber-100">
        0
       </div>
      </div>
     </div>
    </div>
   </header>
   <main class="max-w-6xl mx-auto px-6 py-8"><!-- INTRO SCREEN -->
    <section id="introScreen" class="fade-in">
     <div class="paper text-stone-800 p-8 md:p-12 rounded-sm relative max-w-3xl mx-auto">
      <div class="absolute top-6 right-6 stamp px-4 py-2 text-sm">
       ARQUIVO SIGILOSO
      </div>
      <div class="typewriter text-xs text-stone-500 mb-4">
       DELEGACIA CENTRAL — SETOR DE INVESTIGAÇÕES
      </div>
      <h2 class="title-font text-3xl md:text-4xl mb-4 text-stone-900">Bem-vindo, Detetive.</h2>
      <div class="space-y-4 text-lg leading-relaxed">
       <p>Cinco casos chegaram à sua mesa. Cinco crimes distintos. Cinco elencos de suspeitos.</p>
       <p>Seu trabalho é simples — ler os depoimentos, examinar as provas, e apontar <span class="italic font-semibold">a pessoa culpada</span> em cada caso.</p>
       <p class="text-sm italic text-stone-600 border-l-2 border-stone-400 pl-4 mt-6">"Os fatos falam mais alto que as aparências. Confie nas evidências."</p>
      </div>
      <div class="mt-8 flex justify-end"><button id="startBtn" class="btn-primary px-8 py-3 rounded-sm text-sm uppercase tracking-widest"> Abrir Primeiro Caso → </button>
      </div>
     </div>
    </section><!-- CASE SCREEN -->
    <section id="caseScreen" class="hidden"><!-- Case Header -->
     <div class="mb-6 fade-in">
      <div class="flex items-center gap-3 mb-2"><span id="caseBadge" class="case-badge px-3 py-1 text-xs uppercase tracking-widest rounded-sm">Caso 01</span> <span class="text-amber-200/50 text-sm italic">— Classificação: Homicídio</span>
      </div>
      <h2 id="caseTitle" class="title-font text-3xl md:text-4xl text-amber-100 mb-2"></h2>
      <p id="caseLocation" class="text-amber-200/70 italic"></p>
     </div>
     <div class="grid grid-cols-1 lg:grid-cols-3 gap-6"><!-- Left: Case File -->
      <div class="lg:col-span-2 space-y-6"><!-- Report -->
       <div class="paper text-stone-800 p-6 md:p-8 rounded-sm relative">
        <div class="typewriter text-xs text-stone-500 mb-3 flex justify-between"><span>RELATÓRIO OFICIAL</span> <span id="caseDate"></span>
        </div>
        <h3 class="title-font text-xl mb-4 text-stone-900 border-b border-stone-400 pb-2">Sumário da Ocorrência</h3>
        <p id="caseReport" class="text-base md:text-lg leading-relaxed"></p>
       </div><!-- Evidence -->
       <div class="bg-black/40 border border-amber-900/30 rounded-sm p-6">
        <div class="flex items-center gap-2 mb-4"><i data-lucide="search" class="text-amber-400"></i>
         <h3 class="title-font text-lg text-amber-100">Evidências Recolhidas</h3><span class="text-xs text-amber-200/50 ml-auto">(clique para examinar)</span>
        </div>
        <div id="evidenceList" class="space-y-2"></div>
       </div><!-- Testimonies -->
       <div class="bg-black/40 border border-amber-900/30 rounded-sm p-6">
        <div class="flex items-center gap-2 mb-4"><i data-lucide="message-square-quote" class="text-amber-400"></i>
         <h3 class="title-font text-lg text-amber-100">Depoimentos</h3>
        </div>
        <div id="testimoniesList" class="space-y-3"></div>
       </div>
      </div><!-- Right: Suspects -->
      <div class="lg:col-span-1">
       <div class="sticky top-28">
        <div class="flex items-center gap-2 mb-4"><i data-lucide="users" class="text-amber-400"></i>
         <h3 class="title-font text-lg text-amber-100">Suspeitos</h3>
        </div>
        <div id="suspectsList" class="space-y-3 mb-6"></div><button id="accuseBtn" disabled class="btn-primary w-full py-3 rounded-sm text-sm uppercase tracking-widest"> Fazer Acusação </button>
        <p id="accuseHint" class="text-xs text-amber-200/50 italic text-center mt-2">Selecione um suspeito</p>
       </div>
      </div>
     </div>
    </section><!-- VERDICT SCREEN -->
    <section id="verdictScreen" class="hidden fade-in">
     <div class="paper text-stone-800 p-8 md:p-12 rounded-sm relative max-w-3xl mx-auto">
      <div id="verdictStamp" class="absolute top-8 right-8 stamp stamp-animate px-6 py-3 text-lg"></div>
      <div class="typewriter text-xs text-stone-500 mb-4">
       VEREDICTO FINAL
      </div>
      <h2 id="verdictTitle" class="title-font text-3xl md:text-4xl mb-6 text-stone-900"></h2>
      <div id="verdictContent" class="space-y-4 text-base md:text-lg leading-relaxed"></div>
      <div class="mt-8 flex justify-between items-center">
       <div class="text-sm text-stone-600 italic" id="verdictCaseInfo"></div><button id="nextBtn" class="btn-primary px-8 py-3 rounded-sm text-sm uppercase tracking-widest"> Próximo Caso → </button>
      </div>
     </div>
    </section><!-- FINAL SCREEN -->
    <section id="finalScreen" class="hidden fade-in">
     <div class="paper text-stone-800 p-8 md:p-12 rounded-sm relative max-w-3xl mx-auto">
      <div class="absolute top-6 right-6 stamp px-4 py-2 text-sm">
       CASO ENCERRADO
      </div>
      <div class="typewriter text-xs text-stone-500 mb-4">
       DOSSIÊ FINAL — TODAS AS INVESTIGAÇÕES
      </div>
      <h2 class="title-font text-3xl md:text-4xl mb-4 text-stone-900">O Padrão Revelado</h2>
      <div class="space-y-4 text-base md:text-lg leading-relaxed">
       <p>Detetive, seu trabalho revelou algo perturbador.</p>
       <p>Em <span id="finalScore" class="font-semibold">todos os cinco</span> casos, um único nome se repete nas evidências, nos depoimentos e nos rastros deixados:</p>
       <div class="text-center my-6">
        <div id="finalCulprit" class="title-font text-4xl md:text-5xl text-red-900 tracking-widest">
         MILENA
        </div>
        <div class="text-sm text-stone-600 italic mt-2">
         a mente por trás de cada crime
        </div>
       </div>
       <p>Cinco disfarces. Cinco cenários. Uma única culpada.</p>
       <p class="text-sm italic text-stone-600 border-l-2 border-stone-400 pl-4 mt-6">"Alguns padrões só são visíveis quando se olha para o conjunto."</p>
      </div>
      <div class="mt-8 flex justify-end"><button id="restartBtn" class="btn-secondary px-8 py-3 rounded-sm text-sm uppercase tracking-widest"> ↻ Reabrir Arquivos </button>
      </div>
     </div>
    </section>
   </main>
   <footer class="max-w-6xl mx-auto px-6 py-6 text-center text-xs text-amber-200/40 italic">
    — Todos os suspeitos são fictícios. Milena também. —
   </footer>
  </div>
  <script>
  const defaultConfig = {
    game_title: "O Mistério de Milena",
    game_subtitle: "Arquivos Confidenciais — Delegacia Central",
    culprit_name: "Milena"
  };

  // Build cases — culprit is always "Milena" (via config.culprit_name)
  function buildCases(culprit) {
    return [
      {
        title: "A Herança da Mansão Vale",
        location: "Mansão Vale — noite chuvosa de outubro",
        date: "12/10, 23:47",
        type: "Homicídio",
        report: `O industrial Arnaldo Vale foi encontrado morto em seu escritório, envenenado pelo chá das 22h. A porta estava trancada por dentro, mas a janela do jardim estava aberta. Três pessoas estavam na mansão: a governanta, o sobrinho e a secretária particular, ${culprit}, que serviu o chá naquela noite.`,
        evidence: [
          `Xícara com resíduo de cicuta — digitais apenas de ${culprit}.`,
          `Livro de farmacologia encontrado no quarto de ${culprit}, com a página sobre cicuta marcada.`,
          "A janela do jardim foi aberta por dentro, sem sinais de arrombamento.",
          `Testamento recém-alterado: ${culprit} passou a receber 40% da fortuna.`
        ],
        testimonies: [
          { who: "Governanta", text: `"Eu preparei o jantar, mas o chá da noite era sempre servido pela ${culprit}. Só ela mexia na despensa depois das dez."` },
          { who: "Sobrinho", text: `"Meu tio tinha medo de alguém na casa nas últimas semanas. Ele disse: 'confio em todos, menos em ${culprit}.'"` }
        ],
        suspects: ["Governanta Dona Zilda", "Sobrinho Ricardo", culprit],
        culprit: culprit,
        explanation: `A cicuta estava na xícara que só ${culprit} manuseou. O livro em seu quarto, o testamento alterado e a janela aberta de dentro (para simular invasão) completam o quadro. Motivo, meio e oportunidade — todos apontam para ${culprit}.`
      },
      {
        title: "O Roubo do Diamante Azul",
        location: "Museu Nacional — galeria de gemas",
        date: "03/03, 02:15",
        type: "Roubo qualificado",
        report: `O lendário Diamante Azul desapareceu da vitrine do museu durante a madrugada. O alarme foi desativado com um código interno. Apenas quatro funcionários tinham acesso ao código: o curador, o chefe de segurança, a restauradora e a conservadora noturna ${culprit}.`,
        evidence: [
          `Registro do sistema: o código foi inserido às 02:11 do terminal usado por ${culprit}.`,
          `Fibras de um casaco cinza na vitrine — idênticas ao casaco que ${culprit} usava naquela noite.`,
          "A câmera do corredor oeste foi desligada manualmente — ação feita pela conservadora de plantão.",
          `Uma dívida de jogo recente de ${culprit} foi descoberta: R$ 380 mil.`
        ],
        testimonies: [
          { who: "Curador", text: `"Só três pessoas sabiam o novo código: eu, o chefe de segurança, e a ${culprit}, que insistiu para recebê-lo 'por emergência'."` },
          { who: "Chefe de Segurança", text: `"Eu estava em casa às 02h. A única pessoa no museu era a ${culprit}."` }
        ],
        suspects: ["Curador Dr. Horácio", "Chefe de Segurança", "Restauradora Lívia", culprit],
        culprit: culprit,
        explanation: `O código inserido partiu do terminal de ${culprit}, no horário em que ela era a única pessoa no prédio. As fibras do casaco, a câmera desligada e o motivo financeiro não deixam margem para dúvida.`
      },
      {
        title: "O Incêndio no Teatro Áureo",
        location: "Teatro Áureo — véspera da estreia",
        date: "28/07, 01:30",
        type: "Incêndio criminoso",
        report: `O cenário principal do Teatro Áureo foi consumido por um incêndio horas antes da estreia. A perícia confirmou: o fogo foi proposital. A peça estrelaria a atriz Helena Rios — e o papel principal havia sido disputado até o fim com sua substituta, ${culprit}.`,
        evidence: [
          `Câmeras do corredor dos bastidores mostram ${culprit} entrando às 01:12 e saindo às 01:28.`,
          `Um frasco de solvente industrial com digitais de ${culprit} foi achado no camarim.`,
          "O detector de fumaça do palco foi desligado por alguém que conhecia o painel técnico.",
          `Mensagens deletadas no celular de ${culprit}: "se não for eu no palco, não será ninguém".`
        ],
        testimonies: [
          { who: "Diretor", text: `"A ${culprit} ficou furiosa quando perdeu o papel. Disse que 'daria um jeito'."` },
          { who: "Técnico de Luz", text: `"Vi a ${culprit} mexendo no painel técnico na noite do incêndio. Achei estranho, mas não falei nada."` }
        ],
        suspects: ["Atriz Helena Rios", "Diretor Bruno Caldas", "Técnico Paulinho", culprit],
        culprit: culprit,
        explanation: `Motivo (rivalidade e mágoa), meio (solvente com suas digitais), oportunidade (presença filmada nos bastidores) e confissão indireta nas mensagens. ${culprit} é a única responsável.`
      },
      {
        title: "O Envenenamento no Restaurante Aurora",
        location: "Restaurante Aurora — jantar beneficente",
        date: "15/11, 21:05",
        type: "Tentativa de homicídio",
        report: `Durante um jantar beneficente, o filantropo Samuel Peixoto quase morreu após beber sua taça de vinho. O exame toxicológico apontou arsênico. A taça havia sido servida pessoalmente pela sommelière contratada para o evento: ${culprit}.`,
        evidence: [
          `Somente ${culprit} tocou na taça da vítima — confirmado por imagens.`,
          `Pó de arsênico encontrado no bolso do avental de ${culprit} na revista policial.`,
          `${culprit} havia sido demitida de uma empresa de Samuel seis meses antes.`,
          "Nenhuma outra taça do evento apresentou contaminação."
        ],
        testimonies: [
          { who: "Garçom-chefe", text: `"A ${culprit} fez questão de servir a mesa principal sozinha. Disse que era 'protocolo dela'."` },
          { who: "Organizadora", text: `"Eu não queria contratá-la, mas ela baixou o preço pela metade para pegar o serviço."` }
        ],
        suspects: ["Garçom-chefe Otávio", "Organizadora Sueli", "Chef Marcos", culprit],
        culprit: culprit,
        explanation: `O arsênico estava com ela, a taça foi servida apenas por ela, o motivo (vingança pela demissão) é claro, e ela manipulou o contrato para estar ali. ${culprit} é a culpada.`
      },
      {
        title: "O Desaparecimento do Manuscrito",
        location: "Biblioteca Particular Montenegro",
        date: "07/01, madrugada",
        type: "Furto qualificado",
        report: `Um manuscrito medieval avaliado em milhões desapareceu do cofre da biblioteca particular Montenegro. O cofre estava intacto — foi aberto com o código correto. O código era conhecido por três pessoas: o dono, o bibliotecário-chefe e a pesquisadora-residente, ${culprit}.`,
        evidence: [
          `O sistema registra acesso ao cofre às 04:22 com o código pessoal de ${culprit}.`,
          `Um cartão de embarque internacional em nome de ${culprit}, marcado para o dia seguinte, foi apreendido em sua bolsa.`,
          `Fotografias de alta resolução do manuscrito foram encontradas no laptop de ${culprit}, datadas de semanas antes.`,
          "Nenhum sinal de arrombamento em portas ou janelas."
        ],
        testimonies: [
          { who: "Sr. Montenegro", text: `"Eu estava em Lisboa na data. A ${culprit} tinha acesso total à casa."` },
          { who: "Bibliotecário-chefe", text: `"Eu troquei meu código na semana passada. Só a ${culprit} ainda usava o antigo — o que foi registrado na madrugada."` }
        ],
        suspects: ["Sr. Montenegro", "Bibliotecário Augusto", "Faxineira Dona Rita", culprit],
        culprit: culprit,
        explanation: `Acesso pelo seu próprio código, viagem internacional marcada para o dia seguinte, fotos premeditadas no laptop. ${culprit} planejou e executou o furto sozinha.`
      }
    ];
  }

  // State
  let cases = buildCases(defaultConfig.culprit_name);
  let currentCaseIndex = 0;
  let currentSelection = null;
  let score = 0;
  let answered = false;

  // Screens
  const introScreen = document.getElementById('introScreen');
  const caseScreen = document.getElementById('caseScreen');
  const verdictScreen = document.getElementById('verdictScreen');
  const finalScreen = document.getElementById('finalScreen');

  function showScreen(screen) {
    [introScreen, caseScreen, verdictScreen, finalScreen].forEach(s => s.classList.add('hidden'));
    screen.classList.remove('hidden');
    screen.classList.remove('fade-in');
    void screen.offsetWidth;
    screen.classList.add('fade-in');
  }

  function pad(n) { return String(n).padStart(2, '0'); }

  function renderCase() {
    const c = cases[currentCaseIndex];
    currentSelection = null;
    answered = false;

    document.getElementById('caseBadge').textContent = `Caso ${pad(currentCaseIndex + 1)}`;
    document.getElementById('caseBadge').nextElementSibling.textContent = `— Classificação: ${c.type}`;
    document.getElementById('caseTitle').textContent = c.title;
    document.getElementById('caseLocation').textContent = c.location;
    document.getElementById('caseDate').textContent = c.date;
    document.getElementById('caseReport').textContent = c.report;
    document.getElementById('caseCounter').textContent = `${pad(currentCaseIndex + 1)} / ${pad(cases.length)}`;
    document.getElementById('scoreCounter').textContent = score;

    // Evidence
    const evEl = document.getElementById('evidenceList');
    evEl.innerHTML = '';
    c.evidence.forEach((ev, i) => {
      const div = document.createElement('div');
      div.className = 'evidence-item px-4 py-3 rounded-sm cursor-pointer text-amber-50/90 text-sm md:text-base';
      div.innerHTML = `<span class="text-amber-400 font-bold mr-2">#${pad(i+1)}</span>${ev}`;
      div.addEventListener('click', () => div.classList.toggle('examined'));
      evEl.appendChild(div);
    });

    // Testimonies
    const tEl = document.getElementById('testimoniesList');
    tEl.innerHTML = '';
    c.testimonies.forEach(t => {
      const div = document.createElement('div');
      div.className = 'border-l-2 border-amber-700/50 pl-4 py-1';
      div.innerHTML = `<div class="text-xs uppercase tracking-wider text-amber-400/70 mb-1">${t.who}</div><div class="italic text-amber-50/90 text-base">${t.text}</div>`;
      tEl.appendChild(div);
    });

    // Suspects
    const sEl = document.getElementById('suspectsList');
    sEl.innerHTML = '';
    // Shuffle suspect order
    const shuffled = [...c.suspects].sort(() => Math.random() - 0.5);
    shuffled.forEach(name => {
      const card = document.createElement('div');
      card.className = 'suspect-card rounded-sm p-4 cursor-pointer flex items-center gap-3';
      card.dataset.name = name;
      card.innerHTML = `
        <div class="w-10 h-10 rounded-full bg-amber-900/40 flex items-center justify-center text-amber-300 title-font">
          ${name.charAt(0).toUpperCase()}
        </div>
        <div class="flex-1">
          <div class="title-font text-amber-100 text-sm">${name}</div>
          <div class="text-xs text-amber-200/50">Suspeito</div>
        </div>
        <i data-lucide="chevron-right" class="text-amber-200/30 suspect-arrow"></i>
      `;
      card.addEventListener('click', () => {
        if (answered) return;
        document.querySelectorAll('.suspect-card').forEach(c => c.classList.remove('selected'));
        card.classList.add('selected');
        currentSelection = name;
        document.getElementById('accuseBtn').disabled = false;
        document.getElementById('accuseHint').textContent = `Acusação: ${name}`;
      });
      sEl.appendChild(card);
    });

    document.getElementById('accuseBtn').disabled = true;
    document.getElementById('accuseHint').textContent = 'Selecione um suspeito';

    if (window.lucide) lucide.createIcons();
    showScreen(caseScreen);
  }

  function renderVerdict() {
    const c = cases[currentCaseIndex];
    const correct = currentSelection === c.culprit;
    if (correct) score++;
    answered = true;

    const stamp = document.getElementById('verdictStamp');
    stamp.textContent = correct ? 'CASO RESOLVIDO' : 'ERRO JUDICIAL';
    stamp.style.color = correct ? '#1a5c1a' : '#8b0000';
    stamp.style.borderColor = correct ? '#1a5c1a' : '#8b0000';
    stamp.classList.remove('stamp-animate');
    void stamp.offsetWidth;
    stamp.classList.add('stamp-animate');

    document.getElementById('verdictTitle').textContent = correct
      ? `${c.culprit} foi desmascarada.`
      : `A pista certa escapou por pouco.`;

    const content = document.getElementById('verdictContent');
    if (correct) {
      content.innerHTML = `
        <p>Sua acusação está correta, Detetive. <span class="font-semibold">${c.culprit}</span> é a responsável.</p>
        <p>${c.explanation}</p>
      `;
    } else {
      content.innerHTML = `
        <p>Você apontou <span class="font-semibold">${currentSelection}</span>, mas as provas levavam a outro caminho.</p>
        <p>A verdadeira responsável era <span class="font-semibold">${c.culprit}</span>.</p>
        <p class="text-sm italic text-stone-600 border-l-2 border-stone-400 pl-4">${c.explanation}</p>
      `;
    }

    document.getElementById('verdictCaseInfo').textContent = `Caso ${pad(currentCaseIndex + 1)} de ${pad(cases.length)} — Placar: ${score}`;
    document.getElementById('nextBtn').textContent = currentCaseIndex === cases.length - 1 ? 'Ver Dossiê Final →' : 'Próximo Caso →';
    showScreen(verdictScreen);
  }

  function renderFinal() {
    document.getElementById('finalScore').textContent = score === cases.length
      ? 'todos os cinco'
      : `${score} dos 5`;
    document.getElementById('finalCulprit').textContent = (window.elementSdk?.config?.culprit_name || defaultConfig.culprit_name).toUpperCase();
    document.getElementById('scoreCounter').textContent = score;
    showScreen(finalScreen);
  }

  // Events
  document.getElementById('startBtn').addEventListener('click', () => {
    currentCaseIndex = 0;
    score = 0;
    renderCase();
  });

  document.getElementById('accuseBtn').addEventListener('click', () => {
    if (!currentSelection) return;
    renderVerdict();
  });

  document.getElementById('nextBtn').addEventListener('click', () => {
    if (currentCaseIndex === cases.length - 1) {
      renderFinal();
    } else {
      currentCaseIndex++;
      renderCase();
    }
  });

  document.getElementById('restartBtn').addEventListener('click', () => {
    currentCaseIndex = 0;
    score = 0;
    cases = buildCases(window.elementSdk?.config?.culprit_name || defaultConfig.culprit_name);
    showScreen(introScreen);
  });

  // Element SDK
  function applyConfigToUI(config) {
    document.getElementById('gameTitle').textContent = config.game_title || defaultConfig.game_title;
    document.getElementById('gameSubtitle').textContent = config.game_subtitle || defaultConfig.game_subtitle;
    const culprit = config.culprit_name || defaultConfig.culprit_name;
    cases = buildCases(culprit);
    document.getElementById('finalCulprit').textContent = culprit.toUpperCase();
  }

  if (window.elementSdk) {
    window.elementSdk.init({
      defaultConfig,
      onConfigChange: async (config) => {
        applyConfigToUI(config);
      },
      mapToCapabilities: () => ({
        recolorables: [],
        borderables: [],
        fontEditable: undefined,
        fontSizeable: undefined
      }),
      mapToEditPanelValues: (config) => new Map([
        ["game_title", config.game_title || defaultConfig.game_title],
        ["game_subtitle", config.game_subtitle || defaultConfig.game_subtitle],
        ["culprit_name", config.culprit_name || defaultConfig.culprit_name]
      ])
    });
  }

  // Initial icons
  if (window.lucide) lucide.createIcons();
</script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9f495f5014c098e7',t:'MTc3NzU4MTczOS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
