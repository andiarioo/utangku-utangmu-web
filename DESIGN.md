# DESIGN.md · Situs Utangku Utangmu

| | |
|---|---|
| **Status** | Revisi 3 (Struk Resmi), disetujui pemilik produk 18 November 2026. Revisi 1 disetujui 13 November, revisi 2 disetujui 17 November 2026 (tersimpan di commit `cf04595`) |
| **Berlaku untuk** | Landing page (satu halaman), ikut dipakai `kebijakan-privasi.html` dan `penguji.html` |
| **Sumber visual** | Papan **1B · Struk Resmi · tanpa antislop (revisi 7)** di kanvas "Utangku Utangmu, Opsi Landing Page", dipilih pemilik 18 November 2026 dari enam opsi (tiga ide, masing-masing dengan dan tanpa antislop) |

**Kenapa revisi 3.** Pemilik masih kurang suka revisi 2. Supaya lebih hemat waktu, desain digarap dulu di kanvas, bukan langsung di situs. Pemilik memilih versi **tanpa antislop**, lalu menyempurnakannya lewat tujuh putaran revisi. Dokumen ini menurunkan papan itu menjadi aturan untuk kode. Kalau dokumen ini dan papan 1B berbeda, papan 1B yang benar, kecuali untuk hal yang ditulis di bagian 7.2 (perilaku di HP, yang tidak ada di papan).

---

## 0. Sumber, dan mana yang menang

| Urutan | Sumber | Dipakai untuk |
|---|---|---|
| 1 | `docs/panduan-merek-utangku-utangmu-v1.3.svg` | Mark, nama, warna, tipografi, nada suara, larangan |
| 2 | `docs/BRAND-GUIDELINE.md`, terutama **bagian 5 (materi pemasaran)** | Yang boleh di situs tapi tidak di aplikasi: bayangan, pendar gradien, dan warna arah pada panah serta nominal contoh |
| 3 | Papan 1B di kanvas | Susunan, bentuk, isi teks |
| 4 | Layar aplikasi yang dirender dari kode | Kebenaran tentang aplikasi. Kalau papan dan layar berbeda, layar yang benar |
| 5 | `lib/pesan/susun_pesan.dart`, `lib/pengingat/jadwal_pengingat.dart`, `deskripsi-play-store.md` | Isi pesan contoh dan fakta yang boleh diklaim |
| 6 | Pedoman lencana Google Play | Bentuk dan pemakaian tombol unduh |

---

## 1. Arah

> **Struk Resmi: pesan resmi jadi bintangnya.** Pesan gaya resmi tampil sebagai struk kertas bertepi sobek, berdampingan dengan gelembung chat gaya santai dan sopan. Di sekelilingnya: kartu putih berbayang lembut, pita hijau bergradien, dan layar aplikasi asli di dalam bingkai HP.

- **Hidup, tidak polos.** Bayangan, gradien, kartu, dan kemiringan ringan dipakai dengan sengaja. Keluhan "terlalu polos dan seperti tumpukan teks" adalah alasan utama revisi ini.
- **Tetap resmi.** Teks struk memakai huruf mono, tanpa emoji, tanpa tanda seru, tanpa perayaan.
- **Tanpa antislop.** Aturan gaya antislop (larangan bayangan, gradien, FAQ, tiga langkah, kartu) tidak berlaku untuk revisi ini. Pemeriksaan teknisnya tetap dijalankan (bagian 12).

---

## 2. Konsep

**Dua arah, satu aplikasi.** Nama produk adalah dua arah itu sendiri. Bagian kedua halaman langsung menunjukkan kartu Utangmu dan Utangku berdampingan, masing-masing dengan pesan yang disiapkan untuknya.

**Tunjukkan pesannya.** Pembeda produk adalah pesan siap-kirim. Struk resmi muncul di hero, lalu muncul lagi di bagian pesan bersama gelembung santai dan sopan.

**Jujur.** Tidak ada testimoni, angka pengguna, rating, atau klaim yang tidak bisa ditunjukkan di aplikasi.

---

## 3. Warna

### 3.1 Palet

