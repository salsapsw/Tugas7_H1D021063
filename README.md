
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
