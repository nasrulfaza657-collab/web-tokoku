# TokoKu Admin Panel — PHP Native

## Kebutuhan
- XAMPP (Apache + MySQL/MariaDB)
- PHP 8.0+
- Database `db_tokoku`

## Instalasi
1. Ekstrak folder `tokoku_native` ke `C:\xampp\htdocs\`.
2. Jalankan Apache dan MySQL dari XAMPP.
3. Buka phpMyAdmin: `http://localhost/phpmyadmin`.
4. Import file `db_tokoku.sql` yang kamu miliki ke database `db_tokoku`.
   - Jika database sudah ada dan berisi tabel, jangan import ulang agar tidak terjadi duplikasi.
5. Periksa `config.php`. Default XAMPP biasanya:
   - host: `localhost`
   - database: `db_tokoku`
   - user: `root`
   - password: kosong
6. Buka `http://localhost/tokoku_native/`.

## Fitur
- Dashboard statistik dari tabel pelanggan dan transaksi.
- CRUD pelanggan.
- Tambah dan daftar transaksi.
- VIEW: `view_pelanggan`, `view_total_belanja`, `view_transaksi_pelanggan`.
- JOIN: `tbl_transaksi` dan `tbl_pelanggan`.
- Subquery analisis total belanja pelanggan di atas rata-rata.
- Stored Procedure: `TampilPelanggan`, `CariPelanggan`, `HitungPelanggan`, `LaporanTransaksi`, `TambahPelanggan`.
- Function: `HitungDiskon`, `HitungPajak`, `HitungTotal`, `KategoriBelanja`, `KonversiNilai`.
- Trigger dan tabel log.
- Uji transaksi COMMIT / ROLLBACK.
- EXPLAIN query.

## Catatan
- Ini panel admin lokal untuk tugas/pengujian, belum dilengkapi sistem login/role.
- Gunakan hanya di localhost. Sebelum dipublikasikan, tambahkan autentikasi, CSRF token, validasi tambahan, dan pengamanan konfigurasi.
- Menu Produk/Stock tidak ditampilkan karena database yang diberikan belum memiliki tabel produk atau stok.
- Chart.js dan Google Fonts dimuat dari CDN sehingga perlu koneksi internet saat halaman dibuka.

Dibuat oleh: AL- FAZA
