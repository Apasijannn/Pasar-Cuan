<div align="center">

<br/>

<!-- HERO SECTION -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:F59E0B,50:EF4444,100:DC2626&height=200&section=header&text=Pasar%20Cuan&fontSize=72&fontColor=FFFFFF&fontAlignY=38&desc=Economy%20Management%20Simulation&descSize=20&descAlignY=60&descColor=FDE68A&animation=fadeIn" width="100%"/>

<br/>

<!-- BADGES ROW 1 -->
<img src="https://img.shields.io/badge/Engine-Godot_4.6_Stable-478CBF?style=for-the-badge&logo=godot-engine&logoColor=white"/>
&nbsp;
<img src="https://img.shields.io/badge/Language-GDScript-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
&nbsp;
<img src="https://img.shields.io/badge/Platform-Windows_%7C_macOS_%7C_Linux-0078D4?style=for-the-badge&logo=windows&logoColor=white"/>

<br/><br/>

<!-- BADGES ROW 2 -->
<img src="https://img.shields.io/badge/Genre-Simulation_%2F_Strategy-7C3AED?style=for-the-badge"/>
&nbsp;
<img src="https://img.shields.io/badge/Visual_Style-2D_Pixel_Art_Top--Down-EC4899?style=for-the-badge"/>
&nbsp;
<img src="https://img.shields.io/badge/Duration-30_Hari-F59E0B?style=for-the-badge"/>
&nbsp;
<img src="https://img.shields.io/badge/Status-In_Development-22C55E?style=for-the-badge"/>

<br/><br/>

> **💰 Pasar Cuan** adalah simulasi manajemen ekonomi mikro berbasis data yang mengambil jiwa kebudayaan lokal Indonesia — **Pasar UMKM**.  
> Ubah lahan kosong menjadi mesin bisnis legendaris dalam **30 Hari** penuh tekanan finansial!

<br/>

