# Perencanaan Implementasi Portofolio Bisnis Profesional (Vanilla JS & Tailwind CSS)

## 📌 Deskripsi Proyek
Tujuan dari proyek ini adalah membangun sebuah website portofolio satu halaman (Single Page Application) untuk seorang pebisnis. Website ini harus mengusung tema **clean, interaktif, modern, dan minimalis**, dan diperkaya dengan elemen grafis modern (seperti shadow yang elegan, transisi yang halus, layout yang lega/luas). Desain ini harus merepresentasikan nilai profesionalisme dan keunggulan pebisnis dengan tipografi yang kuat, serta disajikan seluruhnya menggunakan Bahasa Indonesia.

## 🛠 Tech Stack
- **Struktur**: HTML5 (Clean dan Semantic)
- **Styling**: Tailwind CSS (Pendekatan Utility-First)
- **Interaktivitas**: Vanilla JavaScript (Sederhana tanpa framework tambahan)
- **Font**: Google Fonts (Direkomendasikan: *Inter*, *Outfit*, atau *Roboto*)
- **Ikon**: Heroicons, Phosphor Icons, atau CDN FontAwesome

## 📁 Arsitektur Proyek
```text
/
├── index.html        (Struktur utama satu halaman)
├── CSS/
│   └── style.css     (Custom styling/opsional Tailwind layer)
├── JS/
│   └── script.js     (Fungsi interaktif Vanilla JS)
└── Assets/
    ├── images/       (Foto profil, gambar project, dsb)
    └── icons/        (Ikon opsional)
```

## 📐 Struktur Halaman dan Desain (DOM Structure)
Website ini terdiri dari 1 halaman responsif yang terbagi menjadi seksi (Section) berurutan berikut:

1. **HERO SECTION**
   - **Isi**: Nama Lengkap, Peran/Profesi Bisnis, dan Tagline Singkat.
   - **CTA (Call To Action)**: Dua Tombol ("Lihat Proyek" & "Hubungi Saya").
   - **Petunjuk Desain**: Pastikan terdapat hero image yang terpusat atau layout split (teks di kiri, foto di kanan). Gunakan tipografi besar untuk nama dan profesi. Animasi *fade-up* sangat direkomendasikan saat halaman pertama dimuat.

2. **ABOUT ME**
   - **Isi**: Deskripsi singkat mengenai latar belakang pebisnis, cerita profesional, skill utama, tools/strategi yang digunakan, dan cara kerja / *value* yang diberikan pada klien.
   - **Petunjuk Desain**: Buat layout yang nyaman dibaca dengan *line-height* yang cukup, bagi paragraf agar tidak terlalu padat.

3. **SKILLS / TECH STACK**
   - **Isi**: Daftar skill/keahlian pendukung bisnis/teknis. Dibagi ke dalam beberapa kategori seperti (Keahlian Teknis, Tools, dsb).
   - **Petunjuk Desain**: Susun menggunakan sistem Grid atau Card yang minimalis.

4. **PROJECTS (PORTOFOLIO UTAMA)**
   - **Isi**: Katalog proyek atau hasil kerja. Tiap proyek memiliki: Nama Proyek, Gambar/Preview, Deskripsi Singkat, Teknologi yang digunakan, Link Live Demo, dan Link Repository/Detail.
   - **Petunjuk Desain**: Gunakan perpaduan Grid. Setiap Card Proyek harus memiliki efek *Hover* yang halus (seperti *scale up* sedikit atau bayangan menjadi lebih dalam) agar responsif dan terlihat modern.

5. **EXPERIENCE (OPSIONAL)**
   - **Isi**: Rangkuman pengalaman kerja (Timeline Perjalanan), proyek *freelance*, dan *internship*.
   - **Petunjuk Desain**: Desain berbasis *Vertical Timeline* menggunakan border di bagian kiri dan *node* bulat untuk titik waktu.

6. **TESTIMONIALS (OPSIONAL)**
   - **Isi**: Kumpulan kutipan komentar/review dari klien atau rekan kerja (dilengkapi dengan Nama dan Posisi).
   - **Petunjuk Desain**: Layout grid/card layout mendatar (*carousel* statis dengan flexbox overflow).

7. **CONTACT**
   - **Isi**: Email, Formulir kontak (Tampilan antarmuka: Nama, Email, Pesan, Tombol Kirim), Tautan Sosial Media (LinkedIn, GitHub, Instagram).

