

<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Stefania Wurlianty | Portofolio Interaktif</title>
    <!-- W3.CSS Framework dari W3Schools -->
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
    <!-- Font Awesome Icons (untuk mempercantik) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Custom style tambahan untuk melengkapi W3.CSS */
        body {
            background: #fef7e8; /* cream lembut */
            font-family: 'Segoe UI', 'Poppins', 'Roboto', sans-serif;
        }
        .hero-photo {
            max-width: 280px;
            margin: 0 auto;
            transition: transform 0.2s;
        }
        .hero-photo:hover {
            transform: scale(1.02);
        }
        .photo-frame {
            background: #fff2e0;
            padding: 8px;
            border-radius: 50%;
            box-shadow: 0 20px 30px -12px rgba(0,0,0,0.1);
            display: inline-block;
        }
        .photo-frame img {
            width: 100%;
            height: auto;
            border-radius: 50%;
            object-fit: cover;
            aspect-ratio: 1/1;
            border: 3px solid #f3e1be;
        }
        .nav-card {
            cursor: pointer;
            transition: all 0.2s ease;
            border-radius: 40px;
            background: white;
            box-shadow: 0 2px 8px rgba(0,0,0,0.03);
        }
        .nav-card:hover {
            background: #fcf5e8;
            transform: translateY(-3px);
            box-shadow: 0 12px 20px -12px rgba(0,0,0,0.1);
        }
        .nav-card i {
            font-size: 1.8rem;
            color: #b48c48;
        }
        .detail-panel {
            background: #ffffffdd;
            background: #fffbf5;
            border-radius: 40px;
            padding: 1.8rem;
            border: 1px solid #f3e9da;
            box-shadow: 0 8px 20px rgba(0,0,0,0.05);
            transition: all 0.2s;
        }
        .section-badge {
            background: #eedfc7;
            color: #4a3a22;
            border-radius: 60px;
            padding: 0.2rem 1rem;
            display: inline-block;
            font-weight: 500;
        }
        .footer-custom {
            background: #f5ecdf;
            border-radius: 32px;
            color: #7a6848;
        }
        .btn-reset-photo {
            background: #e7d9c6;
            border: none;
            border-radius: 40px;
            font-size: 0.7rem;
            transition: 0.1s;
        }
        .btn-reset-photo:hover {
            background: #dacbaa;
        }
        /* responsif tambahan */
        @media (max-width: 600px) {
            .detail-panel {
                padding: 1.2rem;
            }
            .nav-card i {
                font-size: 1.4rem;
            }
            .nav-card span {
                font-size: 0.75rem;
            }
        }
        .menu-active {
            background: #f3e9dc !important;
            border-left: 4px solid #d6b575;
        }
    </style>
</head>
<body>

