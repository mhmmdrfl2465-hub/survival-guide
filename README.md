# survival-guide
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Panduan Ekstraksi Biji Pala - Survival Guide</title>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #e74c3c;
            --accent: #f39c12;
            --light: #ecf0f1;
            --dark: #1a1a1a;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background: var(--primary);
            color: white;
            padding: 2rem 0;
            text-align: center;
            border-bottom: 5px solid var(--accent);
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "⚠️";
            position: absolute;
            font-size: 200px;
            opacity: 0.1;
            top: -50px;
            right: -50px;
            transform: rotate(45deg);
        }
        
        .survivor-badge {
            background: var(--secondary);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            display: inline-block;
            margin-bottom: 10px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .alert {
            background: #fff3cd;
            border: 1px solid #ffeaa7;
            border-radius: 10px;
            padding: 15px;
            margin: 20px 0;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .alert-icon {
            font-size: 2rem;
            color: var(--accent);
        }
        
        .tabs {
            display: flex;
            gap: 10px;
            margin: 30px 0;
            flex-wrap: wrap;
        }
        
        .tab {
            padding: 12px 24px;
            background: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .tab:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        
        .tab.active {
            background: var(--primary);
            color: white;
        }
        
        .tab-content {
            display: none;
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            margin-bottom: 30px;
        }
        
        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .team-member {
            background: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .team-member:hover {
            transform: translateY(-5px);
        }
        
        .member-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .step-card {
            background: #f8f9fa;
            border-left: 4px solid var(--accent);
            padding: 20px;
            margin: 20px 0;
            border-radius: 0 8px 8px 0;
        }
        
        .step-number {
            background: var(--accent);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-bottom: 15px;
        }
        
        .substeps {
            margin-left: 20px;
            margin-top: 10px;
        }
        
        .substep {
            margin: 8px 0;
            padding-left: 20px;
            position: relative;
        }
        
        .substep::before {
            content: "•";
            position: absolute;
            left: 0;
            color: var(--secondary);
            font-weight: bold;
        }
        
        .chemical-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        .chemical-table th,
        .chemical-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        
        .chemical-table th {
            background: var(--primary);
            color: white;
        }
        
        .chemical-table tr:hover {
            background: #f5f5f5;
        }
        
        .warning {
            background: #ffeaa7;
            border: 2px solid #fdcb6e;
            padding: 15px;
            border-radius: 8px;
            margin: 20px 0;
            font-weight: bold;
        }
        
        .download-btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 15px 30px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            margin: 20px 0;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .download-btn:hover {
            background: #c0392b;
            transform: scale(1.05);
        }
        
        .qr-code {
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background: white;
            border-radius: 10px;
            display: inline-block;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 50px;
            background: var(--primary);
            color: white;
            border-top: 5px solid var(--accent);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .tabs {
                flex-direction: column;
            }
            
            .team-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="survivor-badge">🚨 SURVIVAL TEAM DOCUMENTATION</div>
            <h1>Panduan Lengkap Ekstraksi Miristisin dari Biji Pala</h1>
            <p class="subtitle">Dokumentasi teknis untuk produksi ekstrak konsentrat tinggi - Disusun dalam kondisi darurat oleh tim survivor</p>
        </div>
    </header>

    <div class="container">
        <div class="alert">
            <div class="alert-icon">⚠️</div>
            <div>
                <strong>DOKUMEN SURVIVAL:</strong> Panduan ini dibuat dalam kondisi darurat setelah kecelakaan pesawat. Informasi diberikan untuk tujuan kelangsungan hidup dan pertukaran sumber daya dengan komunitas lokal.
            </div>
        </div>

        <div class="tabs">
            <button class="tab active" data-tab="team">👥 Tim Survivor</button>
            <button class="tab" data-tab="extraction">⚗️ Proses Ekstraksi</button>
            <button class="tab" data-tab="materials">🧪 Bahan & Peralatan</button>
            <button class="tab" data-tab="formulation">🚬 Formulasi Rokok</button>
            <button class="tab" data-tab="safety">⚠️ Keamanan</button>
            <button class="tab" data-tab="download">📥 Download</button>
        </div>

        <!-- Tab 1: Team -->
        <div id="team" class="tab-content active">
            <h2>👥 Tim Survivor</h2>
            <div class="team-grid">
                <div class="team-member">
                    <div class="member-icon">💻</div>
                    <h3>Colin</h3>
                    <p><strong>Expert Programmer</strong></p>
                    <p>Membuat script dan automasi proses. Bertanggung jawab atas dokumentasi digital.</p>
                </div>
                <div class="team-member">
                    <div class="member-icon">🧪</div>
                    <h3>Maya</h3>
                    <p><strong>Pharmacologist & Chemist</strong></p>
                    <p>Ahli kimia dan farmakologi. Menyusun prosedur ekstraksi dan formulasi.</p>
                </div>
                <div class="team-member">
                    <div class="member-icon">🔫</div>
                    <h3>Jimmy</h3>
                    <p><strong>Weapons Manufacturer</strong></p>
                    <p>Ahli produksi dan keamanan. Memastikan prosedur aman dan efektif.</p>
                </div>
                <div class="team-member">
                    <div class="member-icon">🍳</div>
                    <h3>Michael</h3>
                    <p><strong>Food & Beverage Expert</strong></p>
                    <p>Ahli formulasi dan produksi. Mengatur rasio dan kualitas bahan.</p>
                </div>
                <div class="team-member">
                    <div class="member-icon">🎰</div>
                    <h3>Johnson</h3>
                    <p><strong>3-Wish Lottery Winner</strong></p>
                    <p>Sumber solusi darurat ketika pengetahuan tim tidak mencukupi.</p>
                </div>
                <div class="team-member">
                    <div class="member-icon">👑</div>
                    <h3>Khan</h3>
                    <p><strong>Team Coordinator</strong></p>
                    <p>Koordinator tim dan komunikator dengan desa lokal.</p>
                </div>
            </div>
        </div>

        <!-- Tab 2: Extraction Process -->
        <div id="extraction" class="tab-content">
            <h2>⚗️ Proses Ekstraksi Miristisin</h2>
            
            <div class="step-card">
                <div class="step-number">1</div>
                <h3>Preparasi Bahan Baku</h3>
                <div class="substeps">
                    <div class="substep">Pilih biji pala tua berwarna coklat gelap</div>
                    <div class="substep">Bersihkan permukaan dengan etanol 70%</div>
                    <div class="substep">Keringkan pada suhu 40°C selama 24 jam</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">2</div>
                <h3>Size Reduction</h3>
                <div class="substeps">
                    <div class="substep">Giling biji hingga ukuran 80 mesh (0.18 mm)</div>
                    <div class="substep">Gunakan penggiling mekanik untuk hasil optimal</div>
                    <div class="substep">Simpan bubuk dalam wadah kedap udara</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">3</div>
                <h3>Ekstraksi Soxhlet</h3>
                <div class="substeps">
                    <div class="substep">Masukkan 100g bubuk dalam thimble Soxhlet</div>
                    <div class="substep">Gunakan 500mL pelarut non-polar (aseton/n-heksana)</div>
                    <div class="substep">Ekstrak selama 6-8 jam pada suhu 60°C</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">4</div>
                <h3>Penyaringan</h3>
                <div class="substeps">
                    <div class="substep">Saring ekstrak panas dengan kertas saring Whatman No.1</div>
                    <div class="substep">Cuci residu dengan 100mL pelarut fresh</div>
                    <div class="substep">Gabungkan semua filtrat</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">5</div>
                <h3>Evaporasi Pelarut</h3>
                <div class="substeps">
                    <div class="substep">Gunakan rotary evaporator pada suhu 40°C</div>
                    <div class="substep">Atau evaporasi alami di tempat berventilasi</div>
                    <div class="substep">Hentikan ketika volume 10-20% dari awal</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">6</div>
                <h3>Pemurnian</h3>
                <div class="substeps">
                    <div class="substep">Lakukan kromatografi kolom cepat dengan silika gel</div>
                    <div class="substep">Elusi dengan n-heksana:EtOAc (gradien 100:0 → 70:30)</div>
                    <div class="substep">Kumpulkan fraksi mengandung miristisin</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">7</div>
                <h3>Konsentrasi</h3>
                <div class="substeps">
                    <div class="substep">Evaporasi fraksi murni hingga kering</div>
                    <div class="substep">Timbang ekstrak yang diperoleh</div>
                    <div class="substep">Hitung rendemen (%)</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">8</div>
                <h3>Analisis Kualitas</h3>
                <div class="substeps">
                    <div class="substep">Uji dengan TLC (Rf ≈ 0.65 dalam n-heks:EtOAc 8:2)</div>
                    <div class="substep">Spektrofotometri UV pada λ 235 nm</div>
                    <div class="substep">Verifikasi dengan uji Liebermann-Burchard</div>
                </div>
            </div>
        </div>

        <!-- Tab 3: Materials -->
        <div id="materials" class="tab-content">
            <h2>🧪 Bahan & Peralatan</h2>
            
            <table class="chemical-table">
                <thead>
                    <tr>
                        <th>Bahan Kimia</th>
                        <th>Jumlah</th>
                        <th>Fungsi</th>
                        <th>Alternatif</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Biji pala utuh</td>
                        <td>500 g</td>
                        <td>Sumber miristisin</td>
                        <td>Minimal 100 g</td>
                    </tr>
                    <tr>
                        <td>Aseton teknis</td>
                        <td>1000 mL</td>
                        <td>Pelarut utama</td>
                        <td>N-Heksana, Petroleum eter</td>
                    </tr>
                    <tr>
                        <td>Etanol absolut</td>
                        <td>200 mL</td>
                        <td>Pembersih & formulasi</td>
                        <td>Spiritus 96%</td>
                    </tr>
                    <tr>
                        <td>Silika gel 60</td>
                        <td>100 g</td>
                        <td>Media kromatografi</td>
                        <td>Alumina netral</td>
                    </tr>
                    <tr>
                        <td>Arang aktif</td>
                        <td>10 g</td>
                        <td>Penjernih ekstrak</td>
                        <td>Tanpa alternatif</td>
                    </tr>
                </tbody>
            </table>

            <h3 style="margin-top: 30px;">🛠️ Peralatan</h3>
            <div class="substeps">
                <div class="substep">Alat Soxhlet lengkap dengan kondensor</div>
                <div class="substep">Labu alas bulat 2000 mL</div>
                <div class="substep">Penggiling biji/coffee grinder</div>
                <div class="substep">Kertas saring Whatman No. 1</div>
                <div class="substep">Rotary evaporator (opsional)</div>
                <div class="substep">Penangas air dengan pengatur suhu</div>
                <div class="substep">Pipet ukur berbagai volume</div>
                <div class="substep">Wadah kaca kedap udara</div>
            </div>
        </div>

        <!-- Tab 4: Formulation -->
        <div id="formulation" class="tab-content">
            <h2>🚬 Formulasi untuk Rokok</h2>
            
            <div class="warning">
                ⚠️ DOSIS AWAL RENDAH: Mulai dengan 5mg per rokok untuk uji sensitivitas
            </div>

            <h3>Perhitungan Dosis</h3>
            <table class="chemical-table">
                <thead>
                    <tr>
                        <th>Potensi</th>
                        <th>Ekstrak/Rokok</th>
                        <th>Etanol</th>
                        <th>Onset</th>
                        <th>Durasi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Rendah</td>
                        <td>5-10 mg</td>
                        <td>1 mL</td>
                        <td>30-60 menit</td>
                        <td>2-4 jam</td>
                    </tr>
                    <tr>
                        <td>Medium</td>
                        <td>10-25 mg</td>
                        <td>2 mL</td>
                        <td>20-40 menit</td>
                        <td>4-8 jam</td>
                    </tr>
                    <tr>
                        <td>Tinggi</td>
                        <td>25-50 mg</td>
                        <td>3 mL</td>
                        <td>10-20 menit</td>
                        <td>8-12 jam</td>
                    </tr>
                </tbody>
            </table>

            <h3>Prosedur Pencampuran</h3>
            <div class="step-card">
                <div class="step-number">A</div>
                <h3>Persiapan Larutan</h3>
                <div class="substeps">
                    <div class="substep">Timbang ekstrak sesuai dosis yang diinginkan</div>
                    <div class="substep">Larutkan dalam etanol absolut (1-3 mL)</div>
                    <div class="substep">Aduk hingga homogen sempurna</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">B</div>
                <h3>Infusi ke Tembakau</h3>
                <div class="substeps">
                    <div class="substep">Siapkan 1 gram tembakau kering per rokok</div>
                    <div class="substep">Semprotkan larutan ekstrak secara merata</div>
                    <div class="substep">Aduk dengan sendok kaca hingga merata</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">C</div>
                <h3>Pengeringan</h3>
                <div class="substeps">
                    <div class="substep">Ratakan tembakau di atas kertas perkamen</div>
                    <div class="substep">Keringkan pada suhu ruang selama 24 jam</div>
                    <div class="substep">Pastikan etanol menguap sepenuhnya</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">D</div>
                <h3>Pengemasan</h3>
                <div class="substeps">
                    <div class="substep">Gunakan tembakau yang telah diinfus untuk menggulung</div>
                    <div class="substep">Simpan rokok jadi dalam wadah kedap udara</div>
                    <div class="substep">Berikan label dengan informasi dosis</div>
                </div>
            </div>
        </div>

        <!-- Tab 5: Safety -->
        <div id="safety" class="tab-content">
            <h2>⚠️ Protokol Keamanan</h2>
            
            <div class="warning">
                🔥 PELARUT MUDAH TERBAKAR: Kerjakan di area berventilasi, jauh dari api
            </div>

            <h3>Data Toksisitas</h3>
            <div class="substeps">
                <div class="substep">LD50 oral (tikus): 1000 mg/kg</div>
                <div class="substep">Toksisitas utama: Hepatotoksik (kerusakan hati)</div>
                <div class="substep">Efek samping: Mual, pusing, takikardia, halusinasi</div>
                <div class="substep">Durasi efek: 6-12 jam tergantung dosis</div>
            </div>

            <h3>Prosedur Darurat</h3>
            <div class="step-card">
                <div class="step-number">1</div>
                <h3>Kontak Kulit</h3>
                <div class="substeps">
                    <div class="substep">Segera cuci dengan sabun dan air mengalir</div>
                    <div class="substep">Lepaskan pakaian yang terkontaminasi</div>
                    <div class="substep">Cari pertolongan medis jika iritasi berlanjut</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">2</div>
                <h3>Tertelan</h3>
                <div class="substeps">
                    <div class="substep">Jangan dimuntahkan kecuali diinstruksikan profesional</div>
                    <div class="substep">Berikan arang aktif jika tersedia</div>
                    <div class="substep">Segera cari pertolongan medis</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">3</div>
                <h3>Kebakaran</h3>
                <div class="substeps">
                    <div class="substep">Gunakan pemadam CO₂ atau buskim</div>
                    <div class="substep">Jangan gunakan air untuk pelarut organik</div>
                    <div class="substep">Evakuasi area jika api membesar</div>
                </div>
            </div>

            <h3>Penyimpanan</h3>
            <div class="substeps">
                <div class="substep">Simpan ekstrak dalam wadah gelap kedap udara</div>
                <div class="substep">Suhu penyimpanan optimal: 2-8°C</div>
                <div class="substep">Umur simpan: 6 bulan dalam atmosfer nitrogen</div>
                <div class="substep">Jauhkan dari jangkauan anak-anak</div>
            </div>
        </div>

        <!-- Tab 6: Download -->
        <div id="download" class="tab-content">
            <h2>📥 Download Dokumentasi</h2>
            
            <p>Download versi lengkap untuk akses offline:</p>
            
            <div style="display: flex; gap: 20px; flex-wrap: wrap; margin: 30px 0;">
                <a href="#" class="download-btn" onclick="generatePDF()">
                    📄 Download PDF Guide
                </a>
                
                <a href="#" class="download-btn" onclick="generateWord()">
                    📝 Download Word Document
                </a>
                
                <a href="#" class="download-btn" onclick="generateLaTeX()">
                    📚 Download LaTeX Source
                </a>
            </div>

            <div class="qr-code">
                <h3>📱 Scan untuk Akses Cepat</h3>
                <div id="qrcode" style="width: 200px; height: 200px; margin: 20px auto; background: #eee; display: flex; align-items: center; justify-content: center; border-radius: 10px;">
                    [QR Code akan digenerate]
                </div>
                <p>Scan untuk membuka halaman ini di perangkat lain</p>
            </div>

            <h3>🌐 Deploy ke GitHub Pages</h3>
            <div class="step-card">
                <div class="step-number">1</div>
                <h3>Buat Repository GitHub</h3>
                <div class="substeps">
                    <div class="substep">Login ke GitHub.com</div>
                    <div class="substep">Buat repository baru: "survival-guide"</div>
                    <div class="substep">Upload file HTML ini</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">2</div>
                <h3>Aktifkan GitHub Pages</h3>
                <div class="substeps">
                    <div class="substep">Settings → Pages</div>
                    <div class="substep">Branch: main, folder: / (root)</div>
                    <div class="substep">Save, tunggu 1-2 menit</div>
                </div>
            </div>

            <div class="step-card">
                <div class="step-number">3</div>
                <h3>Akses Online</h3>
                <div class="substeps">
                    <div class="substep">URL: https://[username].github.io/survival-guide</div>
                    <div class="substep">Bisa diakses dari perangkat mana pun</div>
                    <div class="substep">Tidak perlu instalasi khusus</div>
                </div>
            </div>

            <div style="background: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 30px;">
                <h4>💡 Tip untuk Desa:</h4>
                <p>Halaman web ini dapat diakses offline setelah di-download. Cukup buka file HTML di browser ponsel atau komputer tanpa koneksi internet.</p>
            </div>
        </div>

        <div style="text-align: center; margin: 50px 0;">
            <button class="download-btn" onclick="shareDocument()">
                📤 Bagikan ke Desa
            </button>
            <p style="margin-top: 15px; font-size: 0.9rem; color: #666;">
                Dokumen ini berisi informasi untuk kelangsungan hidup tim<br>
                Dibuat dengan ❤️ oleh survivor penerbangan 231
            </p>
        </div>
    </div>

    <footer>
        <div class="container">
            <p>🚨 Survival Documentation v1.0 | Emergency Use Only</p>
            <p style="margin-top: 10px; font-size: 0.9rem; opacity: 0.8;">
                Untuk pertukaran dengan: Makanan, Tempat Tinggal, Pertolongan Medis
            </p>
        </div>
    </footer>

    <script>
        // Tab Navigation
        document.querySelectorAll('.tab').forEach(tab => {
            tab.addEventListener('click', () => {
                // Remove active class from all tabs and contents
                document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
                document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
                
                // Add active class to clicked tab
                tab.classList.add('active');
                
                // Show corresponding content
                const tabId = tab.getAttribute('data-tab');
                document.getElementById(tabId).classList.add('active');
            });
        });

        // Generate Simple QR Code (text-based)
        function generateSimpleQR() {
            const qrDiv = document.getElementById('qrcode');
            const url = window.location.href;
            qrDiv.innerHTML = `
                <div style="text-align: center; padding: 20px;">
                    <div style="font-family: monospace; font-size: 10px; letter-spacing: 2px;">
                        ██████████████<br>
                        █░░░░░░░░░░░█<br>
                        █░█████████░█<br>
                        █░█░░░░░░░█░█<br>
                        █░█░█████░█░█<br>
                        █░█░█░░░█░█░█<br>
                        █░█░█████░█░█<br>
                        █░█░░░░░░░█░█<br>
                        █░█████████░█<br>
                        █░░░░░░░░░░░█<br>
                        ██████████████<br>
                    </div>
                    <small>Scan simulation</small>
                </div>
            `;
        }

        // Generate PDF function
        function generatePDF() {
            alert('📄 Generating PDF...\n\nSimpan halaman ini sebagai PDF:\n1. Ctrl+P (Windows) / Cmd+P (Mac)\n2. Pilih "Save as PDF"\n3. Klik "Save"\n\nPDF siap digunakan offline!');
            window.print();
        }

        function generateWord() {
            const content = document.body.innerText;
            const blob = new Blob([content], { type: 'text/plain' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'survival-guide.txt';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            alert('📝 Dokumentasi telah di-download sebagai file teks (.txt)');
        }

        function generateLaTeX() {
            const latexCode = `\\documentclass{article}\n\\begin{document}\n\\title{Survival Guide}\n\\maketitle\n\\section{Ekstraksi Biji Pala}\nDokumentasi lengkap tersedia di: ${window.location.href}\n\\end{document}`;
            const blob = new Blob([latexCode], { type: 'text/plain' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'survival-guide.tex';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            alert('📚 File LaTeX telah di-download');
        }

        function shareDocument() {
            if (navigator.share) {
                navigator.share({
                    title: 'Panduan Ekstraksi Biji Pala - Survival Guide',
                    text: 'Dokumentasi lengkap ekstraksi miristisin untuk pertukaran sumber daya',
                    url: window.location.href
                });
            } else {
                alert('📤 Bagikan URL ini ke desa:\n\n' + window.location.href + '\n\nAtau simpan halaman untuk akses offline (Ctrl+S / Cmd+S)');
            }
        }

        // Initialize
        generateSimpleQR();
        
        // Auto-save for offline use
        if ('serviceWorker' in navigator) {
            navigator.serviceWorker.register('/sw.js').catch(console.error);
        }

        // Add last updated
        document.addEventListener('DOMContentLoaded', () => {
            const footer = document.querySelector('footer .container');
            const date = new Date().toLocaleDateString('id-ID', {
                weekday: 'long',
                year: 'numeric',
                month: 'long',
                day: 'numeric',
                hour: '2-digit',
                minute: '2-digit'
            });
            const updateElement = document.createElement('p');
            updateElement.style.marginTop = '10px';
            updateElement.style.fontSize = '0.8rem';
            updateElement.style.opacity = '0.7';
            updateElement.textContent = `🕐 Diperbarui: ${date}`;
            footer.appendChild(updateElement);
        });
    </script>
</body>
</html>
