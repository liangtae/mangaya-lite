<div align="center">

# 📚 Mangaya Lite

**Pembaca komik / manga offline-first dalam satu file HTML — tanpa server, tanpa instalasi, tanpa akun.**

[![License: MIT](https://img.shields.io/badge/License-MIT-e8758a.svg)](LICENSE)
![Single file](https://img.shields.io/badge/single--file-HTML-68a37f)
![No backend](https://img.shields.io/badge/backend-none-7482d6)
![Bahasa](https://img.shields.io/badge/UI-Bahasa%20Indonesia-f08a5d)

[Demo Langsung](https://USERNAME.github.io/mangaya-lite/) · [Laporkan Bug](../../issues) · [Usul Fitur](../../issues)

</div>

---

## ✨ Tentang

**Mangaya Lite** adalah rak komik pribadi yang berjalan sepenuhnya di browser. Impor file `.cbz`, `.zip`, `.pdf`, atau kumpulan gambar, lalu baca dengan pembaca yang nyaman: mode 1 halaman, 2 halaman, atau gulir vertikal, lengkap dengan arah baca manga (kanan → kiri).

Seluruh koleksi, rating, tag, dan progres baca disimpan **lokal di perangkatmu** (IndexedDB + localStorage). Tidak ada yang diunggah ke server mana pun.

## 🚀 Fitur

### Rak koleksi
- Impor **CBZ / ZIP, PDF**, dan gambar lepas (JPG, PNG, WebP, GIF, AVIF, BMP)
- Impor banyak file sekaligus, termasuk **drag & drop**
- Deteksi duplikat otomatis saat impor
- Sampul dibuat otomatis dari halaman pertama
- Cari berdasarkan judul atau tag (tekan `/` untuk fokus ke kolom pencarian)
- Urutkan: terbaru ditambah, judul, rating, terakhir dibaca, ukuran, jumlah halaman
- Filter: semua, favorit ♥, belum dibaca, sedang dibaca, selesai
- Rating bintang 1–5, favorit, tag/kategori, dan ganti judul
- **Mode pilih banyak** untuk rating, tag, tandai dibaca, favorit, dan hapus massal
- Paginasi (12 / 24 / 48 / 96 per halaman) dan kartu **"Lanjutkan membaca"**

### Pembaca
- Mode **1 halaman**, **2 halaman** (dengan opsi sampul tunggal), dan **gulir vertikal**
- Arah baca **kanan → kiri** untuk manga
- Penyesuaian gambar: sesuai tinggi, lebar, layar, atau ukuran asli
- Zoom, layar penuh, slider halaman, dan lompat ke halaman
- Pengaturan jarak antar gambar pada mode gulir
- Progres baca tersimpan otomatis

### Tampilan & data
- Tema **otomatis / terang / gelap**
- 4 warna aksen: sakura, matcha, indigo, sunset
- Ukuran kartu bisa diatur, animasi kelopak sakura bisa dimatikan
- **Cadangan lengkap** (`.zip`, termasuk file komik) atau **cadangan ringan** (`.json`, metadata saja)
- Pulihkan cadangan kapan saja
- Responsif untuk ponsel (mendukung *safe-area* iOS/Android)

## ⌨️ Pintasan Keyboard

| Tombol | Fungsi |
|---|---|
| `/` | Fokus ke pencarian |
| `←` `→` | Halaman sebelumnya / berikutnya |
| `1` `2` `3` | Mode 1 halaman / 2 halaman / gulir |
| `+` `-` `0` | Perbesar / perkecil / reset zoom |
| `F` | Layar penuh |
| `Esc` | Tutup pembaca |

## 🛠️ Cara Pakai

### Opsi 1 — Langsung buka
1. Unduh `index.html` (atau clone repo ini)
2. Buka file tersebut di browser modern
3. Klik **＋ Impor** atau seret file komik ke jendela

```bash
git clone https://github.com/USERNAME/mangaya-lite.git
cd mangaya-lite
# buka index.html di browser, atau jalankan server lokal:
python3 -m http.server 8000
```

### Opsi 2 — GitHub Pages
Repo ini sudah menyertakan workflow deploy. Aktifkan di **Settings → Pages → Source: GitHub Actions**, lalu aplikasi tersedia di `https://USERNAME.github.io/mangaya-lite/`.

## 📦 Format yang Didukung

| Format | Status |
|---|---|
| `.cbz` / `.zip` berisi gambar | ✅ |
| `.pdf` | ✅ |
| Gambar lepas (JPG, PNG, WebP, GIF, AVIF, BMP) | ✅ (digabung otomatis menjadi satu judul) |
| `.cbr` / `.rar` | ❌ Belum didukung — konversi ke CBZ dulu |

## 🧱 Teknologi

- HTML, CSS, dan JavaScript murni (*vanilla*), semuanya dalam satu file
- [JSZip](https://stuk.github.io/jszip/) 3.10.1 untuk membaca arsip CBZ/ZIP dan membuat cadangan
- [PDF.js](https://mozilla.github.io/pdf.js/) 3.11.174 untuk membaca PDF (dimuat hanya saat dibutuhkan)
- IndexedDB untuk menyimpan file komik, localStorage untuk pengaturan
- Font: Zen Maru Gothic & Shippori Mincho (Google Fonts)

> ℹ️ Library dan font dimuat dari CDN, jadi kunjungan pertama membutuhkan koneksi internet. Setelah itu browser biasanya men-*cache*-nya. Untuk penggunaan benar-benar offline, unduh library tersebut dan arahkan tag `<script>` ke salinan lokal.

## 🔒 Privasi

- Tidak ada backend, akun, analitik, maupun pelacakan
- File komik **tidak pernah meninggalkan perangkatmu**
- Data tersimpan di browser yang dipakai. Menghapus data situs akan menghapus koleksi, jadi buat **cadangan** secara berkala lewat ⚙ Pengaturan

## ⚠️ Catatan Hak Cipta

Mangaya Lite hanyalah aplikasi pembaca dan **tidak menyertakan atau menyediakan konten komik apa pun**. Gunakan hanya untuk file yang kamu miliki secara sah atau yang berlisensi bebas.

## 🗺️ Rencana Pengembangan

- [ ] Dukungan CBR / RAR
- [ ] PWA (bisa dipasang & benar-benar offline)
- [ ] Koleksi / seri dan pengelompokan volume
- [ ] Bahasa antarmuka tambahan (English)

## 🤝 Berkontribusi

Kontribusi sangat diterima! Lihat [CONTRIBUTING.md](CONTRIBUTING.md) untuk panduannya.

## 📄 Lisensi

Dirilis di bawah lisensi [MIT](LICENSE).
