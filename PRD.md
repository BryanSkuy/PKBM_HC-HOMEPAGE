# 📋 Product Requirements Document (PRD)

## Website PKBM Hardiansyah Cerdasio

---

| Informasi Proyek | Detail |
|---|---|
| **Nama Produk** | Website PKBM Hardiansyah Cerdasio |
| **Versi Dokumen** | 2.1.0 |
| **Tanggal Dibuat** | 27 Juli 2026 |
| **Terakhir Diperbarui** | 27 Juli 2026 |
| **Tipe Proyek** | Website Statis (Multi-Page) |
| **Platform Target** | Desktop & Mobile (Responsive) |
| **Teknologi** | HTML5, CSS3 (Vanilla), JavaScript (Vanilla) |
| **Status** | ✅ MVP Selesai — Siap untuk pengembangan di Canva Code |

---

## 1. 🎯 Ringkasan Eksekutif

### 1.1 Latar Belakang
PKBM (Pusat Kegiatan Belajar Masyarakat) Hardiansyah Cerdasio adalah lembaga pendidikan nonformal yang berlokasi di Sawangan, Depok, Jawa Barat. Lembaga ini menyediakan program pendidikan kesetaraan (Paket A, B, dan C) bagi masyarakat yang belum menyelesaikan pendidikan formal.

### 1.2 Tujuan Proyek
Membangun website profil dan pendaftaran online untuk PKBM Hardiansyah Cerdasio yang berfungsi sebagai:
- **Branding digital** — Membangun citra profesional dan terpercaya secara online.
- **Pusat informasi** — Menyediakan informasi lengkap tentang program, syarat pendaftaran, biaya, dan jadwal.
- **Kanal pendaftaran** — Memfasilitasi pendaftaran peserta didik baru melalui formulir online yang terintegrasi dengan WhatsApp.
- **Alat komunikasi** — Mempermudah calon peserta didik dan orang tua menghubungi pihak PKBM.

### 1.3 Target Pengguna

| Persona | Deskripsi | Kebutuhan Utama |
|---|---|---|
| **Calon Peserta Didik** | Usia 12+ tahun, putus sekolah atau belum selesai pendidikan formal | Info program, syarat pendaftaran, jadwal fleksibel |
| **Orang Tua / Wali** | Orang tua yang mencari program pendidikan alternatif untuk anaknya | Legitimasi lembaga, biaya, testimoni |
| **Masyarakat Umum** | Warga Sawangan, Depok dan sekitarnya | Info lokasi, kontak, galeri kegiatan |
| **Pihak Dinas Pendidikan** | Instansi terkait yang memverifikasi legalitas | Profil lembaga, akreditasi, visi misi |

---

## 2. 🏗️ Arsitektur & Struktur Proyek

### 2.1 Struktur Direktori

```
APP PKBM/
├── index.html              # Halaman Beranda (Landing Page)
├── program.html            # Halaman Program Pendidikan
├── tentang.html            # Halaman Tentang Kami
├── kontak.html             # Halaman Kontak & Pendaftaran
├── PRD.md                  # Product Requirements Document (file ini)
├── css/
│   └── style.css           # Stylesheet utama (Design System + Komponen) — ~58KB
├── js/
│   └── main.js             # JavaScript utama (Interaktivitas) — ~10KB
└── assets/
    └── images/
        └── logo.png        # Logo PKBM Hardiansyah Cerdasio
```

### 2.2 Arsitektur Teknis

| Aspek | Detail |
|---|---|
| **Tipe** | Static Multi-Page Application (MPA) |
| **Rendering** | Client-side rendering |
| **Styling** | Vanilla CSS dengan Design System (CSS Custom Properties) |
| **JavaScript** | Vanilla JS, ES6+ (no framework) |
| **Font** | Google Fonts — `Inter` (body), `Outfit` (heading) |
| **Ikon** | Inline SVG (tidak ada dependensi library ikon) |
| **Gambar** | Unsplash untuk placeholder + logo lokal |
| **Framework** | Tanpa framework — 100% vanilla |

### 2.3 Design System (CSS Custom Properties)

#### Palet Warna
| Token | Hex | Penggunaan |
|---|---|---|
| `--primary` | `#0E6B3A` | Warna utama (hijau tua), CTA utama |
| `--primary-dark` | `#084D29` | Hover state hijau |
| `--primary-light` | `#1A8E4E` | Gradient hijau, aksen |
| `--secondary` | `#1C5BA5` | Warna sekunder (biru), Paket B |
| `--secondary-light` | `#2E78C8` | Gradient biru |
| `--tertiary` | `#1A3C6E` | Warna tersier (biru tua), Paket C |
| `--tertiary-light` | `#2E5A9A` | Gradient tersier |
| `--accent-gold` | `#C8963E` | Warna aksen (emas), CTA premium |
| `--accent-gold-light` | `#E2B861` | Gradient emas |
| `--accent-red` | `#C0392B` | Warna darurat/error |
| `--leaf-green` | `#2E7D32` | Hijau daun, elemen dekoratif |
| `--bg` | `#FAFDF8` | Background halaman |
| `--surface` | `#EDF5E9` | Background section alternatif |
| `--surface-gold` | `#FFF8EC` | Background emas |
| `--surface-dark` | `#0A1F12` | Background dark (footer) |
| `--card-bg` | `rgba(255,255,255,0.94)` | Background card |

