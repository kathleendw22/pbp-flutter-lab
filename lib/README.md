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




# TUGAS 8 PBP

## Navigator.push VS Navigator.pushReplacement
Pada aplikasi Flutter, terdapat class Navigator yang berfungsi untuk melakukan navigasi. Navigator menyediakan metode push untuk mendorong suatu halaman ke stack sehingga pengguna akan diarahkan ke halaman yang baru dipush tersebut. Metode ini tidak akan menghilangkan halaman paling atas stack sebelum halaman baru dipush sehingga halaman-halaman lama dapat diakses kembali jika ingin. Sementara itu, navigator juga menyediakan metode pushReplacement yang memiliki fungsi yang sama. Bedanya adalah metode pushReplacement ini akan menghilangkan halaman yang lama dan menggantinya dengan yang baru sehingga halaman-halaman lama tidak akan bisa diakses lagi.

## Widgets in Budget Tracking App
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
- Drawer: menampilkan menu untuk melakukan navigasi ke berbagai halaman berbeda
- ListTile: membentuk sebuah list yang berisi widget-widget lain
- Navigator: melakukan navigasi ke berbagai halaman berbeda
- SingleChildScrollView: melakukan scrolling pada satu child
- Container: membungkus widget-widget lain
- BoxDecoration: menyediakan metode-metode untuk membuat sebuah box
- SizedBox: membuat sebuah box dengan ukuran tertentu
- Form: menerima input dari pengguna
- InputDecoration: menampilkan elemen visual dari widget
- TextFormField: mengizinkan pengguna untuk menulis sebuah teks pada bagian form
- DateTime: merepresentasikan waktu dan tanggal
- DropdownButton: menyediakan beberapa pilihan untuk dipilih oleh pengguna
- Dialog: memberikan informasi kepada pengguna
- OutlineInputBorder: membuat border sebagai input decoration widget
- DropdownMenuItem: pilihan-pilihan yang disediakan pada dropdown button
- ListView: menampilkan setiap widget child satu per satu dengan scrolling

## Flutter Events
- onPressed: ketika widget ditekan
- onSaved: ketika widget disimpan
- onChanged: ketika widget diubah
- onTap: ketika widget diklik

## How Navigator Works
Class Navigation memiliki struktur berupa stack. Saat melakukan metode push, suatu halaman dimasukkan ke dalam stack. Berdasarkan struktur stack, maka elemen paling atas dari stack adalah halaman yang dapat dilihat pada layar gawai. Sementara itu, suatu halaman akan dihilangkan dari stack saat melakukan metode pop. Dengan metode ini, maka halaman yang berada pada layar gawai adalah halaman yang dipush sebelum halaman yang dipop tersebut. 

## Checklist Implementation
1. Masuk ke counter_7/lib/main.dart
2. Menambahkan widget Drawer pada class _MyHomePageState. Widget ini berisi menu untuk melakukan navigasi ke halaman counter, form budget, atau data budget.

```
drawer: Drawer(
    child: Column(
        children: [
            // Menambahkan clickable menu
            ListTile(
                title: const Text('counter_7'),
                onTap: () {
                    // Route menu ke halaman utama
                    Navigator.pushReplacement(
                        context,
                        MaterialPageRoute(builder: (context) => const MyHomePage()),
                    );
                },
            ),
            ListTile(
                title: const Text('Tambah Budget'),
                onTap: () {
                    // Route menu ke halaman form
                    Navigator.pushReplacement(
                        context,
                        MaterialPageRoute(builder: (context) => const MyFormPage()),
                    );
                },
            ),
            ListTile(
                title: const Text('Data Budget'),
                onTap: () {
                    // Route menu ke halaman form
                    Navigator.pushReplacement(
                        context,
                        MaterialPageRoute(builder: (context) => const MyInputPage()),
                    );
                },
            ),
        ],
    ),
),
```

3. Membuat file dart baru bernama form.dart untuk menangani halaman form budget dan data.dart untuk menangani halaman data budget.

4. Pada file form.dart, digunakan widget DateTime untuk meminta input tanggal, TextFormField untuk meminta input judul dan nominal, DropdownButton untuk memilih tipe budget yaitu pemasukan atau pengeluaran, FloatingButtonAction.extended untuk menyimpan data pada sebuah list, dan Dialog untuk menginfokan bahwa data telah berhasil disimpan.

