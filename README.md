<!DOCTYPE html>
<html lang="id" class="h-full">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Klinik Tumbuh Kembang Anak</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="/_sdk/data_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&family=Fredoka+One&display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
    }
    
    .font-display {
      font-family: 'Fredoka One', cursive;
    }
    
    .font-body {
      font-family: 'Nunito', sans-serif;
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }
    
    @keyframes wiggle {
      0%, 100% { transform: rotate(-3deg); }
      50% { transform: rotate(3deg); }
    }
    
    @keyframes bounce-slow {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }
    
    @keyframes slide-up {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    .animate-float {
      animation: float 3s ease-in-out infinite;
    }
    
    .animate-wiggle {
      animation: wiggle 2s ease-in-out infinite;
    }
    
    .animate-bounce-slow {
      animation: bounce-slow 2s ease-in-out infinite;
    }
    
    .animate-slide-up {
      animation: slide-up 0.5s ease-out;
    }
    
    .page {
      display: none;
      animation: slide-up 0.5s ease-out;
    }
    
    .page.active {
      display: block;
    }
    
    .card-hover {
      transition: all 0.3s ease;
    }
    
    .card-hover:active {
      transform: translateY(-4px) scale(1.01);
    }
    
    .btn-bounce:active {
      transform: scale(0.98);
    }
    
    .input-focus {
      transition: all 0.3s ease;
    }
    
    .input-focus:focus {
      box-shadow: 0 0 0 3px rgba(255, 154, 139, 0.1);
    }
    
    .toast {
      position: fixed;
      bottom: 20px;
      left: 20px;
      right: 20px;
      z-index: 1000;
      animation: slide-up 0.3s ease-out;
    }
  </style>
</head>
<body class="h-full font-body overflow-auto">
  <div id="app-wrapper" class="w-full h-full">
    
    <!-- HOME PAGE -->
    <div id="home-page" class="page active w-full min-h-full" id="main-bg" style="background: linear-gradient(180deg, #FFF5E6 0%, #FFE4CC 50%, #FFDAB3 100%);">
      
      <!-- Navigation -->
      <nav class="sticky top-0 z-50 px-4 py-3" style="background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,255,255,0.8)); backdrop-filter: blur(10px);">
        <div class="flex justify-between items-center" id="nav-container" style="background: white; border-radius: 30px; padding: 8px 16px; box-shadow: 0 2px 10px rgba(255, 154, 139, 0.2);">
          <div class="flex items-center gap-2">
            <div class="animate-wiggle">
              <svg width="32" height="32" viewBox="0 0 45 45">
                <circle cx="22.5" cy="22.5" r="20" fill="#FF9A8B"/>
                <circle cx="16" cy="18" r="4" fill="white"/>
                <circle cx="29" cy="18" r="4" fill="white"/>
                <circle cx="16" cy="18" r="2" fill="#333"/>
                <circle cx="29" cy="18" r="2" fill="#333"/>
                <path d="M 15 28 Q 22.5 35 30 28" stroke="#333" stroke-width="2.5" fill="none" stroke-linecap="round"/>
              </svg>
            </div>
            <span class="font-display text-sm" id="nav-title" style="color: #FF6B6B;">KidsCare</span>
          </div>
          <button class="btn-bounce font-bold px-3 py-1 rounded-full text-xs transition-all" id="nav-btn" style="background: #FF9A8B; color: white;" onclick="showPage('register')">
            Daftar 📞
          </button>
        </div>
      </nav>
      
      <!-- Hero Section -->
      <section class="px-4 py-6 text-center">
        <div class="animate-float mb-4">
          <svg width="200" height="200" viewBox="0 0 200 200">
            <circle cx="100" cy="100" r="90" fill="#FFF5E6" stroke="#FF9A8B" stroke-width="3"/>
            
            <!-- Child 1 -->
            <circle cx="70" cy="90" r="22" fill="#FFD93D"/>
            <circle cx="62" cy="82" r="3" fill="#333"/>
            <circle cx="78" cy="82" r="3" fill="#333"/>
            <path d="M 62 95 Q 70 102 78 95" stroke="#333" stroke-width="2" fill="none" stroke-linecap="round"/>
            <path d="M 48 85 Q 70 60 92 85" stroke="#8B4513" stroke-width="5" fill="none" stroke-linecap="round"/>
            
            <!-- Child 2 -->
            <circle cx="130" cy="82" r="25" fill="#A8E6CF"/>
            <circle cx="118" cy="72" r="4" fill="#333"/>
            <circle cx="142" cy="72" r="4" fill="#333"/>
            <path d="M 115 88 Q 130 100 145 88" stroke="#333" stroke-width="2" fill="none" stroke-linecap="round"/>
            <circle cx="105" cy="65" r="8" fill="#333"/>
            <circle cx="155" cy="65" r="8" fill="#333"/>
            
            <!-- Heart -->
            <path d="M 100 140 C 100 133 108 133 108 140 C 108 133 116 133 116 140 C 116 155 108 162 108 162 C 108 162 100 155 100 140" fill="#FF6B6B"/>
          </svg>
        </div>
        <h1 class="font-display text-2xl mb-2" id="hero-title" style="color: #FF6B6B;">Klinik Tumbuh Kembang Si Kecil 🌟</h1>
        <p class="text-sm mb-6 leading-relaxed" id="hero-tagline" style="color: #666;">Tempat terbaik untuk memantau dan mendukung tumbuh kembang buah hati Anda dengan penuh kasih sayang! 💕</p>
      </section>
      
      <!-- Stats Section -->
      <section class="px-4 py-4">
        <div id="stats-container" style="background: white; border-radius: 20px; padding: 16px; box-shadow: 0 4px 20px rgba(255, 154, 139, 0.15);">
          <div class="grid grid-cols-2 gap-3 text-center">
            <div class="p-2">
              <div class="text-2xl mb-1">👶</div>
              <div class="font-display text-xl" id="stat-1" style="color: #FF6B6B;">5000+</div>
              <div class="text-xs" style="color: #666;">Pasien</div>
            </div>
            <div class="p-2">
              <div class="text-2xl mb-1">👨‍⚕️</div>
              <div class="font-display text-xl" id="stat-2" style="color: #A8E6CF;">15+</div>
              <div class="text-xs" style="color: #666;">Dokter</div>
            </div>
            <div class="p-2">
              <div class="text-2xl mb-1">🏆</div>
              <div class="font-display text-xl" id="stat-3" style="color: #FFD93D;">10</div>
              <div class="text-xs" style="color: #666;">Tahun</div>
            </div>
            <div class="p-2">
              <div class="text-2xl mb-1">⭐</div>
              <div class="font-display text-xl" id="stat-4" style="color: #DDA0DD;">4.9</div>
              <div class="text-xs" style="color: #666;">Rating</div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Services Section -->
      <section class="px-4 py-6">
        <h2 class="font-display text-xl text-center mb-4" id="services-title" style="color: #FF6B6B;">Layanan Kami 🎨</h2>
        <div class="space-y-3">
          <div class="card-hover rounded-2xl p-4 text-center" id="service-card-1" style="background: white; box-shadow: 0 4px 15px rgba(255, 154, 139, 0.12);">
            <div class="text-3xl mb-2">🧠</div>
            <h3 class="font-display text-sm" id="service-1-name" style="color: #FF6B6B;">Terapi Wicara</h3>
            <p class="text-xs mt-1" style="color: #666;">Kemampuan berbicara & komunikasi</p>
          </div>
          
          <div class="card-hover rounded-2xl p-4 text-center" id="service-card-2" style="background: white; box-shadow: 0 4px 15px rgba(168, 230, 207, 0.15);">
            <div class="text-3xl mb-2">🤸</div>
            <h3 class="font-display text-sm" id="service-2-name" style="color: #4CAF50;">Fisioterapi Anak</h3>
            <p class="text-xs mt-1" style="color: #666;">Kekuatan & koordinasi gerak</p>
          </div>
          
          <div class="card-hover rounded-2xl p-4 text-center" id="service-card-3" style="background: white; box-shadow: 0 4px 15px rgba(255, 217, 61, 0.12);">
            <div class="text-3xl mb-2">🧩</div>
            <h3 class="font-display text-sm" id="service-3-name" style="color: #FF9800;">Okupasi Terapi</h3>
            <p class="text-xs mt-1" style="color: #666;">Kemandirian aktivitas sehari-hari</p>
          </div>
          
          <div class="card-hover rounded-2xl p-4 text-center" id="service-card-4" style="background: white; box-shadow: 0 4px 15px rgba(221, 160, 221, 0.15);">
            <div class="text-3xl mb-2">💝</div>
            <h3 class="font-display text-sm" id="service-4-name" style="color: #9C27B0;">Konsultasi Psikolog</h3>
            <p class="text-xs mt-1" style="color: #666;">Perkembangan emosi & sosial</p>
          </div>
        </div>
      </section>
      
      <!-- About Section -->
      <section class="px-4 py-6">
        <div id="about-container" style="background: white; border-radius: 20px; padding: 16px; box-shadow: 0 4px 20px rgba(255, 154, 139, 0.12);">
          <h2 class="font-display text-lg mb-3" id="about-title" style="color: #FF6B6B;">Tentang Kami 💫</h2>
          <p class="text-xs mb-3 leading-relaxed" style="color: #666;">
            Klinik Tumbuh Kembang Anak kami hadir dengan misi memberikan layanan terbaik untuk mendukung setiap tahap perkembangan si kecil.
          </p>
          <p class="text-xs leading-relaxed" style="color: #666;">
            Dengan tim dokter dan terapis berpengalaman, fasilitas modern, dan suasana yang ramah anak, kami berkomitmen menjadi partner terpercaya para orang tua.
          </p>
        </div>
      </section>
      
      <!-- Testimonials -->
      <section class="px-4 py-6">
        <h2 class="font-display text-lg text-center mb-4" id="testimonials-title" style="color: #FF6B6B;">Kata Orang Tua 💬</h2>
        <div class="space-y-3">
          <div class="card-hover rounded-2xl p-3" style="background: white; box-shadow: 0 4px 15px rgba(255, 154, 139, 0.12);">
            <div class="flex gap-2 mb-2">
              <div class="w-8 h-8 rounded-full flex items-center justify-center text-xs" style="background: #FFE4CC;">👩</div>
              <div>
                <div class="text-xs font-bold" style="color: #333;">Ibu Sarah</div>
                <div class="text-xs" style="color: #999;">Mama Raffa</div>
              </div>
            </div>
            <p class="text-xs leading-relaxed" style="color: #666;">"Raffa sudah bisa berbicara lancar! 🥰"</p>
            <div class="mt-2 text-xs text-yellow-400">⭐⭐⭐⭐⭐</div>
          </div>
          
          <div class="card-hover rounded-2xl p-3" style="background: white; box-shadow: 0 4px 15px rgba(168, 230, 207, 0.15);">
            <div class="flex gap-2 mb-2">
              <div class="w-8 h-8 rounded-full flex items-center justify-center text-xs" style="background: #E8F5E9;">👨</div>
              <div>
                <div class="text-xs font-bold" style="color: #333;">Bapak Andi</div>
                <div class="text-xs" style="color: #999;">Papa Keyla</div>
              </div>
            </div>
            <p class="text-xs leading-relaxed" style="color: #666;">"Pelayanan ramah & profesional 💪"</p>
            <div class="mt-2 text-xs text-yellow-400">⭐⭐⭐⭐⭐</div>
          </div>
        </div>
      </section>
      
      <!-- Contact Section -->
      <section class="px-4 py-6">
        <div id="contact-container" style="background: linear-gradient(135deg, #FF9A8B, #FFECD2); border-radius: 20px; padding: 16px; box-shadow: 0 4px 20px rgba(255, 154, 139, 0.2);">
          <h2 class="font-display text-lg mb-4 text-center" style="color: white;">Hubungi Kami 📞</h2>
          <div class="space-y-3">
            <div class="rounded-2xl p-3 text-center" style="background: white;">
              <div class="text-2xl mb-1">📱</div>
              <div class="text-xs font-bold" style="color: #333;">Telepon</div>
              <div class="font-display text-xs" id="contact-phone" style="color: #FF6B6B;">0812-3456-7890</div>
            </div>
            
            <div class="rounded-2xl p-3 text-center" style="background: white;">
              <div class="text-2xl mb-1">📍</div>
              <div class="text-xs font-bold" style="color: #333;">Alamat</div>
              <div class="text-xs" id="contact-address" style="color: #666;">Jl. Kebahagiaan No. 123, Jakarta Selatan</div>
            </div>
            
            <div class="rounded-2xl p-2 text-center" style="background: rgba(255,255,255,0.9);">
              <div class="text-xs font-semibold" style="color: #666;">🕐 Senin-Sabtu: 08:00-20:00 | 🌟 Minggu: 09:00-15:00</div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- CTA Button -->
      <section class="px-4 py-6">
        <button class="btn-bounce w-full font-bold py-3 rounded-2xl text-white transition-all active:scale-95" id="home-cta-btn" style="background: linear-gradient(135deg, #FF9A8B, #FF6B6B); box-shadow: 0 4px 15px rgba(255, 107, 107, 0.3);" onclick="showPage('register')">
          Buat Janji Sekarang ✨
        </button>
      </section>
      
      <!-- Footer -->
      <footer class="px-4 py-4 text-center" id="footer-bg" style="background: #FF6B6B;">
        <div class="flex justify-center items-center gap-2 mb-2">
          <svg width="24" height="24" viewBox="0 0 45 45">
            <circle cx="22.5" cy="22.5" r="20" fill="white"/>
            <circle cx="16" cy="18" r="4" fill="#FF9A8B"/>
            <circle cx="29" cy="18" r="4" fill="#FF9A8B"/>
          </svg>
          <span class="font-display text-sm" id="footer-title" style="color: white;">KidsCare Clinic</span>
        </div>
        <p class="text-xs" style="color: rgba(255,255,255,0.8);">© 2024 Menemani tumbuh kembang si kecil 💕</p>
      </footer>
    </div>

    <!-- REGISTER PAGE -->
    <div id="register-page" class="page w-full min-h-full" id="register-bg" style="background: linear-gradient(180deg, #FFF5E6 0%, #FFE4CC 50%, #FFDAB3 100%);">
      
      <!-- Header -->
      <div class="sticky top-0 z-50 px-4 py-3" style="background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,255,255,0.8)); backdrop-filter: blur(10px);">
        <div style="background: white; border-radius: 30px; padding: 8px 16px; box-shadow: 0 2px 10px rgba(255, 154, 139, 0.2); display: flex; justify-content: space-between; align-items: center;">
          <button class="font-bold px-3 py-1 rounded-full text-xs" style="background: #F0F0F0; color: #333;" onclick="showPage('home')">
            ← Kembali
          </button>
          <span class="font-display text-sm" style="color: #FF6B6B;">Daftar Sekarang</span>
          <div style="width: 60px;"></div>
        </div>
      </div>
      
      <!-- Form Section -->
      <section class="px-4 py-6">
        <div style="background: white; border-radius: 20px; padding: 20px; box-shadow: 0 4px 20px rgba(255, 154, 139, 0.15);">
          
          <div class="text-center mb-6 animate-slide-up">
            <div class="text-4xl mb-2">📝</div>
            <h2 class="font-display text-lg mb-1" style="color: #FF6B6B;">Daftar Konsultasi</h2>
            <p class="text-xs" style="color: #666;">Isi data untuk membuat janji dengan dokter kami</p>
          </div>
          
          <form id="registration-form" style="display: flex; flex-direction: column; gap: 12px;">
            <!-- Nama Orang Tua -->
            <div>
              <label class="text-xs font-bold mb-1 block" style="color: #666;">👨‍👩 Nama Orang Tua</label>
              <input 
                type="text" 
                id="parent-name" 
                placeholder="Masukkan nama orang tua" 
                required
                class="input-focus w-full px-4 py-2 rounded-2xl border-2 text-sm focus:outline-none"
                style="border-color: #FFE4CC; background: #FFF9F5; color: #333;"
              >
            </div>
            
            <!-- Nama Anak -->
            <div>
              <label class="text-xs font-bold mb-1 block" style="color: #666;">👶 Nama Anak</label>
              <input 
                type="text" 
                id="child-name" 
                placeholder="Masukkan nama anak" 
                required
                class="input-focus w-full px-4 py-2 rounded-2xl border-2 text-sm focus:outline-none"
                style="border-color: #FFE4CC; background: #FFF9F5; color: #333;"
              >
            </div>
            
            <!-- Usia Anak -->
            <div>
              <label class="text-xs font-bold mb-1 block" style="color: #666;">🎂 Usia Anak</label>
              <select 
                id="child-age" 
                required
                class="input-focus w-full px-4 py-2 rounded-2xl border-2 text-sm focus:outline-none"
                style="border-color: #FFE4CC; background: #FFF9F5; color: #333;"
              >
                <option value="">-- Pilih Usia --</option>
                <option value="0-6 bulan">0-6 bulan</option>
                <option value="6-12 bulan">6-12 bulan</option>
                <option value="1-2 tahun">1-2 tahun</option>
                <option value="2-3 tahun">2-3 tahun</option>
                <option value="3-5 tahun">3-5 tahun</option>
                <option value="5+ tahun">5+ tahun</option>
              </select>
            </div>
            
            <!-- Nomor Telepon -->
            <div>
              <label class="text-xs font-bold mb-1 block" style="color: #666;">📱 Nomor Telepon</label>
              <input 
                type="tel" 
                id="phone" 
                placeholder="Masukkan nomor telepon" 
                required
                class="input-focus w-full px-4 py-2 rounded-2xl border-2 text-sm focus:outline-none"
                style="border-color: #FFE4CC; background: #FFF9F5; color: #333;"
              >
            </div>
            
            <!-- Pilih Layanan -->
            <div>
              <label class="text-xs font-bold mb-1 block" style="color: #666;">🎨 Pilih Layanan</label>
              <select 
                id="service" 
                required
                class="input-focus w-full px-4 py-2 rounded-2xl border-2 text-sm focus:outline-none"
                style="border-color: #FFE4CC; background: #FFF9F5; color: #333;"
              >
                <option value="">-- Pilih Layanan --</option>
                <option value="Terapi Wicara">🧠 Terapi Wicara</option>
                <option value="Fisioterapi Anak">🤸 Fisioterapi Anak</option>
                <option value="Okupasi Terapi">🧩 Okupasi Terapi</option>
                <option value="Konsultasi Psikolog">💝 Konsultasi Psikolog</option>
              </select>
            </div>
            
            <!-- Catatan -->
            <div>
              <label class="text-xs font-bold mb-1 block" style="color: #666;">📋 Catatan Tambahan</label>
              <textarea 
                id="notes" 
            <!DOCTYPE html>
<html lang="id" class="h-full">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Klinik Tumbuh Kembang Anak</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&family=Fredoka+One&display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
    }
    
    .font-display {
      font-family: 'Fredoka One', cursive;
    }
    
    .font-body {
      font-family: 'Nunito', sans-serif;
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }
    
    @keyframes wiggle {
      0%, 100% { transform: rotate(-3deg); }
      50% { transform: rotate(3deg); }
    }
    
    @keyframes bounce-slow {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }
    
    .animate-float {
      animation: float 3s ease-in-out infinite;
    }
    
    .animate-wiggle {
      animation: wiggle 2s ease-in-out infinite;
    }
    
    .animate-bounce-slow {
      animation: bounce-slow 2s ease-in-out infinite;
    }
    
    .cloud {
      position: absolute;
      opacity: 0.6;
    }
    
    .bubble {
      position: absolute;
      border-radius: 50%;
      opacity: 0.3;
    }
    
    .card-hover {
      transition: all 0.3s ease;
    }
    
    .card-hover:hover {
      transform: translateY(-8px) scale(1.02);
    }
    
    .btn-bounce:hover {
      animation: bounce-slow 0.5s ease-in-out;
    }
  </style>
