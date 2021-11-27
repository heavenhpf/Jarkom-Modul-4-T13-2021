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
Untuk VLSM, kami membuat topologinya pada Cisco Packet Tracer. Pertama, buat topologi sesuai dengan soal.
![image](https://user-images.githubusercontent.com/73151823/143683184-32271052-3510-4adc-8140-96e663d8fcc7.png)

Pengaturan router dibuat sesuai dengan tree, sebagai berikut:
#### FOOSHA
- IP pada interface FOOSHA yang mengarah ke BLUENO (1000 Host)
![image](https://user-images.githubusercontent.com/73151823/143683318-8a2a9fba-3f8d-44da-adb1-873c9c6ca830.png)

- IP pada interface FOOSHA yang mengarah ke DORIKI
![image](https://user-images.githubusercontent.com/73151823/143683324-0bad07bf-98bf-494b-9917-7bfee85ae1c8.png)

- IP pada interface FOOSHA yang mengarah ke WATER7
![image](https://user-images.githubusercontent.com/73151823/143683347-0f2339ae-04cb-45fb-accc-4cd44d20cd0f.png)

- IP pada interface FOOSHA yang mengarah ke GUANHAO
![image](https://user-images.githubusercontent.com/73151823/143683356-5d804b09-6945-4794-870d-e604d40c2669.png)

#### BLUENO (1000 Host)
- IP pada interface BLUENO yang mengarah ke FOOSHA
![image](https://user-images.githubusercontent.com/73151823/143683445-142f4c5f-3d77-4ff5-b781-19b98fa75097.png)

#### DORIKI
- IP pada interface DORIKI yang mengarah ke FOOSHA
![image](https://user-images.githubusercontent.com/73151823/143683473-f046737b-2d55-45c6-9391-20aee3e487bc.png)

#### WATER7
- IP pada interface WATER7 yang mengarah ke FOOSHA
![image](https://user-images.githubusercontent.com/73151823/143683859-53259d78-5415-4411-b4fa-52a59f11ec2c.png)

- IP pada interface WATER7 yang mengarah ke CIPHER (700 Host)
![image](https://user-images.githubusercontent.com/73151823/143683870-185d7d10-b842-450c-8554-8e8439cca32e.png)

- IP pada interface WATER7 yang mengarah ke FOOSHA (PUCCI)
![image](https://user-images.githubusercontent.com/73151823/143683883-ec46bfc9-cce0-433f-9f63-e641402ea4df.png)

#### GUANHAO
- IP pada interface GUANHAO yang mengarah ke FOOSHA
![image](https://user-images.githubusercontent.com/73151823/143684002-9829c688-9c63-4b7b-b0df-3ce2bec39ade.png)

- IP pada interface GUANHAO yang mengarah ke JABRA (520 Host)
![image](https://user-images.githubusercontent.com/73151823/143684029-5639965b-1cdd-4993-8fc0-a034c4e94e3a.png)

- IP pada interface GUANHAO yang mengarah ke MAIN GATE (500 Host) dan ALABASTA
![image](https://user-images.githubusercontent.com/73151823/143684024-344fb038-8127-48d2-8c8c-30c238797512.png)

- IP pada interface GUANHAO yang mengarah ke OIMO
![image](https://user-images.githubusercontent.com/73151823/143684036-14a7b42c-c4fb-430f-9ae2-34c9c6e96050.png)

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
