# Data Permohonan PPE Baru

Repository tujuan: `smartlab738-max/Data-permohonan-PPE-baru`.

## Mulai cepat (tanpa token/path)

- Ekstrak ZIP. Untuk pratinjau, buka `index.html` dengan browser; data lokal disimpan menggunakan localStorage jika browser mengizinkan.
- Untuk penyimpanan permanen di file server: pasang Node.js 20+ (LTS), klik dua kali `Jalankan-Windows.bat` atau jalankan `npm start` di folder proyek. Buka http://127.0.0.1:3000. Tidak perlu npm install, token, maupun konfigurasi path. Jangan tutup proses server saat digunakan. Data disimpan otomatis di `data/requests.json` (dibuat saat server pertama kali berjalan). Simpan cadangan file tersebut atau ekspor CSV secara berkala.
- Semua perubahan sel disimpan setelah 650 ms tanpa mengetik, dengan tombol Simpan sebagai pilihan tambahan. Konflik antar pengguna ditampilkan untuk menghindari penimpaan diam-diam. Nomor mengikuti urutan baris. Statistik mengabaikan baris yang belum berisi nama maupun uraian.

## GitHub

Upload file proyek ke root repository tujuan (pertahankan `.gitignore`). Untuk mode statis, aktifkan GitHub Pages dari Settings → Pages → Deploy from a branch → pilih branch yang berisi `index.html` dan folder `/ (root)`. URL lazimnya https://smartlab738-max.github.io/Data-permohonan-PPE-baru/ setelah Pages berhasil diterbitkan. Mode Pages hanya menyimpan di browser masing-masing, bukan file GitHub dan bukan data bersama.

## Penyimpanan bersama

Jalankan server Node.js pada komputer/server internal yang selalu aktif. Set `HOST=0.0.0.0` untuk menerima koneksi jaringan; gunakan firewall/jaringan tepercaya atau reverse proxy dengan HTTPS dan autentikasi untuk membatasi akses. Aplikasi ini tidak memiliki autentikasi bawaan; jangan mengekspos port ke internet publik tanpa perlindungan. Gunakan satu proses server dan disk persisten; `DATA_DIR` opsional untuk menentukan lokasi disk permanen oleh admin hosting. Pengguna akhir cukup membuka URL server; tidak perlu token atau path. Data runtime tidak otomatis dikomit ke repository GitHub. GitHub menyimpan source code, sedangkan server menyimpan data operasional. Hosting statis tidak bisa menjalankan `server.mjs`.

Jika server tidak terhubung, perubahan yang belum terkirim dicadangkan di browser bila memungkinkan. Jangan menghapus data browser sebelum sinkronisasi. Konflik versi memerlukan keputusan pengguna; ekspor CSV cadangan sebelum menimpa versi server.

## Keamanan

Jangan memasukkan personal access token ke HTML, JavaScript, GitHub Pages, atau file repository. Cabut token yang telah dibagikan melalui chat, lalu gunakan integrasi GitHub yang sah atau autentikasi Git lokal jika perlu mengunggah source code. Tidak ada token pada paket ini.
