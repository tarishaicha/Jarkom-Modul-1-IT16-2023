# Jarkom-Modul-1-IT16-2023

## Soal 1
![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/9f2705a1-714f-4bdd-8576-5b93b8133bb8)

Untuk menemukan sequence number (raw) dan acknowledge number (raw) pada paket yang menunjukkan aktivitas pengunggahan (upload) file dengan protokol FTP, diperlukan analisis capture packet dalam Wireshark.

Pertama-tama lakukan filter dengan `ftp || ftp-data`. Dalam hal ini, `ftp || ftp-data` adalah filter yang mengidentifikasi dan menyaring paket-paket yang terkait dengan FTP, baik untuk perintah kontrol maupun transfer data. Lalu setelah terfilter, carilah format data STOR. Dikarena format STOR digunakan untuk pengunggahan suatu file ke FTP server.

![WhatsApp Image 2023-09-18 at 8 26 12 PM](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/15f84159-2dff-4592-bf1e-6f0f70dcd335)

a). Lalu, akan ditemukan sequence number raw pada aktivitas tersebut yaitu  258040667 

b). Lalu, acknowledgement number rawnya yaitu 1044861039

Setelah itu, lakukan hal yang sama pada aktivitas response tersebut

![WhatsApp Image 2023-09-18 at 8 30 17 PM](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/7dceb3c3-136d-4109-979a-55685e37c814)

c). Lalu, akan ditemukan sequence number raw pada aktivitas response tersebut yaitu 1044861039

d). Lalu, acknowledgement number rawnya yaitu 258040667 

![WhatsApp Image 2023-09-18 at 8 29 15 PM](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/c64fed2d-31d0-4ca1-9a27-a8b99f3be461)

Setelah itu, lakukan `nc` pada ip yang disediakan dan masukan jawaban yang telah diketahui. Maka, akan ditemukan flagnya yaitu Jarkom2023{y0u_r_g00d_4t_4dr3ssing_MxIrFsF93371059}

## Soal 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/48c527f6-186c-4fdf-96e9-b0317763aefc)
Filter dengan memasukan Ip Address yang dicari yang telah diberikan pada soal

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/eff582ff-f610-43d8-b492-43533d4b53d1)
Follow stream IP addressnya lalu, tertulis Server: gunicorn

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/065aa1ac-f42c-46a6-a599-6f5dd7bb2238)
Nama Servernya gunicorn, dan ditemukan flagnya

## Soal 3
![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/88af8e97-bce0-4a30-8838-d85660c6222f)

Gunakan `(ip.src == 239.255.255.250 || ip.dst == 239.255.255.250) && (udp.port == 3702)` , filter ini akan mencari semua paket dengan IP source atau destination address 239.255.255.250 dan port 3702. Lalu, setelah terfilter hitung paket IP yang ada.

![WhatsApp Image 2023-09-18 at 7 29 43 PM (1)](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/09f7f713-a7bc-40c9-a6a9-cc12bf11b091)

a). Maka ditemukan jumlah paketnya ada 21.

b). Protokol yang digunakan adalah UDP.

![WhatsApp Image 2023-09-18 at 7 34 08 PM](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/d7101b37-5115-4c2a-9e3a-39f4f6199087)

Buka wsl dan lakukan `nc` sesuai dengan ip soal lalu isi dengan jawaban yang sudah ditemukan. Maka, akan ditemukan flagnya = Jarkom2023{4nalyz3_is_9224_BmSjBkCmDmS_gr3at}

## Soal 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

Pertama-tama, scroll untuk menemukan paket ke 130. Lalu, klik kanan dan buka seluruh text yang ada dikiri box. Maka akan ditemukan checksum yang tertera yaitu 0x18e5.

![WhatsApp Image 2023-09-18 at 8 05 52 PM](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/91f58c17-54e9-45f1-bd60-ec628e1a6dfe)

Buka wsl dan lakukan `nc` sesuai dengan ip soal lalu isi dengan jawaban yang sudah ditemukan. Maka, akan ditemukan flagnya = Jarkom2023{ch3cksum_is_u5eful_0xa7y6}

