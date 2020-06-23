# Skema eKTP

![eKTP](eKTP.jpg)

![Nomor eKTP](nomorktp.png)

| # | keterangan |
|---|---|
| A | Propinsi |
| B | Kota/Kabupaten |
| C | Kecamatan |
| D | Tanggal lahir, jika wanita, tanggal lahir akan ditambah 40 |
| E | Bulan lahir |
| F | Tahun lahir |
| G | Urutan terdaftar pada Disdukcapil untuk yang tanggal lahirnya sama|
| JK | **Wanita**, tanggal lahir diatas angka 40, jika **Pria** tanggal lahir tetap |
| Jumlah | 16 digit |


## Contoh

| # | keterangan |
|---|---|
| 31 | DKI JAKARTA |
| 74 | KOTA JAKARTA BARAT |
| 09 | JAGAKARSA |
| 61 | Tanggal lahir, karena diatas 40 berati wanita, dikurangi 40 untuk mendapatkan tanggal aslinya, 61-40 = **21** |
| 12 | Bulan 12, Desember |
| 90 | Tahun 1990 |
| 0001 | Pendaftar pertama di Disdukcapil untuk tanggal lahir tersebut |
| JK | Wanita Dikarenakan tanggal lahir diatas angka 40 |

Bila mana hasil perhitungan berbeda, maka bisa jadi eKTP palsu atau pihak Disdukcapil tidak teliti

## eKTP Palsu?
![eKTP Palsu](ektp_palsu.jpg)

| # | keterangan |
|---|---|
| 36 | BANTEN |
| 01 | KAB. PANDEGLANG |
| 18 | CIMANUK |
| 50 | Tanggal lahir, karena diatas 40 berati wanita, dikurangi 40 untuk mendapatkan tanggal aslinya, 50-40 = **10** |
| 09 | Bulan 9, September |
| 86 | Tahun 1986 |
| 0001 | Pendaftar pertama di Disdukcapil untuk tanggal lahir tersebut|
| JK | Wanita, Dikarenakan tanggal lahir diatas angka 40 |

Tetapi jika dilihat di eKTP, tertulis tanggal 17-10-1986, 17 Oktober 1986, sedangkan di nomor eKTP berbeda.

Ada juga yang Wanita tapi tanggal lahir dibawah angka 40, atau yang Pria, tapi tanggal lahir diatas 40.

## Validasi

Dengan skema diatas, maka kita dapat memvalidasi apakah eKTP itu benar, sebagai tahap awal verifikasi. pastikan Jumlah karakter 16 digit, tanggal lahir sama, dan jenis kelamin sama

Apakah bisa validasi dari 6 digit pertama?
bisa, tetapi hanya cek apakah wilayahnya ada atau ngga, karena 6 digit pertama merupakan wilayah pertama kali orang tersebut membuat KTP, seperti iBNuX lahir di Bandung - Jawa Barat, Pertama kali bikin KTP di Kab. Serang - Banten, jadinya nomor KTP saya **360423**

bisa dicek apakah wilayahnya ada dengan mengambil URL

[https://ibnux.github.io/data-indonesia/kelurahan/360423.json](https://ibnux.github.io/data-indonesia/kelurahan/360423.json)

cek [disini](https://ibnux.github.io/data-indonesia/) cara kerjanya

## Masalah di negara ini
Data NIK ini tidak 100% valid juga, dikarenakan Disdukcapil sering mengisi data tidak sesuai dengan NIKnya, jadi validasi ini hanya untuk proses awal, jika gagal disini, dilanjutkan dengan validasi ke Disdukcapil dan BI Checking.

Semoga ke depan pembuatan NIK lebih serius.

## Singkatan
| Singkatan | keterangan |
|---|---|
| JK | Jenis Kelamin |
| KAB | KABUPATEN |

## Link Development

* [Android & iOS eKTP - OCR for Indonesia ID card](https://github.com/anilbattini/eKTP)
* [Javascript NIK Parser](https://github.com/bachors/nik_parse.js)

### Traktir kopi

[<img src="https://ibnux.github.io/KaryaKarsa-button/karyaKarsaButton.png" width="128">](https://karyakarsa.com/ibnux)
[<img src="https://ibnux.github.io/Trakteer-button/trakteer_button.png" width="120">](https://trakteer.id/ibnux)
