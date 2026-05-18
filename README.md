# 💰 Pasar Cuan - Economy Management Simulation Game

[![Godot Engine](https://img.shields.io/badge/Engine-Godot_4.6-blue?logo=godot-engine&logoColor=white)](https://godotengine.org)
[![Platform](https://img.shields.io/badge/Platform-PC_%2F_Laptop-green)](#)
[![Genre](https://img.shields.io/badge/Genre-Simulation_%2F_Strategy-orange)](#)
[![Visual Style](https://img.shields.io/badge/Visual_Style-2D_Pixel_Art_Top--Down-purple)](#)

[![Demo Gameplay Pasar Cuan](https://img.youtube.com/vi/NaTvAf2HT9M/maxresdefault.jpg)](https://www.youtube.com/watch?v=NaTvAf2HT9M)

**Pasar Cuan** adalah sebuah permainan simulasi manajemen ekonomi mikro berbasis data yang mengambil latar unik kebudayaan lokal Indonesia, yaitu **Pasar UMKM**. Di game ini, Anda berperan sebagai pengelola kawasan pasar malam yang ditantang untuk mengubah lahan kosong menjadi mesin bisnis yang legendaris dalam batasan waktu **30 Hari**.

Berbeda dengan game pembangun kota (*city builder*) tradisional yang rumit, *Pasar Cuan* berfokus penuh pada penyusunan tata letak strategis (**Zoning**) dan elastisitas permainan harga (**Pricing**) untuk menguji ketahanan finansial Anda dari serbuan pengunjung pasar yang dinamis.

---

## 🧠 Pilar Utama & Fitur Unggulan

### 1. Pengunjung Berotak Mandiri (*Agent-Based Modeling*)
Game ini tidak menggunakan sistem kerumunan massal yang kaku (*top-down*). Setiap pengunjung (NPC) yang lahir di trotoar bertindak sebagai agen independen dengan karakteristik unik bawaan:
* **Dompet (*Budget*):** Batas maksimal uang tunai yang rela dikeluarkan untuk bertransaksi.
* **Kesabaran (*Patience*):** Batas toleransi antrean sebelum mereka memutuskan pergi karena lelah menunggu.
* **Niat Beli (*Intention*):** Probabilitas ketertarikan acak yang membuat simulasi terasa organik.

Kekecewaan massal (seperti munculnya *emoji* 😠 *Mahal!* atau 😠 *Antre!*) terbentuk secara alami dari reaksi individual agen terhadap harga dan tata letak yang Anda buat.

### 2. Siklus Tiga Fase Harian (*State Machine*)
Permainan berjalan dalam ritme harian yang memisahkan wewenang perencanaan dan simulasi secara mekanis:
* **🌅 Fase Pagi (Perencanaan):** Waktu berhenti total (*pause*). Anda bebas membaca prediksi tren harian dari Asisten Pintar, membeli lapak baru, mengatur posisi bangunan agar areanya (AoE) menyentuh trotoar, dan menetapkan slider harga produk.
* **☀️ Fase Siang (Simulasi):** Pasar dibuka dan Anda kehilangan kontrol interaksi. Tugas Anda murni mengobservasi pergerakan agen, membaca keluhan lewat *emoji* melayang, dan mengumpulkan metrik performa secara langsung.
* **🌙 Fase Malam (Evaluasi Keuangan):** Waktu kembali berhenti untuk proses audit buku harian. Biaya operasional (OpEx) dipotong secara otomatis, dan grafik laporan performa disajikan bersama kritik tajam atau pujian dari **AI Advisor**.

### 3. Sistem Ekonomi Makro yang Kejam & Dinamis
* **Target Kemenangan Bergerak (*High-Water Mark*):** Syarat menang di Hari ke-30 bukan angka statis. Target uang tunai Anda ditetapkan sebesar **1,5x lipat dari rekor nilai aset tertinggi** yang pernah Anda miliki. Semakin rakus Anda membangun, semakin besar target tabungan akhir bulan Anda!
* **Biaya Operasional Progresif (OpEx):** Pajak kebersihan harian akan meningkat secara progresif seiring bertambahnya jumlah dan kemewahan lapak yang berdiri.
* **Likuidasi Cepat (*Refund* 80%):** Lapak yang merugi atau sepi bisa dijual kembali secara instan di Fase Pagi untuk mencairkan 80% dana segar dari harga beli awal.

### 4. Rantai Pasok & Aturan Paguyuban
Kenaikan Level membuka peluang bisnis yang lebih besar tetapi memiliki tantangan rantai pasokan dan pengawasan ketat dari Paguyuban Pasar:
* **Level 1–4 (Era Minuman):** Hanya membuka akses **Lapak Minuman** (modal murah, menyasar pengunjung berdompet tipis).
* **Level 5 (Era Makanan):** Membuka kunci **Lapak Makanan**, dengan syarat Anda wajib memiliki minimal **2 Lapak Minuman** yang aktif berdiri. Pengunjung kelas menengah mulai berdatangan.
* **Level 10 (Era Pakaian):** Membuka kunci **Lapak Pakaian** untuk mengincar pasar para "Sultan", dengan syarat minimal memiliki **2 Lapak Minuman DAN 2 Lapak Makanan** yang aktif. Jika Anda naik level tetapi pelit berekspansi, Paguyuban akan menyita lahanmu secara paksa!

---

## 🛠️ Arsitektur Teknis Kode Utama

Game ini dirancang menggunakan arsitektur pemrograman yang bersih (*clean code*) dan modular di **Godot Engine 4.6 (GDScript)**:

1. **`EconomyManager.gd` (Global Autoload / Singleton):** Pusat kendali kebenaran data tunggal (*Single Source of Truth*). Mengatur pengelolaan saldo kas harian, sistem kurva EXP polinomial, perhitungan rating kepuasan *real-time*, akumulasi data pengunjung harian, serta melacak status ambang batas kebangkrutan (3 hari saldo minus berturut-turut).
2. **`CameraController.gd`:** Sistem kendali kamera 2D yang mendukung fitur menyeret tanah (*panning*) menggunakan klik roda tengah *mouse* serta *zoom-scroll* halus berbasis interpolasi delta. Dilengkapi dengan fitur **Anti-Void Dinamis** yang menjatuhkan batas mundur kamera agar latar abu-abu di luar map tidak pernah bocor ke layar pemain.
3. **`day_night_cycle.gd`:** Menggunakan node `CanvasModulate` dikombinasikan dengan sistem pembagian babak waktu (`Tween`) untuk meredupkan langit secara *real-time* dari putih terang (pagi-siang), oranye senja (sore), hingga biru gelap elegan (malam) secara otomatis seiring jalannya waktu simulasi.

---

## 🚀 Cara Instalasi & Menjalankan Proyek

Jika Anda ingin menguji atau mengembangkan kode sumber *Pasar Cuan* di komputer lokal Anda, ikuti langkah berikut:

### Persyaratan Sistem
* **Godot Engine versi 4.6 Stable** (Standard Version / Non-.NET).
* Sistem Operasi Windows, macOS, atau Linux.

### Langkah Eksekusi
1. Unduh atau klon repositori ini ke penyimpanan lokal Anda:
   ```bash
   git clone [https://github.com/UsernameAnda/Pasar-Cuan.git](https://github.com/UsernameAnda/Pasar-Cuan.git)
2. Buka aplikasi Godot Engine 4.6.
3. Klik tombol Import di panel kanan atas proyek manager.
4. Arahkan folder ke direktori hasil klon, pilih file project.godot, lalu klik Import & Edit.
5. Setelah Editor Godot berhasil memuat seluruh aset, tekan tombol F5 (atau ikon Play di pojok kanan atas) untuk langsung menjalankan permainan.

## 👥 Tim Pengembang 
Proyek simulasi manajemen ini dirancang dan dikembangkan sepenuhnya oleh Kelompok 3 Open Recruitment GIGA 2026:

- Farras Abdurrazaq Ar-Rasyid — 5025241091

- Jorell Ramos Sinaga — 5025241202

- Muhammad Dayyan Ghazanfar Latief — 5054241036
