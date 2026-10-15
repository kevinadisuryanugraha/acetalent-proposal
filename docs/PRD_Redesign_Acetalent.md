# DOKUMEN SPESIFIKASI KEBUTUHAN PRODUK (PRODUCT REQUIREMENT DOCUMENT - PRD)
## PROYEK PENGEMBANGAN DAN REDESIGN WEBSITE RESMI ACETALENT MALAYSIA
**Dokumentasi Resmi Standar Rekayasa Perangkat Lunak & Transformasi Digital Bisnis**

---

### INFORMASI DOKUMEN

| Parameter | Keterangan |
| :--- | :--- |
| **Nama Proyek** | Pengembangan & Redesign Platform Website Korporat Acetalent (acetalent.my) |
| **Klien** | Acetalent (Dahulu: HR & Staffing Solutions Sdn Bhd) |
| **Lokasi Operasional** | Public Bank Tower, Jalan Wong Ah Fook, Johor Bahru & Head Office Kuching, Sarawak, Malaysia |
| **Penulis (Author)** | Tim Solusi Digital & Rekayasa Sistem (BMAD Framework) |
| **Tanggal Pembuatan** | 14 Oktober 2025 |
| **Versi Dokumen** | 2.0 (Comprehensive Corporate Edition) |
| **Status Dokumen** | Siap Diajukan (Final Proposal & Technical PRD) |

---

### RIWAYAT PERUBAHAN DOKUMEN (VERSION HISTORY)

| Tanggal | Versi | Inisiator | Ringkasan Modifikasi |
| :--- | :--- | :--- | :--- |
| 14/10/2025 | 1.0 | Tim Pengembang | Pembuatan draf awal penawaran dan telaah teknis server Exabytes |
| 14/10/2025 | 2.0 | Tim Pengembang | Integrasi penuh SWOT Analysis, Arsitektur Sistem, Business Case B2B, dan PRD Standar Korporat |

---

### DAFTAR SINGKATAN & AKRONIM

| Singkatan / Istilah | Definisi & Keterangan Kontekstual |
| :--- | :--- |
| **B2B** | *Business-to-Business* : Model interaksi bisnis antara Acetalent dengan perusahaan pengguna jasa tenaga kerja |
| **B2C / Talent** | *Business-to-Candidate* : Interaksi antara Acetalent dengan para pencari kerja (kandidat pelamar) |
| **CMS** | *Content Management System* : Antarmuka pengelolaan konten tanpa koding untuk staf non-IT |
| **CRO** | *Conversion Rate Optimization* : Desain antarmuka yang memaksimalkan konversi pengunjung menjadi prospek kontak |
| **CV / Resume** | *Curriculum Vitae* : Dokumen riwayat hidup dan kualifikasi pencari kerja (format PDF/DOCX) |
| **EOL** | *End of Life* : Status perangkat lunak (seperti PHP 5.6) yang sudah dihentikan dukungannya dan rentan serangan siber |
| **GSC** | *Google Search Console* : Alat verifikasi dan optimasi indeks pencarian resmi milik Google |
| **JS-SEZ** | *Johor-Singapore Special Economic Zone* : Koridor ekonomi strategis yang mendorong lonjakan kebutuhan staf korporat |
| **NAP** | *Name, Address, Phone Number* : Konsistensi data identitas bisnis untuk penguatan SEO lokal |
| **PRD** | *Product Requirement Document* : Dokumen spesifikasi teknis dan fungsional produk digital |
| **ROI** | *Return on Investment* : Rasio perolehan laba finansial dibandingkan modal biaya pengembangan |
| **SEO** | *Search Engine Optimization* : Rekayasa teknis agar website mudah ditemukan di peringkat teratas mesin pencari |
| **SSL / HTTPS** | *Secure Sockets Layer* : Protokol enkripsi keamanan transmisi data pengguna |
| **SWOT** | *Strengths, Weaknesses, Opportunities, Threats* : Kerangka analisis strategis komprehensif |
| **UAT** | *User Acceptance Testing* : Uji coba kelayakan fungsi oleh perwakilan klien sebelum peluncuran resmi |

