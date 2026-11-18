# DESIGN.md · Situs Utangku Utangmu

| | |
|---|---|
| **Status** | Disetujui pemilik produk, 13 November 2026. Revisi 2 disetujui 17 November 2026 |
| **Berlaku untuk** | Landing page (satu halaman), ikut dipakai `kebijakan-privasi.html` dan `penguji.html` |
| **Dial** | ENERGY 2 / RHYTHM 3 / MOTION 1 |

Dokumen ini menurunkan arah visual situs dari referensi yang sudah ada. Tidak ada nilai warna, huruf, atau radius baru yang dikarang di sini. Tambahan khusus web hanya dua jarak antarbagian (64 dan 96), karena skala aplikasi berhenti di 40.

**Revisi 2 (17 November 2026).** Versi pertama dinilai pemilik terlalu polos, kurang bervariasi, dan terasa seperti tumpukan teks. Penyebabnya dial yang dikunci terlalu rendah (ENERGY 1 / RHYTHM 2). Revisi 2 menaikkan dial, memangkas teks dari ±630 menjadi ±300 kata, menambah demo pesan interaktif, bingkai HP, lencana resmi Google Play, dan menyusun halaman menjadi tiga babak yang menyambung.

---

## 0. Sumber, dan mana yang menang

| Urutan | Sumber | Dipakai untuk |
|---|---|---|
| 1 | `docs/panduan-merek-utangku-utangmu-v1.3.svg` | Konsep, mark, nama, warna, tipografi, nada suara, larangan |
| 2 | `docs/BRAND-GUIDELINE.md` (pelengkap v1.3) | Privasi sebagai merek, kata ganti, aturan materi pemasaran (bagian 5) |
| 3 | Kanvas "Desain Utangku Utangmu", papan *Sistem desain* | Token lengkap termasuk mode gelap dan Latar Pratinjau |
| 4 | `docs/DESIGN-SYSTEM.md` + `lib/tampilan/token_desain.dart` | Radius, jarak, garis, komponen |
| 5 | Layar aplikasi yang dirender dari kode (`test/aset/buat_tangkapan_layar.dart`) | Kebenaran tentang aplikasi. Kalau dokumen dan layar berbeda, layar yang benar |
| 6 | `lib/pesan/susun_pesan.dart`, `TEMPLATE-PESAN.md`, `deskripsi-play-store.md` | Isi pesan di demo dan fakta yang boleh diklaim |
| 7 | Pedoman lencana Google Play | Bentuk dan pemakaian tombol unduh |

Kalau dua sumber berselisih, yang lebih atas menang. Pedoman Google Play berlaku penuh untuk lencananya sendiri.

---

## 1. Design Read

> Halaman produk untuk pengguna Android di Indonesia yang punya utang atau piutang dengan teman, keluarga, atau rekan kerja, dalam bahasa visual **pencatat resmi yang datar, tapi hidup**, dial ENERGY 2 / RHYTHM 3 / MOTION 1.

- **ENERGY 2.** Judul besar, dua HP bertumpuk di hero, panah raksasa, dan pita gelap memberi tenaga. Tetap tanpa bayangan, gradien, atau perayaan, supaya kesan pencatat resmi yang dipinjam pesan tidak hilang.
- **RHYTHM 3.** Setiap bagian punya susunan sendiri: hero terbelah, pernyataan besar dengan panah, demo interaktif, deret tiga HP, baris buku catatan. Bagian-bagian itu diikat menjadi **tiga babak** supaya bervariasi tanpa terputus.
- **MOTION 1.** Hanya perubahan keadaan pada hover, tekan, fokus, dan pergantian pilihan demo (150ms). Tanpa animasi saat menggulir. Aplikasinya tanpa animasi perayaan; situsnya juga.

---

## 2. Konsep yang dibawa ke situs

**Pihak ketiga yang netral.** Situs berbicara dengan suara yang sama seperti aplikasi: menyatakan keadaan tanpa menilai. Ia tidak membujuk, tidak berjanji lebih dari yang ada di aplikasi.

