# Cara Menambah Directory Ke PATH Ubuntu

## Apa itu Ubuntu?

Ubuntu adalah salah satu distro Linux yang cukup popular di kalangan pengguna Linux.

Kepopuleran Ubuntu sebagai alternatif dari Windows sudah terjadi sejak lama.

Ubuntu memiliki keunggulan dibandingkan dengan sistem operasi lainnya.

Sebagai contoh, Ubuntu bersifat gratis dan open source.

Jadi, jika Anda ingin sistem operasi yang ori tapi gratis, Anda bisa coba Ubuntu.

Walaupun demikian bagi user yang tidak terbiasa menggunakan command line, mungkin Ubuntu akan terkesan sedikit rumit.

Tapi kerumitan itu mungkin hanya sementara, karena setelah Anda paham terminal dan command line, Anda mungkin akan terbiasa.

## Apa itu directory?

Directory adalah penampung file atau directory lain dalam filesystem dari suatu sistem operasi.

Jika Anda pengguna Windows dan pernah menggunakan explorer, maka icon folder berwarna kuning itulah yang disebut directory.

Directory bisa tersusun secara bercabang.

Jadi satu directory bisa memiliki banyak directory, tapi satu directory hanya bisa dimiliki satu parent directory.

## Apa itu PATH (Dengan Huruf Besar)?

PATH, di Ubuntu, adalah sebuah variable yang menampung directory sedemikian rupa sehingga file executable di dalam directory yang terdaftar di dalamnya bisa dijalankan tanpa harus masuk ke dalam directory-nya dan tanpa perlu menuliskan full path-nya.

Sebagai contoh, jika ada program bernama nano di dalam directory "/etc/opt" dan kita tidak mendaftarkan "/etc/opt" di PATH, maka nano hanya bisa dijalankan dari dalam directory tersebut atau dengan menuliskan path lengkapnya di command line.

Apa bedanya PATH (Dengan Huruf Besar) dengan path (Dengan Huruf Kecil)?
Path (path) tidak perlu dibingungkan dengan PATH.

Path "/home/namasaya/downloads/file.zip" adalah path lengkap dari file.zip.

Directory "/home/namasaya/downloads/" bisa ditambahkan ke PATH.

## Kenapa kita perlu menambah directory ke PATH?

Karena mungkin kita ingin mengakses suatu executable di directory tertentu dengan lebih ringkas dari directory manapun dengan terminal.

Sebagai contoh, jika saya punya program bernama "list" di path "/home/username/projects/list", dan saya berada di path "/home/username/" maka tanpa menambah directory ke PATH, saya menjalankannya dengan:

```
/home/username/projects/list
```

Tapi, dengan menambahkannya ke PATH, saya bisa gunakan perintah ini dari path manapun:

list

## Apakah kita perlu meng-install aplikasi tambahan untuk menambah directory ke PATH di Ubuntu?

Tidak perlu. Kita bisa melakukannya dengan aplikasi bawaan dari Ubuntu.

Bahkan, jika kita ingin menambahkannya secara permanen, kita hanya perlu aplikasi nano yang sudah ada secara default di Ubuntu.

## Tadi disebutkan penambahan directory ke PATH secara permanen. Apakah yang sementara juga ada/bisa?

Ya.

Penambahan directory ke PATH bisa secara sementara dan permanen.

Caranya juga berbeda.

Penambahan directory ke PATH secara sementara hanya berlaku dalam satu session dari command line.

Jika command line ditutup, kemudian dibuka lagi, maka sudah tidak berlaku lagi.

Berbeda dengan yang permanen, karena dengan penambahan directory ke PATH secara permanen, efeknya akan terus berlanjut meskipun command line ditutup, kemudian dibuka lagi.

## OK. Sekarang, bagaimana cara menambahkan directory ke PATH secara sementara?

Caranya, buka aplikasi command line terlebih dahulu, misalnya dengan terminal.

Kemudian jalankan:

```
export PATH="/directory/baru:$PATH"
```

Jadi, jika Anda ingin menambahkan directory "/home/namasaya/programs/", maka:

```
export PATH="/home/namasaya/programs:$PATH"
```

Untuk memastikan PATH sudah berubah:

```
echo $PATH
```

Begitu caranya.

## Lalu, kenapa ada tanda titik dua ":" dan "$" sebelum PATH?

Tanda ":" adalah pembatas antar directory yang didaftarkan.

Adapun tanda "$" adalah karakter untuk menerima variabel PATH dalam command line.

Jika Anda jalankan:

```
echo $PATH
```

Maka Anda akan mendapati directory-directory yang dipisahkan dengan tanda ":".

## OK. Sekarang, bagaimana cara menambahkan directory ke PATH secara permanen?

Perubahan PATH secara permanen bisa dilakukan secara lokal maupun system-wide.

Pada perubahan secara lokal, maka file konfigurasi yang diubah ada di file "~/.profile" yang ada di masing-masing directory user.

Karena secara lokal, maka ini tidak akan mempengaruhi konfigurasi user yang lain.

Pada perubahan secara system-wide, file konfigurasi yang diubah ada di file "/etc/profile".

Dalam jawaban kami kali ini, saya akan memberi contoh untuk yang lokal saja.

Pertama, buka "~/.profile" dengan nano:

```
nano ~/.profile
```

Scroll hingga baris terbawah.

Kemudian tambahkan kode ini di baris terbawah:

```
export PATH="/directory/tambahan:$PATH"
```

Save dan tutup nano dengan ctrl+x, kemudian y, dan kemudian enter.

Agar hasilnya dapat dilihat, reboot Ubuntu Anda:

```
sudo reboot now
```

Setelah Ubuntu Anda menyala kembali, cek dengan:

```
echo $PATH
```

Jika sudah benar, maka directory tadi akan tampil di output.

## OK. Sekarang saya mengerti. Terima kasih ya…

Sama-sama.