#### Warna Teks
| Token | Hex | Penggunaan |
|---|---|---|
| `--text-primary` | `#152A1D` | Teks utama |
| `--text-secondary` | `#37634A` | Teks sekunder |
| `--text-light` | `#6B9C7E` | Teks ringan |
| `--text-on-dark` | `#D4F0DC` | Teks pada background gelap |
| `--text-white` | `#FFFFFF` | Teks putih |

#### Warna Border
| Token | Hex | Penggunaan |
|---|---|---|
| `--border` | `#A8D9B2` | Border standar |
| `--border-light` | `#D4EDDA` | Border tipis |

#### Tipografi
| Elemen | Font | Size | Weight |
|---|---|---|---|
| `h1` | Outfit | clamp(2.2rem, 5vw, 3.5rem) | 700-800 |
| `h2` | Outfit | clamp(1.8rem, 4vw, 2.8rem) | 700 |
| `h3` | Outfit | clamp(1.3rem, 3vw, 1.8rem) | 700 |
| `h4` | Outfit | clamp(1.1rem, 2.5vw, 1.4rem) | 700 |
| Body | Inter | 16px | 400 |
| Button | Inter | 0.95rem | 600 |

#### Spacing
| Token | Nilai |
|---|---|
| `--space-xs` | 0.25rem |
| `--space-sm` | 0.5rem |
| `--space-md` | 1rem |
| `--space-lg` | 1.5rem |
| `--space-xl` | 2rem |
| `--space-2xl` | 3rem |
| `--space-3xl` | 4rem |
| `--space-4xl` | 6rem |

#### Border Radius
| Token | Nilai | Penggunaan |
|---|---|---|
| `--radius-sm` | 8px | Input, badge kecil |
| `--radius-md` | 12px | Card content |
| `--radius-lg` | 16px | Card utama |
| `--radius-xl` | 24px | Hero elements |
| `--radius-full` | 9999px | Pill button, badge |

#### Shadows
| Token | Nilai | Penggunaan |
|---|---|---|
| `--shadow-sm` | `0 2px 8px rgba(14,107,58,0.08)` | Elemen ringan |
| `--shadow-md` | `0 4px 16px rgba(14,107,58,0.12)` | Card standar |
| `--shadow-lg` | `0 8px 32px rgba(14,107,58,0.15)` | Card hover |
| `--shadow-xl` | `0 16px 48px rgba(14,107,58,0.18)` | Elemen menonjol |
| `--shadow-glow` | `0 0 30px rgba(14,107,58,0.22)` | Glow effect |

#### Transitions
| Token | Nilai | Penggunaan |
|---|---|---|
| `--ease` | `cubic-bezier(0.4, 0, 0.2, 1)` | Transisi standar |
| `--ease-spring` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Efek bounce |
| `--duration-fast` | 200ms | Interaksi cepat |
| `--duration-normal` | 350ms | Transisi standar |
| `--duration-slow` | 500ms | Animasi halus |

---

## 3. 📄 Spesifikasi Halaman

### 3.1 Halaman Beranda (`index.html`)

**Tujuan**: Landing page utama yang memberikan kesan pertama yang kuat dan mengarahkan pengunjung ke informasi penting serta pendaftaran.

#### Komponen & Seksi:

| # | Seksi | Deskripsi | Fitur Interaktif |
|---|---|---|---|
| 1 | **Navbar** | Navigasi fixed dengan logo, menu links (Beranda, Program, Tentang, Kontak), dan CTA "Daftar Sekarang" | Scroll effect (transparent → glassmorphism), hamburger menu mobile |
| 2 | **Hero** | Full-viewport hero dengan **aurora mesh background** (3 blob animasi) + **8 floating particles**, tagline centered, deskripsi, 2 CTA buttons | Aurora blob animation, particle animation, wave SVG separator di bawah |
| 3 | **Tentang Preview** | Grid 2 kolom: gambar KBM + teks profil singkat + 4 fitur unggulan + link "Selengkapnya" | Scroll reveal (left/right) |
| 4 | **Program Pendidikan** | Grid 3 kolom: card Paket A, B, C masing-masing dengan emoji ikon, deskripsi, fitur, dan link detail | Hover lift effect, color-coded top border |
| 5 | **Keunggulan** | Grid 4 kolom: Ijazah Resmi, Jadwal Fleksibel, Biaya Terjangkau, Tutor Profesional | Scroll reveal animation |
| 6 | **Testimoni** | Slider/carousel: 3 testimoni alumni dengan nama, program, dan tahun | Auto-slide (5 detik), dot navigation, touch swipe |
| 7 | **CTA Section** | Banner ajakan daftar dengan 2 tombol: "Daftar Sekarang" + "Chat WhatsApp" | — |
| 8 | **Footer** | 4 kolom: Brand info + Social links (FB, IG, YT), Menu navigasi, Program links, Info kontak | — |
| 9 | **WhatsApp Float** | Tombol floating WhatsApp di pojok kanan bawah | Link ke wa.me |
| 10 | **Lightbox** | Modal overlay untuk melihat gambar full-screen | Keyboard ESC, click overlay to close |

