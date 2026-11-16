# HUNIDAYA v1.6.1 (PWA)

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

- **Putar demo:** menjalankan contoh Bu Rina melewati 5 langkah dalam 15 adegan, sekitar 105 detik. Tombol Jeda, Kembali, Lanjut, dan Selesai tersedia; tombol Esc menghentikan demo. Alamat yang diakhiri `#demo` langsung memutar demo, berguna untuk merekam video.
- **Bantuan istilah (v1.4):** tombol "Bantuan istilah" membuka kamus 39 istilah (FLPP, SBUM, KPP, DSR, plafon, SLIK, dan lainnya) dalam bahasa sehari-hari, bisa dicari dan dikelompokkan. Tanda tanya kecil di samping isian langsung membuka penjelasan istilah itu.
- **Tampilan buku kas (v1.6):** isi aplikasi tampil sebagai satu lembar seperti buku kas, dengan garis baris biru dan garis margin merah. Blok pembuka gelap tetap dipertahankan. Kotak hanya dipakai untuk status dan peringatan. Fungsi dan hitungan tidak berubah.
- **Pemasukan bersih (v1.6):** kolom catatan bulanan kini bernama "Pemasukan bersih", dengan tombol tanda tanya yang menjelaskan cara mengisinya untuk pedagang, pekerja lepas atau remote, dan karyawan, serta peringatan agar biaya bersama seperti internet tidak dicatat dua kali.
- **Harga rumah yang aman (v1.5):** di Langkah 3, aplikasi mencari harga rumah tertinggi yang masih berstatus Aman dan Waspada dengan data pengguna. Bila angkanya jauh di bawah batas wilayah, aplikasi menjelaskan penyebabnya (tabungan atau cicilan).
- **Rencana menuju Aman (v1.5):** kotak "bagaimana jika" untuk mencoba harga, tenor, uang muka, dan kemampuan menabung tanpa mengubah isian utama. Hasilnya: tambahan tabungan yang dibutuhkan dan perkiraan lama menabung, atau saran harga dan tenor bila cicilan yang terlalu besar. Usia lunas di atas 65 tahun diberi peringatan.
- **Rencana persiapan 30 hari (v1.5):** di Langkah 5, daftar langkah berurutan (bukti transaksi, NPWP, NIB, cek SLIK, menabung, ke bank) disusun dari jawaban pengguna. Bisa diunduh sebagai file kalender `.ics` setelah pengguna setuju.
- **Bacakan hasil (v1.5):** tombol "Bacakan" membacakan ringkasan dengan suara bahasa Indonesia di perangkat. Bila perangkat belum punya suara Indonesia, aplikasi memberi tahu cara memasangnya.
- **Mode pendamping (v1.5):** untuk kader, koperasi, atau petugas. Menyimpan banyak profil anggota dengan kode (tanpa nama) di perangkat pendamping, setelah anggota setuju. Tersedia tabel ringkas, rekap `.csv`, ekspor `.json`, dan hapus semua.
- **Uji pengguna:** 5 pertanyaan sebelum dan sesudah memakai aplikasi (skala 1 sampai 5), ditambah satu pertanyaan kemudahan dan dua isian singkat. Hasil disimpan di perangkat dengan kode peserta tanpa nama, lalu bisa diunduh sebagai `.csv` atau `.json`.
- **Bilah panduan uji (v1.6.1):** selama sesi uji, bilah gelap di bawah layar menunjukkan "langkah X dari 5" dengan tombol "Lanjut ke langkah berikutnya". Di Langkah 5 tombolnya menjadi "Isi jawaban akhir". Tombol contoh, demo, mode pendamping, dan cetak disembunyikan selama sesi agar peserta memakai datanya sendiri. Label "Uji berjalan" di atas bisa diketuk untuk kembali ke kuesioner. Kartu "Mulai sesi uji baru" kini memuat urutan empat tahap untuk pendamping.
- **Bagikan ringkasan:** teks ringkasan tanpa nama lewat menu bagikan ponsel atau salin, serta kode QR yang bisa dipindai pendamping. Keduanya baru aktif setelah pengguna mencentang persetujuan.

## Memperbarui aplikasi

Jika `index.html` diubah, naikkan juga nama cache di baris kedua `sw.js` (misalnya `hunidaya-v1.5`). Tanpa itu, ponsel yang sudah memasang aplikasi bisa tetap memakai versi lama.

## Lisensi pihak ketiga

Pembuat kode QR: *QR Code Generator for JavaScript*, Kazuhiko Arase, lisensi MIT (tercantum di dalam `index.html`).