[![▶️ TONTON DEMO GAMEPLAY](https://img.shields.io/badge/▶%20TONTON%20DEMO%20GAMEPLAY-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=NaTvAf2HT9M)

[![Demo Gameplay Pasar Cuan](https://img.youtube.com/vi/NaTvAf2HT9M/hqdefault.jpg)](https://www.youtube.com/watch?v=NaTvAf2HT9M)

</div>

---

## 📖 Tentang Game

**Pasar Cuan** bukan *city builder* biasa yang rumit dan membingungkan. Game ini berfokus pada dua senjata utama seorang manajer pasar sejati:

| ⚙️ Zoning | 💲 Pricing |
|:---:|:---:|
| Susun tata letak lapak secara strategis agar area pengaruh (**AoE**) menyentuh jalur pengunjung | Mainkan elastisitas harga untuk memaksimalkan pendapatan tanpa mengusir pembeli |

Setiap keputusan Anda diuji oleh pengunjung yang **berpikir mandiri**, sistem ekonomi yang **kejam**, dan target kemenangan yang **selalu bergerak**.

---

## 🧠 Pilar Utama & Fitur Unggulan

### 👤 1. Pengunjung Berotak Mandiri — *Agent-Based Modeling*

> Game ini **tidak** menggunakan sistem kerumunan massal yang kaku. Setiap NPC adalah agen independen dengan jiwa sendiri.

Setiap pengunjung yang lahir di trotoar membawa tiga atribut unik:

```
┌─────────────────────────────────────────────────────────┐
│  💵  DOMPET (Budget)    → Batas maksimal uang tunai      │
│  ⏳  KESABARAN (Patience) → Toleransi antrean sebelum   │
│                             menyerah dan pulang          │
│  🎯  NIAT BELI (Intention) → Probabilitas ketertarikan  │
│                               acak yang menciptakan      │
│                               perilaku organik           │
└─────────────────────────────────────────────────────────┘
```

Kekecewaan massal terbentuk **secara alami** dari reaksi individual — bukan dari skrip yang diprogram!

| Ekspresi | Pemicu |
|:---:|:---|
| 😠 *Mahal!* | Harga produk melampaui batas dompet pengunjung |
| 😠 *Antre!* | Jumlah orang menunggu melampaui batas kesabaran |

---

### 🔄 2. Siklus Tiga Fase Harian — *State Machine*

Permainan berjalan dalam ritme harian yang tegas. Waktu wewenang Anda dan waktu simulasi **tidak pernah tumpang tindih**.

```
 ╔══════════════════════════════════════════════════════════════╗
 ║                    SIKLUS SATU HARI                          ║
 ╠══════════════════╦═══════════════════╦═════════════════════╣
 ║  🌅 PAGI         ║  ☀️ SIANG         ║  🌙 MALAM           ║
 ║  [PERENCANAAN]   ║  [SIMULASI]       ║  [EVALUASI]         ║
 ╠══════════════════╬═══════════════════╬═════════════════════╣
 ║ • Waktu berhenti ║ • Pasar dibuka    ║ • Waktu berhenti    ║
 ║ • Baca prediksi  ║ • Kontrol DIKUNCI ║ • OpEx dipotong     ║
 ║   AI Advisor     ║ • Observasi agen  ║ • Laporan harian    ║
 ║ • Beli/atur lapak║ • Baca emoji NPC  ║ • Kritik AI Advisor ║
 ║ • Set slider     ║ • Kumpul metrik   ║ • Rencanakan besok  ║
 ║   harga          ║                   ║                     ║
 ╚══════════════════╩═══════════════════╩═════════════════════╝
```

---

### 📈 3. Sistem Ekonomi Makro yang Kejam & Dinamis

<details>
<summary><b>🏆 Target Kemenangan Bergerak — <i>High-Water Mark</i></b></summary>

<br/>

Syarat menang di Hari ke-30 **bukan angka statis**. Target ditetapkan sebesar:

$$\text{Target Akhir} = 1.5 \times \text{Rekor Nilai Aset Tertinggi yang Pernah Anda Miliki}$$

> ⚠️ **Semakin rakus Anda membangun, semakin besar target tabungan akhir bulan!**  
> Strategi pertumbuhan agresif = risiko yang jauh lebih tinggi.

</details>

<details>
<summary><b>💸 Biaya Operasional Progresif (OpEx)</b></summary>

<br/>

Pajak kebersihan harian meningkat secara **progresif** seiring bertambahnya jumlah dan kemewahan lapak. Ekspansi berlebihan tanpa pemasukan yang sepadan = kebangkrutan terselubung.

</details>

<details>
<summary><b>♻️ Likuidasi Cepat — Refund 80%</b></summary>

<br/>

Lapak yang merugi atau sepi bisa dijual kembali secara **instan** di Fase Pagi untuk mencairkan **80% dana segar** dari harga beli awal. Rotasi lapak adalah senjata, bukan kekalahan!

</details>

<details>
<summary><b>📛 Status Kebangkrutan</b></summary>

<br/>

Sistem melacak **3 hari saldo minus berturut-turut**. Jika terjadi, game over — pasar Anda resmi bangkrut.

</details>

---

### 🏪 4. Rantai Pasok & Aturan Paguyuban

Naik Level membuka peluang bisnis lebih besar — tapi Paguyuban Pasar mengawasi ketat!

```
LEVEL  1 ──────────────────────────── LEVEL  5 ───────── LEVEL 10
  │                                       │                  │
  ▼                                       ▼                  ▼
🥤 ERA MINUMAN                       🍱 ERA MAKANAN     👕 ERA PAKAIAN
──────────────                       ──────────────     ──────────────
Hanya Lapak Minuman                  Buka Lapak Makanan  Buka Lapak Pakaian
Modal rendah                         Syarat: min. 2      Syarat: min. 2 Minuman
Target: pengunjung                   Lapak Minuman aktif + 2 Makanan aktif
berdompet tipis                      Target: kelas        Target: para "Sultan"
                                     menengah
                                     
                    ⚠️  PERINGATAN PAGUYUBAN  ⚠️
                    Naik level tapi pelit ekspansi?
                    → Lahan Anda akan DISITA PAKSA!
```

---

## 🛠️ Arsitektur Teknis

Game dirancang dengan prinsip ***clean code*** dan arsitektur **modular** di Godot Engine 4.6.

```
Pasar-Cuan/
├── 📁 autoload/
│   └── 🔑 EconomyManager.gd        # Singleton — Single Source of Truth
├── 📁 scripts/
│   ├── 🎥 CameraController.gd      # Panning + Zoom + Anti-Void Dinamis  
│   ├── 🌅 day_night_cycle.gd       # CanvasModulate + Tween State Machine
│   ├── 🧍 visitor_agent.gd         # Agent-Based NPC Logic
│   └── 🏪 stall_manager.gd         # Lapak Placement & AoE System
├── 📁 scenes/
├── 📁 assets/
└── 📄 project.godot
```

<br/>

### 🔑 `EconomyManager.gd` — *Global Autoload / Singleton*

> Pusat kendali **Single Source of Truth** seluruh game.

- ✅ Pengelolaan saldo kas harian
- ✅ Sistem kurva EXP polinomial
- ✅ Perhitungan rating kepuasan *real-time*
- ✅ Akumulasi data pengunjung harian
- ✅ Pelacak status ambang batas kebangkrutan *(3 hari minus berturut-turut)*

---

### 🎥 `CameraController.gd`

> Sistem kendali kamera 2D yang halus dan responsif.

- ✅ **Panning** via klik roda tengah *mouse*
- ✅ **Zoom-scroll** berbasis interpolasi delta
- ✅ **Anti-Void Dinamis** — batas kamera otomatis mencegah latar abu-abu bocor ke layar

---

### 🌅 `day_night_cycle.gd`

> Atmosfer visual yang berubah otomatis seiring waktu simulasi.

```
☀️ Putih Terang  ──▶  🌇 Oranye Senja  ──▶  🌃 Biru Gelap Elegan
   (Pagi-Siang)            (Sore)                  (Malam)
   
   Ditenagai: CanvasModulate + Tween
```

---

## 🚀 Instalasi & Menjalankan Proyek

### 📋 Persyaratan Sistem

| Komponen | Spesifikasi |
|:---|:---|
| **Engine** | [Godot Engine 4.6 Stable](https://godotengine.org/download) — Standard Version *(Non-.NET)* |
| **OS** | Windows / macOS / Linux |
| **Git** | Versi terbaru (opsional, untuk clone) |

---

### ⚡ Langkah Instalasi

**1. Clone repositori**
```bash
git clone https://github.com/UsernameAnda/Pasar-Cuan.git
cd Pasar-Cuan
```

**2. Buka Godot Engine 4.6**

**3. Import proyek**
```
Klik tombol [Import] di Project Manager
→ Arahkan ke folder hasil clone
→ Pilih file: project.godot
→ Klik [Import & Edit]
```

**4. Jalankan game**
```
Tekan  F5  atau klik ikon ▶ Play di pojok kanan atas Editor
```

> 💡 **Tips:** Pastikan Anda menggunakan versi **Standard (Non-.NET)** dari Godot 4.6. Versi .NET memerlukan konfigurasi tambahan yang tidak diperlukan proyek ini.

---

## 👥 Tim Pengembang

> Proyek ini dirancang dan dikembangkan sepenuhnya oleh **Kelompok 3** dalam rangka **Open Recruitment GIGA 2026**.

<br/>

<div align="center">

| <img src="https://github.com/identicons/farras.png" width="80" height="80" style="border-radius:50%"/> | <img src="https://github.com/identicons/jorell.png" width="80" height="80" style="border-radius:50%"/> | <img src="https://github.com/identicons/dayyan.png" width="80" height="80" style="border-radius:50%"/> |
|:---:|:---:|:---:|
| **Farras Abdurrazaq Ar-Rasyid** | **Jorell Ramos Sinaga** | **Muhammad Dayyan Ghazanfar Latief** |
| `5025241091` | `5025241202` | `5054241036` |

</div>

---

## 📜 Lisensi

Proyek ini dikembangkan untuk keperluan rekrutmen internal GIGA 2026. Seluruh aset dan kode sumber merupakan karya orisinal tim pengembang.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:DC2626,50:EF4444,100:F59E0B&height=120&section=footer&text=Pasar%20Cuan%20%C2%A9%202026&fontSize=24&fontColor=FFFFFF&fontAlignY=65&animation=fadeIn" width="100%"/>

<br/>

*Dibuat dengan ❤️ menggunakan Godot Engine 4.6 — Kelompok 3 GIGA 2026*

</div>
