# EAS_Integratif_MVC

Fancista Syarif Hidayatullah - 05311840000027

## Controllers
**SumbanganController.php**
* `index()` digunakan untuk mengatur pengambilan data dari `sumbangan`
* `listed()` digunakan untuk mengatur pengambilan data dari `identitas_sumbangan`
* `add()` digunakan untuk mengatur penambahan data pada `log_sumbangan` sekaligus mengatur pembaruan data pada `sumbangan`
* `donatur()` digunakan untuk mengatur render tampilan menuju ke **`donatur.html`**
* `donate()` digunakan untuk mengatur penambahan data secara massal (banyak) pada `log_sumbangan` sekaligus mengatur pembaruan data secara massal (banyak) pada `sumbangan`

**DompetController.php**
* `index()` digunakan untuk mengatur pengambilan data dari `sumbangan` sesuai dengan *`$_SESSION`*

**HomeController.php**
* `index($params)` digunakan untuk mengatur pengambilan data dari `log_sumbangan` dan `log_penyaluran`

**AkunController.php**
* `index()` digunakan untuk mengatur *`$_SESSION`*
* `login()` digunakan untuk mengatur pengambilan data dari `identitas`
* `register()` digunakan untuk mengatur penambahan data ke `identitas`
* `profile()` digunakan untuk mengatur pengambilan data dari `identitas` sesuai *`$_SESSION`*
* `ubah()` digunakan untuk mengatur pembaruan data pada `identitas` sesuai *`$_SESSION`*
* `exit()` digunakan untuk mengatur penghancuran *`$_SESSION`*

## Models
**Sumbangan.php**
* `findAll()` digunakan untuk mengambil seluruh data dari `sumbangan` dengan diurutkan ascending berdasarkan jenis
* `FindAllListed()` digunakan untuk mengambil seluruh data dari`identitas_sumbangan` dengan diurutkan ascending berdasarkan kategori
* `insert($id, $data)` digunakan untuk menambah data input kedalam `log_sumbangan`
* `update($data)` digunakan untuk memperbarui data pada `sumbangan` dengan melakukan penambahan banyak sumbangan yang terkumpul
* `insertAll($id, $data)` digunakan untuk menambah banyak data input kedalam `log_sumbangan`
* `update($data)` digunakan untuk memperbarui banyak data pada `sumbangan` dengan melakukan penambahan banyak sumbangan yang terkumpul

**Dompet.php**
* `findAll()` digunakan untuk mengambil seluruh data dari `log_sumbangan` yang memiliki kesamaan *`$_SESSION`* dengan diurutkan descending berdasarkan nomor

**Home.php**
* `findSumbangan()` digunakan untuk mengambil seluruh data dari `log_sumbangan` dengan diurutkan descending berdasarkan nomor
* `findPenyaluran()` digunakan untuk mengambil seluruh data dari `log_penyaluran` dengan diurutkan descending berdasarkan nomor

**Akun.php**
* `account($data)` digunakan untuk mengambil data nama, alamat, usia, pekerjaan dari `identitas` sesuai dengan *`$_SESSION`*
* `insert($data)` digunakan untuk menambah data kedalam `identitas`
* `check($data)` digunakan untuk mengambil data id, pass dari `identitas` untuk dicocokkan dengan input user
* `change($id, $data)` digunakan untuk merubah beberapa data kedalam `identitas` sesuai dengan id

**Problem**
* Entah kenapa saat saya coba run ini error, dan saya tidak paham cara memperbaikinya
