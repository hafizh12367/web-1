<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#f6f5ef">
  <meta name="description" content="Portofolio Alya Pramesti, desainer digital dan anggota Ruang Tumbuh Studio.">
  <title>Alya Pramesti — Portofolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Fraunces:opsz,wght@9..144,500;9..144,600&display=swap" rel="stylesheet">
  <style>
    :root {
      color-scheme: light;
      --paper: #f6f5ef;
      --ink: #20342e;
      --muted: #6b7770;
      --line: #d9ded6;
      --green: #d9eddd;
      --coral: #e8795f;
      --blue: #cad9f0;
      --sans: "DM Sans", "Segoe UI", sans-serif;
      --serif: "Fraunces", Georgia, serif;
    }

    * { box-sizing: border-box; }
    [hidden] { display: none !important; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background: var(--paper);
      color: var(--ink);
      font-family: var(--sans);
      font-size: 16px;
      line-height: 1.6;
    }

    a { color: inherit; }
    a:focus-visible, button:focus-visible {
      outline: 3px solid var(--coral);
      outline-offset: 4px;
    }

    .page-shell {
      width: min(1120px, calc(100% - 64px));
      margin: 0 auto;
    }

    .site-header {
      min-height: 88px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
      border-bottom: 1px solid var(--line);
    }

    .wordmark {
      font-family: var(--serif);
      font-size: 25px;
      font-weight: 600;
      text-decoration: none;
    }

    .nav-links { display: flex; gap: 30px; }
    .nav-links a {
      color: var(--muted);
      font-size: 14px;
      text-decoration: none;
      transition: color 160ms ease;
    }
    .nav-links a:hover { color: var(--ink); }

    .edit-bar { display: flex; min-height: 54px; align-items: center; justify-content: flex-end; gap: 14px; border-bottom: 1px solid var(--line); }
    .edit-actions { display: flex; flex-wrap: wrap; gap: 8px; }
    .edit-button {
      min-height: 34px;
      padding: 6px 12px;
      border: 1px solid var(--ink);
      border-radius: 3px;
      background: transparent;
      color: var(--ink);
      font: 600 12px var(--sans);
      cursor: pointer;
    }
    .edit-button:hover { background: var(--ink); color: white; }
    .edit-bar [role="status"] { margin: 0 auto 0 0; color: var(--muted); font-size: 12px; }
    [data-edit-key][contenteditable="true"] { border-bottom: 1px dashed var(--coral); outline: none; cursor: text; }
    [data-edit-key][contenteditable="true"]:focus { background: #fffefa; box-shadow: 0 0 0 3px #fffefa; }
    .filter-button:disabled { opacity: 0.5; cursor: not-allowed; }

    .hero {
      display: grid;
      grid-template-columns: 1.05fr 0.95fr;
      align-items: center;
      gap: 72px;
      padding: 66px 0 78px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      margin: 0 0 23px;
      color: var(--muted);
      font-size: 12px;
      font-weight: 700;
      text-transform: uppercase;
    }
    .eyebrow::before {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--coral);
      content: "";
    }

    h1, h2, p { margin-top: 0; }
    h1 {
      max-width: 580px;
      margin-bottom: 19px;
      font-family: var(--serif);
      font-size: 76px;
      font-weight: 500;
      line-height: 0.99;
    }
    .name-line { display: block; }

    .hero-copy {
      max-width: 480px;
      margin-bottom: 29px;
      color: var(--muted);
      font-size: 18px;
    }

    .hero-actions { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
    .primary-link {
      display: inline-flex;
      min-height: 48px;
      align-items: center;
      justify-content: center;
      padding: 0 20px;
      border-radius: 4px;
      background: var(--ink);
      color: #fff;
      font-size: 14px;
      font-weight: 600;
      text-decoration: none;
      transition: background 160ms ease, transform 160ms ease;
    }
    .primary-link:hover { transform: translateY(-2px); background: #35544a; }
    .text-link { font-size: 14px; font-weight: 600; text-decoration-thickness: 1px; text-underline-offset: 4px; }

    .portrait-wrap {
      position: relative;
      width: 100%;
      max-width: 445px;
      justify-self: end;
      padding: 18px 18px 18px 0;
    }
    .portrait-wrap::before {
      position: absolute;
      inset: 0 0 0 45px;
      border-radius: 4px;
      background: var(--green);
      content: "";
    }
    .portrait {
      position: relative;
      display: block;
      width: 100%;
      aspect-ratio: 4 / 4.5;
      border-radius: 4px;
      object-fit: cover;
      object-position: center 38%;
    }
    .portrait-note {
      position: absolute;
      right: -15px;
      bottom: 39px;
      max-width: 185px;
      padding: 12px 16px;
      border-radius: 3px;
      background: var(--blue);
      color: var(--ink);
      font-family: var(--serif);
      font-size: 17px;
      line-height: 1.25;
      transform: rotate(2deg);
    }

    .section-rule { border-top: 1px solid var(--line); }
    .details {
      display: grid;
      grid-template-columns: 0.8fr 1.2fr 1fr;
      gap: 44px;
      padding: 38px 0 46px;
    }
    .detail-label {
      margin-bottom: 11px;
      color: var(--muted);
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
    }
    .detail-value { margin-bottom: 0; font-size: 15px; font-weight: 600; }
    .detail-value a { text-decoration: none; }
    .detail-value a:hover { text-decoration: underline; text-underline-offset: 4px; }
    .contact-line { display: flex; align-items: center; gap: 10px; }
    .copy-button {
      min-height: 32px;
      padding: 4px 9px;
      border: 1px solid var(--line);
      border-radius: 3px;
      background: transparent;
      color: var(--muted);
      font: 500 12px var(--sans);
      cursor: pointer;
    }
    .copy-button:hover { border-color: var(--ink); color: var(--ink); }

    .about {
      display: grid;
      grid-template-columns: 0.8fr 1.2fr;
      gap: 44px;
      padding: 58px 0 66px;
    }
    .section-kicker {
      margin: 7px 0 0;
      color: var(--coral);
      font-size: 12px;
      font-weight: 700;
      text-transform: uppercase;
    }
    h2 {
      margin-bottom: 16px;
      font-family: var(--serif);
      font-size: 38px;
      font-weight: 500;
      line-height: 1.12;
    }
    .about-copy { max-width: 630px; color: var(--muted); font-size: 16px; }
    .about-copy p:last-child { margin-bottom: 0; }

    .work { padding: 58px 0 62px; }
    .section-heading { display: flex; align-items: end; justify-content: space-between; gap: 30px; margin-bottom: 28px; }
    .section-heading h2, .journey h2 { margin-bottom: 0; }
    .filters { display: flex; flex-wrap: wrap; gap: 18px; }
    .filter-button {
      padding: 7px 0;
      border: 0;
      border-bottom: 2px solid transparent;
      background: transparent;
      color: var(--muted);
      font: 500 13px var(--sans);
      cursor: pointer;
    }
    .filter-button:hover, .filter-button.is-active { border-bottom-color: var(--coral); color: var(--ink); }
    .project-grid { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 22px; }
    .project img { display: block; width: 100%; aspect-ratio: 1.42; border-radius: 3px; object-fit: cover; background: var(--green); }
    .project-meta { display: flex; justify-content: space-between; gap: 14px; margin: 16px 0 6px; color: var(--muted); font-size: 11px; font-weight: 700; text-transform: uppercase; }
    .project h3, .expertise-row h3, .timeline-item h3 { margin: 0 0 6px; font-size: 18px; font-weight: 600; }
    .project > p, .expertise-row p, .timeline-item p { margin: 0; color: var(--muted); font-size: 14px; }
    .sample-note { margin: 20px 0 0; color: var(--muted); font-size: 12px; }

    .expertise { display: grid; grid-template-columns: 0.8fr 1.2fr; gap: 44px; padding: 58px 0 64px; }
    .expertise-intro h2 { margin-bottom: 0; }
    .expertise-row { display: grid; grid-template-columns: 36px 1fr; gap: 12px; padding: 17px 0; border-bottom: 1px solid var(--line); }
    .expertise-row:first-child { padding-top: 0; }
    .expertise-row > span { color: var(--coral); font-size: 12px; font-weight: 700; }

    .journey { display: grid; grid-template-columns: 0.8fr 1.2fr; gap: 28px 44px; padding: 58px 0 62px; }
    .timeline-item { display: grid; grid-template-columns: 130px 1fr; gap: 18px; padding: 0 0 23px; margin-bottom: 23px; border-bottom: 1px solid var(--line); }
    .timeline-date { color: var(--coral) !important; font-size: 12px !important; font-weight: 700; }
    .journey > .sample-note { grid-column: 2; margin-top: -28px; }

    .contact { display: grid; grid-template-columns: 0.8fr 1.2fr; gap: 44px; padding: 58px 0 66px; }
    .contact-intro > p:not(.section-kicker) { max-width: 330px; color: var(--muted); }
    .contact-email { display: inline-block; margin-top: 10px; font-size: 15px; font-weight: 600; text-decoration-thickness: 1px; text-underline-offset: 4px; }
    .contact-form { display: grid; grid-template-columns: 1fr; gap: 8px; }
    .contact-form label { margin-top: 7px; font-size: 13px; font-weight: 600; }
    .contact-form input, .contact-form textarea {
      width: 100%;
      padding: 11px 12px;
      border: 1px solid var(--line);
      border-radius: 3px;
      background: #fffefa;
      color: var(--ink);
      font: 15px var(--sans);
    }
    .contact-form input:focus, .contact-form textarea:focus { border-color: var(--ink); outline: 2px solid transparent; }
    .contact-form textarea { resize: vertical; }
    .form-submit { width: fit-content; margin-top: 8px; border: 0; font-family: var(--sans); cursor: pointer; }
    .form-submit span { margin-left: 9px; font-size: 18px; }
    .form-note { margin: 2px 0 0; color: var(--muted); font-size: 12px; }

    .site-footer {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      padding: 22px 0 28px;
      color: var(--muted);
      font-size: 12px;
    }

    @media (max-width: 760px) {
      .page-shell { width: min(100% - 40px, 560px); }
      .site-header { min-height: 72px; }
      .edit-bar { justify-content: space-between; gap: 8px; }
      .edit-bar [role="status"] { font-size: 11px; }
      .nav-links { gap: 14px; }
      .nav-links a { font-size: 12px; }
      .hero { grid-template-columns: 1fr; gap: 36px; padding: 48px 0 54px; }
      h1 { font-size: 58px; }
      .hero-copy { font-size: 16px; }
      .portrait-wrap { width: min(100%, 410px); justify-self: center; }
      .details { grid-template-columns: 1fr 1fr; gap: 27px 22px; }
      .details > :last-child { grid-column: 1 / -1; }
      .about { grid-template-columns: 1fr; gap: 16px; padding: 44px 0 52px; }
      h2 { font-size: 34px; }
      .section-heading { align-items: start; flex-direction: column; gap: 18px; }
      .project-grid { grid-template-columns: 1fr 1fr; gap: 28px 18px; }
      .expertise, .journey, .contact { grid-template-columns: 1fr; gap: 25px; padding: 46px 0 50px; }
      .journey > .sample-note { grid-column: auto; margin-top: -12px; }
      .timeline-item { grid-template-columns: 115px 1fr; }
    }

    @media (max-width: 420px) {
      .page-shell { width: calc(100% - 32px); }
      .wordmark { font-size: 22px; }
      .edit-bar { align-items: flex-start; flex-direction: column-reverse; padding: 9px 0; }
      .nav-links { gap: 10px; }
      .nav-links a { font-size: 11px; }
      h1 { font-size: 49px; }
      .details { grid-template-columns: 1fr; gap: 22px; }
      .details > :last-child { grid-column: auto; }
      .contact-line { align-items: flex-start; flex-wrap: wrap; }
      .site-footer { flex-direction: column; gap: 4px; }
      .portrait-note { right: -5px; }
      .project-grid { grid-template-columns: 1fr; }
      .filters { gap: 13px; }
      .filter-button { font-size: 12px; }
      .timeline-item { grid-template-columns: 1fr; gap: 4px; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { scroll-behavior: auto !important; transition-duration: 0.01ms !important; }
    }
  </style>
</head>
<body>
  <div class="page-shell">
    <header class="site-header">
      <a class="wordmark" href="#beranda" aria-label="Alya Pramesti, beranda"><span data-initials>AP</span>.</a>
      <nav class="nav-links" aria-label="Navigasi utama">
        <a href="#karya">Karya</a>
        <a href="#tentang">Tentang</a>
        <a href="#perjalanan">Perjalanan</a>
        <a href="#kontak">Kontak</a>
      </nav>
    </header>
    <div class="edit-bar" aria-label="Pengaturan konten portofolio">
      <p id="edit-status" role="status">Konten bisa diubah dan disimpan di browser ini.</p>
      <button class="edit-button" id="edit-start" type="button">Edit halaman</button>
      <div class="edit-actions" id="edit-actions" hidden>
        <button class="edit-button" id="edit-save" type="button">Simpan</button>
        <button class="edit-button" id="edit-cancel" type="button">Batalkan</button>
        <button class="edit-button" id="edit-reset" type="button">Reset contoh</button>
      </div>
    </div>

    <main id="beranda">
      <section class="hero" aria-labelledby="nama">
        <div>
          <p class="eyebrow"><span data-edit-key="lokasi">Profil contoh · Jakarta, Indonesia</span></p>
          <h1 id="nama"><span class="name-line" data-edit-key="nama-depan">Alya</span><span class="name-line" data-edit-key="nama-belakang">Pramesti</span></h1>
          <p class="hero-copy" data-edit-key="ringkasan">Desainer digital yang senang merapikan ide rumit menjadi pengalaman yang terasa sederhana dan manusiawi.</p>
          <div class="hero-actions">
            <a class="primary-link" href="mailto:alya.pramesti@example.com" data-email-link>Hubungi saya</a>
            <a class="text-link" href="#tentang">Kenali lebih dekat</a>
          </div>
        </div>
        <div class="portrait-wrap">
          <img class="portrait" src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="Potret perempuan untuk profil contoh Alya Pramesti" fetchpriority="high">
          <span class="portrait-note" data-edit-key="catatan-foto">Ide baik tumbuh saat dikerjakan bersama.</span>
        </div>
      </section>

      <section class="details section-rule" id="kontak" aria-label="Informasi kontak dan afiliasi">
        <div>
          <p class="detail-label">Email</p>
          <div class="contact-line">
            <p class="detail-value"><a href="mailto:alya.pramesti@example.com" data-edit-key="email">alya.pramesti@example.com</a></p>
            <button class="copy-button" type="button" data-copy-email="alya.pramesti@example.com" aria-label="Salin alamat email">Salin</button>
          </div>
        </div>
        <div>
          <p class="detail-label">Telepon</p>
          <p class="detail-value"><a href="tel:+6281200002468" data-edit-key="telepon" data-phone-link>+62 812-0000-2468</a></p>
        </div>
        <div>
          <p class="detail-label">Organisasi afiliasi</p>
          <p class="detail-value" data-edit-key="organisasi">Ruang Tumbuh Studio</p>
        </div>
      </section>

      <section class="about section-rule" id="tentang" aria-labelledby="tentang-judul">
        <p class="section-kicker" data-edit-key="label-tentang">Sedikit tentang saya</p>
        <div class="about-copy">
          <h2 id="tentang-judul" data-edit-key="judul-tentang">Ruang untuk ide, perhatian pada detail.</h2>
          <p data-edit-key="tentang-paragraf-1">Saya bekerja bersama tim kecil di Ruang Tumbuh Studio, membantu organisasi merancang produk digital yang berguna dan mudah dipahami.</p>
          <p data-edit-key="tentang-paragraf-2">Di luar pekerjaan, saya suka membuat catatan visual, mengunjungi kedai kopi baru, dan belajar hal-hal kecil yang membuat sebuah produk terasa lebih dekat.</p>
        </div>
      </section>

      <section class="work section-rule" id="karya" aria-labelledby="karya-judul">
        <div class="section-heading">
          <div>
            <p class="section-kicker" data-edit-key="label-karya">Pilihan terbaru</p>
            <h2 id="karya-judul" data-edit-key="judul-karya">Karya yang berarti.</h2>
          </div>
          <div class="filters" role="group" aria-label="Filter karya">
            <button class="filter-button is-active" type="button" data-filter="semua" aria-pressed="true">Semua</button>
            <button class="filter-button" type="button" data-filter="produk" aria-pressed="false">Produk digital</button>
            <button class="filter-button" type="button" data-filter="identitas" aria-pressed="false">Identitas</button>
          </div>
        </div>
        <div class="project-grid" aria-live="polite">
          <article class="project" data-category="produk">
            <img src="https://images.unsplash.com/photo-1559028006-448665bd7c7f?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="Meja kerja dengan perangkat dan catatan untuk proyek aplikasi kesehatan" loading="lazy">
            <div class="project-meta"><span>Produk digital</span><span data-edit-key="proyek-1-tahun">2025</span></div>
            <h3 data-edit-key="proyek-1-nama">Ruang Sehat</h3>
            <p data-edit-key="proyek-1-deskripsi">Pengalaman membuat janji konsultasi terasa lebih tenang dan mudah diikuti.</p>
          </article>
          <article class="project" data-category="identitas">
            <img src="https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="Buku catatan dan perlengkapan menulis untuk proyek identitas merek" loading="lazy">
            <div class="project-meta"><span>Identitas</span><span data-edit-key="proyek-2-tahun">2024</span></div>
            <h3 data-edit-key="proyek-2-nama">Temu Buku</h3>
            <p data-edit-key="proyek-2-deskripsi">Sistem identitas hangat untuk komunitas baca yang tumbuh dari pertemuan kecil.</p>
          </article>
          <article class="project" data-category="produk">
            <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="Tampilan dashboard analitik pada layar komputer" loading="lazy">
            <div class="project-meta"><span>Produk digital</span><span data-edit-key="proyek-3-tahun">2024</span></div>
            <h3 data-edit-key="proyek-3-nama">Jejak Baik</h3>
            <p data-edit-key="proyek-3-deskripsi">Dashboard sederhana untuk membantu organisasi memahami dampak program sosial.</p>
          </article>
        </div>
        <p class="sample-note" data-edit-key="catatan-proyek">Nama proyek dan ringkasan di atas adalah contoh fiktif.</p>
      </section>

      <section class="expertise section-rule" aria-labelledby="keahlian-judul">
        <div class="expertise-intro">
          <p class="section-kicker" data-edit-key="label-keahlian">Cara saya berkontribusi</p>
          <h2 id="keahlian-judul"><span class="name-line" data-edit-key="judul-keahlian-1">Dari pertanyaan</span><span class="name-line" data-edit-key="judul-keahlian-2">hingga solusi.</span></h2>
        </div>
        <div class="expertise-list">
          <div class="expertise-row"><span>01</span><div><h3 data-edit-key="keahlian-1">Riset dan strategi</h3><p data-edit-key="keahlian-1-deskripsi">Memahami kebutuhan orang sebelum menentukan arah desain.</p></div></div>
          <div class="expertise-row"><span>02</span><div><h3 data-edit-key="keahlian-2">Desain pengalaman</h3><p data-edit-key="keahlian-2-deskripsi">Menyusun alur, struktur, dan antarmuka produk digital.</p></div></div>
          <div class="expertise-row"><span>03</span><div><h3 data-edit-key="keahlian-3">Sistem visual</h3><p data-edit-key="keahlian-3-deskripsi">Membangun identitas dan komponen yang konsisten serta mudah dikembangkan.</p></div></div>
        </div>
      </section>

      <section class="journey section-rule" id="perjalanan" aria-labelledby="perjalanan-judul">
        <div>
          <p class="section-kicker" data-edit-key="label-perjalanan">Pengalaman</p>
          <h2 id="perjalanan-judul" data-edit-key="judul-perjalanan">Perjalanan sejauh ini.</h2>
        </div>
        <div class="timeline">
          <article class="timeline-item">
            <p class="timeline-date" data-edit-key="riwayat-1-tahun">2023 — sekarang</p>
            <div><h3 data-edit-key="riwayat-1-peran">Desainer digital · Ruang Tumbuh Studio</h3><p data-edit-key="riwayat-1-deskripsi">Berkolaborasi dengan tim produk dan mitra sosial untuk merancang layanan digital.</p></div>
          </article>
          <article class="timeline-item">
            <p class="timeline-date" data-edit-key="riwayat-2-tahun">2021 — 2023</p>
            <div><h3 data-edit-key="riwayat-2-peran">Desainer visual · Kawan Kreatif</h3><p data-edit-key="riwayat-2-deskripsi">Mengerjakan identitas visual dan materi kampanye untuk bisnis lokal.</p></div>
          </article>
          <article class="timeline-item">
            <p class="timeline-date" data-edit-key="riwayat-3-tahun">2017 — 2021</p>
            <div><h3 data-edit-key="riwayat-3-peran">Desain Komunikasi Visual · Institut Seni Jakarta</h3><p data-edit-key="riwayat-3-deskripsi">Mempelajari dasar komunikasi visual, tipografi, dan desain interaksi.</p></div>
          </article>
        </div>
        <p class="sample-note" data-edit-key="catatan-riwayat">Riwayat ini juga merupakan data contoh.</p>
      </section>

      <section class="contact section-rule" id="kontak-lanjut" aria-labelledby="kontak-judul">
        <div class="contact-intro">
          <p class="section-kicker" data-edit-key="label-kontak">Mari terhubung</p>
          <h2 id="kontak-judul" data-edit-key="judul-kontak">Ada ide menarik?</h2>
          <p data-edit-key="deskripsi-kontak">Saya terbuka untuk obrolan tentang desain, kolaborasi, atau proyek baru.</p>
          <a class="contact-email" href="mailto:alya.pramesti@example.com" data-email-link data-mirror-key="email">alya.pramesti@example.com</a>
        </div>
        <form class="contact-form" id="contact-form">
          <label for="visitor-name">Nama</label>
          <input id="visitor-name" name="name" autocomplete="name" required>
          <label for="visitor-email">Email</label>
          <input id="visitor-email" name="email" type="email" autocomplete="email" required>
          <label for="visitor-message">Pesan</label>
          <textarea id="visitor-message" name="message" rows="4" required></textarea>
          <button class="primary-link form-submit" type="submit">Buka aplikasi email <span aria-hidden="true">↗</span></button>
          <p class="form-note" id="form-status" role="status">Pesan akan disiapkan di aplikasi email Anda.</p>
        </form>
      </section>
    </main>

    <footer class="site-footer section-rule">
      <span>© 2026 <span data-mirror-key="nama-depan">Alya</span> <span data-mirror-key="nama-belakang">Pramesti</span> · Data profil ini fiktif.</span>
      <a href="#beranda">Kembali ke atas ↑</a>
    </footer>
  </div>

  <script>
    const storageKey = "alyaPortfolioContent";
    const editableFields = [...document.querySelectorAll("[data-edit-key]")];
    const defaultContent = Object.fromEntries(editableFields.map((field) => [field.dataset.editKey, field.textContent.trim()]));
    const editStartButton = document.querySelector("#edit-start");
    const editActions = document.querySelector("#edit-actions");
    const editStatus = document.querySelector("#edit-status");
    const filterButtons = document.querySelectorAll("[data-filter]");
    const copyButton = document.querySelector("[data-copy-email]");
    const projects = document.querySelectorAll(".project[data-category]");
    const contactForm = document.querySelector("#contact-form");
    const formStatus = document.querySelector("#form-status");
    let savedContent = { ...defaultContent };
    let isEditing = false;

    try {
      const storedContent = JSON.parse(localStorage.getItem(storageKey) || "null");
      if (storedContent && typeof storedContent === "object" && !Array.isArray(storedContent)) {
        for (const key of Object.keys(defaultContent)) {
          if (typeof storedContent[key] === "string") savedContent[key] = storedContent[key];
        }
      }
    } catch {
      editStatus.textContent = "Penyimpanan browser tidak tersedia; perubahan hanya sementara.";
    }

    function getContentValue(key) {
      return editableFields.find((field) => field.dataset.editKey === key)?.textContent.trim() || "";
    }

    function applyContent(content) {
      editableFields.forEach((field) => {
        if (typeof content[field.dataset.editKey] === "string") {
          field.textContent = content[field.dataset.editKey];
        }
      });

      document.querySelectorAll("[data-mirror-key]").forEach((field) => {
        const mirroredValue = content[field.dataset.mirrorKey];
        if (typeof mirroredValue === "string") field.textContent = mirroredValue;
      });

      const fullName = [getContentValue("nama-depan"), getContentValue("nama-belakang")].filter(Boolean).join(" ");
      document.title = `${fullName || "Portofolio"} — Portofolio`;
      document.querySelector('meta[name="description"]').content = `Portofolio ${fullName}. ${getContentValue("ringkasan")}`;
      document.querySelector("[data-initials]").textContent = [getContentValue("nama-depan"), getContentValue("nama-belakang")]
        .map((name) => name.charAt(0))
        .join("") || "P";
      document.querySelector(".wordmark").setAttribute("aria-label", `${fullName || "Portofolio"}, beranda`);
      document.querySelector(".portrait").alt = `Potret profil ${fullName || "portofolio"}`;

      const email = getContentValue("email");
      copyButton.dataset.copyEmail = email;
      document.querySelectorAll("[data-email-link]").forEach((link) => {
        link.href = `mailto:${email}`;
      });
      document.querySelectorAll("[data-phone-link]").forEach((link) => {
        const phoneNumber = getContentValue("telepon").replace(/[^\d+]/g, "");
        link.href = `tel:${phoneNumber}`;
      });
    }

    function setEditing(enabled) {
      isEditing = enabled;
      editableFields.forEach((field) => {
        field.contentEditable = String(enabled);
        field.spellcheck = enabled;
      });
      filterButtons.forEach((button) => { button.disabled = enabled; });
      editStartButton.hidden = enabled;
      editActions.hidden = !enabled;
      editStatus.textContent = enabled
        ? "Klik teks bergaris untuk mengubahnya, lalu simpan atau batalkan."
        : "Konten bisa diubah dan disimpan di browser ini.";
    }

    function collectContent() {
      return Object.fromEntries(editableFields.map((field) => [field.dataset.editKey, field.innerText.trim()]));
    }

    applyContent(savedContent);

    editStartButton.addEventListener("click", () => {
      setEditing(true);
      editableFields[0]?.focus();
    });

    document.querySelector("#edit-save").addEventListener("click", () => {
      const updatedContent = collectContent();
      try {
        localStorage.setItem(storageKey, JSON.stringify(updatedContent));
      } catch {
        editStatus.textContent = "Perubahan belum tersimpan. Periksa pengaturan penyimpanan browser.";
        return;
      }
      savedContent = updatedContent;
      applyContent(savedContent);
      setEditing(false);
      editStatus.textContent = "Perubahan tersimpan di browser ini.";
    });

    document.querySelector("#edit-cancel").addEventListener("click", () => {
      applyContent(savedContent);
      setEditing(false);
      editStatus.textContent = "Perubahan yang belum disimpan dibatalkan.";
    });

    document.querySelector("#edit-reset").addEventListener("click", () => {
      if (!window.confirm("Kembalikan semua teks ke data contoh awal?")) return;
      try {
        localStorage.removeItem(storageKey);
      } catch {
        editStatus.textContent = "Data contoh gagal dipulihkan karena penyimpanan browser tidak tersedia.";
        return;
      }
      savedContent = { ...defaultContent };
      applyContent(savedContent);
      setEditing(false);
      editStatus.textContent = "Semua konten kembali ke data contoh awal.";
    });

    editableFields.forEach((field) => {
      field.addEventListener("click", (event) => {
        if (isEditing && field instanceof HTMLAnchorElement) event.preventDefault();
      });
      field.addEventListener("keydown", (event) => {
        if (event.key === "Enter" && field.tagName !== "P") event.preventDefault();
      });
    });

    filterButtons.forEach((button) => {
      button.addEventListener("click", () => {
        const selectedFilter = button.dataset.filter;

        filterButtons.forEach((filterButton) => {
          const isSelected = filterButton === button;
          filterButton.classList.toggle("is-active", isSelected);
          filterButton.setAttribute("aria-pressed", String(isSelected));
        });

        projects.forEach((project) => {
          project.hidden = selectedFilter !== "semua" && project.dataset.category !== selectedFilter;
        });
      });
    });

    copyButton.addEventListener("click", async () => {
      const email = copyButton.dataset.copyEmail;
      try {
        await navigator.clipboard.writeText(email);
      } catch {
        const temporaryInput = document.createElement("textarea");
        temporaryInput.value = email;
        temporaryInput.setAttribute("readonly", "");
        temporaryInput.style.position = "absolute";
        temporaryInput.style.left = "-9999px";
        document.body.append(temporaryInput);
        temporaryInput.select();
        document.execCommand("copy");
        temporaryInput.remove();
      }

      copyButton.textContent = "Tersalin";
      window.setTimeout(() => { copyButton.textContent = "Salin"; }, 1800);
    });

    contactForm.addEventListener("submit", (event) => {
      event.preventDefault();
      const formData = new FormData(contactForm);
      const subject = `Pesan portofolio dari ${formData.get("name")}`;
      const message = [
        `Nama: ${formData.get("name")}`,
        `Email: ${formData.get("email")}`,
        "",
        formData.get("message")
      ].join("\n");
      const mailto = `mailto:${getContentValue("email")}?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(message)}`;

      formStatus.textContent = "Aplikasi email sedang dibuka untuk mengirim pesan.";
      window.location.href = mailto;
    });
  </script>
</body>
</html>