> **Catatan**: Seksi **Statistik** (counter animation) sudah **dihapus** dari implementasi beranda saat ini. Elemen `.stat-number` dan counter animation di JS tetap tersedia jika ingin diaktifkan kembali.

#### Hero Detail:
- **Layout**: Centered single-column (bukan 2 kolom seperti v1)
- **Background**: Aurora mesh dengan 3 blob animasi (`.hero-aurora-blob`) + overlay gelap
- **Particles**: 8 partikel floating (`.particle.p1` — `.particle.p8`)
- **Wave Separator**: SVG wave di bagian bawah hero, transisi mulus ke section berikutnya
- **Tidak ada logo** di dalam hero (logo hanya di navbar)

#### Testimoni:
1. **Ahmad Suryana** — Alumni Paket C 2023: Berhasil mendapatkan ijazah SMA dan bekerja di perusahaan baik.
2. **Siti Rahayu** — Alumni Paket C 2024: Melanjutkan kuliah berkat ijazah Paket C.
3. **Budi Hartono** — Orang Tua 2024: Anak berhasil menyelesaikan pendidikan SD melalui Paket A.

---

### 3.2 Halaman Program (`program.html`)

**Tujuan**: Menampilkan detail lengkap ketiga program pendidikan kesetaraan.

#### Komponen & Seksi:

| # | Seksi | Deskripsi |
|---|---|---|
| 1 | **Navbar** | Navbar dengan class `scrolled` (selalu solid) |
| 2 | **Page Header** | Breadcrumb + Judul + Deskripsi |
| 3 | **Program Tabs** | 3 tab buttons: Paket A, Paket B, Paket C |
| 4 | **Tab Content** | Detail program (Main + Sidebar) |
| 5 | **CTA Section** | Ajakan konsultasi/daftar |
| 6 | **Footer** | Footer standard (FB + IG, tanpa YouTube) |

#### Detail Per Program:

##### Paket A — Setara SD/MI
- **Usia**: 12+ Tahun
- **Durasi**: 3 Tahun (Fleksibel)
- **Ijazah**: Setara SD
- **Jadwal**: Pagi / Sore / Weekend
- **Kurikulum**: Merdeka Belajar
- **Mata Pelajaran**: Pendidikan Agama, PKn, Bahasa Indonesia, Matematika, IPA, IPS, Seni Budaya & Prakarya, PJOK
- **Syarat Pendaftaran**:
  - Fotokopi KTP / Kartu Keluarga
  - Pas foto 3x4 (4 lembar)
  - Fotokopi Akta Kelahiran
  - Mengisi formulir pendaftaran

##### Paket B — Setara SMP/MTs
- **Prasyarat**: Lulusan SD / Paket A
- **Durasi**: 3 Tahun (Fleksibel)
- **Ijazah**: Setara SMP
- **Jadwal**: Pagi / Sore / Weekend
- **Kurikulum**: Merdeka Belajar
- **Mata Pelajaran**: Pendidikan Agama, PKn, Bahasa Indonesia, Bahasa Inggris, Matematika, IPA, IPS, Seni Budaya & Keterampilan, PJOK, Prakarya
- **Syarat Pendaftaran**:
  - Fotokopi Ijazah SD/Paket A
  - Fotokopi KTP / Kartu Keluarga
  - Pas foto 3x4 (4 lembar)
  - Mengisi formulir pendaftaran

##### Paket C — Setara SMA/MA
- **Prasyarat**: Lulusan SMP / Paket B
- **Durasi**: 3 Tahun (Fleksibel)
- **Ijazah**: Setara SMA (bisa untuk kuliah & kerja)
- **Jadwal**: Pagi / Sore / Weekend
- **Kurikulum**: Merdeka Belajar
- **Mata Pelajaran**: Pendidikan Agama, PKn, Bahasa Indonesia, Bahasa Inggris, Matematika, Sejarah Indonesia, Ekonomi/Sosiologi, Geografi, Seni Budaya, PJOK, Prakarya & Kewirausahaan
- **Syarat Pendaftaran**:
  - Fotokopi Ijazah SMP/Paket B
  - Fotokopi KTP / Kartu Keluarga
  - Pas foto 3x4 (4 lembar)
  - Mengisi formulir pendaftaran

---

### 3.3 Halaman Tentang (`tentang.html`)

**Tujuan**: Menampilkan profil lengkap lembaga, sejarah, visi misi, keunggulan, struktur organisasi, dan legalitas.

#### Komponen & Seksi:

| # | Seksi | Deskripsi |
|---|---|---|
| 1 | **Navbar** | Navbar dengan class `scrolled` (selalu solid) |
| 2 | **Page Header** | Breadcrumb + Judul + Deskripsi |
| 3 | **Sejarah Singkat** | Grid 2 kolom: gambar + teks sejarah |
| 4 | **Visi & Misi** | Grid 2 kolom: card Visi + card Misi |
| 5 | **Keunggulan** | Grid 4 kolom: 4 keunggulan utama |
| 6 | **Struktur Organisasi** | Grid 6 card: anggota organisasi |
| 7 | **Legalitas & Akreditasi** | Card dengan daftar legalitas |
| 8 | **CTA Section** | Ajakan bergabung |
| 9 | **Footer** | Footer standard (FB + IG, tanpa YouTube) |

#### Visi:
> "Menjadi Pusat Kegiatan Belajar Masyarakat yang unggul, terpercaya, dan bermutu dalam menyelenggarakan pendidikan kesetaraan guna mewujudkan masyarakat yang cerdas, terampil, dan berakhlak mulia."

#### Misi:
1. Menyelenggarakan pendidikan kesetaraan Paket A, B, dan C yang berkualitas dan terjangkau.
2. Mengembangkan kurikulum yang relevan dengan kebutuhan masyarakat dan dunia kerja.
3. Membentuk peserta didik yang memiliki karakter kuat, berakhlak mulia, dan berdaya saing.
4. Menyediakan tenaga pengajar yang profesional dan berdedikasi tinggi.
5. Membangun kemitraan dengan berbagai pihak untuk pengembangan program pendidikan.
6. Memanfaatkan teknologi informasi untuk mendukung proses pembelajaran.

#### Struktur Organisasi:
| Nama | Jabatan |
|---|---|
| Hardiansyah, S.Pd | Ketua PKBM |
| Siti Aminah, S.Pd | Sekretaris |
| Rina Wati, S.E | Bendahara |
| Ahmad Fauzi, S.Pd | Koordinator Paket A |
| Dewi Lestari, M.Pd | Koordinator Paket B |
| Budi Santoso, M.Pd | Koordinator Paket C |

#### Legalitas:
- ✅ Terdaftar di Dinas Pendidikan Kota Depok
- ✅ Nomor Induk Lembaga (NILEM) Resmi
- ✅ Ijazah Diakui Kemdikbudristek
- ✅ Terdaftar di DAPODIK (Data Pokok Pendidikan)

---

### 3.4 Halaman Kontak & Pendaftaran (`kontak.html`)

**Tujuan**: Menyediakan informasi kontak lengkap dan formulir pendaftaran online yang terintegrasi dengan WhatsApp.

#### Komponen & Seksi:

| # | Seksi | Deskripsi |
|---|---|---|
| 1 | **Navbar** | Navbar dengan class `scrolled` (selalu solid) |
| 2 | **Page Header** | Breadcrumb + Judul + Deskripsi |
| 3 | **Contact Grid** | Grid 2 kolom: Info Kontak + Form Pendaftaran |
| 4 | **Peta Lokasi** | Embedded Google Maps (Sawangan, Depok) |
| 5 | **Footer** | Footer standard (FB + IG, tanpa YouTube) |

#### Informasi Kontak:
| Jenis | Detail |
|---|---|
| **Alamat** | Jl. Raya Sawangan, Kec. Sawangan, Kota Depok, Jawa Barat 16511 |
| **Telepon/WA** | 0812-3456-7890 |
| **Email** | info@pkbmhc.id |
| **Jam Operasional** | Senin–Jumat: 08.00–16.00 WIB, Sabtu: 08.00–12.00 WIB |

#### Formulir Pendaftaran:
| Field | Tipe | Required | Placeholder |
|---|---|---|---|
| Nama Lengkap | `text` | ✅ | Masukkan nama lengkap Anda |
| Nomor HP / WhatsApp | `tel` | ✅ | Contoh: 08123456789 |
| Program yang Diminati | `select` | ✅ | Options: Paket A (Setara SD), Paket B (Setara SMP), Paket C (Setara SMA) |
| Pesan / Pertanyaan | `textarea` | ❌ | Tulis pesan atau pertanyaan Anda di sini... |

#### Alur Submit Form:
```
User mengisi form → Klik "Kirim Pendaftaran" →
JavaScript memformat data → Redirect ke wa.me dengan pesan terformat →
WhatsApp terbuka dengan pesan pre-filled ke nomor PKBM
```

**Format Pesan WhatsApp:**
```
Halo, saya *[Nama]* ingin mendaftar di PKBM Hardiansyah Cerdasio.

📱 No. HP: [Nomor HP]
📚 Program: [Program Dipilih]
💬 Pesan: [Pesan/Pertanyaan]
```

---

## 4. 🧩 Komponen UI Global

### 4.1 Navbar
- **Posisi**: Fixed di atas halaman
- **Tinggi**: 80px (`--nav-height`)
- **State**:
  - *Default (hero — hanya index.html)*: Background transparent, teks putih
  - *Scrolled*: Background putih dengan glassmorphism (`backdrop-filter: blur(20px)`), shadow
  - *Sub-halaman*: Selalu menggunakan class `scrolled` (solid state)
