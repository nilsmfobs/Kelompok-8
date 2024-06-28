# Image Compressor
Tugas Project UAS Informatika B/Genap Aljabar Linier

Aplikasi Singular Value Decomposition ( Svd ) Untuk Kompresi Image

## Daftar Isi
* [Informasi Umum](#informasi-umum)
* [Anggota Kelompok](#anggota-kelompok)
* [Teknologi yang Digunakan](#teknologi-yang-digunakan)
* [Fitur](#fitur)
* [Setup](#setup)

## Informasi Umum
Pada Tugas Project UAS Informatika B/Genap Aljabar Linier kali ini kita diminta untuk membuat sebuah program kompresi gambar dengan memanfaatkan Singular Value Decomposition (SVD) yang berjalan di suatu web lokal sederhana. 

Pada tugas proyek ini, algoritma yang digunakan untuk mencari nilai dan vektor eigen serta membentuk matriks SVD adalah dekomposisi Singular Value Decomposition (SVD). Matriks gambar dipecah menjadi tiga matriks yaitu \(U\), \(S\), dan \(V^T\), di mana \(U\) dan \(V^T\) adalah matriks ortogonal dan \(S\) adalah matriks diagonal yang berisi nilai-nilai singular. Untuk kompresi, hanya sebagian nilai singular terbesar yang disimpan, mengurangi dimensi gambar secara signifikan. Nilai-nilai singular terbesar berkontribusi paling signifikan terhadap struktur asli matriks. Dengan menyimpan hanya k nilai singular terbesar, matriks aproksimasi dibentuk kembali untuk menghasilkan versi terkompresi dari gambar asli. Implementasi ini dilakukan dengan memisahkan gambar menjadi saluran warna RGB, menerapkan SVD pada setiap saluran, dan kemudian menggabungkan kembali saluran yang telah dikompresi untuk membentuk gambar akhir yang terkompresi.

## Anggota Kelompok
### Kelompok VIII
| Nama                           | NIM      |
| ------------------------------ | -------- |
| Clementine Dwayani Danitasari  | L0123041 |
| Diva Muthi'ah Sholihah         | L0123044 |
| Kezia Manuella Tambunan        | L0123074 |

## Teknologi yang Digunakan
* **numpy v.1.21.4**: untuk melakukan operasi-operasi pada matriks, array, dan operasi matematika lainnya.
* **Pillow v.8.4.0**: untuk segala pemrosesan gambar termasuk mengkonversinya menjadi matriks dan sebaliknya serta mengetahui mode warna yang digunakan.
* **Flask v.2.0.2**: untuk menghubungkan program Python pada backend dengan frontend website dan menangani request dari keduanya.
* **Bootstrap v5.1.3**: untuk membangun web yang elegan dan responsif dengan cepat. (Tidak perlu diinstall lagi karena sudah terdapat pada folder `/src/static/bootstrap`).
* **OpenCV v.4.5.4**: untuk membaca, menulis, dan memproses gambar.
* **Werkzeug v.2.0.2**: untuk menangani upload file secara aman.

## Fitur
Beberapa fitur yang dapat diakses oleh pengguna saat menggunakan website/program ini:
* **Unggah dan Kompres Gambar**: Pengguna dapat mengunggah gambar dan memilih tingkat kompresi (1-100%) untuk mengompresi gambar tersebut.
* **Pratinjau Gambar Asli dan Terkompresi**: Pengguna dapat melihat perbandingan antara gambar asli dan gambar yang sudah dikompresi.
* **Unduh Gambar Terkompresi**: Pengguna dapat mengunduh hasil kompresi gambar.
* **Format Gambar yang Didukung**: Mendukung berbagai format gambar yang didukung sepenuhnya oleh library PILLOW, seperti BMP, JPEG, PNG, TIFF, dan banyak lagi.
* **Mode Warna yang Didukung**: Mendukung gambar dengan mode warna L, LA, P, PA, RGB, RGBA, dan CMYK.
* **Informasi Runtimes**: Menampilkan waktu kompresi untuk memberi informasi kepada pengguna tentang efisiensi kompresi.
* **Pesan Kesalahan yang Jelas**: Menampilkan pesan kesalahan yang jelas jika file yang diunggah tidak didukung atau jika tingkat kompresi di luar rentang yang diizinkan.

## Setup
Untuk menjalankan aplikasi ini, ikuti langkah-langkah berikut:

1. **Instal Python 3**:
   Pastikan Python 3 telah terinstal pada komputer Anda. Jika belum, unduh dan instal Python 3 dari [sini](http://www.python.org/downloads/).

2. **Tambahkan Python dan PIP ke PATH**:
   Pastikan Python dan PIP sudah ditambahkan ke PATH. Bila belum, Anda bisa melihat panduan [ini](http://stackoverflow.com/questions/3701646/how-to-add-to-the-pythonpath-in-windows-so-it-finds-my-modules-packages) untuk menambahkan Python dan [ini](http://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command) untuk menambahkan PIP.

3. **Instal Library yang Dibutuhkan**:
   Gunakan PIP untuk menginstal library Flask, numpy, Pillow, OpenCV, dan Werkzeug yang dibutuhkan untuk menjalankan program. Jalankan perintah berikut di terminal atau command prompt:
   ```bash
   pip install Flask
   pip install numpy
   pip install Pillow
   pip install opencv-python
   pip install Werkzeug
   ```

4. **Download atau Clone Repository**:
   Download atau clone repository project ke komputer Anda.

5. **Jalankan Aplikasi**:
   Buka terminal atau command prompt, arahkan ke folder project, dan jalankan file `app.py` dengan perintah berikut:
   ```bash
   python app.py
   ```

6. **Akses Website**:
   Pada terminal Python akan muncul pesan yang menunjukkan bahwa server sedang berjalan:
   ```bash
    * Restarting with stat
    * Debugger is active!
    * Debugger PIN: 727-607-683
    * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
   ```
   Buka browser pilihan Anda dan akses link yang terdapat pada baris terakhir (misalnya, `http://127.0.0.1:5000/`). Selamat! Sekarang Anda dapat menjalankan website kompresi gambar.