---

## 1. LATAR BELAKANG DAN TUJUAN BISNIS

### 1.1. Latar Belakang Masalah
Acetalent (sebelumnya beroperasi dengan nama legal *HR & Staffing Solutions Sdn Bhd*) merupakan entitas penyedia jasa tenaga kerja terkemuka yang melayani penempatan karyawan sementara (*temporary*), kontrak (*contract*), dan tetap (*permanent*) di seluruh penjuru Malaysia dan Singapura. Memiliki basis operasional strategis di pusat komersial Johor Bahru (24th Floor, Public Bank Tower, Jalan Wong Ah Fook) serta kantor pusat di Kuching, Sarawak, Acetalent menempati posisi geografis emas di koridor industri lintas batas Malaysia-Singapura.

Namun, hasil audit teknis langsung terhadap domain resmi (`https://acetalent.my/`) menunjukkan anomali kritis yang menghambat pertumbuhan bisnis:
1. **Kegagalan Halaman Utama (Critical Error):** Halaman depan website mengalami *blank shortcode error* dengan tampilan teks mentah `[layerslider id="4"]`. Pengunjung korporat yang hendak mencari mitra ketenagakerjaan mendapati website dalam kondisi rusak.
2. **Infrastruktur Usang & Rentan (Security Hazard):** Server berjalan pada versi PHP 5.6.40 yang telah *End-of-Life* (tidak lagi menerima pembaruan keamanan sejak 2018), menggunakan CMS WordPress versi 5.2.17 serta tema Divi versi 2017. Ini merupakan kerentanan terbuka bagi serangan siber dan injeksi malware.
3. **Ketiadaan Tim IT Internal:** Perusahaan tidak memiliki divisi pengembangan perangkat lunak in-house, mengakibatkan website terbengkalai tanpa perawatan dan pembaruan berkala.
4. **Kehilangan Potensi Klien Korporat B2B:** Di tengah maraknya investasi asing di kawasan industri Johor Bahru (kawasan manufaktur Iskandar, pusat data, dan koridor JS-SEZ), ketiadaan portal digital yang representatif menyebabkan Acetalent kehilangan ratusan calon prospek kontrak bernilai tinggi.

### 1.2. Tujuan Proyek
Tujuan utama proyek perancangan ulang (*redesign*) dan pembaruan sistem ini meliputi:
1. **Pemulihan Kredibilitas & Reputasi Digital:** Mengganti tampilan beranda yang rusak dengan arsitektur visual modern berstandar agensi rekrutmen internasional.
2. **Sistem Penjualan Otomatis (B2B Lead Engine):** Menyediakan sarana kontak kilat satu klik menuju WhatsApp representatif bisnis serta formulir spesifikasi kebutuhan tenaga kerja korporat.
3. **Penyederhanaan Pengumpulan Talenta:** Membuka gerbang bagi para kandidat untuk melampirkan berkas CV secara terorganisir langsung ke email manajemen.
4. **Dominasi Visibilitas di Google (SEO Terarah):** Memastikan nama dan layanan Acetalent terindeks secara sempurna saat calon klien korporat mencari penyedia tenaga kerja di Malaysia.
5. **Solusi Siap Pakai Bebas Beban (Zero Maintenance Overhead):** Memberikan infrastruktur yang stabil pada hosting Exabytes yang telah dimiliki klien, tanpa memerlukan biaya langganan server baru maupun staf IT internal.

### 1.3. Hasil yang Akan Dicapai (Deliverables)
1. Platform website korporat baru yang berjalan 100% responsif di seluruh perangkat (smartphone, tablet, laptop, dan desktop).
2. Perbaikan infrastruktur hosting cPanel Exabytes (peningkatan ke PHP 8.1+, aktivasi modul akselerasi LiteSpeed, dan sertifikat enkripsi SSL).
3. Pemisahan jalur navigasi audiens (*Dual-Audience User Journey*) antara perusahaan pencari karyawan dan individu pencari kerja.
4. Terintegrasinya modul Google Search Console, Google Analytics 4, dan XML Sitemap otomatis.
5. Dokumentasi operasional dan pendampingan pasca-peluncuran dengan garansi resmi.

