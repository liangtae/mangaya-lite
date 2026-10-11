# Panduan Kontribusi

Terima kasih sudah tertarik berkontribusi ke **Mangaya Lite**! 🌸

## Cara berkontribusi
1. Fork repo ini
2. Buat branch: `git checkout -b fitur/nama-fitur`
3. Edit `index.html` (seluruh aplikasi ada di satu file)
4. Uji manual di browser: impor CBZ, PDF, dan gambar; coba tema terang/gelap dan layar ponsel
5. Commit dengan pesan jelas, mis. `feat: dukungan CBR` atau `fix: progres baca tidak tersimpan`
6. Buka Pull Request dan jelaskan perubahanmu

## Prinsip proyek
- **Satu file, tanpa build step**, supaya mudah dipakai dan dibagikan
- **Tanpa backend dan tanpa pelacakan**, semua data tetap lokal
- Hindari dependensi baru kecuali benar-benar perlu; pin versi library di CDN
- Jangan menyertakan komik berhak cipta di repo (termasuk untuk pengujian)

## Melaporkan bug
Sertakan: browser & versi, perangkat, format file (CBZ/PDF/gambar), langkah mengulang, dan pesan error di konsol bila ada.
