# Cara Reboot Ubuntu Dengan Command Line

## Mengenal Ubuntu

Ubuntu adalah sistem operasi berbasis linux yang cukup popular di kalangan pengguna Linux.

Ubuntu adalah salah satu distribusi Linux yang paling populer dan sering digunakan di dunia.

Dikembangkan oleh Canonical, Ubuntu didesain untuk menjadi sistem operasi sumber terbuka yang ramah pengguna, dapat diakses secara gratis, dan mendukung berbagai perangkat keras.

Ubuntu menggunakan lingkungan desktop GNOME sebagai antarmuka pengguna standarnya, namun variasi lain dengan lingkungan desktop yang berbeda juga tersedia.

Sebagai distribusi Linux, Ubuntu memiliki kestabilan dan keamanan yang tinggi, dan merupakan pilihan umum untuk penggunaan pribadi, pengembangan perangkat lunak, dan implementasi server.

Ubuntu juga memiliki siklus rilis reguler dan mendukung model LTS (Long Term Support) untuk versi tertentu, memberikan fleksibilitas kepada pengguna untuk memilih tingkat dukungan jangka panjang atau pembaruan lebih sering sesuai kebutuhan mereka.

## Mengenal Reboot

Reboot adalah istilah lain dari restart, yaitu sebuah proses untuk mematikan dan menyalakan ulang komputer.

Reboot atau "restart" merujuk pada proses memulai ulang suatu sistem komputer atau perangkat elektronik.

Saat suatu sistem di-reboot, semua program yang berjalan dan konfigurasi yang ada dimuat ulang, membawa sistem ke dalam keadaan awal saat dinyalakan.

Tindakan reboot sering digunakan untuk mengatasi masalah perangkat lunak yang mungkin muncul selama penggunaan sistem, seperti kegagalan program atau kinerja yang tidak responsif.

Reboot juga dapat diperlukan setelah instalasi perangkat lunak baru atau pembaruan sistem agar perubahan tersebut berlaku sepenuhnya.

Pada sistem operasi yang stabil, reboot tidak hanya membantu memperbaiki masalah sementara tetapi juga membantu memulai kembali layanan dan proses yang mungkin telah terhenti atau terganggu.

Meskipun reboot umumnya aman, tetapi harus dilakukan dengan hati-hati, terutama pada sistem yang sedang menjalankan tugas kritis atau sistem server untuk meminimalkan downtime yang tidak diinginkan.

## Mengenal Command Line

Command line adalah suatu interface tekstual untuk menjalankan tugas tertentu pada sistem operasi.

Command line, atau sering disebut sebagai terminal atau shell, adalah antarmuka teks yang memungkinkan pengguna berinteraksi dengan sistem operasi atau program dengan memasukkan perintah-perintah secara langsung melalui baris perintah.

Pengguna dapat menggunakan command line untuk menjalankan program, mengelola file dan direktori, memeriksa status sistem, dan melakukan berbagai tugas lainnya dengan menggunakan sintaks perintah yang sesuai dengan aturan sistem operasi tertentu.

Command line sering digunakan oleh pengembang, administrator sistem, dan pengguna lanjutan karena memberikan kontrol yang lebih langsung dan efisien terhadap sistem dibandingkan antarmuka grafis.

Meskipun mungkin memiliki kurva belajar, command line dapat memberikan kekuatan dan fleksibilitas tambahan dalam mengelola dan mengotomatisasi tugas pada sistem komputer.

## Apa yang Akan Dilakukan di Tutorial Ini

Tutorial ini membahas cara melakukan reboot di Ubuntu dengan command line.

Secara default, command line yang digunakan di Ubuntu adalah Terminal.

Di sini, ada 3 cara utama untuk melakukan reboot dengan command line.

## Alasan Melakukan Reboot di Ubuntu dengan Command Line

Saat dihadapkan dengan Ubuntu desktop, mungkin reboot bisa dilakukan dengan mudah karena fitur tersebut sudah ada user interface-nya.

Namun, bagaimana dengan Ubuntu Server?

Ubuntu server user interface-nya hanya berupa command line.

Jadi, mau tidak mau Anda harus mengetikkan perintahnya di command line.

## Tingkat Kesulitan Command Line untuk Reboot

Reboot dengan command line termasuk sederhana.

Pada umumnya, hanya diperlukan satu baris perintah saja, walaupun caranya beragam.

## Cara Reboot Ubuntu di Command Line: Langkahnya

Ada 3 cara utama untuk reboot Ubuntu.

Syarat utamanya, kita harus memiliki super user privileges.

### Cara utama pertama adalah dengan menggunakan perintah reboot.

```
sudo reboot
```

Perlu diingat bahwa jika kita login sebagai root, kita tidak perlu perintah sudo-nya.

```
reboot
```

Dengan perintah ini, maka Ubuntu akan di-restart, kecuali jika ada process yang menghalanginya.

Jika ada process yang menghalangi reboot, kita bisa memaksanya untuk tetap reboot.

```
sudo reboot --force
```

Tapi perlu diingat bahwa dengan cara tadi, kemungkinan akan ada kerusakan data.

Jadi, gunakan secara bijak.

### Cara utama kedua adalah dengan menggunakan perintah shutdown.

```
sudo shutdown -r
```

Dengan cara ini, Ubuntu akan di-restart setelah satu menit sesudah perintah tadi dijalankan.

Jika ingin lebih lama lagi, misalnya 3 menit sesudahnya, maka jalankan perintah ini:

```
sudo shutdown -r +3
```

Dan jika kita tidak ingin menunggu:

```
sudo shutdown -r now
```

### Cara utama ketiga adalah dengan perintah systemctl

Bagi Linux yang menerapkan systemd, kita bisa reboot dengan cara ini:

```
sudo systemctl reboot
```

## Penutup

Sebagai tambahan, sebelum Anda menjalankan perintah ini, pastikan Anda sudah men-save pekerjaan Anda ke file agar tidak kehilangan data akibat reboot.