```
body: Form(
    key: _formKey,
    child: SingleChildScrollView(
        child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
                Padding(
                    // Menggunakan padding sebesar 8 pixels
                    padding: const EdgeInsets.all(8.0),
                    child: TextFormField(
                        controller: _tanggal,
                        decoration: InputDecoration(
                            icon: Icon(Icons.calendar_today), //icon of text field
                            labelText: "Tanggal", //label text of field
                        ),
                        readOnly: true,
                        //set it true, so that user will not able to edit text
                        onTap: () async {
                            DateTime? _dateTime = await showDatePicker(
                                context: context,
                                initialDate: DateTime.now(),
                                firstDate: DateTime(2000),
                                lastDate: DateTime(2023),
                            );
                            if (_dateTime != null) {
                                String _dateFormat = DateFormat('dd-MM-yyyy').format(_dateTime);
                                setState(() {
                                    _tanggal.text = _dateFormat;
                                });
                            }
                        }
                    ),
                ),
                Padding(
                    // Menggunakan padding sebesar 8 pixels
                    padding: const EdgeInsets.all(8.0),
                    child: TextFormField(
                        decoration: InputDecoration(
                            hintText: "Contoh: Beli Sate Pacil",
                            labelText: "Judul",
                            // Menambahkan circular border agar lebih rapi
                            border: OutlineInputBorder(
                                borderRadius: BorderRadius.circular(5.0),
                            ),
                        ),
                        // Menambahkan behavior saat nama diketik
                        onChanged: (String? value) {
                            setState(() {
                                _judul = value!;
                            });
                        },
                        // Menambahkan behavior saat data disimpan
                        onSaved: (String? value) {
                            setState(() {
                                _judul = value!;
                            });
                        },
                        // Validator sebagai validasi form
                        validator: (String? value) {
                            if (value == null || value.isEmpty) {
                                return 'Judul tidak boleh kosong!';
                            }
                            return null;
                        },
                    ),
                ),
                Padding(
                    // Menggunakan padding sebesar 8 pixels
                    padding: const EdgeInsets.all(8.0),
                    child: TextFormField(
                        decoration: InputDecoration(
                            hintText: "Contoh: 15000",
                            labelText: "Nominal",
                            // Menambahkan circular border agar lebih rapi
                            border: OutlineInputBorder(
                                borderRadius: BorderRadius.circular(5.0),
                            ),
                        ),
                        keyboardType: TextInputType.number,
                        // Menambahkan behavior saat nama diketik
                        onChanged: (String value) {
                            final v = int.tryParse(value);
                            if (v == null) {
                                setState(() {
                                    _nominalIsValid = false;
                                });
                            } else {
                                setState(() {
                                    _nominalIsValid = true;
                                    _nominal = value;
                                });
                            }
                        },
                        // Menambahkan behavior saat data disimpan
                        onSaved: (String? value) {
                            setState(() {
                                _nominal = value!;
                            });
                        },
                        // Validator sebagai validasi form
                        validator: (String? value) {
                            if (value == null || value.isEmpty) {
                                return 'Nominal tidak boleh kosong!';
                            } else if (_nominalIsValid == false) {
                                return 'Input tidak valid!';
                            }
                            return null;
                        },
                    ),
                ),
                ListTile(
                    title: const Text(
                        'Pilih Jenis',
                    ),
                    trailing: DropdownButton(
                        value: _tipe,
                        icon: const Icon(Icons.keyboard_arrow_down),
                        items: listTipe.map((String items) {
                            return DropdownMenuItem(
                                value: items,
                                child: Text(items),
                            );
                        }).toList(),
                        onChanged: (String? newValue) {
                            setState(() {
                                _tipe = newValue!;
                            });
                        },
                    ),
                ),
            ],
        ),
    ),
),
floatingActionButton: FloatingActionButton.extended(
    label: const Text('Simpan'),
    onPressed: () {
        if (_formKey.currentState!.validate()) {
            List<String> listData = [];
            listData.addAll([_judul, _nominal, _tipe, _tanggal.text]);
            data.add(listData);
            showDialog(
                context: context,
                builder: (context) {
                    return Dialog(
                        shape: RoundedRectangleBorder(
                            borderRadius: BorderRadius.circular(10),
                        ),
                        elevation: 15,
                        child: Container(
                            child: ListView(
                                padding: const EdgeInsets.only(top: 20, bottom: 20),
                                shrinkWrap: true,
                                children: <Widget>[
                                    Center(
                                        child: const Text('Data berhasil disimpan!'),
                                    ),
                                    SizedBox(height: 20),
                                    // TODO: Munculkan informasi yang didapat dari form
                                    TextButton(
                                        onPressed: () {
                                            Navigator.pop(context);
                                        },
                                        child: Text('Kembali'),
                                    ),
                                ],
                            ),
                        ),
                    );
                },
            );
        }
    },
),
floatingActionButtonLocation: FloatingActionButtonLocation.centerFloat,
```

5. Pada file data.dart, dilakukan iterasi pada list untuk mengambil data yang sudah berhasil disimpan. Setiap data yang berhasil disimpan akan ditampilkan melalui widget Container.

```
body: SingleChildScrollView(
    child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: <Widget>[
            for (var items in data)
                Container(
                    margin: const EdgeInsets.all(8),
                    decoration: BoxDecoration(
                        border: Border.all(color: Colors.grey),
                        borderRadius: BorderRadius.circular(5),
                    ),
                    padding: const EdgeInsets.all(20.0),
                    child: Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        children: <Widget>[
                            Row(
                                children: [
                                    Text(
                                        items[0],
                                        style: TextStyle(
                                            fontWeight: FontWeight.bold,
                                            fontSize: 20,
                                        ),
                                    ),
                                    Spacer(),
                                    Text(items[3], style: TextStyle(fontSize: 20)),
                                ],
                            ),
                            SizedBox(height: 20),
                            Row(
                                children: [
                                    Text(items[1]),
                                    Spacer(),
                                    Text(items[2]),
                                ],
                            ),
                        ],
                    ),
                ),
        ],
    ),
),
```