**Dua arah yang setara.** Setiap kali kedua arah disebut, keduanya tampil **berdampingan dengan bobot sama** (bertumpuk menyiratkan yang atas lebih utama). Di HP keduanya bertumpuk karena lebar, dengan ukuran yang sama.

**Tunjukkan, jangan jelaskan.** Pembeda produk adalah pesannya, jadi pesan itu dipertontonkan lewat demo yang bisa dicoba, bukan diterangkan dengan paragraf.

---

## 3. Warna

### 3.1 Peran di situs

| Token | Terang | Gelap | Peran di situs |
|---|---|---|---|
| Hutan | `#123F2E` | `#123F2E` (pita tetap) | Pita hero dan babak 3, pilihan demo yang aktif, tautan, cincin fokus di latar terang |
| Hutan Terang | `#8FC7AC` | `#8FC7AC` | Teks pendamping dan cincin fokus di pita gelap, motif panah (13%), pilihan demo aktif di mode gelap |
| Hutan Halus | `#E6EFEA` | `#16241D` (Merek Halus) | Latar babak 2 (demo dan deret) |
| Hutan Sekunder | `#7D958C` | sama | Kata kedua wordmark di latar terang; garis rambut dan cincin hover lencana di pita gelap (3.69:1, non-teks). Tidak pernah untuk teks biasa |
| Kertas | `#F1F4F1` | `#0E1014` | Latar halaman; area status kosong di layar HP |
| Permukaan | `#FFFFFF` | `#1A1D24` | Kotak pratinjau pesan, tombol pilihan demo |
| Latar Pratinjau | `#EDEFF2` | `#15181E` | Cadangan untuk kotak isi pesan |
| Tinta | `#171A21` | `#E8EAEE` | Teks utama; nilai Tinta terang juga dipakai sebagai warna bezel HP |
| Redup | `#5C636F` | `#969DAA` | Teks pendamping, keterangan |
| Garis | `#E2E5EA` | `#2C313A` | Garis rambut; nilai Garis gelap juga dipakai sebagai bezel HP di mode gelap |
| Teks di atas Hutan Terang | `#0B1A13` | sama | Label pilihan demo aktif di mode gelap |

### 3.2 Warna yang sengaja tidak dipakai di luar layar aplikasi

**Lumut, Bata, dan Kunyit** hanya muncul **di dalam** layar aplikasi di dalam bingkai HP (warna arah hanya untuk data). Panah ↙ ↗ di situs memakai Hutan atau Hutan Terang. **Gagal** tidak dipakai; situs statis ini tidak punya keadaan gagal. Warna lencana Google Play (hitam dan warna logo Play) milik Google dan tidak dihitung sebagai bagian palet.

### 3.3 Satu aksen

Aksen yang disengaja hanya **Hutan Terang** di pita gelap: teks pendamping, motif panah, cincin fokus. Inti palet: Kertas, Tinta, Hutan, dengan Hutan Halus sebagai latar babak 2.

### 3.4 Kontras

Diukur pada halaman jadi (17 November 2026): teks terendah **5.16:1** di mode terang dan **5.9:1** di mode gelap. Pasangan kunci: putih di atas Hutan 11.82, Hutan Terang di atas Hutan 6.16, Redup di atas Kertas 5.46, Redup di atas Hutan Halus 5.16, Hutan di atas Kertas 10.67. Hutan Sekunder di atas Hutan 3.69: gagal untuk teks, jadi hanya dipakai untuk garis dan cincin.

---

## 4. Tipografi

| Huruf | Dipakai untuk | Alasan |
|---|---|---|
| **Plus Jakarta Sans** 400 · 600 · 700 · 800 | Semua judul, isi, label, tombol, pesan gaya santai dan sopan | Huruf antarmuka aplikasi, karya Tokotype (foundry Indonesia) |
| **IBM Plex Mono** 400 · 600 | **Hanya** isi pesan gaya resmi di demo | Panduan v1.3 halaman 10: otoritas pencatat resmi. Aturan CLAUDE.md nomor 10 |