---

## 2. ANALISIS SWOT KOMPREHENSIF ACETALENT

Berikut adalah pemetaan analisis SWOT menyeluruh mengenai posisi strategis bisnis Acetalent dan kehadiran digitalnya:

```
+---------------------------------------------------+---------------------------------------------------+
|                   STRENGTHS (S)                   |                  WEAKNESSES (W)                   |
| 1. Lokasi emas: Public Bank Tower Johor Bahru     | 1. Halaman utama rusak ([layerslider id="4"]).    |
|    & Head Office Kuching, Sarawak.                | 2. Server usang: PHP 5.6 (EOL) & WordPress 5.2.   |
| 2. Pengalaman puluhan tahun (eks HR & Staffing).  | 3. Tidak memiliki tim teknis/pengembang internal. |
| 3. Spektrum industri luas (Migas, IT, Manufaktur, | 4. Jalur konversi B2B tidak ada (tanpa WA cepat). |
|    Perbankan, Logistik, Layanan Pelanggan).       | 5. Tidak ada modul penerimaan CV pelamar online.  |
| 4. Legalitas lengkap & domain terdaftar (.my).    | 6. Ketiadaan strategi kata kunci SEO terarah.     |
+---------------------------------------------------+---------------------------------------------------+
|                 OPPORTUNITIES (O)                 |                    THREATS (T)                    |
| 1. Ledakan ekonomi Johor-Singapore (JS-SEZ)       | 1. Klien multinasional batal kontrak karena       |
|    mendorong lonjakan rekrutmen ratusan pabrik.   |    meragukan kredibilitas website yang rusak.     |
| 2. Perusahaan Singapura mencari mitra outsourcing | 2. Kompetitor (Manpower, Recruit Express, Hays)   |
|    tenaga kerja terampil berbiaya efisien.        |    terus mendominasi pencarian teratas Google.    |
| 3. Kebutuhan tenaga kerja proyek Migas Pengerang  | 3. Resiko peretasan atau injeksi malware akibat   |
|    dan Kawasan Industri Iskandar Puteri.          |    celah keamanan PHP versi 2017 pada server.     |
| 4. Membangun database talenta mandiri gratis      | 4. Kehilangan pelamar berkualitas ke portal lain. |
|    tanpa terus bergantung pada JobStreet/LinkedIn.|                                                   |
+---------------------------------------------------+---------------------------------------------------+
```

### Strategi Eksekusi Berbasis Matriks SWOT:
* **Strategi S-O (Memaksimalkan Kekuatan untuk Merebut Peluang):**  
  Menonjolkan portofolio keahlian industri (terutama Manufaktur dan Migas) pada halaman depan baru untuk menarik penanaman modal asing yang masuk ke Johor Bahru dan Singapura.
* **Strategi W-O (Mengatasi Kelemahan dengan Memanfaatkan Peluang):**  
  Memperbaiki tampilan website yang rusak dan mengaktifkan tombol kontak WhatsApp langsung agar setiap pencarian perusahaan di Google langsung terkonversi menjadi panggilan bisnis ke sales Acetalent.
* **Strategi S-T (Menggunakan Kekuatan untuk Menangkal Ancaman):**  
  Mengukuhkan keunggulan lokal Acetalent di Johor Bahru dan Kuching sebagai agensi yang memahami regulasi ketenagakerjaan setempat, mengimbangi dominasi agensi multinasional berbiaya mahal.
* **Strategi W-T (Meminimalkan Kelemahan dan Menghindari Ancaman Kehancuran):**  
  Melakukan peremajaan kode dan pembaruan versi PHP server Exabytes secara kilat untuk menutup celah keamanan, menyelamatkan reputasi korporat sebelum klien besar membatalkan kerjasama.

