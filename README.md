
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 17th Birthday Irene</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #f8fafc;
            --card-bg: #ffffff;
            --text-dark: #0f172a;
            --text-muted: #64748b;
            --primary-color: #2563eb; /* Biru kalem */
            --accent-soft: #eff6ff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-dark);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* --- CARD UTAMA --- */
        .birthday-card {
            background: var(--card-bg);
            width: 100%;
            max-width: 800px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        /* Responsive: Bersebelahan jika di layar monitor/tablet */
        @media (min-width: 768px) {
            .birthday-card {
                flex-direction: row;
                min-height: 450px;
            }
        }

        /* --- BAGIAN FOTO (KIRI) --- */
        .photo-section {
            flex: 1;
            background: #cbd5e1;
            position: relative;
            min-height: 300px;
        }

        .photo-section img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        /* --- BAGIAN SLIDESHOW (KANAN) --- */
        .slideshow-section {
            flex: 1.2;
            padding: 40px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            position: relative;
        }

        .header-title {
            font-size: 1.6rem;
            font-weight: 800;
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .subtitle {
            font-size: 0.85rem;
            color: var(--text-muted);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 30px;
        }

        /* CONTAINER SLIDE */
        .slides-container {
            position: relative;
            min-height: 160px; /* Menjaga tinggi agar tombol tidak lompat-lompat */
        }

        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.5s ease, visibility 0.5s ease;
        }

        .slide.active {
            opacity: 1;
            visibility: visible;
            position: relative; /* Membuat slide aktif yang mengatur tinggi container */
        }

        .slide p {
            font-size: 0.95rem;
            line-height: 1.6;
            color: #334155;
            font-weight: 500;
        }

        /* --- TOMBOL NAVIGASI (PANAH) --- */
        .controls {
            display: flex;
            gap: 12px;
            margin-top: 30px;
            align-items: center;
        }

        .nav-btn {
            background: var(--accent-soft);
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            color: var(--primary-color);
            font-weight: bold;
            font-size: 1.1rem;
            transition: background 0.2s;
        }

        .nav-btn:hover {
            background: #dbeafe;
        }

        /* --- INDIKATOR TITIK (DOTS) --- */
        .dots-container {
            display: flex;
            gap: 6px;
        }

        .dot {
            width: 8px;
            height: 8px;
            background: #e2e8f0;
            border-radius: 50%;
            cursor: pointer;
            transition: background 0.2s, width 0.2s;
        }

        .dot.active {
            background: var(--primary-color);
            width: 20px;
            border-radius: 4px;
        }
    </style>
</head>
<body>

    <div class="birthday-card">
        
        <!-- BAGIAN KIRI: FOTO -->
        <div class="photo-section">
            <img src="56499815-b037-4e3d-b737-28da27921690.jpeg" alt="Foto Irene">
        </div>

        <!-- BAGIAN KANAN: SLIDESHOW UCAPAN -->
        <div class="slideshow-section">
            <h1 class="header-title">Happy Sweet 17th</h1>
            <p class="subtitle">Special Wishes for Irene ✨</p>

            <!-- Wadah Slide -->
            <div class="slides-container">
                
                <div class="slide active">
                    <p>"Selamat ulang tahun yang ke-17, Irene. Semoga kamu selalu diberikan kesehatan, umur yang panjang, dan kebahagiaan setiap hari. Semoga apa yang kamu cita-citakan bisa tercapai."</p>
                </div>

                <div class="slide">
                    <p>"Happy Sweet 17th, Irene! Semoga di usia yang baru ini kamu semakin dewasa, dilancarkan dalam segala urusan sekolah, dan selalu dikelilingi oleh hal-hal baik."</p>
                </div>

                <div class="slide">
                    <p>"Happy birthday, Irene. Semoga umur 17 ini menjadi awal yang indah untuk perjalanan masa depanmu. Sukses selalu untuk studi dan semua impian yang ingin kamu raih."</p>
                </div>

                <div class="slide">
                    <p>"Selamat menyambut umur 17 tahun, Irene. Semoga kamu tetap menjadi pribadi yang baik, selalu ceria, sehat, dan sukses dalam segala hal yang kamu kerjakan."</p>
                </div>

                <div class="slide">
                    <p>"Selamat ulang tahun, Irene. Doa terbaik untukmu di usia 17 tahun ini. Semoga kamu selalu diberikan kemudahan, kekuatan untuk melewati setiap tantangan, dan kebahagiaan yang tulus."</p>
                </div>

            </div>

            <!-- Navigasi & Indikator -->
            <div class="controls">
                <button class="nav-btn" id="prevBtn">&lsaquo;</button>
                <div class="dots-container" id="dotsContainer"></div>
                <button class="nav-btn" id="nextBtn">&rsaquo;</button>
            </div>

        </div>

    </div>

    <!-- LOGIKAL JAVASCRIPT SLIDESHOW -->
    <script>
        const slides = document.querySelectorAll('.slide');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const dotsContainer = document.getElementById('dotsContainer');
        
        let currentSlide = 0;
        let slideInterval;

        // 1. Buat titik indikator (dots) otomatis berdasarkan jumlah slide
        slides.forEach((_, index) => {
            const dot = document.createElement('div');
            dot.classList.add('dot');
            if (index === 0) dot.classList.add('active');
            dot.addEventListener('click', () => goToSlide(index));
            dotsContainer.appendChild(dot);
        });

        const dots = document.querySelectorAll('.dot');

        // 2. Fungsi untuk mengubah slide aktif
        function updateSlides() {
            slides.forEach((slide, index) => {
                if (index === currentSlide) {
                    slide.classList.add('active');
                    dots[index].classList.add('active');
                } else {
                    slide.classList.remove('active');
                    dots[index].classList.remove('active');
                }
            });
        }

        function nextSlide() {
            currentSlide = (currentSlide + 1) % slides.length;
            updateSlides();
        }

        function prevSlide() {
            currentSlide = (currentSlide - 1 + slides.length) % slides.length;
            updateSlides();
        }

        function goToSlide(index) {
            currentSlide = index;
            updateSlides();
            resetTimer(); // Reset waktu otomatis kalau user klik manual
        }

        // 3. Kontrol Tombol
        nextBtn.addEventListener('click', () => {
            nextSlide();
            resetTimer();
        });

        prevBtn.addEventListener('click', () => {
            prevSlide();
            resetTimer();
        });

        // 4. Pengatur Waktu Otomatis (Berpindah tiap 5 detik)
        function startTimer() {
            slideInterval = setInterval(nextSlide, 5000);
        }

        function resetTimer() {
            clearInterval(slideInterval);
            startTimer();
        }

        // Jalankan timer saat halaman dibuka
        startTimer();
    </script>
</body>
