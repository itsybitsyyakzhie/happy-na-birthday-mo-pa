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
</head>
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
    o10, wala pa
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
