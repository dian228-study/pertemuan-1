<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Biodata Dian</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #7dd3fc, #9333ea);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    .frame {
      border: 18px solid transparent;
      border-image: url('https://i.ibb.co/7Qbq2GH/kamboja-border.png') 30 round;
      border-radius: 18px;
      background: rgba(0,0,0,0.2);
      width: 90%;
      max-width: 400px;
      height: 90%;
      overflow: hidden;
      position: relative;
      box-shadow: 0 4px 10px rgba(0,0,0,0.4);
    }

    .page {
      display: none;
      padding: 20px;
      text-align: center;
      height: 100%;
      overflow-y: auto;
    }

    .active {
      display: block;
      animation: slide 0.6s;
    }

    @keyframes slide {
      from { opacity: 0; transform: translateX(40px);}
      to { opacity: 1; transform: translateX(0);}
    }

    h1 {
      color: #ffeb3b;
    }

    p {
      font-size: 15px;
      line-height: 1.6;
      color: #fff;
    }

    .btn {
      background: #ffeb3b;
      color: #333;
      padding: 10px 16px;
      border-radius: 8px;
      font-weight: bold;
      text-decoration: none;
      font-size: 14px;
      display: inline-block;
      margin-top: 10px;
      transition: 0.3s;
    }

    .btn:hover {
      background: #facc15;
    }

    /* Sosmed */
    .social {
      display: flex;
      align-items: center;
      background: rgba(255,255,255,0.15);
      padding: 10px;
      margin: 10px 0;
      border-radius: 10px;
      gap: 10px;
    }
    .social img {
      width: 28px;
      height: 28px;
    }
    .social span {
      font-size: 14px;
      color: #fff;
    }

    .foto-diri {
      margin: 15px 0;
    }
    .foto-diri img {
      width: 150px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.3);
    }
  </style>
</head>
<body>

  <div class="frame">
    <!-- Cover -->
    <div class="page active" id="page1">
      <h1>📖 Biodata Dian</h1>
      <p>Selamat datang di buku biodata sederhana</p>
      <button class="btn" onclick="nextPage(2)">Mulai Membaca ➡️</button>
    </div>

    <!-- Biodata -->
    <div class="page" id="page2">
      <h1>Biodata Dian Ayu Dhiya</h1>
      
      <div class="foto-diri">
        <img src="https://img.freepik.com/free-vector/cute-doctor-cartoon-character_1308-133544.jpg" 
             alt="Foto Dokter Kartun">
      </div>

      <p>
        Perkenalkan, namaku <b>Dian Ayu Dhiya</b>.  
        Seorang gadis berusia 16 tahun, yang masih belajar menapaki jalan panjang kehidupan.  
      </p>
      <p>
        Sejak kecil, aku memiliki mimpi: menjadi seorang dokter.  
        Aku ingin hadir untuk orang lain di saat mereka paling membutuhkan.
      </p>
      <p>
        Aku hanyalah remaja sederhana yang mencintai hal-hal kecil.  
        Membaca buku, menulis kata-kata, mendengarkan musik — semuanya adalah teman perjalanan.
      </p>
      <p>
        Teman-teman mengenalku ramah dan ceria, meski aku percaya bahwa setiap orang punya luka dan cerita yang tak selalu terlihat.
      </p>
      <button class="btn" onclick="prevPage(1)">⬅️ Kembali</button>
      <button class="btn" onclick="nextPage(3)">Lanjut ➡️</button>
    </div>

    <!-- Media Sosial -->
    <div class="page" id="page3">
      <h1>Media Sosial Favorit</h1>

      <div class="social">
        <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" alt="Instagram">
        <span>@dyanue</span>
      </div>

      <div class="social">
        <img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" alt="Telegram">
        <span>@renaa</span>
      </div>

      <div class="social">
        <img src="https://cdn-icons-png.flaticon.com/512/5968/5968812.png" alt="TikTok">
        <span>@amertha</span>
      </div>

      <div class="social">
        <img src="https://cdn-icons-png.flaticon.com/512/3670/3670051.png" alt="WhatsApp">
        <span>@arena</span>
      </div>

      <button class="btn" onclick="prevPage(2)">⬅️ Kembali</button>
    </div>
  </div>

  <script>
    function nextPage(n){
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById('page'+n).classList.add('active');
    }
    function prevPage(n){
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById('page'+n).classList.add('active');
    }
  </script>
</body>
</html>)
