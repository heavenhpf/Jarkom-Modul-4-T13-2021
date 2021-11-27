# Jarkom-Modul-4-T13-2021

## Anggota Kelompok

| No. | Nama | NRP |
| ------ | ------ | ------ |
| 1. | Heaven Happyna Putra F. | (05311940000026) |
| 2. | Gavin Bagus Kenzie Narain | (05311940000028) |
| 3. | Tera Nurwahyu Pratama | (05311940000039) |

## Daftar Isi

* [VLSM](vlsm)
    * [Subnetting](subnetting)
    * [Tree](tree)
    * [Routing](routing)
* [CIDR](cidr)
    * [Subnetting](subnetting)
    * [Tree](tree)
    * [Routing](routing)
* [Kesulitan yang dihadapi](kesulitan-yang-dihadapi)

## VLSM
### Subnetting
Untuk VLSM, kami melakukan subnetting pada topologi yang diberikan. Total dari subnet yang diperoleh adalah 15 seperti pada gambar berikut:

![image]()

Kami juga menentukan panjang sekaligus IP yang digunakan dari setiap subnetnya. Kemudian, kami menjumlah total subnet yang kami perlukan tersebut sehinga diperoleh hasil sebagai berikut:

![image]()

Diperoleh hasilnya 5845 total IP yang digunakan, sehingga length dari parent tree nya adalah /19.

### Tree
Untuk membuat tree, berdasarkan tabel subnetting sebelumnya, kami menurunkannya sesuai dengan aturan pembagian subnet dan di sini kami memasukkan penggunaan IP yang terbesar terlebih dahulu di sebelah kanan, dilanjutkan sampai semua subnet yang diminta pada topologi memperoleh bagiannya:

![image]()

### Routing


## CIDR
### Subnetting
Untuk subnetting pada CIDR ini, dilakukan secara bertahap dari subnet yang terjauh. Berdasarkan subnetting yang dilakukan pada VLSM sebelumnya, urutan subnet yang dilakukan adalah sebagai berikut:

#### B
A15 + A13 -> B1

#### C
B1 + A14 -> C1 <br>
A1 + A2 -> C2

#### D
C1 + A12 -> D1 <br>
C2 + A3 -> D2 <br>
A9 + A10 -> D3

#### E
D1 + A11 -> E1 <br>
D2 + A4 -> E2

#### F
E1 + D3 -> F1

#### G
E2 + A5 -> G1 <br>
F1 + A8 -> G2

#### H
G1 + A6 -> H1 <br>
G2 + A7 -> H2

#### I
H1 + H2 -> I1

Dari setiap penggabungan subnet kami menggunakan aturan di mana panjang subnet parent merupakan N-1 dari subnet child terbesarnya. Sehingga diperoleh hasil subnetting sebagai berikut:

![image]()
### Tree
Untuk memperoleh pembagian IP yang sesuai, langkah selanjutnya adalah kita perlu menyabangkan dari hasil subnetting dari subnet terbesar ke subnet terkecilnya/subnet A. Untuk pembagiannya dapat dilihat pada tree berikut:

![image]()

### Routing

## Kesulitan yang dihadapi
1. Dalam membuat subnetting CIDR agak kebingungan pas udah masuk router FOOSHA, harus digabungkan yang mana dulu
