# Laporan Resmi Jarkom Modul 4
## Kelompok IT01
| NRP | Nama |
| ------ | ------ |
| 5027221042 |Nicholas Marco Weinandra |
| 5027221052 | Mochamad Zidan Hadipratama |

# Topologi

# VLSM
## Pembagian Subnet
- Dari topologi yang telah dibuat, akan dibagi menjadi 21 subnet sebagai berikut:
<img width="1572" alt="prak4jarkom" src="https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/faabf537-d351-4a0e-9940-14b7e4a63a66">

## Tree VLSM
- Perhitungan Pembagian Network ID dan Mask dilakukan berdasarkan jumlah host yang dibutuhkan untuk setiap subnet. Untuk mempermudah perhitungan, dibuat tree VLSM sebagai berikut
![VLSM TREE](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/e7cba8ca-f9fa-45e7-87cf-543d8eba28d1)


## Tabel Rute
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/51f0088c-5442-4f32-b545-bbe2d290be66)

## VLSM Routing - Konfigurasi IP
| SUBNET  | NODE               | IP            | SUBNET MASK     | GATEAWAY      |
| ------- | ------------------ | ------------- | --------------- | -------      |
| `A1`    | JAWA               | 10.64.21.177  | 255.255.255.252 |              |
|         | SUMATERA           | 10.64.21.178  | 255.255.255.252 |              |
| `A2`    | SUMATERA           | 10.64.21.65   | 255.255.255.224 |              |
|         | SUMATERA-UTARA     | 10.64.21.66   | 255.255.255.224 |              |
|         | SAMOSIR            | 10.64.21.67   | 255.255.255.224 | 10.64.21.65  |
|         | SIBANDANG          | 10.64.21.68   | 255.255.255.224 | 10.64.21.65  |
| `A3`    | SUMATERA-UTARA     | 10.64.21.181  | 255.255.255.252 |              |
|         | ACEH               | 10.64.21.182  | 255.255.255.252 |              |
| `A4`    | ACEH               | 10.64.20.1    | 255.255.255.128 |              |
|         | BERAWANG-TAMPU     | 10.64.20.2    | 255.255.255.128 | 10.64.20.1   |
|         | ENANG-ENANG        | 10.64.20.3    | 255.255.255.128 | 10.64.20.1   |
|         | STARLAND           | 10.64.20.4    | 255.255.255.128 | 10.64.20.1   |
| `A5`    | ACEH               | 10.64.21.129  | 255.255.255.224 |              |
|         | SABANG             | 10.64.21.130  | 255.255.255.224 | 10.64.21.129 |
|         | LAMBARO            | 10.64.21.131  | 255.255.255.224 | 10.64.21.129 |
| `A6`    | SUMATERA           | 10.64.21.185  | 255.255.255.252 |              |
|         | LAMPUNG            | 10.64.21.186  | 255.255.255.252 |              |
| `A7`    | LAMPUNG            | 10.64.19.1    | 255.255.255.0   |              |
|         | SEBESI             | 10.64.19.2    | 255.255.255.0   | 10.64.19.1   |
|         | SEBUKU             | 10.64.19.3    | 255.255.255.0   | 10.64.19.1   |
| `A8`    | JAWA               | 10.64.21.189  | 255.255.255.252 |              |
|         | KALIMANTAN         | 10.64.21.190  | 255.255.255.252 |              |
| `A9`    | KALIMANTAN         | 10.64.21.193  | 255.255.255.252 |              |
|         | KALIMANTAN-UTARA   | 10.64.21.194  | 255.255.255.252 |              |
| `A10`   | KALIMANTAN-UTARA   | 10.64.18.1    | 255.255.255.0   |              |
|         | SELIMAU            | 10.64.18.2    | 255.255.255.0   | 10.64.18.1   |
| `A11`   | KALIMANTAN-UTARA   | 10.64.21.197  | 255.255.255.252 |              |
|         | KALIMANTAN-TIMUR   | 10.64.21.198  | 255.255.255.252 |              |
| `A12`   | KALIMANTAN-TIMUR   | 10.64.16.1    | 255.255.254.0   |              |
|         | BANGKIRAI          | 10.64.16.2    | 255.255.254.0   | 10.64.16.1   |
|         | LAMARU             | 10.64.16.3    | 255.255.254.0   | 10.64.16.1   |
| `A13`   | KALIMANTAN-TIMUR   | 10.64.21.201  | 255.255.255.252 |              |
|         | KALIMANTAN-SELATAN | 10.64.21.202  | 255.255.255.252 |              |
| `A14`   | KALIMANTAN-SELATAN | 10.64.21.97   | 255.255.255.224 |              |
|         | ANGSANA            | 10.64.21.98   | 255.255.255.224 | 10.64.21.97  |
| `A15`   | KALIMANTAN-SELATAN | 10.64.0.1     | 255.255.248.0   |              |
|         | BAJUIN             | 10.64.0.2     | 255.255.248.0   | 10.64.0.1    |
|         | TAKISUNG           | 10.64.0.3     | 255.255.248.0   | 10.64.0.1    |
|         | BATAKAN            | 10.64.0.4     | 255.255.248.0   | 10.64.0.1    |
| `A16`   | JAWA               | 10.64.21.205  | 255.255.255.252 |              |
|         | SULAWESI           | 10.64.21.206  | 255.255.255.252 |              |
| `A17`   | SULAWESI           | 10.64.20.129  | 255.255.255.128 |              |
|         | MALUKU-UTARA       | 10.64.20.130  | 255.255.255.128 |              |
|         | GORONTALO          | 10.64.20.131  | 255.255.255.128 | 10.64.20.129 |
|         | MARISA             | 10.64.20.132  | 255.255.255.128 | 10.64.20.129 |
| `A18`   | MALUKU-UTARA       | 10.64.8.1     | 255.255.248.0   |              |
|         | MOROTAI            | 10.64.8.2     | 255.255.248.0   | 10.64.8.1    |
|         | TOBELO             | 10.64.8.3     | 255.255.248.0   | 10.64.8.1    |
|         | TERNATE            | 10.64.8.4     | 255.255.248.0   | 10.64.8.1    |
| `A19`   | SULAWESI           | 10.64.21.161  | 255.255.255.248 |              |
|         | BELAWA             | 10.64.21.162  | 255.255.255.248 |              |
|         | MAKASAR            | 10.64.21.163  | 255.255.255.248 |              |
| `A20`   | MAKASAR            | 10.64.21.169  | 255.255.255.248 |              |
|         | GALESONG           | 10.64.21.170  | 255.255.255.248 | 10.64.21.169 |
|         | TOPEJAWA-TAKALAR   | 10.64.21.171  | 255.255.255.248 | 10.64.21.169 |
| `A21`   | BELAWA             | 10.64.21.1    | 255.255.255.192 |              |
|         | MADINI             | 10.64.21.2    | 255.255.255.192 | 10.64.21.1   |
|         | BARU               | 10.64.21.3    | 255.255.255.192 | 10.64.21.1   |

