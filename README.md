# HUNIDAYA v1.3.2 (PWA)

*Pahami kemampuanmu, rencanakan rumahmu.*

Aplikasi cek kesiapan cicilan rumah bagi pekerja berpenghasilan tidak tetap. Semua perhitungan berjalan di perangkat pengguna. Tidak ada akun, tidak ada server, dan tidak ada data yang dikirim.

## Isi folder

| File | Fungsi |
|---|---|
| `index.html` | Aplikasi lengkap (satu file) |
| `manifest.webmanifest` | Nama, warna, dan ikon saat dipasang di ponsel |
| `sw.js` | Service worker: aplikasi tetap terbuka tanpa internet |
| `icons/` | Ikon 192, 512, maskable 512, dan ikon Apple 180 |

## Cara terbit di GitHub Pages (sekitar 5 menit)

1. Buat repositori baru, misalnya `hunidaya`, di akun atau organisasi GitHub Anda.
2. Unggah **seluruh isi folder ini** (bukan foldernya) ke cabang `main`.
3. Buka **Settings > Pages**, pilih **Deploy from a branch**, cabang `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu 1 sampai 2 menit. Alamatnya akan berbentuk `https://<nama-akun>.github.io/hunidaya/`.

Service worker hanya berjalan di alamat `https://` atau `localhost`. Membuka `index.html` langsung dari folder tetap bisa dipakai, tetapi tanpa fitur pasang dan offline.

## Cara pasang di ponsel

- **Android (Chrome):** buka alamatnya, ketuk menu titik tiga, pilih **Tambahkan ke layar utama** atau **Instal aplikasi**.
- **iPhone (Safari):** buka alamatnya, ketuk tombol **Bagikan**, pilih **Tambahkan ke Layar Utama**.

Setelah dibuka sekali dengan internet, aplikasi tetap bisa dipakai tanpa internet.

## Fitur baru di v1.3

Versi 1.3.1 mengganti nama dari JEJAK CICIL menjadi HUNIDAYA. Versi 1.3.2 mengganti kunci penyimpanan hasil uji pengguna menjadi `hunidaya.uji.v1`; sesi lama dipindahkan otomatis saat aplikasi pertama kali dibuka, lalu kunci lama dihapus.

- **Putar demo:** menjalankan contoh Bu Rina melewati 5 langkah dalam sekitar 77 detik. Tombol Jeda, Kembali, Lanjut, dan Selesai tersedia; tombol Esc menghentikan demo. Alamat yang diakhiri `#demo` langsung memutar demo, berguna untuk merekam video.
- **Uji pengguna:** 5 pertanyaan sebelum dan sesudah memakai aplikasi (skala 1 sampai 5), ditambah satu pertanyaan kemudahan dan dua isian singkat. Hasil disimpan di perangkat dengan kode peserta tanpa nama, lalu bisa diunduh sebagai `.csv` atau `.json`.
- **Bagikan ringkasan:** teks ringkasan tanpa nama lewat menu bagikan ponsel atau salin, serta kode QR yang bisa dipindai pendamping. Keduanya baru aktif setelah pengguna mencentang persetujuan.

## Memperbarui aplikasi

Jika `index.html` diubah, naikkan juga nama cache di baris kedua `sw.js` (misalnya `hunidaya-v1.4`). Tanpa itu, ponsel yang sudah memasang aplikasi bisa tetap memakai versi lama.

## Lisensi pihak ketiga

Pembuat kode QR: *QR Code Generator for JavaScript*, Kazuhiko Arase, lisensi MIT (tercantum di dalam `index.html`).