---

## 3. LINGKUP PENGERJAAN & BATASAN PROYEK

### 3.1. Lingkup Pengerjaan (Scope of Work)
1. **Audit & Penyelamatan Aset Awal:**
   - Pencadangan penuh (*full backup*) berkas dan basis data MySQL yang tersimpan pada hosting Exabytes.
   - Peningkatan konfigurasi lingkungan server pada cPanel Exabytes dari PHP 5.6 ke PHP 8.1+ yang aman.
2. **Pembersihan & Penghapusan Komponen Error:**
   - Menghapus pustaka *LayerSlider* yang rusak dan membersihkan sisa kode usang tema Divi tahun 2017.
   - Menggantinya dengan arsitektur visual modern berbasis komponen ringan berkecepatan tinggi.
3. **Penyusunan Arsitektur Informasi & Halaman Baru:**
   - **Beranda (Home):** Banner hero representatif, ringkasan keunggulan, daftar industri yang dilayani, statistik pencapaian, dan tombol panggilan aksi cepat (*Call to Action*).
   - **Tentang Kami (About Acetalent):** Sejarah transformasi, visi misi, legalitas, serta jangkauan operasional Johor Bahru dan Sarawak.
   - **Keunggulan Kompetitif (Why Acetalent):** Alasan korporat memilih Acetalent dibandingkan agensi lain.
   - **Spesialisasi Sektor Industri (Industries):** Rincian penempatan tenaga kerja pada 7 pilar: Manufaktur, Minyak & Gas, TI, Kesehatan, Perbankan, Logistik, dan Pusat Kontak.
   - **Layanan Solusi SDM (Services):** Penjelasan skema penempatan tenaga kerja *Permanent*, *Contract*, dan *Temporary*.
   - **Karier & Lowongan (Available Jobs):** Katalog informasi lowongan kerja yang rapi disertai formulir pengiriman lamaran.
   - **Hubungi Kami (Contact Us):** Peta integrasi lokasi Public Bank Tower Johor Bahru, nomor telepon resmi, email, serta formulir permintaan penawaran SDM.
4. **Integrasi Konversi & Komunikasi:**
   - Tombol mengambang (*Floating Button*) WhatsApp yang langsung terhubung ke nomor admin/sales.
   - Formulir interaktif pengunggahan berkas CV (PDF/DOCX) berkapasitas aman dengan verifikasi anti-spam.
5. **Konfigurasi SEO & Pengindeksan Google:**
   - Penataan judul (*Meta Title*), deskripsi (*Meta Description*), dan *OpenGraph Social Share Card*.
   - Pembuatan dan pengiriman sitemap XML serta berkas robots.txt ke Google Search Console.
   - Pendaftaran penandaan lokal (*Local SEO*) konsisten untuk alamat Johor Bahru dan Kuching.
6. **Uji Coba & Peluncuran (Go-Live):**
   - Pengujian responsivitas pada perangkat iOS dan Android.
   - Verifikasi kecepatan muat halaman (*PageSpeed score target Grade A*).

### 3.2. Batasan Proyek (Project Constraints)
1. **Batas Waktu Pengerjaan:** Seluruh tahapan diselesaikan dalam kurun waktu maksimal **1 minggu + 2 hari kerja (8-9 hari kerja)** sesuai kesepakatan percepatan peluncuran.
2. **Infrastruktur Server:** Memaksimalkan hosting cPanel Exabytes yang saat ini telah aktif; tidak mencakup pemindahan server ke penyedia lain di luar kebutuhan klien.
3. **Penyediaan Materi Dasar:** Data legalitas, logo resolusi tinggi, dan daftar kontak resmi bersumber dari perwakilan resmi Acetalent.

---

## 4. JADWAL & RENCANA KERJA (TIMELINE PELAKSANAAN)

Siklus pengerjaan dijalankan dengan metode *Agile Sprint* terstruktur selama 8-9 hari kerja:

