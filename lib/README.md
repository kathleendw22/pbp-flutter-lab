Kathleen Daniella Wijaya | 2106637366

# TUGAS 7 PBP

## Stateless Widget VS Stateful Widget
Stateless widget adalah widget yang tidak memiliki state sehingga widget ini tidak akan berubah secara internal. Contoh dari stateless widget adalah Icon, Text, dan lain sebagainya. Sementara itu, stateful widget adalah widget yang memiliki state sehingga dapat berubah secara internal. Misalnya, stateful widget dapat berubah saat pengguna melakukan interaksi dengan widget tersebut atau saat ada data yang diterima. Contoh dari stateful widget adalah Checkbox, TextField, Radio, dan masih banyak lagi.

## Widgets in Counter_7
- MaterialApp: mengakses semua komponen dan widget yang disediakan oleh Flutter
- Scaffold: menyediakan API yang beragam dan aplikasi menempati seluruh layar perangkat
- AppBar: komponen paling atas dari aplikasi
- Text: menampilkan teks pada aplikasi
- Center: menyelaraskan widget ke center pada layar
- Column: memposisikan widget secara vertikal
- TextStyle: menambahkan style pada teks 
- Theme: menambahkan tema pada aplikasi
- Padding: mengatur posisi widget dengan menambahkan padding (ruang kosong)
- Row: memposisikan widget secara horizontal
- FloatingActionButton: button berbentuk lingkar yang berada di atas widget lain pada aplikasi
- Spacer: menambahkan spasi atau ruang antar widget
- Icon: menampilkan gambar grafis yang diinginkan pada aplikasi

## setState()
setState() memberi tahu framework Flutter bahwa terdapat sesuatu yang berubah pada state sehingga Flutter akan menjalankan kembali fungsi build yang sudah di-override agar aplikasi dapat menampilkan nilai yang telah diperbarui. Jika mengubah suatu nilai tanpa memanggil setState(), maka fungsi build tidak akan dipanggil lagi sehingga tidak akan terjadi apa-apa pada interface aplikasi.

## Const VS Final
Kata kunci final digunakan untuk mengunci nilai (state) dari suatu variabel sehingga tidak akan bisa diubah oleh jenis operasi apapun. Sementara itu, kata kunci const memiliki fungsi yang sama persis dengan kata kunci final. Akan tetapi, const mengunci nilai (state) variabel pada compile-time saja. Saat menggunakan kata kunci const pada suatu objek, state objek akan bersifat tetap pada waktu kompilasi sehingga state objek sepenuhnya tidak dapat diubah.

## Checklist Implementation
- Membuat program counter_7 dengan "flutter create counter_7" pada terminal
- Masuk ke counter_7/lib/main.dart
- Mengubah title homepage menjadi "Program Counter"
- Secara default, sudah terdapat fungsi "_incrementCounter" yang akan menambahkan angka _counter sebanyak satu satuan pada class _MyHomePageState.
- Membuat sebuah fungsi baru bernama "_decrementCounter" pada class _MyHomePageState. Pada fungsi ini, setState() menjadi _counter yang telah di-decrement (dikurangi satu satuan) jika _counter lebih dari 0 sehingga _counter tidak akan dikurangi jika _counter bernilai 0.
- Menambahkan if-else statement pada fungsi build -> body -> children. Jika _counter bernilai genap (if _counter % 2 == 0), maka teks indikator adalah GENAP dengan style warna merah. Jika _counter bernilai ganjil (else), maka teks indikator adalah GANJIL dengan style warna biru.
- Menggunakan widget Padding (untuk mengatur posisi button), Spacer (untuk memberikan jarak antar button), dan Row (untuk memposisikan button secara horizontal) pada floatingActionButton serta set FloatingActionButtonLocation menjadi center untuk membuat button - berada di kiri dan button + berada di kanan dengan jarak vertikal dan horizontal yang simetris
- Menggunakan widget FloatingActionButton dan Icon untuk membuat button - (Icons.remove) dan button + (Icons.add). Saat mengklik button -, fungsi _decrementCounter akan dipanggil. Saat mengklik button +, fungsi _incrementCounter akan dipanggil.

