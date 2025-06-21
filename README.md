<style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #cce7ff;
      overflow-x: hidden;
    }
    header {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color: #cce7ff;
      animation: fadeIn 2s ease-in;
    }
    header h1 {
      font-size: 2.5rem;
      color: #003366;
      margin-bottom: 20px;
    }
    .next-button {
      padding: 12px 20px;
      font-size: 1rem;
      border: none;
      border-radius: 25px;
      background-color: #0077cc;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .next-button:hover {
      background-color: #005fa3;
    }
    section {
      padding: 40px 20px;
      text-align: center;
      display: none;
    }
    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }
     .gallery img {
      width: 250px;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      opacity: 0;
      transform: translateY(20px);
      animation: slideIn 1s forwards;

    }
    .gallery img:nth-child(1) { animation-delay: 0.3s; }
    .gallery img:nth-child(2) { animation-delay: 0.6s; }
    .gallery img:nth-child(3) { animation-delay: 0.9s; }
    
    .letter {
      max-width: 600px;
      margin: 40px auto;
      padding: 20px;
      background-color: #e6f2ff;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      white-space: pre-wrap;
      animation: fadeIn 2s ease-in;
    }
    @keyframes slideIn {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
<body>

  <!-- 🎉 Homepage Section -->
  <header id="homepage">
    <h1>Happy Birthday Seig!! </h1>
    <div> to our chismosa, makulit, maingay, madaldal and moody guy friend</div>
    <div>hihi my gift to u kasi wala na ako pera</div>
    <br>
     <button class="next-button" onclick="showSection('memories')">Ready ka na? HAHAHA</button>
  </header>

  <!-- 📸 Memories Section -->
  <section id="memories">
    <h2>Memories (puw8)</h2>
    <div class="gallery">
      <img src="https://i.imgur.com/X2sjrUN.jpeg" alt="Memory 1">
     <img src="https://i.imgur.com/nhrNUkQ.jpeg" alt="Memory 2">
     <img src="https://i.imgur.com/dWhziDQ.jpeg" alt="Memory 3">
     <img src="https://i.imgur.com/uhrmL6Y.jpeg" alt="Memory 4">
     <img src="https://i.imgur.com/hd2ZkyC.jpeg" alt="Memory 5">
     <img src="https://i.imgur.com/LXGiTPQ.jpeg" alt="Memory 6">
     <img src="https://i.imgur.com/UoiUBdl.jpeg" alt="Memory 7">
     <img src="https://i.imgur.com/E47FJ4n.jpeg" alt="Memory 8">
    </div>
    <br>
    <button class="next-button" onclick="showSection('letter')">Next naman </button>
  </section>

  <!-- 💌 Letter Section -->
<section id="letter">
  <h2>Corny na, egul egul</h2>
  <div class="letter">
Happy 16th Birthday, Seigy!!!
  <br>
First of all, thank you, soafer. Thank you sa lahat ng kakulitan, sa mga moments na kahit super asar ka na or naiirita ka na sakin, andiyan ka pa rin BWAHAH kahit ilang ulit na akong kulit nang kulit, hindi ka pa rin sumusuko (slight lang). Thank you rin sa mga times na tinutulungan mo ako kahit hindi mo naman kailangan, sa mga simpleng bagay na hindi mo alam, sobrang laking tulong na pala sakin.
<br>
You’ve always been that one consistent energy sa group :ppp mapagbirong kuya-ish figure na minsan sabaw, minsan seryoso, minsan chaotic, pero laging present. Ikaw ‘yung nagpapasaya sa COF sa mga panahong tahimik, awkward, o malungkot kami kahit ikaw lang yung lalaki sa group, hindi ka nagkulang sa pagiging part ng barkada, actually, sobra pa nga... sobra sa kakulitan.
<br>
Hindi ko makakalimutan ‘yung mga times na down kaming lahat, pero nandun ka, minsan para magpatawa, minsan para makinig lang. Soafer laki ng impact mo, inang impacto ka, kahit hindi mo sinasabi o pinapakita madalas. Ang dami mong binigay na good memories... good at bad and ang dami mong na-save na moments from becoming sad or heavy just by being you kahit hindi mo sinasadyang maging light sa paligid namin, you always are.
<br>
Corny pero you deserve so much love and happiness. You’ve given so much of that to us, sa bawat tawa, hirit, at asar mo  and I hope on your special day, maramdaman mo rin lahat ng pagmamahal na deserve mong matanggap. You're not just a friend really, you've become a part of our lives na that despite your... nakakainis na ugali, we still love ya.
<br>
Enjoy your 16th birthday! Kumain ka ng madami, tumawa ka ng malakas, at magpahinga ka rin (kung pwede HAHA). Lagi mong tatandaan na mahalaga ka samin, at hindi ka nag-iisa kasi lagi kaming nasa tabi mo, nangkulit HAHAHAHAHA
<br>
Happy birthday ulit!! 
  </div>
  <br>
  <button class="next-button" onclick="showSection('final')">Last na to.</button>
</section>

<!-- 🎂 Final Surprise Section -->
<section id="final" style="display: none; text-align: center; padding: 40px 20px;">
  <h2>Last na talaga</h2>
  <p>Click mo cake, may secret diyan</p>
  <button class="next-button" onclick="revealCake()">🎂</button>
  
  <div id="cake" style="margin-top: 30px; opacity: 0; transition: opacity 1.5s ease;">
    <p style="margin-top: 15px;">badingggggg</p>
  </div>
</section>
<script> function showSection(id) {
  document.getElementById('homepage').style.display = 'none';
  document.getElementById('memories').style.display = 'none';
  document.getElementById('letter').style.display = 'none';
  document.getElementById('final').style.display = 'none';
  document.getElementById(id).style.display = 'block';
}

function revealCake() {
  const cake = document.getElementById('cake');
  cake.style.opacity = 1;
}
</script>