```
+-----------------------------------------------------------------------------------------------+
| HARI KE  | FASE / MILESTONE            | AKTIVITAS UTAMA & OUTPUT                             |
+-----------------------------------------------------------------------------------------------+
| Hari 1   | Persiapan & Akses Server    | Backup data Exabytes, update PHP 5.6 -> 8.1+,        |
|          |                             | pembersihan error shortcode [layerslider].           |
+-----------------------------------------------------------------------------------------------+
| Hari 2-3 | Perancangan UI/UX & Layout  | Pembuatan struktur Beranda, About, Why Us,           |
|          |                             | dan penataan navigasi Dual-Audience (Klien & Pelamar)|
+-----------------------------------------------------------------------------------------------+
| Hari 4-5 | Implementasi Fitur Konversi | Integrasi tombol WhatsApp, form upload CV,           |
|          |                             | halaman spesialisasi industri, dan katalog lowongan. |
+-----------------------------------------------------------------------------------------------+
| Hari 6-7 | Optimasi SEO & LiteSpeed    | Konfigurasi cache server, kompresi aset gambar WebP, |
|          |                             | submit sitemap ke Google Search Console, meta tag.   |
+-----------------------------------------------------------------------------------------------+
| Hari 8   | Pengujian Sistem (UAT)      | Uji responsif di semua HP, uji form ke email,        |
|          |                             | penyesuaian revisi minor bersama perwakilan klien.   |
+-----------------------------------------------------------------------------------------------+
| Hari 9   | Peluncuran Resmi (Go-Live)  | Publikasi live di domain acetalent.my, penyerahan    |
|          |                             | dokumen panduan admin, dan aktivasi garansi resmi.   |
+-----------------------------------------------------------------------------------------------+
```

---

## 5. PERSYARATAN NON-TEKNIS (NON-TECHNICAL REQUIREMENTS)

### 5.1. Kemudahan Penggunaan (Usability)
1. **Navigasi Intuitif:** Pengunjung dalam kurun waktu 3 detik pertama dapat langsung memahami apa layanan Acetalent dan bagaimana cara menghubungi tim rekruter.
2. **Kemudahan Akses Ponsel:** Ukuran tombol aksi minimal 44x44 piksel dengan jarak sentuh yang aman agar tidak terjadi salah klik pada layar ponsel.
3. **Pengelolaan Tanpa Koding:** Area administrasi pembaruan informasi kontak atau artikel lowongan kerja dirancang dengan format visual menyerupai dokumen teks biasa (*WYSIWYG*).

### 5.2. Keamanan Sistem (Security)
1. **Enkripsi Data (SSL/HTTPS):** Seluruh pertukaran data formulir terenkripsi penuh melalui protokol HTTPS.
2. **Sanitasi Berkas Unggahan:** Berkas lamaran yang diunggah kandidat disaring secara ketat (hanya format `.pdf`, `.docx`, dan `.doc` dengan batas ukuran maksimal 5 MB) guna mencegah injeksi skrip berbahaya ke server.
3. **Perlindungan Anti-Spam:** Formulir dilengkapi validasi pencegah robot spam tanpa menyulitkan calon klien manusia (*invisible honeypot protection*).
4. **Pemberantasan Celah PHP Lama:** Penghentian penggunaan pustaka PHP 5.6 yang rentan eksploitasi keamanan siber.

### 5.3. Pemeliharaan & Keandalan (Maintainability)
1. **Kemudahan Pencadangan:** Struktur website dirancang kompatibel dengan fitur pencadangan berkala cPanel Exabytes.
2. **Kemandirian Operasional:** Klien tidak dibebani ketergantungan pada tim koding untuk sekadar mengganti nomor WhatsApp atau alamat kantor.

### 5.4. Kinerja Sistem (Performance)
1. **Waktu Muat Cepat:** Waktu muat awal (*First Contentful Paint*) ditargetkan berada di bawah 2 detik pada koneksi internet seluler 4G.
2. **Pemanfaatan Web Server LiteSpeed:** Mengaktifkan mekanisme *server-level caching* bawaan hosting Exabytes untuk melayani ratusan pengunjung secara bersamaan tanpa lonjakan beban server.
3. **Format Aset Terkompresi:** Penggunaan gambar berformat modern WebP yang menghemat bandwidth hingga 60% dibandingkan format JPEG konvensional.

