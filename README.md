
# Tugas7_H1D021063
Salsabilla PSW/H1D021063/F

![image](https://github.com/user-attachments/assets/97cfe230-e1bb-4152-82f0-28692df3ba38)

![image](https://github.com/user-attachments/assets/3821f7c3-3c81-4231-85e9-4a540e116c8f)

Sistem login ini menggunakan ionic sebagai frontend nya lalu menggunakan PHP di backendnya, secara singkat sepemahaman saya prosesnya adalah sebagai berikut:
1. user mengisi username dan password (yang sudah terdaftar didatabase) lewat form
2. form ini mengirim data ke server (file php) untuk diproses
3. server memeriksa kredensial pengguna ke database
4. kalau valid, server mengembalikan token dan status login ke frontend
5. frontend menyimpan token dan username untuk sesi berikutnya

Detail : 
1. di file login.page.ts itu terdapat login function untuk mengambil inputan username dan password dari user, lalu memanggil data ke server dengan menggunakan metod postMethod dari AuthenticationService ke login.php
2. di file login.page.htlm itu menampilkan form input dan menerima input username dan password dari user, terdapat juga tombol login yang memanggil fungsi login() saat di klik
3. di file koneksi.php itu digunakan untuk membuka koneksi ke database MySQL memakai mysqli_connect() ke coba-ionic, jika gagal akan mengembalikan pesan "koneksi gagal"
4. file login.php digunakan untuk mengambil data JSON yang dikirim frontend untuk dikonversi menjadi array dengan json_decode() lalu data diolah apakah username dan password ada dalam database, jika data ada, maka dibuat array $pesan dengan username, token, dan status loginnya 'berhasil, jika data tidak ada maka status login menjadi 'gagal', setelah itu mengembalikan respon lagi ke dalam format JSON dengan menggunakan json_encode()
5. file authentication.service.ts digunakan untuk mengelola logika autentikasi dan menyimpan data pengguna