8. **FOOTER**
   - **Isi**: Teks Copyright, navigasi cepat berupa teks, dan tautan ikon ke media sosial.

---

## 🚀 Tahapan Implementasi Untuk Junior Programmer / Model AI

Ikuti tahapan logis ini secara berurutan tanpa melewatkan detail desain. Ingatlah bahwa kualitas visual dan kemewahan (premium feel) adalah prioritas:

### Fase 1: Setup Proyek & Layout Utama
1. **Inisialisasi File**: Buat semua struktur folder sesuai arsitektur (`index.html`, `style.css`, `script.js`).
2. **Setup Tailwind & Font**: Pasang Tailwind CSS via CDN (atau CLI jika diminta setup package manager) di dalam tag `<head>`. Import jenis font modern (misalnya `Inter`) menggunakan Google Fonts di baris awal. Atur di file CSS (`* { font-family: 'Inter', sans-serif; }`).
3. **Inisialisasi Navigasi (Navbar)**: Buat komponen *Header* yang menempel (Sticky/Fixed) di layar atas. Sertakan tautan navigasi (semua tautan mengarah pada Anchor tag, misal: `href="#about"`). Sediakan juga tombol *Hamburger Menu* untuk perangkat tampilan Mobile.

### Fase 2: Pengerjaan Styling Setiap Seksi (Section-by-Section)
1. Ciptakan kelas `section` padat dengan *padding* yang rapi. Contoh kontainer: `<section id="about" class="max-w-6xl mx-auto px-6 py-24">`.
2. Kerjakan seksi demi seksi berdasarkan **Struktur Halaman**, pastikan penataan layout dilakukan sesuai metodologi **Mobile-First**.
3. Gunakan warna-warna profesional yang netral. Misalnya latar putih yang diselingi dengan `bg-gray-50` berulangkali per *section* agar terlihat jeda yang jelas. Gunakan warna teks `text-gray-900` untuk judul (H1, H2, dsb.) dan `text-gray-600` untuk body paragraf.
4. Pada tombol/CTA dan border interaktif, gunakan variasi minimal dari warna primer *Brand* pilihan (misal hitam legam modern atau aksen biru `bg-blue-600`).

### Fase 3: Detil Interaktif & Modernisasi UI
1. **Tambahan Tampilan Card & Bayangan**: Pastikan setiap elemen kartu profil, *skill*, maupun bagian proyek (`div`) diberikan kelas `rounded-xl`, `border`, atau sedikit shadow moderen (`shadow-sm`, *hover* menjadi `shadow-md`).
2. **Hover dan Transisi**: Selalu aplikasikan `transition-all duration-300` agar efek sorotan oleh pengguna pada tombol maupun *card* tidak kaku.

### Fase 4: Penambahan Interaktivitas Menggunakan Vanilla JavaScript
1. **Scroll Halus (Smooth Scrolling)**: Pastikan saat navigasi diklik atau *CTA Button* ditekan, laju halaman ke bawah terasa halus (bisa disetel di css dengan `html { scroll-behavior: smooth; }`).
2. **Navbar Mobile**: Tuliskan logika JS sederhana agar navigasi dapat membuka/menutup di perangkat *smartphone* (mengganti kelas `hidden` Tailwind) saat hamburger menu diklik.
3. **(Skor Plus) Scroll Animations**: Gunakan `IntersectionObserver` sederhana via JS untuk mengidentifikasi setiap section masuk viewport dan tambahkan kelas `opacity-100 translate-y-0` (pada awalnya di-*hide* dengan kelas khusus).

### Fase 5: Finalisasi & QA
1. **Pengujian Responsivitas**: Uji semua elemen desain (Navbar, Grid Proyek, Formulir Contact) di berbagai profil resolusi (_Mobile_, _Tablet_, _Desktop_).
2. Tinjau kembali tipografi. Pastikan spasi, margin, paddings tidak terlalu sesak, dengan kata lain *white-space* atau ruang kosong (ruang napas desain) yang lebar cukup diandalkan agar terlihat *Clean* & *Mature*.
3. Lengkapi placeholder dengan *dummy content* (contoh gambar).

> ⚠️ **Pesan Penting**: Desain yang dikerjakan tidak boleh kaku atau monoton, manfaatkan layout flex-grid serta utility classes di tailwind agar situs portofolio benar-benar profesional, dinamis, hidup, serta memberikan efek *wow* bagi para pengunjung.