- **Mobile**: Hamburger menu → slide-in dari kanan dengan **overlay backdrop** (dibuat via JavaScript)
  - Swipe kanan (>50px) pada nav-links untuk menutup menu
  - Klik overlay untuk menutup
  - ESC keyboard untuk menutup

### 4.2 Tombol (Buttons)
| Varian | Background | Penggunaan |
|---|---|---|
| `btn-primary` | Gradient hijau (`--primary` → `--primary-light`) | Aksi utama |
| `btn-secondary` | Gradient biru (`--secondary` → `--secondary-light`) | Aksi sekunder |
| `btn-gold` | Gradient emas (`--accent-gold` → `--accent-gold-light`) | CTA premium (Daftar) |
| `btn-outline` | Transparent + border putih | Aksi alternatif di hero |
| `btn-whatsapp` | `#25D366` | Integrasi WhatsApp |
| `btn-sm` | — | Ukuran kecil (card) |
| `btn-lg` | — | Ukuran besar (CTA) |

**Hover Effect**: `translateY(-3px)` + intensified box-shadow

### 4.3 Breadcrumb
- Format: `Beranda › Halaman Aktif`
- Muncul di semua sub-halaman (Program, Tentang, Kontak)

### 4.4 Page Header
- Background: Gradient gelap (sama dengan hero)
- Padding atas: Memperhitungkan navbar height
- Konten: Breadcrumb + H1 + Deskripsi

### 4.5 Footer
- Background: Dark (`--surface-dark`: `#0A1F12`)
- Layout: 4 kolom grid
  1. Brand (Logo + Nama + Deskripsi + Social Links)
  2. Menu navigasi
  3. Program links
  4. Info kontak
- Bottom bar: Copyright © 2025

#### Social Links per Halaman:

| Halaman | Facebook | Instagram | YouTube |
|---|---|---|---|
| Beranda (`index.html`) | ✅ | ✅ | ✅ |
| Program (`program.html`) | ✅ | ✅ | ❌ |
| Tentang (`tentang.html`) | ✅ | ✅ | ❌ |
| Kontak (`kontak.html`) | ✅ | ✅ | ❌ |

### 4.6 WhatsApp Floating Button
- Posisi: Fixed, bottom-right
- Ikon: WhatsApp SVG
- Background: `#25D366`
- Link: `https://wa.me/6281234567890`
- Muncul di **semua halaman**

### 4.7 Lightbox
- Trigger: Klik pada gambar galeri
- Overlay: Background hitam semi-transparent
- Fitur: Close button (×), click outside to close, ESC keyboard
- **Touch**: Swipe vertikal (>60px) untuk menutup di mobile
- Overflow body: Hidden saat lightbox aktif

---

## 5. ⚡ Fitur Interaktif (JavaScript)

### 5.1 Daftar Fitur

| Fitur | File | Selector | Deskripsi |
|---|---|---|---|
| **Navbar Scroll** | `main.js` | `.navbar` | Menambahkan class `scrolled` saat scroll > 50px |
| **Mobile Menu** | `main.js` | `.hamburger`, `.nav-links` | Toggle menu + **dynamically-created overlay** (`.nav-overlay`) + scroll lock |
| **Menu Swipe Close** | `main.js` | `.nav-links` | Swipe kanan (>50px) pada menu untuk menutup di mobile |
| **Scroll Reveal** | `main.js` | `.reveal`, `.reveal-left`, `.reveal-right` | IntersectionObserver (threshold: 0.15, rootMargin: -50px) |
| **Counter Animation** | `main.js` | `.stat-number` | Animasi angka naik dari 0 dengan ease-out cubic (2 detik) — *elemen tidak ada di HTML saat ini* |
| **Testimonial Slider** | `main.js` | `.testimonial-track` | Auto-slide 5 detik, dot navigation, touch swipe (threshold 50px) |
| **Lightbox** | `main.js` | `.gallery-item`, `.lightbox` | Klik gambar → modal, ESC/click close, **touch swipe vertikal close** — *handler tetap ada di JS, halaman galeri sudah dihapus* |
| **Gallery Filter** | `main.js` | `.filter-btn` | Filter kategori dengan fade-in animation — *handler tetap ada di JS, halaman galeri sudah dihapus* |
| **Program Tabs** | `main.js` | `.program-tab` | Tab switching untuk Paket A/B/C + **auto-scroll tab ke center di mobile** |
| **Contact Form → WA** | `main.js` | `#contactForm` | Format data → redirect ke WhatsApp via `window.open()` |
| **Active Nav Link** | `main.js` | `.nav-links a` | Highlight link halaman aktif berdasarkan URL path |
| **Smooth Scroll** | `main.js` | `a[href^="#"]` | Scroll halus untuk anchor links |

### 5.2 Animasi CSS