---

## 6. PERSYARATAN TEKNIS (TECHNICAL REQUIREMENTS)

### 6.1. Kebutuhan Perangkat Keras & Lingkungan Server
* **Penyedia Hosting:** Exabytes Network Malaysia (Shared/Business Cloud Hosting).
* **Web Server:** LiteSpeed Web Server Enterprise.
* **Versi PHP Minimum:** PHP 8.1.x atau PHP 8.2.x dengan ekstensi cURL, OpenSSL, MBString, dan GD/Imagick aktif.
* **Basis Data:** MySQL 5.7+ / MariaDB 10.3+.
* **Dukungan Peramban (Browser):** Google Chrome, Apple Safari, Microsoft Edge, Mozilla Firefox (versi mobile & desktop).

### 6.2. Diagram Alur Pengguna (User Flow & Persona)

#### Alur 1: Calon Klien Korporat (Corporate Employer Flow)
```
[Buka Website] -> [Lihat Kredibilitas & Sektor Industri] -> [Klik Tombol WhatsApp / Isi Form Kebutuhan SDM] -> [Data Masuk ke Sales Acetalent] -> [Negosiasi Kontrak Kerjasama]
```

#### Alur 2: Pencari Kerja / Kandidat (Job Seeker Flow)
```
[Buka Website] -> [Buka Menu Available Jobs] -> [Pilih Lowongan yang Sesuai] -> [Isi Data & Upload Berkas CV] -> [Email Konfirmasi Terkirim ke Rekruter Acetalent] -> [Pemanggilan Wawancara]
```

#### Alur 3: Staf Kantor Acetalent (Admin Staff Flow)
```
[Login Admin] -> [Buka Menu Lowongan Kerja] -> [Ketik Info Posisi Baru & Simpan] -> [Website Otomatis Tampilkan Info Baru Tanpa Koding]
```

---

## 7. RINCIAN STRUKTUR BIAYA INVESTASI (PRICELIST RESMI)

Tiga tingkatan paket dirancang secara rasional untuk memberikan kepastian hasil sesuai prioritas anggaran perusahaan:

```
+---------------------------------------------------------------------------------------------------+
| PARAMETER EVALUASI         | PAKET 1: STARTER            | PAKET 2: BUSINESS GROWTH    | PAKET 3: ENTERPRISE         |
+---------------------------------------------------------------------------------------------------+
| Biaya Investasi            | Rp 1.500.000                | Rp 3.200.000                | Rp 4.900.000                |
| Status Rekomendasi         | Pemulihan Cepat             | PILIHAN UTAMA (BEST VALUE)  | Solusi Digital Lengkap      |
| Estimasi Waktu Selesai     | 3 - 5 Hari Kerja            | 6 - 7 Hari Kerja (~1 Mgg)   | 8 - 9 Hari Kerja (Max)      |
| Kapasitas Halaman          | 4 - 5 Halaman Inti          | 6 - 8 Halaman Terstruktur   | 10 - 12 Halaman + Landing   |
| Perbaikan Error Homepage   | Termasuk                    | Termasuk                    | Termasuk                    |
| Integrasi Tombol WhatsApp  | Tautan biasa                | Tombol Mengambang (1-Klik)  | Tombol Mengambang Pintar    |
| Pengunggahan Berkas CV     | Belum tersedia              | Formulir Unggah PDF/DOCX    | Unggah Terkoneksi Kategori  |
| Spesialisasi 7 Industri    | Ringkasan teks              | Showcase Visual Lengkap     | Halaman Detail Portofolio   |
| Tingkat Optimasi SEO       | Terdaftar di Google (Dasar) | SEO Lokal Tertarget (Kota)  | SEO Penuh + Google Jobs     |
| Pembaruan Server Exabytes  | Update PHP 5.6 -> 8.1       | Tuning LiteSpeed Cache      | Tuning + Backup Otomatis    |
| Modul Lowongan Mandiri     | Input manual oleh tim dev   | Disediakan panduan ubah     | Portal Job Board Mandiri    |
| Materi Panduan Staf        | Dokumen ringkasan           | Dokumen panduan + tanya-jwb | Dokumen panduan operasional |
| Masa Garansi Resmi         | 14 Hari                     | 30 Hari Penuh               | 60 Hari Penuh               |
+---------------------------------------------------------------------------------------------------+
```