Kedua huruf di-*host* sendiri (`.woff2`, subset Latin) dan di-*preload*, tidak dimuat dari Google Fonts: lebih cepat, dan situs yang menjual privasi tidak mengirim alamat IP pengunjung ke Google hanya untuk huruf.

### 4.1 Skala web

| Peran | Ukuran | Bobot |
|---|---|---|
| H1 (hero) | `clamp(2.25rem, 7vw, 4rem)`, tinggi baris 1.05 | 800 |
| H2 (judul bagian, **satu ukuran di semua bagian**) | `clamp(1.75rem, 4.5vw, 3rem)` | 800 |
| Pernyataan dua arah | `clamp(1.25rem, 2.6vw, 1.625rem)` | 700 |
| H3 | 1.25rem | 700 |
| Pengantar bagian | 1.1875rem, tinggi baris 1.55 | 400 |
| Isi | 1.0625rem (17px), tinggi baris 1.6 | 400 |
| Keterangan | 0.9375rem | 400 |
| Isi pesan resmi | 0.9375rem mono (0.8125rem di ≤400px) | 400, kop 600 |

Tanpa label huruf besar berjarak lebar di atas judul. Judul bagian adalah kalimat yang menyatakan sesuatu.

---

## 5. Bentuk

**Datar.** Tanpa bayangan, tanpa elevasi, tanpa gradien, tanpa blur. Pemisah memakai garis rambut 1px. BRAND-GUIDELINE bagian 5 membolehkan bayangan dan pendar di materi pemasaran; situs ini tidak memakainya. Yang dipakai dari bagian itu hanya **panah hiasan** di pita gelap.

| Elemen | Nilai |
|---|---|
| Radius kolom / tombol pilihan demo | 11 |
| Radius kotak pratinjau pesan | 14 |
| Garis | tipis 1 · tegas 1.6 (tepi tombol pilihan) |
| Jarak | 4 · 8 · 12 · 16 · 20 · 24 · 32 · 40, ditambah **64 · 96** |
| Tepi atas-bawah babak, dan jarak antarbagian di dalam babak | 64px di HP, 96px mulai 900px |
| Tepi kiri-kanan | 16px di bawah 360px, 20px selebihnya |
| Lebar isi maksimal | 1120px; kolom teks 48 sampai 60 karakter |

Bukan bentuk pil. Tidak ada kotak di dalam kotak, tidak ada tombol di dalam kotak. Satu-satunya kotak adalah pratinjau pesan.

### 5.1 Kendali

| Kendali | Rupa | Keadaan |
|---|---|---|
| **Lencana Google Play** (hero dan penutup) | Gambar resmi "Dapatkan di Google Play", tinggi 64px, **tidak diubah** | Hover: cincin 2px Hutan Sekunder di luar lencana. Tekan: cincin 3px putih. Fokus: cincin 3px Hutan Terang. Lencananya sendiri tidak berubah |
| **Pilihan demo** (radio) | Permukaan, tepi 1.6, radius 11, tinggi 48px | Aktif: isi Hutan, teks putih (gelap: Hutan Terang, teks `#0B1A13`). Hover: tepi warna tautan. Tekan: latar Hutan Halus. Fokus: cincin 3px |
| **Tautan** | Garis bawah 1px | Hover 2px, tekan 3px |

Fokus keyboard tidak pernah dihapus tanpa pengganti.

---

## 6. Gambar dan mark

### 6.1 Layar aplikasi dalam bingkai HP

**Layar dirender dari kode aplikasi pada ukuran layar penuh**, bukan dipotong dari gambar toko: 1080 × 2340 piksel (Samsung SM-M215F, HP rujukan proyek, 411 × 891 titik), memakai generator tangkapan layar toko yang disalin dengan ukuran itu dan tanpa bingkai jualan. Gambar toko di `docs/aset-toko/` tidak disentuh. Isi layar tidak disunting.