</head>
<body class="h-full font-body overflow-auto">
  <div id="app-wrapper" class="w-full h-full">
    <!-- Background dengan pattern lucu -->
    <div class="min-h-full w-full relative" id="main-bg" style="background: linear-gradient(180deg, #FFF5E6 0%, #FFE4CC 50%, #FFDAB3 100%);">
      
      <!-- Decorative elements -->
      <div class="absolute inset-0 overflow-hidden pointer-events-none">
        <!-- Clouds -->
        <svg class="cloud animate-float" style="top: 5%; left: 5%; width: 120px;" viewBox="0 0 100 60">
          <ellipse cx="30" cy="40" rx="25" ry="15" fill="white"/>
          <ellipse cx="50" cy="35" rx="30" ry="20" fill="white"/>
          <ellipse cx="75" cy="40" rx="20" ry="12" fill="white"/>
        </svg>
        <svg class="cloud animate-float" style="top: 8%; right: 10%; width: 100px; animation-delay: 1s;" viewBox="0 0 100 60">
          <ellipse cx="30" cy="40" rx="25" ry="15" fill="white"/>
          <ellipse cx="50" cy="35" rx="30" ry="20" fill="white"/>
          <ellipse cx="75" cy="40" rx="20" ry="12" fill="white"/>
        </svg>
        
        <!-- Bubbles -->
        <div class="bubble animate-bounce-slow" style="top: 20%; left: 8%; width: 30px; height: 30px; background: #FF9A8B;"></div>
        <div class="bubble animate-bounce-slow" style="top: 40%; right: 5%; width: 20px; height: 20px; background: #A8E6CF; animation-delay: 0.5s;"></div>
        <div class="bubble animate-bounce-slow" style="top: 60%; left: 3%; width: 25px; height: 25px; background: #88D8B0; animation-delay: 1s;"></div>
        <div class="bubble animate-bounce-slow" style="bottom: 20%; right: 8%; width: 35px; height: 35px; background: #FFEAA7; animation-delay: 1.5s;"></div>
      </div>
      
      <!-- Navigation -->
      <nav class="relative z-10 px-4 py-4">
        <div class="max-w-6xl mx-auto flex justify-between items-center" id="nav-container" style="background: #FFFFFF; border-radius: 50px; padding: 12px 24px; box-shadow: 0 4px 20px rgba(255, 154, 139, 0.2);">
          <div class="flex items-center gap-3">
            <div class="animate-wiggle">
              <svg width="45" height="45" viewBox="0 0 45 45">
                <circle cx="22.5" cy="22.5" r="20" fill="#FF9A8B"/>
                <circle cx="16" cy="18" r="4" fill="white"/>
                <circle cx="29" cy="18" r="4" fill="white"/>
                <circle cx="16" cy="18" r="2" fill="#333"/>
                <circle cx="29" cy="18" r="2" fill="#333"/>
                <path d="M 15 28 Q 22.5 35 30 28" stroke="#333" stroke-width="2.5" fill="none" stroke-linecap="round"/>
                <ellipse cx="10" cy="24" rx="3" ry="2" fill="#FFB6B0"/>
                <ellipse cx="35" cy="24" rx="3" ry="2" fill="#FFB6B0"/>
              </svg>
            </div>
            <span class="font-display text-xl" id="nav-title" style="color: #FF6B6B;">KidsCare</span>
          </div>
          <div class="hidden md:flex gap-6">
            <a href="#home" class="font-semibold hover:scale-110 transition-transform" id="nav-home" style="color: #666;">Beranda</a>
            <a href="#layanan" class="font-semibold hover:scale-110 transition-transform" id="nav-services" style="color: #666;">Layanan</a>
            <a href="#tentang" class="font-semibold hover:scale-110 transition-transform" id="nav-about" style="color: #666;">Tentang</a>
            <a href="#kontak" class="font-semibold hover:scale-110 transition-transform" id="nav-contact" style="color: #666;">Kontak</a>
          </div>
          <button class="btn-bounce font-bold px-5 py-2 rounded-full transition-all hover:shadow-lg" id="nav-btn" style="background: #FF9A8B; color: white;">
            Daftar 📞
          </button>
        </div>
      </nav>
      
      <!-- Hero Section -->
      <section id="home" class="relative z-10 px-4 py-12 md:py-20">
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center gap-8">
          <div class="flex-1 text-center md:text-left">
            <h1 class="font-display text-4xl md:text-5xl lg:text-6xl mb-4 leading-tight" id="hero-title" style="color: #FF6B6B;">
              Klinik Tumbuh Kembang Si Kecil 🌟
            </h1>
            <p class="text-lg md:text-xl mb-8 leading-relaxed" id="hero-tagline" style="color: #666;">
              Tempat terbaik untuk memantau dan mendukung tumbuh kembang buah hati Anda dengan penuh kasih sayang! 💕
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
              <button class="btn-bounce font-bold px-8 py-4 rounded-full text-lg transition-all hover:shadow-xl transform hover:scale-105" id="hero-btn-primary" style="background: #FF9A8B; color: white;">
                Buat Janji Sekarang ✨
              </button>
              <button class="btn-bounce font-bold px-8 py-4 rounded-full text-lg transition-all hover:shadow-xl transform hover:scale-105" id="hero-btn-secondary" style="background: white; color: #FF6B6B; border: 3px solid #FF9A8B;">
                Lihat Layanan 📋
              </button>
            </div>
          </div>
          <div class="flex-1 flex justify-center">
            <div class="relative">
              <div class="animate-float">
                <svg width="320" height="320" viewBox="0 0 320 320">
                  <!-- Main circle background -->
                  <circle cx="160" cy="160" r="140" fill="#FFF5E6" stroke="#FF9A8B" stroke-width="4"/>
                  
                  <!-- Happy kids illustration -->
                  <!-- Child 1 -->
                  <circle cx="110" cy="150" r="35" fill="#FFD93D"/>
                  <circle cx="100" cy="142" r="5" fill="#333"/>
                  <circle cx="120" cy="142" r="5" fill="#333"/>
                  <path d="M 100 158 Q 110 168 120 158" stroke="#333" stroke-width="3" fill="none" stroke-linecap="round"/>
                  <ellipse cx="90" cy="152" rx="4" ry="3" fill="#FFB6B0"/>
                  <ellipse cx="130" cy="152" rx="4" ry="3" fill="#FFB6B0"/>
                  <!-- Hair -->
                  <path d="M 80 130 Q 110 100 140 130" stroke="#8B4513" stroke-width="8" fill="none" stroke-linecap="round"/>
                  
                  <!-- Child 2 -->
                  <circle cx="200" cy="140" r="38" fill="#A8E6CF"/>
                  <circle cx="188" cy="130" r="6" fill="#333"/>
                  <circle cx="212" cy="130" r="6" fill="#333"/>
                  <path d="M 185 150 Q 200 165 215 150" stroke="#333" stroke-width="3" fill="none" stroke-linecap="round"/>
                  <ellipse cx="172" cy="142" rx="5" ry="3" fill="#FFB6B0"/>
                  <ellipse cx="228" cy="142" rx="5" ry="3" fill="#FFB6B0"/>
                  <!-- Pigtails -->
                  <circle cx="165" cy="115" r="12" fill="#333"/>
                  <circle cx="235" cy="115" r="12" fill="#333"/>
                  
                  <!-- Child 3 (smaller, in front) -->
                  <circle cx="155" cy="210" r="30" fill="#DDA0DD"/>
                  <circle cx="145" cy="202" r="5" fill="#333"/>
                  <circle cx="165" cy="202" r="5" fill="#333"/>
                  <ellipse cx="155" cy="218" rx="8" ry="5" fill="#FF9A8B"/>
                  <ellipse cx="132" cy="210" rx="4" ry="3" fill="#FFB6B0"/>
                  <ellipse cx="178" cy="210" rx="4" ry="3" fill="#FFB6B0"/>
                  
                  <!-- Stars around -->
                  <path d="M 60 80 L 63 90 L 73 90 L 65 96 L 68 106 L 60 100 L 52 106 L 55 96 L 47 90 L 57 90 Z" fill="#FFD93D"/>
                  <path d="M 250 70 L 252 77 L 259 77 L 254 81 L 256 88 L 250 84 L 244 88 L 246 81 L 241 77 L 248 77 Z" fill="#FF9A8B"/>
                  <path d="M 270 200 L 272 207 L 279 207 L 274 211 L 276 218 L 270 214 L 264 218 L 266 211 L 261 207 L 268 207 Z" fill="#A8E6CF"/>
                  
                  <!-- Hearts -->
                  <path d="M 80 250 C 80 240 95 240 95 250 C 95 240 110 240 110 250 C 110 270 95 280 95 280 C 95 280 80 270 80 250" fill="#FF6B6B"/>
                  <path d="M 220 250 C 220 243 230 243 230 250 C 230 243 240 243 240 250 C 240 262 230 270 230 270 C 230 270 220 262 220 250" fill="#FF9A8B"/>
                </svg>
              </div>
              
              <!-- Floating badges -->
              <div class="absolute -top-2 -right-2 animate-bounce-slow" id="badge-1" style="background: white; padding: 8px 16px; border-radius: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.1);">
                <span class="font-bold" style="color: #FF6B6B;">⭐ Terpercaya</span>
              </div>
              <div class="absolute -bottom-2 -left-2 animate-bounce-slow" style="animation-delay: 0.5s;" id="badge-2">
                <div style="background: white; padding: 8px 16px; border-radius: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.1);">
                  <span class="font-bold" style="color: #A8E6CF;">💚 Ramah Anak</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Stats Section -->
      <section class="relative z-10 px-4 py-12">
        <div class="max-w-4xl mx-auto" id="stats-container" style="background: white; border-radius: 30px; padding: 32px; box-shadow: 0 10px 40px rgba(255, 154, 139, 0.15);">
          <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
            <div class="card-hover p-4">
              <div class="text-4xl mb-2">👶</div>
              <div class="font-display text-3xl" id="stat-1" style="color: #FF6B6B;">5000+</div>
              <div class="font-semibold" style="color: #666;">Pasien Bahagia</div>
            </div>
            <div class="card-hover p-4">
              <div class="text-4xl mb-2">👨‍⚕️</div>
              <div class="font-display text-3xl" id="stat-2" style="color: #A8E6CF;">15+</div>
              <div class="font-semibold" style="color: #666;">Dokter Spesialis</div>
            </div>
            <div class="card-hover p-4">
              <div class="text-4xl mb-2">🏆</div>
              <div class="font-display text-3xl" id="stat-3" style="color: #FFD93D;">10</div>
              <div class="font-semibold" style="color: #666;">Tahun Pengalaman</div>
            </div>
            <div class="card-hover p-4">
              <div class="text-4xl mb-2">⭐</div>
              <div class="font-display text-3xl" id="stat-4" style="color: #DDA0DD;">4.9</div>
              <div class="font-semibold" style="color: #666;">Rating Kepuasan</div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Services Section -->
      <section id="layanan" class="relative z-10 px-4 py-16">
        <div class="max-w-6xl mx-auto">
          <div class="text-center mb-12">
            <h2 class="font-display text-3xl md:text-4xl mb-4" id="services-title" style="color: #FF6B6B;">Layanan Kami 🎨</h2>
            <p class="text-lg max-w-2xl mx-auto" style="color: #666;">Berbagai layanan lengkap untuk mendukung tumbuh kembang optimal si kecil</p>
          </div>
          
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
            <!-- Service 1 -->
            <div class="card-hover rounded-3xl p-6 text-center" id="service-card-1" style="background: white; box-shadow: 0 8px 30px rgba(255, 154, 139, 0.15);">
              <div class="w-20 h-20 mx-auto mb-4 rounded-full flex items-center justify-center animate-wiggle" style="background: linear-gradient(135deg, #FF9A8B, #FFECD2);">
                <span class="text-4xl">🧠</span>
              </div>
              <h3 class="font-display text-xl mb-3" id="service-1-name" style="color: #FF6B6B;">Terapi Wicara</h3>
              <p class="text-sm" style="color: #666;">Membantu anak mengembangkan kemampuan berbicara dan komunikasi dengan metode yang menyenangkan</p>
            </div>
            
            <!-- Service 2 -->
            <div class="card-hover rounded-3xl p-6 text-center" id="service-card-2" style="background: white; box-shadow: 0 8px 30px rgba(168, 230, 207, 0.2);">
              <div class="w-20 h-20 mx-auto mb-4 rounded-full flex items-center justify-center animate-wiggle" style="background: linear-gradient(135deg, #A8E6CF, #DCEDC1); animation-delay: 0.2s;">
                <span class="text-4xl">🤸</span>
              </div>
              <h3 class="font-display text-xl mb-3" id="service-2-name" style="color: #4CAF50;">Fisioterapi Anak</h3>
              <p class="text-sm" style="color: #666;">Terapi motorik untuk meningkatkan kekuatan dan koordinasi gerak tubuh anak</p>
            </div>
            
            <!-- Service 3 -->
            <div class="card-hover rounded-3xl p-6 text-center" id="service-card-3" style="background: white; box-shadow: 0 8px 30px rgba(255, 217, 61, 0.15);">
              <div class="w-20 h-20 mx-auto mb-4 rounded-full flex items-center justify-center animate-wiggle" style="background: linear-gradient(135deg, #FFD93D, #FFF5CC); animation-delay: 0.4s;">
                <span class="text-4xl">🧩</span>
              </div>
              <h3 class="font-display text-xl mb-3" id="service-3-name" style="color: #FF9800;">Okupasi Terapi</h3>
              <p class="text-sm" style="color: #666;">Melatih kemandirian anak dalam aktivitas sehari-hari dengan cara yang interaktif</p>
            </div>
            
            <!-- Service 4 -->
            <div class="card-hover rounded-3xl p-6 text-center" id="service-card-4" style="background: white; box-shadow: 0 8px 30px rgba(221, 160, 221, 0.2);">
              <div class="w-20 h-20 mx-auto mb-4 rounded-full flex items-center justify-center animate-wiggle" style="background: linear-gradient(135deg, #DDA0DD, #F8E8F8); animation-delay: 0.6s;">
                <span class="text-4xl">💝</span>
              </div>
              <h3 class="font-display text-xl mb-3" id="service-4-name" style="color: #9C27B0;">Konsultasi Psikolog</h3>
              <p class="text-sm" style="color: #666;">Pendampingan psikologis untuk perkembangan emosi dan sosial anak yang sehat</p>
            </div>
          </div>
        </div>
      </section>
      
      <!-- About Section -->
      <section id="tentang" class="relative z-10 px-4 py-16">
        <div class="max-w-6xl mx-auto">
          <div class="rounded-3xl overflow-hidden" id="about-container" style="background: white; box-shadow: 0 10px 40px rgba(255, 154, 139, 0.15);">
            <div class="grid md:grid-cols-2">
              <div class="p-8 md:p-12 flex flex-col justify-center">
                <h2 class="font-display text-3xl md:text-4xl mb-6" id="about-title" style="color: #FF6B6B;">Tentang Kami 💫</h2>
                <p class="mb-4 leading-relaxed" style="color: #666;">
                  Klinik Tumbuh Kembang Anak kami hadir dengan misi memberikan layanan terbaik untuk mendukung setiap tahap perkembangan si kecil.
                </p>
                <p class="mb-6 leading-relaxed" style="color: #666;">
                  Dengan tim dokter dan terapis berpengalaman, fasilitas modern, dan suasana yang ramah anak, kami berkomitmen menjadi partner terpercaya para orang tua.
                </p>
                <div class="flex flex-wrap gap-4">
                  <div class="flex items-center gap-2 px-4 py-2 rounded-full" style="background: #FFF5E6;">
                    <span>✅</span>
                    <span class="font-semibold text-sm" style="color: #666;">Tim Profesional</span>
                  </div>
                  <div class="flex items-center gap-2 px-4 py-2 rounded-full" style="background: #E8F5E9;">
                    <span>✅</span>
                    <span class="font-semibold text-sm" style="color: #666;">Fasilitas Modern</span>
                  </div>
                  <div class="flex items-center gap-2 px-4 py-2 rounded-full" style="background: #FCE4EC;">
                    <span>✅</span>
                    <span class="font-semibold text-sm" style="color: #666;">Ramah Anak</span>
                  </div>
                </div>
              </div>
              <div class="flex items-center justify-center p-8" style="background: linear-gradient(135deg, #FFF5E6, #FFE4CC);">
                <svg width="280" height="280" viewBox="0 0 280 280" class="animate-float">
                  <!-- Hospital building -->
                  <rect x="60" y="100" width="160" height="140" rx="15" fill="white" stroke="#FF9A8B" stroke-width="3"/>
                  
                  <!-- Roof -->
                  <path d="M 40 110 L 140 40 L 240 110" stroke="#FF6B6B" stroke-width="6" fill="none" stroke-linecap="round" stroke-linejoin="round"/>
                  
                  <!-- Windows -->
                  <rect x="80" y="130" width="35" height="35" rx="8" fill="#A8E6CF"/>
                  <rect x="165" y="130" width="35" height="35" rx="8" fill="#FFD93D"/>
                  
                  <!-- Door -->
                  <rect x="115" y="180" width="50" height="60" rx="10" fill="#FF9A8B"/>
                  <circle cx="155" cy="215" r="4" fill="white"/>
                  
                  <!-- Cross symbol -->
                  <rect x="130" y="60" width="20" height="40" rx="3" fill="#FF6B6B"/>
                  <rect x="120" y="70" width="40" height="20" rx="3" fill="#FF6B6B"/>
                  
                  <!-- Cute elements -->
                  <circle cx="97" cy="147" r="8" fill="white"/>
                  <circle cx="94" cy="145" r="2" fill="#333"/>
                  <circle cx="100" cy="145" r="2" fill="#333"/>
                  <path d="M 93 151 Q 97 155 101 151" stroke="#333" stroke-width="1.5" fill="none"/>
                  
                  <circle cx="182" cy="147" r="8" fill="white"/>
                  <circle cx="179" cy="145" r="2" fill="#333"/>
                  <circle cx="185" cy="145" r="2" fill="#333"/>
                  <path d="M 178 151 Q 182 155 186 151" stroke="#333" stroke-width="1.5" fill="none"/>
                  
                  <!-- Hearts -->
                  <path d="M 50 180 C 50 173 58 173 58 180 C 58 173 66 173 66 180 C 66 190 58 196 58 196 C 58 196 50 190 50 180" fill="#FF9A8B" opacity="0.7"/>
                  <path d="M 220 160 C 220 155 226 155 226 160 C 226 155 232 155 232 160 C 232 168 226 172 226 172 C 226 172 220 168 220 160" fill="#DDA0DD" opacity="0.7"/>
                </svg>
              </div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Testimonials -->
      <section class="relative z-10 px-4 py-16">
        <div class="max-w-6xl mx-auto">
          <h2 class="font-display text-3xl md:text-4xl text-center mb-12" id="testimonials-title" style="color: #FF6B6B;">Kata Orang Tua 💬</h2>
          
          <div class="grid md:grid-cols-3 gap-6">
            <div class="card-hover rounded-3xl p-6" style="background: white; box-shadow: 0 8px 30px rgba(255, 154, 139, 0.12);">
              <div class="flex items-center gap-3 mb-4">
                <div class="w-14 h-14 rounded-full flex items-center justify-center text-2xl" style="background: #FFE4CC;">👩</div>
                <div>
                  <div class="font-bold" style="color: #333;">Ibu Sarah</div>
                  <div class="text-sm" style="color: #999;">Mama Raffa</div>
                </div>
              </div>
              <p class="text-sm leading-relaxed" style="color: #666;">"Raffa sekarang sudah bisa berbicara dengan lancar setelah terapi di sini. Terima kasih banyak! 🥰"</p>
              <div class="mt-4 text-yellow-400">⭐⭐⭐⭐⭐</div>
            </div>
            
            <div class="card-hover rounded-3xl p-6" style="background: white; box-shadow: 0 8px 30px rgba(168, 230, 207, 0.15);">
              <div class="flex items-center gap-3 mb-4">
                <div class="w-14 h-14 rounded-full flex items-center justify-center text-2xl" style="background: #E8F5E9;">👨</div>
                <div>
                  <div class="font-bold" style="color: #333;">Bapak Andi</div>
                  <div class="text-sm" style="color: #999;">Papa Keyla</div>
                </div>
              </div>
              <p class="text-sm leading-relaxed" style="color: #666;">"Pelayanan sangat ramah dan profesional. Keyla sangat senang setiap kali terapi. 💪"</p>
              <div class="mt-4 text-yellow-400">⭐⭐⭐⭐⭐</div>
            </div>
            
            <div class="card-hover rounded-3xl p-6" style="background: white; box-shadow: 0 8px 30px rgba(221, 160, 221, 0.15);">
              <div class="flex items-center gap-3 mb-4">
                <div class="w-14 h-14 rounded-full flex items-center justify-center text-2xl" style="background: #FCE4EC;">👩</div>
                <div>
                  <div class="font-bold" style="color: #333;">Ibu Maya</div>
                  <div class="text-sm" style="color: #999;">Mama Dimas</div>
                </div>
              </div>
              <p class="text-sm leading-relaxed" style="color: #666;">"Perkembangan Dimas sangat pesat. Dokternya sabar dan penuh perhatian. Highly recommended! ❤️"</p>
              <div class="mt-4 text-yellow-400">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Contact Section -->
      <section id="kontak" class="relative z-10 px-4 py-16">
        <div class="max-w-4xl mx-auto">
          <div class="rounded-3xl p-8 md:p-12" id="contact-container" style="background: linear-gradient(135deg, #FF9A8B, #FFECD2); box-shadow: 0 10px 40px rgba(255, 154, 139, 0.3);">
            <div class="text-center mb-8">
              <h2 class="font-display text-3xl md:text-4xl mb-4" style="color: white;">Hubungi Kami 📞</h2>
              <p class="text-lg" style="color: rgba(255,255,255,0.9);">Kami siap membantu tumbuh kembang si kecil!</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-6">
              <div class="rounded-2xl p-6 text-center" style="background: white;">
                <div class="text-4xl mb-3">📱</div>
                <div class="font-bold mb-2" style="color: #333;">Telepon / WhatsApp</div>
                <div class="font-display text-xl" id="contact-phone" style="color: #FF6B6B;">0812-3456-7890</div>
              </div>
              
              <div class="rounded-2xl p-6 text-center" style="background: white;">
                <div class="text-4xl mb-3">📍</div>
                <div class="font-bold mb-2" style="color: #333;">Alamat Klinik</div>
                <div class="text-sm" id="contact-address" style="color: #666;">Jl. Kebahagiaan No. 123, Jakarta Selatan</div>
              </div>
            </div>
            
            <div class="mt-8 text-center">
              <div class="inline-flex flex-wrap justify-center gap-4">
                <div class="rounded-full px-4 py-2" style="background: rgba(255,255,255,0.9);">
                  <span class="font-semibold text-sm" style="color: #666;">🕐 Senin - Sabtu: 08.00 - 20.00</span>
                </div>
                <div class="rounded-full px-4 py-2" style="background: rgba(255,255,255,0.9);">
                  <span class="font-semibold text-sm" style="color: #666;">🌟 Minggu: 09.00 - 15.00</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Footer -->
      <footer class="relative z-10 px-4 py-8" id="footer-bg" style="background: #FF6B6B;">
        <div class="max-w-6xl mx-auto text-center">
          <div class="flex justify-center items-center gap-3 mb-4">
            <svg width="35" height="35" viewBox="0 0 45 45">
              <circle cx="22.5" cy="22.5" r="20" fill="white"/>
              <circle cx="16" cy="18" r="4" fill="#FF9A8B"/>
              <circle cx="29" cy="18" r="4" fill="#FF9A8B"/>
              <circle cx="16" cy="18" r="2" fill="#333"/>
              <circle cx="29" cy="18" r="2" fill="#333"/>
              <path d="M 15 28 Q 22.5 35 30 28" stroke="#333" stroke-width="2.5" fill="none" stroke-linecap="round"/>
            </svg>
            <span class="font-display text-xl" id="footer-title" style="color: white;">KidsCare Clinic</span>
          </div>
          <p class="text-sm mb-4" style="color: rgba(255,255,255,0.8);">Menemani tumbuh kembang si kecil dengan penuh cinta 💕</p>
          <div class="flex justify-center gap-4 mb-4">
            <a href="#" class="w-10 h-10 rounded-full flex items-center justify-center transition-transform hover:scale-110" style="background: white;">
              <span style="color: #FF6B6B;">📘</span>
            </a>
            <a href="#" class="w-10 h-10 rounded-full flex items-center justify-center transition-transform hover:scale-110" style="background: white;">
              <span style="color: #FF6B6B;">📸</span>
            </a>
            <a href="#" class="w-10 h-10 rounded-full flex items-center justify-center transition-transform hover:scale-110" style="background: white;">
              <span style="color: #FF6B6B;">📺</span>
            </a>
          </div>
          <p class="text-xs" style="color: rgba(255,255,255,0.6);">© 2024 KidsCare Clinic. Hak Cipta Dilindungi.</p>
        </div>
      </footer>
    </div>
  </div>

  <script>
    const defaultConfig = {
      clinic_name: "KidsCare",
      tagline: "Tempat terbaik untuk memantau dan mendukung tumbuh kembang buah hati Anda dengan penuh kasih sayang! 💕",
      service_1_title: "Terapi Wicara",
      service_2_title: "Fisioterapi Anak",
      service_3_title: "Okupasi Terapi",
      service_4_title: "Konsultasi Psikolog",
      phone_number: "0812-3456-7890",
      address: "Jl. Kebahagiaan No. 123, Jakarta Selatan",
      background_color: "#FFF5E6",
      surface_color: "#FFFFFF",
      text_color: "#666666",
      primary_action_color: "#FF9A8B",
      secondary_action_color: "#FF6B6B",
      font_family: "Nunito",
      font_size: 16
    };

    async function onConfigChange(config) {
      const c = { ...defaultConfig, ...config };
      
      // Update text content
      document.getElementById('nav-title').textContent = c.clinic_name;
      document.getElementById('hero-title').innerHTML = `Klinik Tumbuh Kembang Si Kecil 🌟`;
      document.getElementById('hero-tagline').textContent = c.tagline;
      document.getElementById('service-1-name').textContent = c.service_1_title;
      document.getElementById('service-2-name').textContent = c.service_2_title;
      document.getElementById('service-3-name').textContent = c.service_3_title;
      document.getElementById('service-4-name').textContent = c.service_4_title;
      document.getElementById('contact-phone').textContent = c.phone_number;
      document.getElementById('contact-address').textContent = c.address;
      document.getElementById('footer-title').textContent = c.clinic_name + " Clinic";
      
      // Update colors - Background
      document.getElementById('main-bg').style.background = `linear-gradient(180deg, ${c.background_color} 0%, ${adjustColor(c.background_color, -10)} 50%, ${adjustColor(c.background_color, -20)} 100%)`;
      
      // Update colors - Surface
      document.getElementById('nav-container').style.background = c.surface_color;
      document.getElementById('stats-container').style.background = c.surface_color;
      document.getElementById('service-card-1').style.background = c.surface_color;
      document.getElementById('service-card-2').style.background = c.surface_color;
      document.getElementById('service-card-3').style.background = c.surface_color;
      document.getElementById('service-card-4').style.background = c.surface_color;
      document.getElementById('about-container').style.background = c.surface_color;
      
      // Update colors - Text
      document.getElementById('hero-tagline').style.color = c.text_color;
      
      // Update colors - Primary Action
      document.getElementById('nav-btn').style.background = c.primary_action_color;
      document.getElementById('hero-btn-primary').style.background = c.primary_action_color;
      document.getElementById('hero-btn-secondary').style.borderColor = c.primary_action_color;
      document.getElementById('contact-container').style.background = `linear-gradient(135deg, ${c.primary_action_color}, ${adjustColor(c.primary_action_color, 40)})`;
      
      // Update colors - Secondary Action (headings, accent elements)
      document.getElementById('nav-title').style.color = c.secondary_action_color;
      document.getElementById('hero-title').style.color = c.secondary_action_color;
      document.getElementById('hero-btn-secondary').style.color = c.secondary_action_color;
      document.getElementById('services-title').style.color = c.secondary_action_color;
      document.getElementById('about-title').style.color = c.secondary_action_color;
      document.getElementById('testimonials-title').style.color = c.secondary_action_color;
      document.getElementById('footer-bg').style.background = c.secondary_action_color;
      document.getElementById('contact-phone').style.color = c.secondary_action_color;
      document.getElementById('service-1-name').style.color = c.secondary_action_color;
      
      // Update fonts
      const fontStack = `${c.font_family}, Nunito, sans-serif`;
      document.body.style.fontFamily = fontStack;
      
      // Update font sizes proportionally
      const baseSize = c.font_size;
      document.getElementById('hero-title').style.fontSize = `${baseSize * 3}px`;
      document.getElementById('hero-tagline').style.fontSize = `${baseSize * 1.25}px`;
      document.getElementById('services-title').style.fontSize = `${baseSize * 2}px`;
      document.getElementById('about-title').style.fontSize = `${baseSize * 2}px`;
      document.getElementById('testimonials-title').style.fontSize = `${baseSize * 2}px`;
    }
    
    function adjustColor(hex, amount) {
      const num = parseInt(hex.replace('#', ''), 16);
      const r = Math.min(255, Math.max(0, (num >> 16) + amount));
      const g = Math.min(255, Math.max(0, ((num >> 8) & 0x00FF) + amount));
      const b = Math.min(255, Math.max(0, (num & 0x0000FF) + amount));
      return `#${((r << 16) | (g << 8) | b).toString(16).padStart(6, '0')}`;
    }

    function mapToCapabilities(config) {
      const c = { ...defaultConfig, ...config };
      return {
        recolorables: [
          {
            get: () => c.background_color,
            set: (value) => {
              c.background_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ background_color: value });
            }
          },
          {
            get: () => c.surface_color,
            set: (value) => {
              c.surface_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ surface_color: value });
            }
          },
          {
            get: () => c.text_color,
            set: (value) => {
              c.text_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ text_color: value });
            }
          },
          {
            get: () => c.primary_action_color,
            set: (value) => {
              c.primary_action_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ primary_action_color: value });
            }
          },
          {
            get: () => c.secondary_action_color,
            set: (value) => {
              c.secondary_action_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ secondary_action_color: value });
            }
          }
        ],
        borderables: [],
        fontEditable: {
          get: () => c.font_family,
          set: (value) => {
            c.font_family = value;
            if (window.elementSdk) window.elementSdk.setConfig({ font_family: value });
          }
        },
        fontSizeable: {
          get: () => c.font_size,
          set: (value) => {
            c.font_size = value;
            if (window.elementSdk) window.elementSdk.setConfig({ font_size: value });
          }
        }
      };
    }

    function mapToEditPanelValues(config) {
      const c = { ...defaultConfig, ...config };
      return new Map([
        ["clinic_name", c.clinic_name],
        ["tagline", c.tagline],
        ["service_1_title", c.service_1_title],
        ["service_2_title", c.service_2_title],
        ["service_3_title", c.service_3_title],
        ["service_4_title", c.service_4_title],
        ["phone_number", c.phone_number],
        ["address", c.address]
      ]);
    }

    // Initialize SDK
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities,
        mapToEditPanelValues
      });
    } else {
      onConfigChange(defaultConfig);
    }

    // Smooth scrolling for navigation
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      });
    });
  </script>