| Animasi | Durasi | Penggunaan |
|---|---|---|
| `hero-aurora-blob` | varies (infinite) | Aurora mesh background effect di hero |
| `particle` | varies (infinite) | Floating particles di hero |
| `fadeIn` | 0.4s | Gallery filter transition |
| Scroll reveal | 0.5s (ease) | Elemen muncul dari bawah/kiri/kanan |

### 5.3 JavaScript-Created Elements

| Elemen | Method | Deskripsi |
|---|---|---|
| `.nav-overlay` | `document.createElement('div')` | Backdrop overlay untuk mobile menu, ditambahkan ke `document.body` saat DOMContentLoaded |

---

## 6. 📱 Responsivitas

### 6.1 Breakpoints

| Breakpoint | Target |
|---|---|
| `> 1200px` | Desktop besar |
| `992px - 1200px` | Desktop/Laptop |
| `768px - 991px` | Tablet |
| `< 768px` | Mobile |

### 6.2 Perubahan Layout Per Breakpoint

#### Desktop (default)
- Navbar: Horizontal menu
- Hero: Centered layout dengan aurora mesh
- Program: 3 kolom grid
- Keunggulan: 4 kolom grid
- Kontak: 2 kolom grid

#### Tablet (≤ 991px)
- Program: 2 kolom → wrap
- Detail program: Stack vertikal

#### Mobile (≤ 768px)
- Navbar: Hamburger menu dengan overlay backdrop
- Hero: 1 kolom centered
- Semua grid: 1 kolom full-width
- Button: Full-width
- Footer: Stack vertikal
- Filter/Tab buttons: Horizontal scroll dengan auto-scroll ke center

---

## 7. 🔍 SEO & Meta

### 7.1 Meta Tags Per Halaman

| Halaman | Title | Description |
|---|---|---|
| Beranda | PKBM Hardiansyah Cerdasio — Pusat Kegiatan Belajar Masyarakat Sawangan Depok | PKBM Hardiansyah Cerdasio adalah Pusat Kegiatan Belajar Masyarakat di Sawangan, Depok. Menyediakan program pendidikan kesetaraan Paket A, B, dan C dengan ijazah resmi Kemdikbudristek. |
| Program | Program Pendidikan — PKBM Hardiansyah Cerdasio | Program pendidikan kesetaraan Paket A (SD), Paket B (SMP), dan Paket C (SMA) di PKBM Hardiansyah Cerdasio, Sawangan Depok. Ijazah resmi Kemdikbudristek. |
| Tentang | Tentang Kami — PKBM Hardiansyah Cerdasio | Profil lengkap PKBM Hardiansyah Cerdasio, Sawangan Depok. Visi, misi, sejarah, dan struktur organisasi lembaga pendidikan kesetaraan. |

| Kontak | Kontak & Pendaftaran — PKBM Hardiansyah Cerdasio | Hubungi PKBM Hardiansyah Cerdasio di Sawangan, Depok. Formulir pendaftaran online, WhatsApp, alamat, dan peta lokasi. |

### 7.2 Open Graph (Beranda)
```html
<meta property="og:title" content="PKBM Hardiansyah Cerdasio — Pendidikan Kesetaraan Sawangan Depok">
<meta property="og:description" content="Program pendidikan kesetaraan Paket A, B, C dengan ijazah resmi. Jadwal fleksibel, biaya terjangkau.">
<meta property="og:type" content="website">
```

### 7.3 Elemen SEO Lainnya
- ✅ Semantic HTML5 (`<nav>`, `<header>`, `<section>`, `<footer>`, `<main>`)
- ✅ Satu `<h1>` per halaman
- ✅ Hierarki heading terstruktur (H1 → H2 → H3 → H4)
- ✅ Alt text pada semua gambar
- ✅ `lang="id"` pada `<html>`
- ✅ `aria-label` pada tombol interaktif
- ✅ Favicon (`assets/images/logo.png`)
- ✅ Meta keywords (beranda)

---

## 8. ♿ Aksesibilitas (a11y)

| Fitur | Implementasi |
|---|---|
| **Keyboard Navigation** | ESC untuk menutup lightbox & mobile menu |
| **ARIA Labels** | Tombol hamburger (`aria-label`, `aria-expanded`), social links, WhatsApp float, lightbox close, testimonial dots |
| **Touch Target** | Minimum 48x48px pada hamburger button |
| **Font Scaling** | Menggunakan `clamp()` untuk responsif typography |
| **Color Contrast** | Teks primer gelap (`#152A1D`) di atas background terang (`#FAFDF8`) |
| **iOS Safety** | Input font-size 16px untuk mencegah zoom, safe-area padding |
| **Touch Gestures** | Swipe kanan untuk tutup mobile menu, swipe vertikal untuk tutup lightbox |
| **Passive Listeners** | Semua touch event listeners menggunakan `{ passive: true }` |

---

## 9. 🎨 Panduan Visual untuk Canva Code

### 9.1 Prinsip Desain

1. **Modern & Professional** — Glassmorphism, gradient, smooth animations, aurora mesh
2. **Ramah & Terpercaya** — Palet hijau natural, gold accents, gambar nyata
3. **Mobile-First** — Dioptimalkan untuk mobile experience
4. **Konversi-Oriented** — CTA jelas di setiap halaman, WhatsApp integration