**Bingkai HP Android generik**, dibuat dengan CSS:
- Proporsi layar 9:19,5 mengikuti HP Android umum; layar yang menyesuaikan bingkai, bukan sebaliknya.
- Bezel tipis rata (`#171A21`, mode gelap `#2C313A`), sudut membulat.
- Kamera berlubang di **area status yang dibiarkan kosong** (warna Kertas). Tanpa jam, sinyal, atau baterai karangan.
- Bukan model bermerek (bukan iPhone, bukan Pixel), datar, tanpa bayangan atau kilap.

Pemakaian:
- **Hero:** dua HP bertumpuk dan dimiringkan (daftar di belakang, pesan resmi di depan), dipisah garis Hutan 3px, bukan bayangan.
- **Deret babak 2:** tiga HP berjajar (daftar telat, detail, backup), sama tinggi; di bawah 600px menjadi baris HP 112px dengan teks di kanan.

Berkas: `gambar/hp/*.webp`, lebar 300/450/600 dengan `srcset`, `width`/`height` tertulis. Hero memakai `fetchpriority="high"`, sisanya `loading="lazy"`. Setiap gambar punya `alt` yang menjelaskan isinya.

### 6.2 Mark dan nama

- Mark dari `docs/aset-toko/mark-utangku-utangmu.svg`, tidak digambar ulang. Di pita Hutan: versi satu warna terang, nama putih kedua katanya.
- Ruang bebas setinggi satu bilah. Tidak dibingkai, tidak diputar, tidak berbayang.
- Favicon dari `ikon-play-store-512.png`; gambar Open Graph dari `grafik-unggulan-1024x500.png`, dipotong ke 1200 × 630.

### 6.3 Ikon, panah, dan lencana

- **Tanpa pustaka ikon.**
- **Panah ↙ ↗** dipakai sebagai: teks di tombol pilihan demo; SVG besar di bagian masalah (Hutan); motif latar di pita gelap (Hutan Terang 13%, tidak masuk ruang bebas mark). Panah adalah isi produk, bukan hiasan acak.
- **Lencana Google Play** `gambar/google-play-id.png` diunduh dari `play.google.com` (versi bahasa Indonesia, 646 × 250) dan disimpan sebagai sumber. Yang tampil `google-play-id-330.webp`: diperkecil proporsional ke 330px (dua kali ukuran tampil) dalam WebP lossless, pikselnya tidak diubah. Aturan: tidak diubah warna atau bentuknya, ukuran tidak terlalu kecil, ada ruang bebas di sekelilingnya, dan kaki halaman memuat kalimat "Google Play dan logo Google Play adalah merek dagang Google LLC."

---

## 7. Motif identitas

1. **Demo pesan yang bisa dicoba.** Dua pilihan (arah: menagih/berutang; nada: resmi/santai/sopan), enam pesan. Isinya mengikuti persis keluaran `lib/pesan/susun_pesan.dart` dengan data contoh berlabel. Gaya resmi tampil mono, gaya santai dan sopan tampil huruf biasa, seperti di aplikasi.
2. **Dua arah berdampingan** dengan panah raksasa ↙ ↗.
3. **Baris buku catatan** untuk fakta privasi: label di kiri, nilai di kanan, garis rambut.
4. **Panah di pita gelap**, motif yang sama dengan gambar Play Store, sehingga situs dan halaman toko terbaca satu keluarga.

---

## 8. Nada bahasa

**Suara antarmuka** (panduan v1.3 halaman 11): "Anda", sistematis, tenang, menyatakan keadaan tanpa menilai.