## Soal 5
![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/7b2c6b21-7e37-4529-9c26-cb0a14c17131)

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/05e89de7-f242-48c9-912b-792f960a3756)
Filter menjadi SMTP lalu cari passwordnya dan follow stream

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/37da8d2b-1f86-4483-a417-7cd4230b4ad4)
Telah ditemukan password untuk zipfilenya, passwordnya di dekripsi dengan base 64 lalu ditemukan hasi passwornya yaitu “5implePas5word”

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/2370a010-0ff6-460b-b73a-fcdc264b7b2c)
Masukan Password pada file zip untuk mendapatkan nc untuk menjawab pertanyaan

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/4ecfe12c-9145-4e6d-a9d9-236bb73a193e)
Masukan jawaban yaitu, a.60, b.25, c.74.53.140.153 dan akhirya ditemukan flagnya

## Soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

Pada soal ini, kita diminta untuk menghitung jumlah packet yang menuju `IP 184.87.193.88`.
Menurut modul 1 yang telah diberikan, kita harus memfilter hanya untuk IP yang dituju (destination)

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/81ead330-349f-4059-8cea-24e7c32b6622)

Maka, untuk menampilkan semua paket yang menuju alamat IP 184.87.193.88. Dapat menggunakan kueri filter `ip.dst == 184.87.193.88`. Maka, akan terlihat hasil filter sebagai berikut. 

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/b96913d2-421d-4226-b499-b040f809ce50)
Lalu, kita tinggal menghitung jumlah paket yg ada. Yang mana jumlahnya terdapat 6 paket.

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/d2c8247d-2e1d-4149-9e95-099b73bbbbdb)

Buka wsl dan lakukan `nc` sesuai dengan ip soal lalu isi dengan jawaban yang sudah ditemukan. Maka, akan ditemukan flagnya = Jarkom2023{uVWiqCD5mE0652D3HY_4n0th3r_f1lt3ring}

## Soal 8
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

Untuk mengambil semua paket yang menuju ke port 80 dengan Wireshark dan jika terdapat lebih dari satu port 80 yang digunakan, dapat digunakan filter `tcp.dstport == 80 || udp.dstport == 80` Filter ini akan mencakup semua paket TCP dan UDP yang menuju ke port 80. Selain itu, jika ada beberapa koneksi yang menggunakan port 80, paket akan diurutkan sesuai dengan abjad.
![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/7b0fc484-4b8a-47c7-a3e0-c96b51a4f4bb)


![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/1d3dd277-c532-4b7d-a63b-35f1cae7aa7d)

Buka wsl dan lakukan `nc` sesuai dengan ip soal lalu isi dengan jawaban yang sudah ditemukan. Maka, akan ditemukan flagnya = Jarkom2023{qu3ryyyyying_088427_PxRvPvEzRvP_15_fun}

## Soal 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/e9d98bb7-6ae1-43c0-8c76-c010a9980ebf)

Membuat query `ip.src == 10.51.40.1 && ip.dst != 10.39.55.34`
Dimana `ip.src == 10.51.40.1` Ini akan menampilkan paket yang berasal dari alamat `IP 10.51.40.1` sebagai sumber dan `ip.dst != 10.39.55.34` Ini akan memastikan bahwa paket tidak menuju ke alamat `IP 10.39.55.34` sebagai tujuan.

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/fd16e4ed-5aba-42ed-8d7a-88d6d3a39bb0)
Setelah memasukanya telah didapatkan flagnya.

## Soal 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/dedca0fa-a9c8-4d80-8e14-2b7972e29a50)

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/3d97c048-4115-4f4e-931d-ae28723cbd47)

Pertama filter dengan kata kunci Telnet, lalu cek username dan password yang tertera engan memfollow streamnya 

![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/d7e410b4-466d-4d38-a704-657b669f1d5e)

Ditemukan Usernamenya dhafin dengan password keyanganyak0k0
![image](https://github.com/tarishaicha/Jarkom-Modul-1-IT16-2023/assets/107459188/1f272391-f8eb-44fd-8d46-3beb9e648464)

Setelah diinput dengan format, ditemukan flagnya
