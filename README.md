
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Portofolio Julvin Waruwu</title>

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@300;700&family=Pacifico&display=swap');

        body {
            margin: 0;
            font-family: 'Nunito', sans-serif;
            background: #fff0f6;
            color: #f73dbf;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-bottom: 60px;
        }

        header {
            width: 100%;
            background: linear-gradient(135deg, #f8d7e3, #f3a9c9);
            padding: 30px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(243, 169, 201, 0.6);
        }

        header h1 {
            font-family: 'Pacifico', cursive;
            margin: 0;
            font-size: 3.6rem;
            color: #fc00b0;
            text-shadow: 0 2px 5px #ffffff;
        }

        /* Animated pink ribbons */
        .pink-ribbon {
            position: absolute;
            width: 140px;
            height: 35px;
            background: linear-gradient(45deg, #f9aacd, #f26ca9);
            border-radius: 0 25px 25px 0;
            color: white;
            font-weight: 700;
            font-size: 1rem;
            line-height: 35px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(242, 108, 169, 0.7);
            user-select: none;
            animation: floatRibbon 4.5s ease-in-out infinite alternate;
            z-index: 10;
        }

        .pink-ribbon.left {
            top: 12px;
            left: 10px;
            animation-delay: 0s;
        }

        .pink-ribbon.right {
            bottom: 15px;
            right: 10px;
            animation-delay: 2.2s;
            border-radius: 25px 0 0 25px;
        }

        @keyframes floatRibbon {
            0% {
                transform: translateY(0) rotate(-4deg);
            }
            100% {
                transform: translateY(12px) rotate(4deg);
            }
        }

        nav {
            margin: 30px 0 15px;
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        button.section-btn {
            background-color: #f6c5d6;
            border: none;
            border-radius: 30px;
            padding: 12px 25px;
            font-weight: 700;
            cursor: pointer;
            color: #6f3652;
            box-shadow: 0 3px 10px rgba(242, 108, 169, 0.3);
            transition: background-color 0.3s ease, box-shadow 0.3s ease;
            font-size: 1.1rem;
        }

        button.section-btn:hover,
        button.section-btn.active {
            background-color: #f26ca9;
            color: white;
            box-shadow: 0 5px 18px rgba(242, 108, 169, 0.7);
        }

        main {
            width: 90%;
            max-width: 900px;
            background: white;
            border-radius: 20px;
            padding: 30px 35px;
            box-shadow: 0 7px 20px rgba(242, 108, 169, 0.2);
            min-height: 450px;
        }

        section {
            display: none;
            animation: fadeUp 0.5s ease forwards;
        }

        section.active {
            display: block;
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(18px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Data Pribadi */
        #data-pribadi {
            display: flex;
            flex-wrap: wrap;
            gap: 35px;
            justify-content: center;
            align-items: center;
        }

        .profile-pic {
            width: 250px;
            height: 250px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(242, 108, 169, 0.25);
            flex-shrink: 0;
            border: 6px solid #f26ca9;
        }

        .profile-pic img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        .details {
            flex: 1 1 320px;
            font-size: 1.15rem;
            color: #6b3a55;
            line-height: 1.6;
        }

        .details p {
            margin: 14px 0;
        }

        /* Social media links */
        .social-links {
            margin-top: 25px;
            text-align: center;
        }

        .social-links a {
            display: inline-block;
            width: 52px;
            height: 52px;
            line-height: 52px;
            margin: 0 14px;
            font-size: 1.9rem;
            border-radius: 50%;
            background: #f6a1bf;
            box-shadow: 0 4px 16px rgba(242, 108, 169, 0.6);
            color: white;
            text-align: center;
            text-decoration: none;
            transition: background-color 0.3s ease;
            user-select: none;
        }

        .social-links a:hover {
            background-color: #f26ca9;
            box-shadow: 0 6px 22px rgba(242, 108, 169, 0.9);
        }

        /* Riwayat Pendidikan & Prestasi */
        #riwayat h3,
        #hobi h3,
        #skill h2 {
            color: #b25478;
            margin-bottom: 10px;
        }

        ul {
            line-height: 1.5;
            margin-top: 15px;
            padding-left: 25px;
            color: #7a477e;
        }

        /* Hobi with separate large images per hobby */
        #hobi .hobi-item {
            margin-bottom: 40px;
            text-align: center;
        }

        #hobi .hobi-item img {
            width: 300px;
            max-width: 100%;
            border-radius: 20px;
            box-shadow: 0 10px 28px rgba(242, 108, 169, 0.25);
            transition: transform 0.3s ease;
        }

        #hobi .hobi-item img:hover {
            transform: scale(1.07);
        }

        @media (max-width: 720px) {
            #data-pribadi {
                flex-direction: column;
                align-items: center;
                gap: 20px;
            }

            .profile-pic {
                width: 200px;
                height: 200px;
            }

            .details {
                flex: none;
                width: 100%;
                text-align: center;
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>Get to Know Me : Jujuw 🎀🌺</h1>
        <div class="pink-ribbon left">Hewoo! ✨</div>
        <div class="pink-ribbon right">Welcome! 💐</div>
    </header>

    <nav>
        <button class="section-btn active" data-section="data-pribadi">Data Pribadi</button>
        <button class="section-btn" data-section="riwayat">Riwayat Pendidikan & Prestasi</button>
        <button class="section-btn" data-section="hobi">Hobi</button>
        <button class="section-btn" data-section="skill">Skill</button>
    </nav>

    <main>
        <section id="data-pribadi" class="active">
            <div class="profile-pic">
                <img src="https://github.com/user-attachments/assets/1eb25661-9164-4807-b325-853eaf313c91.jpg" alt="Foto Profil" />
            </div>
            <div class="details">
                <p><strong>Nama:</strong>  Julvin Rut Nasrani Waruwu</p>
                <p><strong>NIM:</strong> 4252250008</p>
                <p><strong>Tempat & Tanggal lahir:</strong> Sisarahili, 14 Juli 2007</p>
                <p><strong>Agama:</strong> Kristen Protestan</p>
                <p><strong>Email:</strong> julvinrnwaruwu@gmail.com</p>
                <p><strong>Status:</strong> Mahasiswa</p>
                <p><strong>Prodi:</strong> S1 - Ilmu Komputer</p>
                <p><strong>Alamat:</strong> Perumnas Mandala, Medan, Sumatera Utara</p>
                <div class="social-links">
                    <a href="https://instagram.com/jlvnnw" target="_blank" aria-label="Instagram" rel="noopener noreferrer" title="Instagram">📱</a>
                    <a href="https://wa.me/6281274330984" target="_blank" aria-label="WhatsApp" rel="noopener noreferrer"
                        title="WhatsApp">💌</a>
                </div>
            </div>
        </section>

        <section id="riwayat">
            <h2>Riwayat Pendidikan & Prestasi</h2>
            <h3>Pendidikan</h3>
            <ul>
                 <li>SD ADVENT CIMINDI BANDUNG (2013 - 2019)</li>
                 <li>UPT SPF SMP NEGERI 5 PERCUT SEI TUAN (2019 - 2022)</li>
                 <li>SMA NEGERI 11 MEDAN (2022 - 2025)</li>
                 <li>Universitas Negeri Medan, Ilmu Komputer (2025 - Sekarang)</li>
            </ul>
            <h3>Prestasi</h3>
            <ul>
                <li>Rangking 1 di dalam kelas selama 3 tahun di SMA Negeri 11 Medan</li>
                <li>Menjadi perwakilan sekolah sebagai dalam Baju adat selama 2 tahun</li>
            </ul>
        </section>

        <section id="hobi">
            <div class="hobi-item">
                <h3>Menari</h3>
                <img src="https://github.com/user-attachments/assets/35833566-9419-44af-a47c-eacd5ead4c1b.JPG" alt="Menari" />
            </div>
            <div class="hobi-item">
                <h3>Editing Foto</h3>
                <img src="https://github.com/user-attachments/assets/75a07801-5045-402e-a5be-b546804b714d.jpg" alt="Editing Foto" />
            </div>
            <div class="hobi-item">
                <h3>Menonton Anime, Film, Drakor</h3>
                <img src="https://github.com/user-attachments/assets/39ce5e6c-ae9d-4214-b9c6-b85ca61c5ca9.jpg" alt="Menonton Anime, Film, Drakor" /> 
                <img src="https://github.com/user-attachments/assets/6c26b040-de5f-4b7b-b539-d108f6560dd7.jpg" alt="Menonton Anime, Film, Drakor" />
            </div>
        </section>

        <section id="skill">
            <h2>Skill</h2>
            <ul>
                <li>Microsoft Office (Word, Presentation, Excel)</li>
                <li>Desain Grafis dengan Canva</li>
                <li>Bahasa Inggris (Conversation)</li>
            </ul>
        </section>
    </main>

    <script>
        const buttons = document.querySelectorAll('.section-btn');
        const sections = document.querySelectorAll('main section');

        buttons.forEach(button => {
            button.addEventListener('click', () => {
                buttons.forEach(btn => btn.classList.remove('active'));
                sections.forEach(sec => sec.classList.remove('active'));

                button.classList.add('active');
                const target = button.getAttribute('data-section');
                document.getElementById(target).classList.add('active');
            });
        });
    </script>
</body>

</html>