| Token | Nilai | Peran di situs |
|---|---|---|
| Hutan | `#123F2E` | Pita hero dan pesan, kartu fitur besar, kartu Utangmu, ikon langkah, judul kecil di kartu terang |
| Hutan Gelap | `#0B261C` | Ujung gelap gradien, latar kaki halaman |
| Hutan Tengah | `#1B5640` | Ujung terang gradien gelap |
| Hutan Terang | `#8FC7AC` | Baris kedua H1, teks pendamping di latar gelap, ikon garis, pendar gradien, cincin di sekitar baki lencana |
| Hutan Halus | `#E6EFEA` | Latar layar langkah, kotak ikon manfaat, tujuan backup, kartu pengingat; teks pendamping di latar gelap |
| Hutan Sekunder | `#7D958C` | Hanya garis: cap putus-putus di struk. **Tidak untuk teks** (3.21:1 di atas putih, gagal AA). Di papan ia dipakai untuk label kecil seperti "Langkah 1" dan "Pesan yang disiapkan"; di situs label itu memakai Redup (6.05:1) |
| Hijau Gelembung | `#D9EEE3` | Gelembung chat keluar |
| Kertas | `#F1F4F1` | Latar halaman |
| Putih | `#FFFFFF` | Kartu, struk, baki lencana, kotak pesan mini |
| Tinta | `#171A21` | Teks utama, bezel HP |
| Redup | `#5C636F` | Teks pendamping di latar terang |
| Garis | `#E2E5EA` | Tepi baris manfaat backup |
| Teks di atas Hutan Terang | `#0B1A13` | Teks di kartu Utangku dan lencana nada |

### 3.2 Warna arah: hanya di data

Pengecualian di `BRAND-GUIDELINE.md` bagian 5 (diputuskan pemilik, 18 November 2026; `CATATAN-TERTUNDA.md` A35 di repo aplikasi):

| Arah | Di latar terang | Di latar gelap | Dipakai pada |
|---|---|---|---|
| Utangmu / Akan diterima | Lumut `#0E7A4C` | Lumut Terang `#5DD69B` | Panah ↙ dan nominal contoh "Sisa: Rp 300.000" |
| Utangku / Harus dibayar | Bata `#C0402C` | Bata Terang `#FA9077` | Panah ↗ dan nominal contoh "Jumlah: Rp 300.000" |

**Hanya panah dan nominal.** Tidak pernah latar, judul, kartu, tombol, lencana, atau mark. Kunyit tidak dipakai di luar layar aplikasi.

### 3.3 Gradien

| Nama | Nilai | Dipakai |
|---|---|---|
| Pita hero | pendar `radial-gradient(900px 500px at 75% 30%, Hutan Terang 35%, transparan 60%)` di atas `linear-gradient(160deg, #1B5640, #123F2E 45%, #0B261C)` | Hero |
| Kartu gelap | `linear-gradient(160deg, #1B5640, #123F2E)` | Kartu Utangmu, kartu fitur besar |
| Kartu Utangku | `linear-gradient(160deg, #E6EFEA, #8FC7AC)` | Kartu Utangku. Kiri atas sengaja paling terang supaya panah Bata terbaca |
| Ajakan | pendar `radial-gradient(600px 300px at 50% 0%, Hutan Terang 45%, transparan 70%)` di atas `linear-gradient(135deg, #1B5640, #0B261C)` | Kotak ajakan penutup |

Pita bagian pesan tetap Hutan rata, tanpa gradien.

### 3.4 Kontras

Diukur ulang pada halaman jadi. Pasangan yang perlu dijaga:

- Panah arah adalah grafik besar (44px), minimal 3:1: Bata di atas `#E6EFEA` 4.46, Lumut Terang dan Bata Terang di atas kartu gelap 3.8 ke atas.
- Nominal berwarna di kotak putih: Bata 5.24, Lumut 5.38.
- Teks di latar gelap: Hutan Terang di atas Hutan 6.16, Hutan Halus di atas Hutan 10.08.
- Redup di atas putih 6.05. Hutan Sekunder tidak dipakai untuk teks (lihat 3.1).

---

## 4. Tipografi

| Huruf | Dipakai untuk |
|---|---|
| **Plus Jakarta Sans** 400 · 600 · 700 · 800 | Semua judul, isi, label, tombol, gelembung santai dan sopan |
| **IBM Plex Mono** 400 · 600 | **Hanya** struk pesan resmi, kotak pesan mini, dan nominal contoh (aturan CLAUDE.md nomor 10) |

Kedua huruf di-*host* sendiri dari `huruf/` dan di-*preload*. Papan memakai Google Fonts; situs tidak, supaya situs yang menjual privasi tidak mengirim alamat IP pengunjung ke Google.