<div class="w3-container w3-padding-32" style="max-width: 1200px; margin: auto;">
    
    <!-- KARTU UTAMA dengan W3.CSS card -->
    <div class="w3-card-4 w3-round-xxlarge w3-white w3-padding-24 w3-margin-bottom" style="background: #fffcf5;">
        
        <!-- FOTO PROFIL (tampilan awal menonjol) -->
        <div class="w3-center hero-photo w3-margin-bottom">
            <div class="photo-frame" id="photoFrame">
                <img id="profileImg" src="fani.jpg" alt="Foto Profil Stefania Wurlianty" style="width: 220px; height: 220px; object-fit: cover;">
            </div>
            <h2 class="w3-text-dark-grey w3-margin-top">Stefania Wurlianty</h2>
            <p class="w3-text-grey"><i class="fas fa-map-marker-alt"></i> Ambon, Indonesia</p>
        </div>

        <!-- MENU NAVIGASI (STATUS, PENGALAMAN, PENDIDIKAN, ALAMAT, SKILL) dengan grid W3.CSS -->
        <div class="w3-row-padding w3-margin-top w3-margin-bottom">
            <div class="w3-col l2 m4 s6 w3-padding-small">
                <div class="nav-card w3-round-xxlarge w3-padding-12 w3-center w3-card-2" data-page="status">
                    <i class="fas fa-user-check"></i>
                    <div class="w3-small w3-margin-top">Status</div>
                </div>
            </div>
            <div class="w3-col l2 m4 s6 w3-padding-small">
                <div class="nav-card w3-round-xxlarge w3-padding-12 w3-center w3-card-2" data-page="pengalaman">
                    <i class="fas fa-briefcase"></i>
                    <div class="w3-small w3-margin-top">Pengalaman</div>
                </div>
            </div>
            <div class="w3-col l2 m4 s6 w3-padding-small">
                <div class="nav-card w3-round-xxlarge w3-padding-12 w3-center w3-card-2" data-page="pendidikan">
                    <i class="fas fa-graduation-cap"></i>
                    <div class="w3-small w3-margin-top">Pendidikan</div>
                </div>
            </div>
            <div class="w3-col l2 m4 s6 w3-padding-small">
                <div class="nav-card w3-round-xxlarge w3-padding-12 w3-center w3-card-2" data-page="alamat">
                    <i class="fas fa-home"></i>
                    <div class="w3-small w3-margin-top">Alamat</div>
                </div>
            </div>
            <div class="w3-col l2 m4 s6 w3-padding-small">
                <div class="nav-card w3-round-xxlarge w3-padding-12 w3-center w3-card-2" data-page="skill">
                    <i class="fas fa-code"></i>
                    <div class="w3-small w3-margin-top">Skill</div>
                </div>
            </div>
        </div>

        <!-- KONTEN DINAMIS (halaman yang berubah sesuai klik) -->
        <div id="dynamicContent" class="detail-panel w3-margin-top">
            <!-- konten awal: hanya tampilan foto? tapi karena kita ingin default menampilkan pesan selamat datang atau instruksi, namun permintaan: "pada tampilan awal hanya menampilkan foto" (foto sudah ada di atas). lalu saat klik salah satu menu baru muncul detail -->
            <div class="w3-center w3-padding-48">
                <i class="fas fa-hand-point-up" style="font-size: 48px; color: #d6b575;"></i>
                <h3 class="w3-text-dark-grey">✨ Selamat datang ✨</h3>
                <div class="w3-margin-top">
                    <span class="section-badge"><i class="far fa-smile"></i> Portofolio interaktif</span>
                </div>
            </div>
        </div>
    </div>

    <!-- FOOTER -->
    <div class="footer-custom w3-padding w3-round-xxlarge w3-center w3-small">
        <i class="far fa-copyright"></i> 2025 Stefania Wurlianty - Biodata Beasiswa & Karir | <i class="fas fa-mobile-alt"></i> Responsif dengan W3.CSS
    </div>
</div>