---

## 8. KETENTUAN KERJASAMA, PEMBAYARAN & KEAMANAN SISTEM

### 8.1. Skema Pembayaran Bertahap (Termin 50/50)
1. **Uang Muka (DP) 50%:** Dibayarkan setelah penawaran disepakati bersama dan sebelum akses konfigurasi server Exabytes dimulai.
2. **Pelunasan 50%:** Dibayarkan setelah seluruh pekerjaan selesai, diuji bersama (UAT), dan situs web siap dipublikasikan penuh ke domain acetalent.my.
3. Tidak ada biaya tersembunyi selama masa pengembangan proyek.

### 8.2. Protokol Keamanan & Perlindungan Server Exabytes
1. **Pencadangan Penuh (Full Backup):** Backup basis data MySQL dan seluruh berkas lama dilakukan sebelum kami menyentuh konfigurasi server.
2. **Kerahasiaan Kredensial:** Akses akun cPanel Exabytes dijamin kerahasiaannya dan hanya digunakan untuk instalasi perbaikan.
3. **Anjuran Pasca-Peluncuran:** Klien dianjurkan mereset kata sandi cPanel setelah serah terima selesai demi kedaulatan keamanan perusahaan.

### 8.3. Batasan Ruang Lingkup Pekerjaan (Scope Boundaries)
1. **Materi & Legalitas:** Bahan teks profil khusus, foto kantor, dan dokumen legalitas disediakan oleh pihak Acetalent.
2. **Biaya Berlangganan Server:** Biaya perpanjangan tahunan domain .my dan hosting Exabytes tetap menjadi kewajiban langsung klien ke pihak Exabytes.
3. **Batasan Revisi:** Revisi mencakup penataan tata letak, warna, teks, dan fungsi fitur yang disepakati (bukan penambahan modul baru di luar paket).

### 8.4. Cakupan Garansi Purnajual Resmi
1. **Jaminan Perbaikan:** Perbaikan cepat tanpa biaya tambahan jika terjadi kendala teknis, tampilan bergeser, atau form email mengalami masalah pasca-peluncuran.
2. **Durasi Garansi Resmi:** Berlaku selama 14 hari (Starter), 30 hari penuh (Business Growth), atau 60 hari penuh (Enterprise).
3. **Ketenangan Manajemen:** Memberikan rasa aman penuh bagi manajemen Acetalent yang tidak memiliki staf pengembang IT internal.

---

## 9. REKOMENDASI DAN RENCANA AKSI (NEXT STEPS)

1. **Pemilihan Paket:** Klien menyetujui salah satu dari 3 opsi paket di atas (Paket 2: *Business Growth* sangat direkomendasikan demi hasil komersial maksimal).
2. **Pemberian Akses cPanel:** Penyerahan akun cPanel Exabytes untuk proses pencadangan dan pembaruan versi PHP.
3. **Pembayaran Uang Muka (DP):** Skema termin disepakati 50% di awal kontrak kerja dan 50% pelunasan setelah proyek dinyatakan tuntas serta disetujui (UAT).
4. **Kickoff Pengerjaan:** Eksekusi langsung dimulai dengan pelaporan progres berkala hingga peluncuran dalam kurun waktu 1 minggu + 2 hari kerja.

---
*Dokumen ini diterbitkan secara sah sebagai cetak biru resmi pengembangan website Acetalent.*