| Peran | Ukuran | Bobot |
|---|---|---|
| H1 | `clamp(34px, 3.9vw, 50px)` (papan: 58px, lihat 7.2), tinggi baris 1.05, spasi huruf -0.03em | 800 |
| Judul bagian (`.judul`) | `clamp(26px, 3vw, 36px)`, tinggi baris 1.2 | 700 |
| Judul ajakan | `clamp(28px, 3.4vw, 40px)` | 700 |
| Label bagian | 15px | 700 |
| H3 kartu | 21 sampai 26px | 700 |
| Pengantar hero | 20px | 400 |
| Isi | 17px, tinggi baris 1.6 | 400 |
| Struk | 13.5px mono, tinggi baris 1.65 | 400, kop 600 |

**Aturan judul** (dari revisi pemilik):
- Satu baris di desktop. Tidak ada judul yang patah ke baris baru dengan janggal.
- Tanpa titik di akhir, tanpa koma di tengah.
- Bukan label huruf besar berjarak lebar.

---

## 5. Bentuk

### 5.1 Radius dan bayangan

| Elemen | Radius | Bayangan |
|---|---|---|
| Kartu | 24 | `0 20px 40px -24px` Hutan 35% + `0 2px 6px` Hutan 6% |
| Kotak backup | 32 | `0 30px 60px -30px` Hutan 40% |
| Kotak ajakan | 36 | `0 40px 80px -40px` Hutan 80% |
| Struk | 18 atas, tepi bawah sobek | `0 40px 80px -30px` hitam 60% |
| Baki lencana | 20 | `0 24px 48px -18px` hitam 60% + cincin 6px Hutan Terang 25% |
| Gelembung chat | 22, sudut kanan bawah 6 dengan ekor | `0 18px 36px -18px` hitam 35% |
| Kotak pesan mini | 14 | `0 16px 32px -18px` hitam 45% |
| Stiker hero | 14 | `0 16px 32px -12px` hitam 50% |
| Baris manfaat backup | 16, tepi 1px Garis | tanpa |
| Tombol "Lihat cara kerja" | 12, tepi 1.5px putih 40% | tanpa |
| Ikon langkah | 14 | tanpa |

### 5.2 Unsur khas

- **Label bagian:** mark Utangku Utangmu (26 × 21) + teks 15px tebal. Latar terang: mark dua warna. Latar gelap: mark putih penuh.
- **Struk:** kertas putih, tepi bawah bergerigi setengah lingkaran (CSS `mask`), sedikit dimiringkan (-3° di hero, -4° di bagian pesan). Di bagian pesan ada cap bergaris putus "STATUS: BELUM JATUH TEMPO".
- **Baki lencana:** lencana resmi Google Play di atas baki putih, dengan teks "Pasang di HP Anda / Tanpa login, tanpa buat akun". Lencananya sendiri tidak diubah.
- **Daftar nada:** tiga baris, lencana Hutan Terang (Resmi, Santai, Sopan) + satu kalimat. Tidak patah baris di desktop.
- **Alur backup:** "1 file backup" → cabang garis putus → Cloud | Folder di HP, vertikal.

---

## 6. Gambar dan mark

### 6.1 Layar aplikasi dalam bingkai HP

Layar dirender dari kode aplikasi pada 1080 × 2340 piksel, sama dengan revisi 2. Isinya tidak disunting.

Bingkai HP Android generik dari CSS (`container-type: inline-size`, ukuran dalam `cqw`): bezel Tinta, kamera berlubang di area status kosong, sudut membulat. Sejak revisi 3 bingkainya **berbayang** (`0 30px 60px -20px` hitam 55%).

| Berkas | Layar | Dipakai di |
|---|---|---|
| `gambar/hp/2-pesan-resmi-*.webp` | Kirim pengingat, format resmi | Hero |
| `gambar/hp/6-telat-*.webp` | Daftar dengan satu catatan telat | Kartu fitur besar |
| `gambar/hp/4-detail-*.webp` | Detail catatan dan riwayat pembayaran | Kartu cicilan |
| `gambar/hp/0b-form-catat-*.webp` **(baru)** | Form catat baru | Langkah 1 |
| `gambar/hp/3-pesan-santai-*.webp` **(baru)** | Pemilihan nada | Langkah 2 |
| `gambar/hp/0c-form-pembayaran-*.webp` **(baru)** | Catat pembayaran | Langkah 3 |