- Tanpa emoji, tanpa tanda seru, tanpa tanda pisah panjang.
- Ejaan baku **utang**; **hutang** sekali saja di meta description.
- Judul menyatakan fakta, bukan janji atau seruan.
- Menyebut kedua arah.
- **Kalimat penyambung antarbagian**, supaya halaman terbaca sebagai satu cerita: "Yang berat … membicarakannya" → "Kalimatnya biar aplikasi yang menyusun" → "Sementara itu, catatannya tetap rapi" → "Catatan Anda tinggal di HP Anda" → "Mulai dari satu catatan".

### 8.1 Fakta yang boleh diklaim, dan sumbernya

| Klaim | Sumber |
|---|---|
| Catat utang dan piutang dua arah | Layar daftar, deskripsi Play Store |
| Daftar dikelompokkan menurut waktu: Perlu ditindak, Masih ada waktu, Tanpa tenggat, Lunas | Layar daftar |
| 10 template; tiga nada Resmi, Santai, Sopan; untuk menagih dan mengakui utang | `TEMPLATE-PESAN.md`, `layar_pesan.dart` |
| Isi keenam pesan di demo | `susun_pesan.dart` (data contoh, dilabeli) |
| Format resmi menyesuaikan tanggal | `layar_pesan.dart` (urgensi ringan, standar, tegas) |
| Pesan bisa diubah di aplikasi chat sebelum dikirim | Layar pesan |
| Cicilan dicatat, sisa dihitung, pindah ke Lunas | Layar detail, deskripsi Play Store |
| Pengingat pagi hari saat jatuh tempo | Deskripsi Play Store |
| Tanpa pendaftaran, tanpa nomor telepon | Deskripsi Play Store |
| Mencatat dan menyiapkan pesan tanpa sinyal; mengirim butuh sinyal | KEPUTUSAN-PRODUK, kebijakan privasi |
| Backup satu file ke Google Drive atau folder mana pun; memulihkan menggabungkan | Layar backup |
| Yang dikirim hanya data pemakaian dan laporan crash, tanpa isi catatan | Kebijakan privasi |
| Saat ini dalam uji tertutup | `ROADMAP.md` |

### 8.2 Yang tidak boleh ditulis

Jumlah pengguna, rating, unduhan, testimoni. "Backup otomatis". "Terenkripsi". "Tidak memakan kuota". "Pesan resmi yang sah / terverifikasi". "Berterima kasih" sebagai jenis pesan. Apa pun tentang pinjaman online atau kredit.

---

## 9. Komposisi: tiga babak

Tujuh blok warna di versi pertama terasa seperti tujuh halaman. Revisi 2 mengikatnya menjadi tiga babak; di dalam satu babak tidak ada potongan warna.

| Babak | Latar | Bagian | Susunan |
|---|---|---|---|
| **1. Masalah** | Pita Hutan → Kertas | Hero; Masalah | Hero: teks kiri, dua HP bertumpuk kanan, lencana + "Saat ini dalam uji tertutup.", motif panah. Masalah: judul, konteks satu baris, dua pernyataan besar berdampingan dengan panah raksasa, kalimat jawaban di bawah garis rambut |
| **2. Produk** | Hutan Halus, menyambung | Demo pesan; Deret fitur | Demo: pilihan di kiri, pratinjau di kanan, kalimat alur ("catat, pilih nada, bagikan") di bawah pilihan. Deret: tiga HP berjajar dengan judul dan satu kalimat |
| **3. Kepercayaan dan ajakan** | Pita Hutan, menyambung | Privasi; Penutup | Privasi: judul besar kiri, baris buku catatan kanan. Penutup: dipisah garis rambut Hutan Sekunder, judul, lencana + keterangan uji. Motif panah |

Kaki halaman di Kertas: penerbit, `nav` (kebijakan privasi, surel bantuan), kalimat merek dagang Google.

**Breakpoint:** 600px (hero dua kolom, deret tiga kolom), 820px (dua arah dan demo berdampingan, privasi dua kolom), 900px (jarak 96px, HP hero lebih besar).

**Navigasi:** tidak ada menu di kepala halaman; kepala hanya mark + nama.