### 9.2 Panduan Warna per Elemen

```
Paket A (SD)  → Hijau (#0E6B3A) — Melambangkan awal/pertumbuhan
Paket B (SMP) → Biru  (#1C5BA5) — Melambangkan perkembangan
Paket C (SMA) → Biru Tua (#1A3C6E) — Melambangkan kedewasaan/profesional
CTA Utama     → Emas  (#C8963E) — Melambangkan nilai/prestasi
WhatsApp      → Hijau (#25D366) — Standar WhatsApp brand
```

### 9.3 Efek Visual

| Efek | CSS | Penggunaan |
|---|---|---|
| **Glassmorphism** | `backdrop-filter: blur(20px)`, `background: rgba(255,255,255,0.95)` | Navbar scrolled |
| **Aurora Mesh** | 3 blob animasi dengan blur(100px+), opacity rendah | Hero background |
| **Floating Particles** | 8 partikel kecil dengan animasi naik-turun | Hero decoration |
| **Card Hover** | `transform: translateY(-8px)`, `box-shadow: var(--shadow-xl)` | Program cards |
| **Wave Separator** | SVG `<path>` di bawah hero section | Transisi hero → content |
| **Glow Effect** | `box-shadow: 0 0 30px rgba()` | Elemen aksen |

---

## 10. 📊 Konten & Copywriting

### 10.1 Tagline Utama (Hero)
> **"Wujudkan Masa Depan Cerah Bersama Kami"**

> *(Catatan: "Masa Depan Cerah" dibungkus dalam `<span class="hero-highlight">` dengan gradient text effect)*

### 10.2 Sub-tagline
> "Pendidikan kesetaraan **Paket A, B, dan C** dengan ijazah resmi dari Kemdikbudristek. Jadwal fleksibel, biaya terjangkau, dan tenaga pengajar berpengalaman."

### 10.3 Unique Selling Points (USP)
1. 🎓 **Ijazah Resmi Negara** — Diakui Kemdikbudristek, untuk kuliah & bekerja
2. ⏰ **Jadwal Fleksibel** — Pilihan pagi, sore, atau akhir pekan
3. 💰 **Biaya Terjangkau** — Dengan pilihan cicilan mudah
4. 👨‍🏫 **Tutor Profesional** — Bersertifikat & berpengalaman
5. 📚 **Kurikulum Modern** — Kurikulum Merdeka Belajar
6. 📍 **Lokasi Strategis** — Sawangan, Depok (mudah dijangkau)

### 10.4 Social Media

| Platform | Link | Halaman |
|---|---|---|
| Facebook | `#` (placeholder) | Semua halaman |
| Instagram | `#` (placeholder) | Semua halaman |
| YouTube | `#` (placeholder) | Hanya beranda |

---

## 11. 🔧 Catatan Teknis & Limitasi

### 11.1 Limitasi Saat Ini
| Area | Limitasi | Solusi Potensial |
|---|---|---|
| **Gambar** | Menggunakan Unsplash (placeholder) | Ganti dengan foto asli kegiatan PKBM |
| **Nomor WA** | Placeholder `6281234567890` | Ganti dengan nomor WhatsApp resmi |
| **Email** | Placeholder `info@pkbmhc.id` | Ganti dengan email resmi |
| **Social Links** | Semua mengarah ke `#` | Ganti dengan URL social media resmi |
| **Google Maps** | Koordinat umum Sawangan | Ganti dengan koordinat persis lokasi PKBM |
| **Backend** | Tidak ada backend/database | Form dikirim langsung ke WhatsApp |
| **Analytics** | Belum ada tracking | Tambahkan Google Analytics / Meta Pixel |
| **Statistik** | Counter animation tersedia di JS tapi elemen HTML tidak ada | Tambahkan elemen `.stat-number` jika diperlukan |

### 11.2 Dependensi Eksternal
| Dependensi | URL | Penggunaan |
|---|---|---|
| Google Fonts | `fonts.googleapis.com` | Font Inter & Outfit |
| Unsplash | `images.unsplash.com` | Placeholder gambar |
| Google Maps | `google.com/maps/embed` | Peta lokasi |
| WhatsApp API | `wa.me` | Chat & form redirect |

### 11.3 Browser Support
- ✅ Chrome (latest 2 versions)
- ✅ Firefox (latest 2 versions)
- ✅ Safari (latest 2 versions)
- ✅ Edge (latest 2 versions)
- ✅ Chrome Mobile / Safari Mobile
- ⚠️ IE 11 — **Tidak didukung**

### 11.4 Ukuran File
| File | Ukuran |
|---|---|
| `index.html` | ~20 KB |
| `program.html` | ~27 KB |
| `tentang.html` | ~14 KB |
| `kontak.html` | ~13 KB |
| `css/style.css` | ~58 KB |
| `js/main.js` | ~10 KB |

---

## 12. 🚀 Roadmap Pengembangan