Lebar 300 dan 450 dengan `srcset`; `width`/`height` tertulis. Hero memakai `fetchpriority="high"`, sisanya `loading="lazy"`. `1-daftar` dan `5-backup` tidak dipakai lagi dan dihapus dari folder.

### 6.2 Mark, nama, logo

- Mark dari `docs/aset-toko/mark-utangku-utangmu.svg`, ditulis langsung sebagai SVG. Di latar gelap: kata pertama putih, bilah bawah Hutan Terang (kepala halaman dan kaki halaman), atau putih penuh (label bagian).
- **Logo Digital Insight Indonesia** (putih, mendatar) di kaki halaman, `gambar/logo-dii.svg`, diambil dari aset di kanvas (SVG, tanpa skrip).
- Favicon, manifest, dan gambar Open Graph tetap dari revisi 2. Gambar Open Graph belum disesuaikan dengan revisi 3 (lihat bagian 13).

### 6.3 Lencana Google Play

`gambar/google-play-id-330.webp`, tinggi tampil 60px, tidak diubah warna atau bentuknya, ada ruang bebas di dalam baki.

---

## 7. Susunan halaman

### 7.1 Urutan bagian

| # | Bagian | Latar | Isi |
|---|---|---|---|
| 1 | Hero | Pita hero | Kepala: mark + nama, menu Fitur · Pesan · Cara kerja · FAQ. H1 "Tagih tanpa canggung / Catat tanpa ribet". Pengantar. Baki lencana + tombol "Lihat cara kerja →". Kanan: HP pesan resmi, struk, stiker "Banyak pilihan pesan · Resmi · Santai · Sopan" |
| 2 | Utangku dan Utangmu | Kertas | "Catat utang orang lain sekaligus utang Anda sendiri". Kartu Utangmu (gelap) dan Utangku (terang) berdampingan, masing-masing dengan kotak pesan mini |
| 3 | Fitur (`#fitur`) | Kertas | "Semua utang piutang tertata rapi di satu tempat". Kartu fitur besar selebar penuh (empat kelompok waktu, dua arah, HP telat), lalu kartu cicilan dan kartu pengingat berdampingan |
| 4 | Pesan (`#pesan`) | Hutan | Kiri: label, "Pilih nada pesannya", pengantar, daftar nada. Kanan: struk resmi bercap + gelembung santai dan sopan |
| 5 | Cara kerja (`#cara`) | Kertas | "Dari catatan pertama sampai pesan terkirim". Tiga kartu: layar asli di atas, ikon + "Langkah N" sebaris, judul di bawahnya (di papan judul ada di samping ikon; dipindah supaya "Kirim, lalu catat bayarannya" muat satu baris), lalu penjelasan |
| 6 | Backup | Kotak putih | "Simpan backup di tempat pilihan Anda". Kiri: Mudah, Praktis, Tetap di tangan Anda. Kanan: alur vertikal |
| 7 | FAQ (`#faq`) | Kertas | Empat pertanyaan, `<details>` bawaan browser, yang pertama terbuka |
| 8 | Ajakan | Kotak ajakan | "Siap menagih tanpa canggung?", "Mulai dari satu catatan.", baki lencana |
| 9 | Kaki halaman | Hutan Gelap | Mark + satu kalimat · Hubungi kami (surel, WhatsApp) · Diterbitkan oleh (logo DII). Garis, lalu "© 2026 PT Digital Insight Indonesia" dan Kebijakan privasi |

Lebar isi maksimal 1200px, tepi kiri-kanan 32px (20px di ≤900px). Jarak antarbagian 100 sampai 110px di desktop.

### 7.2 Di HP (tidak ada di papan, diputuskan saat membangun)

Papan hanya digambar selebar 1440px. Aturan untuk layar kecil:

- **≤900px:** semua grid menjadi satu kolom. Jarak antarbagian turun ke 64px.
- **≤700px:** menu kepala disembunyikan; kepala hanya mark + nama.
- **Hero:** susunan bertumpuk (struk, HP, stiker yang diposisikan absolut) diubah menjadi aliran biasa: HP di tengah, struk menimpa sebagian kiri bawahnya, stiker disembunyikan di ≤480px. Tidak boleh ada yang terpotong atau membuat halaman bisa digeser ke samping.
- **Bagian pesan:** struk dan gelembung bertumpuk ke bawah, kemiringan dikurangi.
- **Kartu fitur besar:** HP di bawah teks, bagian bawahnya terpotong tepi kartu seperti di desktop.
- **Kartu cicilan:** HP pindah ke bawah teks, tidak menimpa teks.
- **≤480px:** daftar nada, kelompok waktu, dan pasangan arah menjadi satu kolom; teksnya boleh patah baris.
- **H1** memakai `clamp(28px, 8.2vw, 48px)` supaya tiap barisnya muat satu baris sampai lebar 340px. Di desktop `clamp(34px, 3.9vw, 50px)`, lebih kecil dari papan (58px), karena di 1280px "Tagih tanpa canggung" patah baris.
- **Nominal** ditulis dengan spasi tak-putus (`Rp&nbsp;500.000`) supaya "Rp" tidak terpisah dari angkanya.
- Diuji di 360, 768, dan 1280px.

