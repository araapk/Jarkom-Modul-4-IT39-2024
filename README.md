# Laporan Resmi Praktikum Jarkom Modul 4 2024

---
|Nama  | NRP |
|--|--|
| Johanes Edward Nathanael | 5027231067 |
| Rafika Az Zahra Kusumastuti | 5027231050 |

## Daftar Isi
- [Laporan Resmi Praktikum Jarkom Modul 4 2024](#laporan-resmi-praktikum-jarkom-modul-4-2024)
	- [Daftar Isi](#daftar-isi)
	- [Topologi Awal](#topologi-awal)
  - [Subnetting](#subnetting)
  - [Tree](#tree)
  - [Konfigurasi](#konfigurasi)

## Topologi Awal
![image](https://github.com/user-attachments/assets/beeccafd-3ac4-4727-a1a6-585a333041e6)

## Subnetting
Cara subnetting:
1. Kelompokkan dari node terjauh dari awan. Hitung router terjauh
2. Gabungkan lagi dari yang sudah dikelompokkan sebelumnya
3. dst.

![langkah1](https://github.com/user-attachments/assets/ff50c0c3-1287-4a8a-b0a4-a271e4e259d9)

### Rute
|**Nama Subnet**|**Rute**	                                                                                    |**Jumlah IP**|**Netmask**|
|---------------|---------------------------------------------------------------------------------------------------|-------------|-----------|
|A1	        |Hololive > Holo-EN > Holo-Myth > HoloPromise > Holo-Council > Switch4 > Kronil_Mumel, Bae_Fauna    |	62	  |/26        |
|A2	        |Hololive > Holo-EN > Holo-Myth > HoloPromise > Holo-Council, Project-Hope                          |	3	  |/29        |
|A3	        |Hololive > Holo-EN > Holo-Myth > HoloPromise > Project-Hope > Irya	                            |3	          |/29        |
|A4	        |Hololive > Holo-EN > Holo-Myth > Switch2 > Gura_Ame_Ina, Kiara_Calli	                            |503	  |/23        |
|A5	        |Hololive > Holo-EN > Holo-Myth > Swith2, HoloPromise	                                            |2	          |/30        |
|A6    	        |Hololive > Holo-EN > HoloAdvent	                                                            |2	          |/30        |
|A7	        |Hololive > Holo-EN > HoloAdvent > Switch5 > FuwaMoco, Shiori_Nerisaa, Biboo	                    |28	          |/27        |
|A8	        |Hololive > Holo-EN > HoloAdvent, Holo-Myth	                                                    |2	          |/30        |
|A9	        |Hololive > Holo-ID > AREA15, holoro, holoh3ro	                                                    |2	          |/30        |
|A10	        |Hololive > Holo-ID > AREA15	                                                                    |2	          |/30        |
|A11	        |Hololive > Holo-ID > AREA15 > Switch6 > Iofi, Moona, Risu	                                    |661	  |/22        |
|A12	        |Hololive > Holo-ID > holoro	                                                                    |2	          |/30        |
|A13	        |Hololive > Holo-ID > holoro > Switch7 > Ollie, Anya, Reine	                                    |34	          |/26        |
|A14	        |Hololive > Holo-ID > holoh3ro	                                                                    |2	          |/30        |
|A15	        |Hololive > Holo-ID > holoh3ro > Switch8 > Zeta, Kaela, Kobo	                                    |299	  |/23        |
|A16	        |Hololive > Holo-JP	                                                                            |2	          |/30        |
|A17	        |Hololive > Holo-JP > Switch1 > DEV_IS, GEN:0	                                                    |3	          |/29        |
|A18	        |Hololive > Holo-JP > Switch1 > DEV_IS > Re:GLOSS > Ririka_Raden, Ao, Hajime_Kanade	            |14	          |/28        |
|A19	        |Hololive > Holo-JP > Switch1 > GEN:0 > Switch3 > GEN:1, MiComet, Sora_Robo_AZKiEN	            |2045	  |/21        |
|A20	        |Hololive > Holo-JP > Switch1 > GEN:0 > Switch3 > GEN:1 > Member > FBK_Matsuri, Aki_Hachama	    |470	  |/23        |
|A21	        |Hololive > Holo-JP > Switch1 > GEN:0 > Switch3 > GEN:1 > GAMERS	                            |2	          |/30        |
|A22	        |Hololive > Holo-JP > Switch1 > GEN:0 > Switch3 > GEN:1 > GAMERS > Fubuki > Korone, Okayu, Mio	    |120	  |/25        |
|Total		|                                                                                                   |4263	  |/19        |

![langkah2](https://github.com/user-attachments/assets/759528f4-41d5-4683-897d-771b85296bd9)
![langkah3](https://github.com/user-attachments/assets/6409a3ea-0cd3-487a-a381-f87529d638cf)
![langkah4](https://github.com/user-attachments/assets/994fb5c0-0d65-4e3f-94d1-b48b41c0fb00)
![langkah5](https://github.com/user-attachments/assets/193f2672-99b4-4705-98cd-071f803ed5db)
![langkah6](https://github.com/user-attachments/assets/b5678851-4f7b-47e4-a412-322afaf8b364)
![langkah7](https://github.com/user-attachments/assets/eb5dadb6-50a7-47aa-83cc-cf332a49f032)
![langkah8](https://github.com/user-attachments/assets/b068a89b-d249-4f3a-b8fb-e1a4f482acfa)
![langkah9](https://github.com/user-attachments/assets/6539a14e-7b86-4cc3-b493-d1e14249c26e)
![langkah10 drawio](https://github.com/user-attachments/assets/befa40a9-0139-43d1-bee3-4694c9524ab9)

### Penggabungan IP - CIDR
Cara menghitung:
1. Lihat subnet gabungan, kemudian tulis subnet tersebut beserta netmasknya
2. Netmask akhir = lihat dari masing-masing netmask, kemudian cari yang paling kecil dan kurangi dengan 1
3. Poin nomor 2, kenapa dikurangi 1 karena tujuan penggabungan ip itu untuk menaikkan subnet mask ke 1 tingkat diatasnya

![Screenshot 2024-11-19 034254](https://github.com/user-attachments/assets/2c837761-dc40-4d3b-8658-55d96c744e73)
![Screenshot 2024-11-19 034308](https://github.com/user-attachments/assets/285433ae-887d-41f3-96ad-800e6c626bc7)
![Screenshot 2024-11-19 034317](https://github.com/user-attachments/assets/f00e0c5d-43b3-4651-8b59-f9d8c8e180af)

## Tree
Cara buat tree:
1. Cari subnet yang paling tinggi/induknya dari penggabungan ip yang sudah kita buat kemudian tentukan ip nya. Karena dia induk jadi ip prefixn belakangnya 0.0 karena dia mengawali dan sertakan netmasknya
2. Cabangkan dari gabungan subnet tersebut kemudian cari netmask terkecil dan prioritaskan jadi netmask terkecil. Kemudian lihat address dari netmasknya dan bagi dengan 256 jika addressnya >256 (kenapa 256 karena panjang oktet di netmask itu stop di 256. 0-255) dan dari perhitungan tersebut bisa didapatkan sisanya kemudian ditambahkan ke ip netmas terbesarnya (jika sisanya masih >256 lempar ke oktet depannya/+1 di oktet depannya) tetapi jika addressnya <256 tidak usah dibagi namun langsung masukkan ke ipnya saja
3. Bedakan warna untuk subnet A dan B atau subnet terakhir dari tree karena nanti akan dibuat untuk pembagian ip

![subnetting_tree drawio](https://github.com/user-attachments/assets/d4ad3f1e-7e06-48fa-ab67-6c7fbe958cfa)

### Pembagian IP - CIDR
Cara menghitung:
1. Lihat ip di tree dan itu sebagai network id
2. Sesuaikan netmask pada subnet mask di tree
3. Broadcast = network id + wildcard
4. Range ip = network id ditambah 1 sd broadcast dikurangi 1

| **Subnet** |  **Network ID**  |   **Netmask**   |   **Broadcast**  |           **Range IP**            |
|------------|------------------|-----------------|------------------|-----------------------------------|
|     A1     |   192.236.194.0  | 255.255.255.192 |  192.236.194.63  |  192.236.194.1 - 192.236.194.62   |
|     A2     |  192.236.194.128 | 255.255.255.248 |  192.236.194.135 | 192.236.194.129 - 192.236.194.134 |
|     A3     |   192.236.194.64 | 255.255.255.248 |  192.236.194.71  |  192.236.194.65 - 192.236.194.70  |
|     A4     |   192.236.192.0  |  255.255.254.0  |  192.236.193.255 |  192.236.192.1 - 192.236.193.254  |
|     A5     |   192.236.196.0  | 255.255.255.252 |  192.236.196.3   |  192.236.196.1 - 192.236.196.2    |
|     A6     |   192.236.200.32 | 255.255.255.240 |  192.236.200.47  |  192.236.200.33 - 192.236.200.46  |
|     A7     |   192.236.200.0  | 255.255.255.224 |  192.236.200.31  |  192.236.200.1 - 192.236.200.30   |
|     A8     |   192.236.208.0  | 255.255.255.252 |  192.236.208.3   |  192.236.208.1 - 192.236.208.2    |
|     A9     |   192.236.160.0  | 255.255.255.252 |  192.236.208.3   |  192.236.160.1 - 192.236.160.2    |
|     A10    |   192.236.192.0  | 255.255.255.252 |  192.236.192.3   |  192.236.192.1 - 192.236.192.2    |
|     A11    |   192.236.128.0  | 255.255.255.192 |  192.236.132.62  |  192.236.128.1 - 192.236.132.61   |
|     A12    |   192.236.136.64 | 255.255.255.252 |  192.236.136.67  |  192.236.136.65 - 192.236.136.66  |
|     A13    |   192.236.136.0  | 255.255.255.192 |  192.236.136.63  |  192.236.136.1 - 192.236.136.62   |
|     A14    |   192.236.146.0  | 255.255.255.252 |  192.236.146.3   |  192.236.146.1 - 192.236.146.2    |
|     A15    |   192.236.144.0  |  255.255.254.0  |  192.236.145.255 |  192.236.144.1 - 192.236.145.254  |
|     A16    |   192.236.64.0   | 255.255.255.252 |   192.236.64.3   |    192.236.64.1 - 192.236.64.2    |
|     A17    |   192.236.32.0   | 255.255.255.248 |   192.236.32.7   |    192.236.32.1 - 192.236.32.6    |
|     A18    |   192.236.16.0   | 255.255.255.240 |  192.236.16.15   |   192.236.16.1 - 192.236.16.14    |
|     A19    |    192.236.0.0   |  255.255.248.0  |  192.236.7.255   |    192.236.0.1 - 192.236.7.254    |
|     A20    |    192.236.8.0   |  255.255.254.0  |  192.236.9.255   |    192.236.8.1 - 192.236.9.254    |
|     A21    |   192.236.10.128 | 255.255.255.252 |  192.236.10.131  |  192.236.10.129 - 192.236.10.130  |
|     A22    |   192.236.10.0   | 255.255.255.128 |  192.236.10.127  |  192.236.10.1 - 192.236.10.126    |