### Fase 1 — MVP ✅ (Saat Ini)
- [x] Halaman Beranda dengan hero aurora mesh & program overview
- [x] Halaman Program dengan detail & tab navigation
- [x] Halaman Tentang dengan visi misi & struktur organisasi
- [x] Halaman Kontak dengan form → WhatsApp
- [x] Responsive design (mobile-first)
- [x] Animasi & micro-interactions (aurora, particles, scroll reveal)
- [x] SEO dasar (meta tags, semantic HTML)
- [x] Touch gestures (swipe close menu, swipe close lightbox)
- [x] ARIA accessibility support

### Fase 2 — Enhancement (Rencana)
- [ ] Ganti semua placeholder dengan konten asli (foto, nomor WA, email, social links)
- [ ] Tambahkan kembali seksi Statistik (counter animation) di beranda
- [ ] Tambahkan halaman FAQ (Pertanyaan yang Sering Diajukan)
- [ ] Implementasi multi-bahasa (Indonesia / Sunda)
- [ ] Dark mode support
- [ ] Performance optimization (minify CSS/JS, image optimization, WebP format)
- [ ] Google Analytics / Meta Pixel integration

### Fase 3 — Advanced (Masa Depan)
- [ ] Blog / Berita & Pengumuman
- [ ] Portal peserta didik (login, lihat nilai, jadwal)
- [ ] Sistem pendaftaran online dengan database (backend)
- [ ] Payment gateway untuk pembayaran SPP
- [ ] Dashboard admin untuk manajemen konten
- [ ] PWA (Progressive Web App) support
- [ ] Integrasi dengan DAPODIK API

---

## 13. 📝 Changelog

### v2.1.0 — 27 Juli 2026
- ➖ **Halaman Galeri**: Dihapus (`galeri.html`) beserta semua link navigasi di navbar dan footer
- 🔄 **Navigasi**: Menu diperbarui menjadi 4 item (Beranda, Program, Tentang, Kontak)
- 🔄 **PRD**: Versi dokumen diperbarui, seksi 3.4 (Galeri) dihapus, penomoran diperbarui

### v2.0.0 — 27 Juli 2026
- 🔄 **Hero redesign**: Ganti floating shapes + 2-kolom layout → aurora mesh (3 blob) + particles (8) + centered layout
- 🔄 **Color palette**: Perbarui seluruh palet warna ke tone lebih gelap & profesional
- ➕ **Hero wave separator**: Tambah SVG wave untuk transisi hero → content
- ➕ **Nav overlay**: Mobile menu overlay dibuat dinamis via JavaScript
- ➕ **Touch gestures**: Swipe-to-close untuk mobile menu dan lightbox
- ➕ **Auto-scroll**: Filter/tab buttons auto-scroll ke center di mobile
- ➕ **ARIA expanded**: Hamburger button mendukung `aria-expanded`
- ➕ **Passive listeners**: Semua touch event menggunakan passive listener
- ➖ **Statistik section**: Dihapus dari beranda (JS handler tetap ada)
- 🔄 **Tagline**: Dipersingkat dari "Bersama PKBM Hardiansyah Cerdasio" → "Bersama Kami"
- 🔄 **Footer social**: Sub-halaman hanya FB + IG (tanpa YouTube)
- 🔄 **Shadow system**: Warna bayangan disesuaikan dengan primary baru
- 🔄 **File sizes**: CSS tumbuh signifikan (~58KB) dengan design system lengkap

### v1.0.0 — 27 Juli 2026
- 🎉 Initial MVP release

---

## 14. 📝 Glosarium

| Istilah | Definisi |
|---|---|
| **PKBM** | Pusat Kegiatan Belajar Masyarakat — lembaga pendidikan nonformal |
| **Paket A** | Program pendidikan kesetaraan setara SD/MI |
| **Paket B** | Program pendidikan kesetaraan setara SMP/MTs |
| **Paket C** | Program pendidikan kesetaraan setara SMA/MA |
| **Kemdikbudristek** | Kementerian Pendidikan, Kebudayaan, Riset, dan Teknologi |
| **NILEM** | Nomor Induk Lembaga — identitas resmi lembaga pendidikan nonformal |
| **DAPODIK** | Data Pokok Pendidikan — database nasional pendidikan Indonesia |
| **Kurikulum Merdeka** | Kurikulum terbaru Indonesia yang fleksibel dan berpusat pada siswa |
| **KBM** | Kegiatan Belajar Mengajar |
| **Canva Code** | Platform pengembangan visual untuk web/aplikasi |
| **Aurora Mesh** | Efek visual dengan blob berwarna yang beranimasi dan di-blur untuk membuat background gradient dinamis |
| **Glassmorphism** | Teknik desain UI dengan efek kaca buram (frosted glass) menggunakan `backdrop-filter: blur()` |

---

> **Dokumen ini dibuat sebagai referensi lengkap untuk pembangunan dan pengembangan website PKBM Hardiansyah Cerdasio di platform Canva Code. Semua spesifikasi teknis, konten, dan desain yang tercantum di atas merepresentasikan state terkini dari proyek (v2.1.0).**