---

## 8. Nada bahasa

Suara antarmuka (panduan v1.3 halaman 11): "Anda", tenang, menyatakan keadaan tanpa menilai. Tanpa emoji, tanpa tanda seru.

**Aturan dari revisi pemilik:**
- Istilah Inggris yang umum dipakai apa adanya: **backup, cloud, preview, login**. Jangan di-Indonesia-kan.
- "Login" dan "buat akun", bukan "pendaftaran".
- Jangan menyebut jumlah template; pakai "banyak variasi".
- Jangan menyebut Google Drive atau "server kami" (suatu saat aplikasi akan memakai cloud).
- Jangan menulis "gratis" (belum diputuskan) atau "Android" di ajakan.
- Hindari koma yang menimbulkan jeda janggal di judul.

### 8.1 Fakta yang boleh diklaim

| Klaim di halaman | Sumber |
|---|---|
| Catat utang dan piutang dua arah | Layar daftar |
| Kelompok Perlu ditindak, Masih ada waktu, Tanpa tenggat, Lunas | Layar daftar |
| Akan diterima dan Harus dibayar selalu terpisah | Layar daftar |
| Banyak variasi template untuk menagih dan mengakui utang; nada Resmi, Santai, Sopan | `TEMPLATE-PESAN.md`, `layar_pesan.dart` |
| Isi struk dan gelembung | `susun_pesan.dart` dengan data contoh |
| Lihat preview, bagikan lewat WhatsApp, isi bisa diubah sebelum dikirim | Layar pesan, menu berbagi Android |
| Cicilan dicatat, sisa dihitung, pindah ke Lunas | Layar detail |
| Notifikasi pagi hari saat jatuh tempo, dan sekali lagi bila tanggalnya lewat | `jadwal_pengingat.dart`: pukul 09.00 hari-H, susulan 3 hari kemudian |
| Tanpa login, tanpa buat akun, tanpa nomor telepon | Deskripsi Play Store |
| Catatan disimpan di HP; mencatat dan menyiapkan pesan jalan tanpa sinyal | KEPUTUSAN-PRODUK, kebijakan privasi |
| Satu file backup ke cloud milik pengguna atau folder di HP; memulihkan menggabungkan, tidak menimpa | Layar backup, KEPUTUSAN-PRODUK bagian 6 |
| Pesan tidak terkirim otomatis | Layar pesan (memakai menu berbagi) |

**Klaim yang akan berubah:** "Tanpa login, tanpa buat akun" harus ditinjau saat login masuk di v1.x.

---

## 9. Gerak

- Hover, tekan, dan fokus: perubahan warna, tepi, atau bayangan 150ms.
- Kemiringan struk, HP, dan stiker statis. Tanpa animasi saat menggulir.
- Gulir halus saat menekan tautan menu dan "Lihat cara kerja".
- Panah di tombol "Lihat cara kerja" bergeser 3px ke kanan saat hover.
- Efek tekan (mengecil ke 97%) hanya pada dua baki lencana dan tombol "Lihat cara kerja". Tautan teks, logo, dan pertanyaan FAQ tidak diberi efek tekan.
- FAQ: panah di kanan berputar dan jawaban muncul pelan (250ms). Tinggi jawaban ikut bergeser hanya di browser yang mendukung `interpolate-size` (Chrome, termasuk Android); browser lain membuka langsung.
- `prefers-reduced-motion: reduce` mematikan semua transisi.

---

## 10. Mode gelap

**Tidak ada.** Situs selalu tampil terang (`color-scheme: light`), termasuk `kebijakan-privasi.html` dan `penguji.html`. Papan 1B hanya didesain terang dan sudah punya bagian gelap sendiri. Diputuskan pemilik 18 November 2026; revisi 2 dulu mengikuti setelan HP.

---

## 11. Kendali

