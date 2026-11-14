# PKBM Hardiansyah Cerdasio

Website profil dan landing page resmi untuk PKBM Hardiansyah Cerdasio, lembaga pendidikan kesetaraan di Sawangan, Depok. Proyek ini dibuat sebagai situs multi-halaman statis yang menampilkan program pendidikan Paket A, Paket B, dan Paket C, informasi lembaga, serta ajakan pendaftaran yang terhubung ke WhatsApp.

## Deskripsi

Repository ini berisi website resmi PKBM Hardiansyah Cerdasio dengan tampilan modern, responsif, dan ramah pengguna. Website ini dirancang untuk:

- Menampilkan profil lembaga secara profesional
- Menjelaskan program pendidikan kesetaraan Paket A, B, dan C
- Menyediakan halaman tentang lembaga dan visinya
- Mempermudah calon peserta didik mendaftar melalui formulir yang terhubung ke WhatsApp
- Menjadi media informasi publik yang mudah diakses dari desktop maupun mobile

## Fitur Utama

- Landing page yang modern dan menarik
- Navigasi responsif untuk desktop dan mobile
- Halaman utama, program, tentang, dan kontak
- CTA untuk pendaftaran langsung ke WhatsApp
- Desain SEO-friendly dengan meta tags yang terstruktur
- Layout yang adaptif untuk berbagai ukuran layar
- Animasi ringan dan efek interaktif tanpa framework tambahan

## Stack Teknologi

- HTML5
- CSS3
- JavaScript (Vanilla)
- Google Fonts
- Inline SVG untuk ikon
- Assets lokal dan gambar dari Unsplash sebagai placeholder

## Struktur Project

```text
PKBM_HC-HOMEPAGE/
├── index.html
├── program.html
├── tentang.html
├── kontak.html
├── PRD.md
├── README.md
├── assets/
│   └── images/
│       └── logo.png
├── css/
│   └── style.css
├── js/
│   └── main.js
└──
```

## Halaman yang Tersedia

- `index.html` — halaman beranda / landing page
- `program.html` — detail program Paket A, B, dan C
- `tentang.html` — profil lembaga, visi, misi, dan organisasi
- `kontak.html` — informasi kontak dan formulir pendaftaran

## Cara Menjalankan Secara Lokal

Karena ini adalah website statis, Anda cukup membuka file HTML di browser atau menjalankan local server sederhana.

### Opsi 1: Buka langsung di browser

Buka file `index.html` di browser favorit Anda.

### Opsi 2: Gunakan local server (direkomendasikan)

Jika Anda ingin menjalankan website dengan server lokal, Anda bisa menggunakan Python:

```bash
python -m http.server 8000
```

Lalu buka:

```text
http://localhost:8000
```

## Catatan Penting

- Repository ini masih memakai data placeholder untuk nomor WhatsApp, email, dan sosial media. Sesuaikan jika sudah ada data resmi.
- Dokumentasi detail proyek dapat dilihat di file `PRD.md`.

## Kontak

PKBM Hardiansyah Cerdasio
- Lokasi: Sawangan, Depok
- WhatsApp: 0812-3456-7890
- Email: info@pkbmhc.id

## Lisensi

Proyek ini dibuat untuk kebutuhan profil dan promosi lembaga pendidikan. Silakan sesuaikan lisensi sesuai kebutuhan organisasi jika akan dipublikasikan secara umum.

---

Dibuat untuk kebutuhan dokumentasi dan pengembangan situs PKBM Hardiansyah Cerdasio.