## Konfigurasi IP VLSM
### Router
- Untuk konfigurasi Router, pertama assign IP dan Gateaway masing-masing router di port Ethernet yang sesuai dengan subnet pada tabel diatas.
- Contoh pada router Sumatera, kemudian lakukan ke semua router lainnya
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/a51d8d5d-ad6a-4f00-9362-44ab86e14494)

### Client & Server
- Konfigurasikan IP, Mask, dan Gateaway sesuai dengan tabel diatas.
- Untuk server, tambahkan DNS Server sesuai dengan Subnet Mask
- Contoh pada client Samosir dan server Sebesi , kemudian lakukan ke semua Client lainnya
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/f7d08fa1-da2d-47e8-a4d8-81cb03b77616)
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/c56fe1bd-ae2c-4788-9ef8-fb0853a5f202)

## Konfigurasi Routing
### Aceh
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/e63622f4-64a1-4969-8416-1a387f4f87b9)
0.0.0.0 berarti mengambil semua pesan dan diarahkan ke next hop Sumatera Utara

### Lampung
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/40ee7734-ce53-41f8-8c86-6d0265e52852)
Next hop ke Sumatera

### Sumatera Utara
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/9c00a222-9f70-49f4-ae07-9f00e6b56297)
Pada Sumatera Utara, kita mengarahkan ke subnet 20.0 (A4) dan 21.187 (A5) dengan next hop ke Aceh

### Sumatera
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/48717136-74d0-4796-8f21-5ccec133f635)
- Pada Sumatera, kita mengarahkan ke subnet 20.0 (A4) dan 21.187 (A5) dengan next hop ke Sumatera Utara
- Subnet 19.0 (A7) dengan next hop ke Lampung
- Subnet 0.0.0.0 (A2) dengan next hop ke Jawa

### Kalimantan Selatan
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/a6ace4e0-d99f-4211-a702-7f94e7a0d75c)
Next hop ke Kalimantan Timur

### Kalimantan Timur
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/dedfe046-4183-4f0d-9f01-9dc44a194008)
- Mengarahkan subnet 21.96(A14) dan 0.0 (A15) dengan next hop ke Kalimantan Selatan
- Subnet 0.0.0.0 (A12) dengan next hop ke Kalimantan Utara

### Kalimantan Utara
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/95dd82f3-751e-4788-bc32-5a09bdf6b280)
- Mengarahkan subnet 21.96 (A14), 0.0 (A15), 16.0 (A12) dengan next hop ke Kalimantan Timur
- Subnet 0.0.0.0 (A10) dengan next hop ke Kalimantan

### Kalimantan
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/2059489e-1be8-4617-8c9d-01c5c48175e2)
- Mengarahkan subnet 21.96 (A14), 0.0 (A15), 16.0 (A12), 18.0 (A10) dengan next hop ke Kalimantan Utara
- Subnet 0.0.0.0 dengan next hop ke Jawa

### Belawa
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/94eb0ba5-2f41-4975-a7b0-53e687ec670d)
Next hop ke Sulawesi

### Makassar
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/c6c1d87f-8703-41a7-b8b1-b7cfb8003474)
Next hop ke Sulawesi

### Maluku Utara
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/2cda504a-4400-4db5-bf45-00cffde6b048)
Next hop ke Sulawesi

### Sulawesi
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/98268aab-0d8d-4665-b89f-c783cfdeb5c5)
- Mengarahkan subnet 8.0 (A18) dengan next hop ke Maluku Utara
- Mengarahkan subnet 21.0 (A21) dengan next hop ke Belawa
- Mengarahkan subnet 21.168 (A20) dengan next hop ke Makassar
- Mengarahkan subnet 0.0.0.0 (A17) dengan next hop ke Jawa

### Jawa
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/b19418bd-a4fe-4159-a7cd-e41b07e09a8a)
![image](https://github.com/nicholasmarco27/jarkom-Modul-4-2024-IT01/assets/80316798/03448087-6932-4c46-b62d-d5e7ccf6db4f)
Jawa akan bertugas untuk membagi dan mensortir request yang masuk pada setiap subnet, kemudian mengarahkan antara ke Sumatera, Kalimantan, atau Sulawesi