**Halaman lain:** `kebijakan-privasi.html` dan `penguji.html` memakai `gaya.css` yang sama; isinya tidak berubah oleh revisi 2.

---

## 10. Gerak

- Hover, tekan, fokus, dan pergantian pilihan demo: perubahan warna latar/tepi 150ms.
- Tanpa animasi saat menggulir, parallax, atau animasi melayang. Kemiringan HP di hero statis.
- `prefers-reduced-motion: reduce` mematikan semua transisi.

---

## 11. Mode gelap

Situs mengikuti setelan perangkat (`prefers-color-scheme`) dengan token gelap dari papan Sistem desain, tanpa tombol ganti tema, sama seperti aplikasinya. Pita Hutan tetap Hutan; layar aplikasi di dalam bingkai tetap versi terang. Ini pengecualian antislop R-21 yang diputuskan pemilik (bagian 15).

---

## 12. Aksesibilitas dan performa

- Kontras WCAG AA di kedua mode (bagian 3.4).
- Fokus keyboard terlihat di semua kendali; urutan Tab mengikuti urutan baca; pilihan demo bisa diganti dengan tombol panah keyboard.
- Sasaran ketuk minimal 44px (pilihan demo 48px, lencana 64px).
- `alt` pada semua gambar; hiasan SVG `aria-hidden`; panah di bagian masalah punya teks khusus pembaca layar.
- `lang="id"`, satu H1, tingkat judul tidak melompat, landmark `header` · `main` · `nav` · `footer`.
- Tanpa horizontal scroll di 360, 600, 768, 820, dan 1280px.
- **Tanpa JavaScript.** Demo berganti lewat CSS `:has()`; browser yang belum mendukungnya tetap menampilkan pesan resmi menagih tanpa tombol pilihan.
- Tanpa langkah build: folder siap unggah ke Cloudflare Pages apa adanya.

---

## 13. Yang tidak masuk situs

Testimoni, angka pengguna, rating, logo "dipercaya oleh", FAQ, harga, bento grid, kartu fitur seragam, bagian "cara kerja" bernomor, gradien, bayangan, emoji, ikon pustaka, ilustrasi, bingkai HP bermerek, status bar karangan, dan semua yang ada di daftar "yang tidak boleh masuk" panduan v1.3 (dompet, koin, lambang Rp, perayaan).

---

## 14. Keputusan atas pertanyaan terbuka

1. **CTA (17 Nov).** Lencana resmi Google Play dengan keterangan "Saat ini dalam uji tertutup."; tautan ke `play.google.com/apps/testing/id.utangkumu.app`. Saat terbit: tautan diganti ke halaman toko dan keterangan dihapus (`CATATAN-TERTUNDA.md` A34 di repo aplikasi).
2. **Domain.** Tanpa domain kustom; alamat kanonis `utangku-utangmu.pages.dev`.
3. **Kanvas "Utangku Utangmu, Landing Page".** Diabaikan.

## 15. Keputusan terhadap aturan antislop

Diputuskan pemilik produk, 17 November 2026.

| Hal | Aturan antislop | Keputusan |
|---|---|---|
| Lencana Google Play saat aplikasi masih uji tertutup | R-38 (konten nyata atau placeholder jujur) | **Sesuai aturan:** lencana + keterangan "Saat ini dalam uji tertutup." |
| Bagian "Tiga langkah" | R-05 (pola template tiga langkah) | **Sesuai aturan:** bagian dihapus; alur disebut di demo pesan |
| Mode gelap tanpa tombol ganti tema | R-21 | **Pengecualian:** mengikuti setelan HP, seperti aplikasinya |
| Keadaan hover/tekan lencana Google Play | R-39 vs pedoman Google (lencana tidak boleh diubah) | **Sesuai keduanya:** cincin di luar lencana |

Dokumen ini dan folder `anti-slop/` ikut terbit karena output Cloudflare adalah root repo, dan repo-nya publik di GitHub. Jangan menulis nama orang atau data pribadi di sini.