<script>

    // ---------- DATA UNTUK MASING-MASING HALAMAN (Status, Pengalaman, Pendidikan, Alamat, Skill) ----------
    const pagesData = {
        status: {
            title: "Status Saat Ini",
            icon: "fas fa-user-check",
            content: `
                <div class="w3-row">
                    <div class="w3-col s12 m4 w3-center"><i class="fas fa-id-card" style="font-size: 48px; color:#b48c48;"></i></div>
                    <div class="w3-col s12 m8">
                        <p><strong><i class="fas fa-circle-check"></i> Status:</strong> Mahasiswa Aktif Semester 4</p>
                        <p><strong><i class="fas fa-university"></i> Universitas Pattimura</strong> – Ilmu Komputer</p>
                        <p><strong><i class="fas fa-chart-line"></i> IPK Sementara:</strong> 3.45 (skala 4.00)</p>
                        <p><strong><i class="fas fa-trophy"></i> Prestasi Terkini:</strong> Juara Harapan 3 Peneliti Belia 2022 (Provinsi)</p>
                        <div class="w3-panel w3-pale-yellow w3-round w3-padding">
                            <i class="fas fa-quote-left"></i> Aktif mengikuti kegiatan riset dan pengembangan diri.
                        </div>
                    </div>
                </div>
            `
        },
        pengalaman: {
            title: "Pengalaman & Kegiatan",
            icon: "fas fa-briefcase",
            content: `
                <div class="w3-row">
                    <div class="w3-col s12 m4 w3-center"><i class="fas fa-microphone-alt" style="font-size: 48px; color:#b48c48;"></i></div>
                    <div class="w3-col s12 m8">
                        <ul class="w3-ul w3-border-0">
                            <li><i class="fas fa-flask"></i> <strong>Peneliti Belia 2022</strong> – Peserta aktif & finalis, mengikuti workshop riset di Surabaya (November 2022).</li>
                            <li><i class="fas fa-pen-fancy"></i> <strong>Penghargaan Baca Puisi</strong> – Apresiasi khusus dalam kegiatan BADAR tingkat Klasis (komunikasi & ekspresi seni).</li>
                        </ul>
                    </div>
                </div>
            `
        },
        pendidikan: {
            title: "Riwayat Pendidikan",
            icon: "fas fa-school",
            content: `
                <div class="w3-row">
                    <div class="w3-col s12 m4 w3-center"><i class="fas fa-graduation-cap" style="font-size: 48px; color:#b48c48;"></i></div>
                    <div class="w3-col s12 m8">
                        <div class="w3-bar-block">
                            <div class="w3-bar-item"><i class="fas fa-university"></i> <strong>Universitas Pattimura</strong> – S1 Ilmu Komputer (2024–sekarang)<div>
                            <div class="w3-bar-item"><i class="fas fa-school"></i> <strong>SMA Swasta Kristen Teon Nila Serua</strong> – IPA (Lulus 2024)<div>
                        </div>
                    </div>
                </div>
            `
        },
        alamat: {
            title: "Alamat & Domisili",
            icon: "fas fa-map-pin",
            content: `
                <div class="w3-row">
                    <div class="w3-col s12 m4 w3-center"><i class="fas fa-location-dot" style="font-size: 48px; color:#b48c48;"></i></div>
                    <div class="w3-col s12 m8">
                        <p><i class="fas fa-home"></i> <strong>Alamat Lengkap:</strong> Jalan Werlofna, negeri Watludan, kec.Teon Nila Serua, kab. Maluku Tengan, Provinsi. Maluku, Indonesia 97558</p>
                        <p><i class="fab fa_whatsapp"></i><a href="https://wa.me/6282146415556" target="_blank">082146415556</a>
                        <p><i class="fa-brands fa-instagram"></i><a href="http://instagram.com/faniwurlianty" target="_blank">@faniwurlianty</a>
                        <p><i class="fas fa-envelope"></i><a href="mailto:faniwurliantymeturan@gmail.com">faniwurliantymeturan@gmail.com</a>
                        <p><i class="fas fa-globe"></i> <strong>Domisili:</strong> Ambon, Indonesia</p>
                        <div class="w3-light-grey w3-round w3-padding-small"><i class="fas fa-clock"></i> Ketersediaan: Magang</div>
                    </div>
                </div>
            `
        },
        skill: {
            title: "Keahlian (Skill)",
            icon: "fas fa-code",
            content: `
                <div class="w3-row">
                    <div class="w3-col s12 m4 w3-center"><i class="fas fa-brain" style="font-size: 48px; color:#b48c48;"></i></div>
                    <div class="w3-col s12 m8">
                        <h6><i class="fas fa-comments"></i> <strong>Soft Skill</strong></h6>
                        <div class="w3-progress-container w3-round w3-margin-bottom" style="background:#f0e2cf;">
                            <div class="w3-progressbar w3-round w3-amber" style="width:90%">Komunikasi Efektif</div>
                        </div>
                        <div class="w3-progress-container w3-round w3-margin-bottom" style="background:#f0e2cf;">
                            <div class="w3-progressbar w3-round w3-amber" style="width:85%">Kerjasama Tim</div>
                        </div>
                        <div class="w3-progress-container w3-round w3-margin-bottom" style="background:#f0e2cf;">
                        </div>
                        <h6 class="w3-margin-top"><i class="fas fa-laptop-code"></i> <strong>Skill Teknis</strong></h6>
                        <div class="w3-progress-container w3-round w3-margin-bottom" style="background:#f0e2cf;">
                            <div class="w3-progressbar w3-round w3-amber" style="width:80%">Microsoft Office (Word, Excel, PPT)</div>
                        </div>
                        <div class="w3-progress-container w3-round w3-margin-bottom" style="background:#f0e2cf;">
                            <div class="w3-progressbar w3-round w3-amber" style="width:75%">Pemrograman Dasar (Python)</div>
                        </div>
                        <div class="w3-progress-container w3-round" style="background:#f0e2cf;">
                        </div>
                        <p class="w3-margin-top"><i class="fas fa-certificate"></i> <strong>Bahasa:</strong> Indonesia (aktif)</p>
                    </div>
                </div>
            `
        }
    };

    // Ambil elemen konten dinamis
    const dynamicDiv = document.getElementById('dynamicContent');

    // Fungsi untuk merender halaman berdasarkan ID (status, pengalaman, dll)
    function renderPage(pageId) {
        const data = pagesData[pageId];
        if (!data) return;
        dynamicDiv.innerHTML = `
            <div class="w3-container">
                <div class="w3-cell-row w3-margin-bottom">
                    <div class="w3-cell w3-cell-middle">
                        <i class="${data.icon}" style="font-size: 42px; color: #c2a15b;"></i>
                        <span class="w3-xxlarge w3-text-dark-grey w3-margin-left">${data.title}</span>
                    </div>
                </div>
                <hr class="w3-border-amber">
                ${data.content}
                <div class="w3-margin-top w3-center">
                    <button id="backToHomeHint" class="w3-button w3-round-xxlarge w3-light-grey"><i class="fas fa-arrow-left"></i> Kembali ke Menu Utama</button>
                </div>
            </div>
        `;
        // event tombol kembali ke tampilan awal (menu utama tanpa detail)
        const backBtn = document.getElementById('backToHomeHint');
        if (backBtn) {
            backBtn.addEventListener('click', function() {
                // Tampilkan halaman awal seperti pertama kali: hanya foto + instruksi
                dynamicDiv.innerHTML = `
                    <div class="w3-center w3-padding-48">
                        <i class="fas fa-hand-point-up" style="font-size: 48px; color: #d6b575;"></i>
                        <h3 class="w3-text-dark-grey">✨ Selamat datang ✨</h3>
                        <div class="w3-margin-top">
                            <span class="section-badge"><i class="far fa-smile"></i> Portofolio interaktif</span>
                        </div>
                    </div>
                `;
                // hapus highlight menu? opsional, kita hilangkan class active
                document.querySelectorAll('.nav-card').forEach(card => {
                    card.classList.remove('menu-active');
                });
            });
        }
        // tambahkan highlight menu aktif
        document.querySelectorAll('.nav-card').forEach(card => {
            card.classList.remove('menu-active');
            if (card.getAttribute('data-page') === pageId) {
                card.classList.add('menu-active');
            }
        });
    }

    // Tambahkan event listener ke semua menu navigasi
    const menuItems = document.querySelectorAll('.nav-card');
    menuItems.forEach(menu => {
        menu.addEventListener('click', function(e) {
            const page = this.getAttribute('data-page');
            if (page && pagesData[page]) {
                renderPage(page);
            } else {
                console.warn("Halaman tidak ditemukan");
            }
        });
    });

    // [IMPORTANT] Tampilan awal: hanya menampilkan foto (sudah ada di header) dan tidak ada detail tambahan yang mengganggu.
    // Namun sesuai requirement: "pada tampilan awal hanya menampilkan foto. Lalu ada status, pengalaman, asal sekolah dan pendidikan saat ini, alamat, dan skill, nah pada bagian ini saat kita mengklik salah satunya maka akan masuk ke halaman berikutnya"
    // Sudah terpenuhi: foto di hero section, menu navigasi muncul. Saat awal belum ada detail, klik menu baru muncul halaman.
    // Untuk membuat lebih elegan dan memastikan asal sekolah & pendidikan saat ini tersedia pada halaman pendidikan, dan status berisi semester dll.
    // Saya juga menambahkan data asal sekolah (SMA) dan pendidikan saat ini di halaman pendidikan.
    // Skill menggunakan progress bar modern dari W3.CSS. Semua responsif dan modern.

    // bonus: drag & drop foto (optional)
    const photoFrame = document.getElementById('photoFrame');
    if (photoFrame) {
        photoFrame.addEventListener('dragover', (e) => {
            e.preventDefault();
            photoFrame.style.opacity = '0.8';
        });
        photoFrame.addEventListener('dragleave', () => {
            photoFrame.style.opacity = '1';
        });
        photoFrame.addEventListener('drop', (e) => {
            e.preventDefault();
            photoFrame.style.opacity = '1';
            const dt = e.dataTransfer;
            const files = dt.files;
            if (files.length > 0) {
                const file = files[0];
                if (file.type.startsWith('image/')) {
                    handleImageUpload(file);
                    // sync input
                    const dataTransfer = new DataTransfer();
                    dataTransfer.items.add(file);
                    fileInput.files = dataTransfer.files;
                } else {
                    alert('Harap drop file gambar (JPG/PNG)');
                }
            }
        });
    }
</script>

<!-- Penjelasan tambahan: Framework CSS yang digunakan adalah W3.CSS (dari w3schools.com) dengan kelas seperti w3-container, w3-card, w3-row-padding, w3-button, w3-progressbar dll. Juga memanfaatkan grid responsif. Tampilan menjadi lebih modern dan rapi, serta tetap mempertahankan warna cream / vintage. -->
</body>
</html>