</body>
</html>
    placeholder="Masukkan catatan atau keluhan (opsional)" 
                rows="3"
                class="input-focus w-full px-4 py-2 rounded-2xl border-2 text-sm focus:outline-none resize-none"
                style="border-color: #FFE4CC; background: #FFF9F5; color: #333;"
              ></textarea>
            </div>
            
            <!-- Loading State -->
            <div id="loading-state" style="display: none; text-align: center; padding: 12px;">
              <div style="display: inline-block; width: 20px; height: 20px; border: 3px solid #FFE4CC; border-top-color: #FF9A8B; border-radius: 50%; animation: spin 1s linear infinite;"></div>
              <p class="text-xs mt-2" style="color: #666;">Sedang memproses...</p>
            </div>
            
            <!-- Submit Button -->
            <button 
              type="submit" 
              id="submit-btn"
              class="btn-bounce w-full font-bold py-3 rounded-2xl text-white transition-all active:scale-95 mt-2"
              style="background: linear-gradient(135deg, #FF9A8B, #FF6B6B); box-shadow: 0 4px 15px rgba(255, 107, 107, 0.3);"
            >
              Daftar Sekarang ✨
            </button>
          </form>
          
          <!-- Success Message -->
          <div id="success-message" style="display: none; text-align: center; padding: 16px; background: #E8F5E9; border-radius: 16px; margin-top: 16px;">
            <div style="font-size: 32px; margin-bottom: 8px;">✅</div>
            <h3 class="font-bold text-sm mb-2" style="color: #4CAF50;">Pendaftaran Berhasil!</h3>
            <p class="text-xs mb-4" style="color: #666;">Kami akan segera menghubungi Anda untuk mengkonfirmasi janji konsultasi.</p>
            <button class="font-bold px-4 py-2 rounded-full text-xs" style="background: #4CAF50; color: white;" onclick="resetForm()">
              Daftar Lagi
            </button>
          </div>
        </div>
      </section>
      
      <!-- Daftar Pendaftar -->
      <section class="px-4 py-6">
        <h3 class="font-display text-lg mb-4" style="color: #FF6B6B;">📊 Pendaftar Kami</h3>
        <div id="registrations-list" style="display: flex; flex-direction: column; gap: 12px;">
          <!-- Will be filled by JavaScript -->
        </div>
      </section>
      
      <div style="height: 20px;"></div>
    </div>
  </div>

  <!-- Toast Messages -->
  <div id="toast-container"></div>

  <style>
    @keyframes spin {
      to { transform: rotate(360deg); }
    }
  </style>

  <script>
    // CONFIG
    const defaultConfig = {
      clinic_name: "KidsCare",
      tagline: "Tempat terbaik untuk memantau dan mendukung tumbuh kembang buah hati Anda dengan penuh kasih sayang! 💕",
      service_1_title: "Terapi Wicara",
      service_2_title: "Fisioterapi Anak",
      service_3_title: "Okupasi Terapi",
      service_4_title: "Konsultasi Psikolog",
      phone_number: "0812-3456-7890",
      address: "Jl. Kebahagiaan No. 123, Jakarta Selatan",
      background_color: "#FFF5E6",
      surface_color: "#FFFFFF",
      text_color: "#666666",
      primary_action_color: "#FF9A8B",
      secondary_action_color: "#FF6B6B",
      font_family: "Nunito",
      font_size: 14
    };

    let currentConfig = { ...defaultConfig };
    let registrationData = [];

    // PAGE NAVIGATION
    function showPage(pageName) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById(`${pageName}-page`).classList.add('active');
      window.scrollTo(0, 0);
    }

    // TOAST NOTIFICATION
    function showToast(message, type = 'success') {
      const toast = document.createElement('div');
      toast.className = 'toast';
      const bgColor = type === 'success' ? '#4CAF50' : '#FF6B6B';
      const icon = type === 'success' ? '✅' : '❌';
      toast.innerHTML = `
        <div style="background: ${bgColor}; color: white; padding: 12px 16px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15); font-weight: bold; text-align: center; font-size: 14px;">
          ${icon} ${message}
        </div>
      `;
      document.getElementById('toast-container').appendChild(toast);
      setTimeout(() => toast.remove(), 3000);
    }

    // DATA HANDLER
    const dataHandler = {
      onDataChanged(data) {
        registrationData = data;
        updateRegistrationsList();
      }
    };

    // UPDATE CONFIG AND UI
    async function onConfigChange(config) {
      currentConfig = { ...defaultConfig, ...config };
      
      document.getElementById('nav-title').textContent = currentConfig.clinic_name;
      document.getElementById('hero-title').innerHTML = `Klinik Tumbuh Kembang Si Kecil 🌟`;
      document.getElementById('hero-tagline').textContent = currentConfig.tagline;
      document.getElementById('service-1-name').textContent = currentConfig.service_1_title;
      document.getElementById('service-2-name').textContent = currentConfig.service_2_title;
      document.getElementById('service-3-name').textContent = currentConfig.service_3_title;
      document.getElementById('service-4-name').textContent = currentConfig.service_4_title;
      document.getElementById('contact-phone').textContent = currentConfig.phone_number;
      document.getElementById('contact-address').textContent = currentConfig.address;
      document.getElementById('footer-title').textContent = currentConfig.clinic_name + " Clinic";
    }

    function mapToCapabilities(config) {
      const c = { ...defaultConfig, ...config };
      return {
        recolorables: [
          {
            get: () => c.background_color,
            set: (value) => {
              c.background_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ background_color: value });
            }
          },
          {
            get: () => c.surface_color,
            set: (value) => {
              c.surface_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ surface_color: value });
            }
          },
          {
            get: () => c.text_color,
            set: (value) => {
              c.text_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ text_color: value });
            }
          },
          {
            get: () => c.primary_action_color,
            set: (value) => {
              c.primary_action_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ primary_action_color: value });
            }
          },
          {
            get: () => c.secondary_action_color,
            set: (value) => {
              c.secondary_action_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ secondary_action_color: value });
            }
          }
        ],
        borderables: [],
        fontEditable: {
          get: () => c.font_family,
          set: (value) => {
            c.font_family = value;
            if (window.elementSdk) window.elementSdk.setConfig({ font_family: value });
          }
        },
        fontSizeable: {
          get: () => c.font_size,
          set: (value) => {
            c.font_size = value;
            if (window.elementSdk) window.elementSdk.setConfig({ font_size: value });
          }
        }
      };
    }

    function mapToEditPanelValues(config) {
      const c = { ...defaultConfig, ...config };
      return new Map([
        ["clinic_name", c.clinic_name],
        ["tagline", c.tagline],
        ["service_1_title", c.service_1_title],
        ["service_2_title", c.service_2_title],
        ["service_3_title", c.service_3_title],
        ["service_4_title", c.service_4_title],
        ["phone_number", c.phone_number],
        ["address", c.address]
      ]);
    }

    // FORM HANDLING
    document.getElementById('registration-form').addEventListener('submit', async (e) => {
      e.preventDefault();
      
      const parentName = document.getElementById('parent-name').value.trim();
      const childName = document.getElementById('child-name').value.trim();
      const childAge = document.getElementById('child-age').value;
      const phone = document.getElementById('phone').value.trim();
      const service = document.getElementById('service').value;
      const notes = document.getElementById('notes').value.trim();

      if (!parentName || !childName || !childAge || !phone || !service) {
        showToast('Mohon lengkapi semua field yang diperlukan', 'error');
        return;
      }

      document.getElementById('loading-state').style.display = 'block';
      document.getElementById('submit-btn').disabled = true;

      const newRegistration = {
        id: Date.now().toString(),
        parent_name: parentName,
        child_name: childName,
        child_age: childAge,
        phone: phone,
        service: service,
        notes: notes || '-',
        created_at: new Date().toISOString()
      };

      const result = await window.dataSdk.create(newRegistration);

      document.getElementById('loading-state').style.display = 'none';
      document.getElementById('submit-btn').disabled = false;

      if (result.isOk) {
        document.getElementById('registration-form').style.display = 'none';
        document.getElementById('success-message').style.display = 'block';
        showToast('Pendaftaran berhasil! Kami akan segera menghubungi Anda 📞', 'success');
      } else {
        showToast('Terjadi kesalahan. Silahkan coba lagi', 'error');
      }
    });

    function resetForm() {
      document.getElementById('registration-form').reset();
      document.getElementById('registration-form').style.display = 'flex';
      document.getElementById('success-message').style.display = 'none';
    }

    function updateRegistrationsList() {
      const listContainer = document.getElementById('registrations-list');
      
      if (registrationData.length === 0) {
        listContainer.innerHTML = '<p style="text-align: center;