| Kendali | Keadaan |
|---|---|
| Baki lencana | Hover: baki terangkat sedikit (bayangan membesar). Fokus: cincin 3px Hutan Terang di luar baki. Lencananya tidak berubah |
| Tombol "Lihat cara kerja" | Hover: tepi putih penuh. Fokus: cincin 3px Hutan Terang |
| Menu kepala dan tautan di latar gelap | Hover: garis bawah. Fokus: cincin 3px Hutan Terang |
| Tautan di latar terang | Garis bawah; fokus: cincin 3px Hutan |
| Pertanyaan FAQ | Seluruh baris bisa diketuk (min. 44px); penanda buka-tutup terlihat; fokus: cincin 3px Hutan |

Fokus keyboard tidak pernah dihapus tanpa pengganti.

---

## 12. Aksesibilitas, performa, dan pemeriksaan

Aturan gaya antislop tidak berlaku. Pemeriksaan teknis berikut tetap wajib sebelum diserahkan:

- Kontras WCAG AA (bagian 3.4), diukur dengan skrip pada halaman jadi.
- Sasaran ketuk minimal 44px.
- Tanpa geser ke samping di 360, 768, dan 1280px.
- Lighthouse mobile dan desktop.
- Tidak ada testimoni, angka pengguna, rating, atau klaim di luar bagian 8.1.
- `lang="id"`, satu H1, tingkat judul tidak melompat, landmark `header` · `nav` · `main` · `footer`, `alt` pada semua gambar, hiasan `aria-hidden`.
- Tanpa JavaScript. FAQ memakai `<details>`.
- Tanpa langkah build: folder siap unggah ke Cloudflare Pages apa adanya.
- Tautan antarhalaman tanpa `.html` (`kebijakan-privasi`, `./`). Cloudflare Pages mengalihkan alamat `.html` ke alamat tanpa akhiran itu, jadi alamat kanonis dan tautan memakai bentuk akhirnya. Akibatnya server lokal `python3 -m http.server` tidak bisa membuka tautan ke subhalaman; buka berkas `.html`-nya langsung.
- `404.html` untuk alamat yang tidak ada (tanpanya Cloudflare menampilkan beranda untuk semua alamat, termasuk `robots.txt`). Alamat di dalamnya dimulai dari `/` karena halaman ini juga tampil di alamat bertingkat.
- `robots.txt` membolehkan semua. `penguji.html` tetap `noindex`.

Laporan audit di `anti-slop/` adalah untuk revisi 1 dan 2, disimpan sebagai riwayat.

---

## 13. Yang tidak masuk situs

Testimoni, angka pengguna, rating, logo "dipercaya oleh", harga, emoji, bingkai HP bermerek, status bar karangan, dan daftar "yang tidak boleh masuk" panduan v1.3 (dompet, koin, lambang Rp, perayaan).

**Juga dihapus atas keputusan pemilik:** keterangan "Saat ini dalam uji tertutup" dan kalimat merek dagang Google di kaki halaman. Catatan: pedoman lencana Google Play meminta kalimat merek dagang itu dicantumkan. Kalau Google mempermasalahkannya, kalimat itu dikembalikan ke kaki halaman.

**Belum dikerjakan:** gambar Open Graph masih desain revisi 2. Bisa disamakan dengan revisi 3 sebagai pekerjaan terpisah.

---

## 14. Keputusan

1. **CTA.** Lencana menuju `https://play.google.com/apps/testing/id.utangkumu.app` (uji tertutup), tanpa keterangan uji. Saat terbit: ganti ke `https://play.google.com/store/apps/details?id=id.utangkumu.app` (`CATATAN-TERTUNDA.md` A34 di repo aplikasi).
2. **Domain.** Tanpa domain kustom; alamat kanonis `utangkuutangmu.pages.dev`.
3. **Kontak.** Surel dan WhatsApp PT Digital Insight Indonesia di kaki halaman, sesuai yang diberikan pemilik.
4. **Revisi 2 disimpan** di commit `cf04595` sebelum diganti.
5. **Mode gelap** tidak ada (bagian 10).
6. **Antislop:** aturan gaya tidak berlaku, pemeriksaan teknis tetap (bagian 12).

Dokumen ini ikut terbit karena output Cloudflare adalah root repo, dan repo-nya publik di GitHub. Jangan menulis data pribadi di sini. Surel dan nomor WhatsApp di atas adalah kontak perusahaan yang memang ditampilkan di halaman.
