# Cara Mencari File Di Ubuntu Dengan Command Line

## Apa itu File?

File adalah kumpulan data yang disimpan di dalam suatu penyimpanan, seperti sistem komputer atau perangkat penyimpanan eksternal.

Setiap file memiliki nama unik dan dapat berisi berbagai jenis informasi, termasuk teks, gambar, audio, atau program.

File memungkinkan pengorganisasian data dalam struktur yang terstruktur, memudahkan penyimpanan, pencarian, dan manipulasi informasi.

Setiap file memiliki format dan ekstensi yang menentukan cara data diorganisir dan dikelola.

Dalam sistem operasi, file diorganisir dalam struktur direktori atau folder untuk memudahkan manajemen dan navigasi.

Proses membaca, menulis, dan menghapus file merupakan operasi dasar dalam pemrograman dan pengelolaan sistem, dan file memainkan peran penting dalam pengembangan perangkat lunak, penyimpanan dokumen, dan pertukaran informasi di dunia komputasi.

## Kenapa kita perlu mencari file?

File perlu dicari karena kita bermaksud menemukannya.

Sebagai contoh, pada hari senin, saya membuat file bernama “catatan.txt” di folder “/home/namasaya”.

Kemudian, keesokan harinya, saya ingin meng-edit file tersebut, tapi saya lupa di mana lokasinya.

Untuk menemukannya, salah satu caranya adalah dengan mencari file.

## Apakah mencari file di Ubuntu dengan command line perlu meng-install aplikasi tambahan?

Tidak.

Walaupun ada aplikasi pencarian lain, yang bawaan dari Ubuntu sebenarnya sudah cukup.

Itu karena Ubuntu telah menyediakan utilitas pencarian bawaan yang cukup kuat. Salah satu utilitas pencarian yang sering digunakan di lingkungan desktop Ubuntu adalah find dan grep, yang dapat digunakan melalui terminal.

## Apakah mencari file di Ubuntu dengan command line itu sulit?

Sama sekali tidak.

Perintahnya bisa dilakukan hanya dengan satu baris saja.

## OK, sekarang jelaskan bagaimana cara mencari file di Ubuntu dengan command line!

Sebenarnya, dasar cara mencari file di Ubuntu dengan command line cukup sederhana.

Perintah yang digunakan adalah “find”.

Perintah tersebut secara umum ada 2 jenis penggunaan.

Yang pertama dengan mode case sensitive, yakni dengan menambahkan parameter “-name”.

Yang kedua dengan mode case insensitive, yakni dengan menambahkan parameter “-iname”.

Jika menggunakan mode case sensitive, maka huruf kapital dan non kapital dianggap berbeda.

Adapun jika menggunakan mode case insensitive, maka huruf kapital dan non kapital dianggap sama.

Kedua mode tersebut diawali dengan input path di mana pencarian akan dimulai.

Rumus umum untuk pencarian secara case insensitive adalah:

```
find /lokasi/pencarian/ -iname *namafile*
```

Untuk pencarian dengan case sensitive:

```
find /lokasi/pencarian/ -name *namafile*
```

Perhatikan bahwa “/lokasi/pencarian/” diisi dengan path di mana pencarian akan dilakukan.

Adapun tanda bintang di "_namafile_" adalah wildcard.

Dengan penggunaan wildcard "\*.conf", maka semua file dengan akhiran ".conf" akan dicari.

Dengan penggunaan wildcard "settings.\*", maka semua file dengan awalan "settings." akan dicari.

Jadi, jika di path "/etc/apache2/" ada file "httpd.conf" maka pencarian ini:

```
find /etc/apache2/ -iname *.conf
```

Akan menemukan file "httpd.conf".

Namun, perlu diingat bahwa tidak semua path mengizinkan pencarian.

Kadang, ada path tertentu yang mengembalikan pesan "Permission denied".

Jika itu terjadi, maka Anda perlu menggunakan perintah sudo jika Anda tidak login sebagai root:

sudo find /lokasi/pencarian/ -iname _namafile_

## Penutup dan Tips

Sekarang, Anda sudah mengetahui teknik dasar pencarian file di Ubuntu dengan Command Line.

Berikut adalah beberapa tips yang dapat membantu Anda dalam menggunakan perintah find di terminal:

-   Pencarian Berdasarkan Nama File: Mencari file berdasarkan nama dapat dilakukan dengan menggunakan opsi -name. Misalnya, find /lokasi/pencarian -name "nama_file".

-   Pencarian dengan Pola (Wildcard): Gunakan wildcard (_) untuk mencocokkan pola dalam nama file. Misalnya, find /lokasi/pencarian -name "file_".

-   Pencarian Tanpa Peduli Huruf Besar/Kecil: Gunakan opsi -iname untuk mencari file tanpa memperdulikan huruf besar atau kecil. Misalnya, find /lokasi/pencarian -iname "Nama_File".

-   Pencarian Berdasarkan Tanggal Modifikasi: Gunakan opsi -mtime untuk mencari file yang dimodifikasi dalam jumlah hari tertentu. Misalnya, find /lokasi/pencarian -mtime -7.

-   Pencarian Berdasarkan Tipe File: Gunakan opsi -type untuk mencari berdasarkan tipe file, seperti f untuk file reguler atau d untuk direktori. Misalnya, find /lokasi/pencarian -type f.

-   Kombinasi Kriteria Pencarian: Gabungkan beberapa kriteria pencarian dengan operator logika seperti -and, -or, dan -not. Misalnya, find /lokasi/pencarian -name "file\*" -and -type f.

-   Menggunakan Eksekusi Command: Eksekusi perintah pada hasil pencarian dengan opsi -exec. Misalnya, find /lokasi/pencarian -name "file\*" -exec ls -l {} \;.

-   Mencari dalam Struktur Direktori Bersarang: Mencari file dalam struktur direktori bersarang dengan memasukkan opsi -maxdepth atau -mindepth. Misalnya, find /lokasi/pencarian -name "file\*" -maxdepth 2.

-   Menampilkan Hasil Pencarian Secara Ringkas: Gunakan opsi -print untuk menampilkan hasil pencarian secara ringkas. Misalnya, find /lokasi/pencarian -name "file\*" -print.

-   Menggunakan Pernyataan Regular Expression: Gunakan opsi -regex untuk pencarian menggunakan ekspresi reguler. Misalnya, find /lokasi/pencarian -regex ".\*\(\.txt\|\.md\)$".

Penting untuk memahami opsi-opsi ini dan menyesuaikannya dengan kebutuhan pencarian Anda. Selain itu, berhati-hatilah saat menggunakan perintah find, terutama jika Anda berencana untuk menghapus file, untuk menghindari penghapusan tidak disengaja.
