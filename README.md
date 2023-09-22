# Kelompok IT10 #

## Anggota: ##
1. Caroline Permatasari Pramestita Gondo Kusumo (5027211048)
2. Vira Datry Maulydina (5027211050)

## Laporan Resmi Modul 1 ##
1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP.
a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?     
b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?  
c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?   
d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
- Filter menggunakan “”ftp || ftp-data” .
- Di sebelah sebelah kiri bawah kita dapat membuka bagian TCP. Di bagian tersebut kita dapat menemukan sequence number dan acknowledge number masing-masing paket Paket request STOR , lalu di double tap.

![dokumentasi-soalno1a](https://i.ibb.co/M2tKCYY/soal-no-1-a.jpg)
- Cari Sequence Number dan Acknowledgement Number untuk mengidentifikasi atau mengurutkan entitas.
![dokumentasi-soalno1b](https://i.ibb.co/6wFG9H8/dokumentasi-soal1-C.jpg)
- Kembali ke page sebelumnya, lalu double tap di “Response 150” 
- Cari Sequence Number dan Acknowledgement Number
![dokumentasi-soalno1c](https://i.ibb.co/Tcfbk7V/dokumentasi-soal1-D.jpg)
- Setelah itu Jawaban di masukan ke dalam nc, dan flag akan di tampilkan Jarkom2023{y0u_r_g00d_4t_4dr3ssing_DnErJzD91329577}
![dokumentasi-flagno1](https://i.ibb.co/gRQrPwV/dokumentasi-flagno1.jpg)


2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
- Kita perlu menganalisis paket-paket HTTP. Kita dapat melakukan ini dengan mengetikkan "http" dalam kotak pencarian di bagian atas jendela Wireshark. untuk menganalisis lalu lintas web dalam sesi jaringan, yang bisa sangat berguna dalam pemecahan masalah, pemantauan, dan analisis aplikasi web dan layanan web.
- Setelah itu kita klik kanan untuk follow TCP Stream. Dengan mengklik opsi "Follow TCP Stream," dapat melihat seluruh percakapan atau aliran data antara dua entitas (biasanya klien dan server) dalam tcp tersebut.
![dokumentasi-soalno2](https://i.ibb.co/mXkrjYp/dokumentasi-soal2.jpg)
- Lalu password (gunicorn) akan muncul, dan masukkan kedalam nc untuk mendapatkan flagnya.
![dokumentasi-soalno2A](https://i.ibb.co/n0SHSyR/dokumentasi-soal2-A.jpg)
- Setelah flag muncul, submit flag Jarkom2023{9unic0rn_1s_54K9cTAo517xmPz_c00l}.
![dokumentasi-flagno2](https://i.ibb.co/0mZSXvp/dokumentasi-flagno2.jpg)

3.
A. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

B. Protokol layer transport apa yang digunakan?
- Yang pertama melakukan filter “ip.addr==239.255.255.250 && udp.port==3702”
- Lalu hitung ada berapa row.
![dokumentasi-soalno3A](https://i.ibb.co/XtNCF5p/dokumentasi-soal3-A.jpg)
- Lalu jawab pertanyaan tampil pada layar wireshark, dan setelah itu dimasukan pada terminal yang akan memunculkan flagnya dan di sumbit.
![dokumentasi-soalno3A](https://i.ibb.co/kKd2MmX/dokumentasi-flagno3.jpg)


4. Untuk menjawab pertanyaan-pertanyaan tersebut berdasarkan file pcap yang diberikan, Kita dapat menggunakan perangkat lunak pemrosesan paket seperti Wireshark.
- Buka file pcap dan dia bakal ke direct ke wireshark dan mencari Filter “frame.number==130”  digunakan untuk memilih dan menampilkan paket jaringan yang memiliki nomor frame (frame number) tertentu dalam kumpulan paket yang sedang dianalisis.
![dokumentasi-soalno4A](https://i.ibb.co/TkFjtGp/dokumentasi-soal4-A.jpg)
- Setelah itu kita melakukan double tap untuk mencari nilai pada “checksum”
![dokumentasi-soalno4B](https://i.ibb.co/TmFnXN6/dokumentasi-soal4-B.jpg)
- Masukan checksum pada nc, lalu pada terminal akan memunculkan flagnya.
![dokumentasi-soalno4C](https://i.ibb.co/KXXGdyx/dokumentasi-flagno4.jpg)


7. Berapa jumlah packet yang menuju IP 184.87.193.88?
- Pertma kita akan melakukan pencarian pada filter “ip.dst==184.87.193.88” sebagai baris atau entri individu dalam tampilan paket. Setiap baris ini mewakili satu paket jaringan dalam sesi penangkapan yang sedang dianalisis. Baris atau "row" ini berisi informasi rinci tentang paket, termasuk nomor frame, waktu perekaman, sumber dan tujuan, protokol yang digunakan, dan data lain yang terkait dengan paket tersebut.
![dokumentasi-soalno7A](https://i.ibb.co/ZSf496Y/dokumentasi-soal7-A.jpg)
- Setelah itu kita menghitung row yang ada pada layar wireshark, setelah menentukan row masukan pada nc untuk mendapatkan flagnya.
![dokumentasi-soalno7B](https://i.ibb.co/Fkpn3pk/dokumentasi-flag7.jpg)

8. Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
- pertama kita masukan kueri “tcp.dstport == 80 or udp.dstport == 80” ke nc.
- Setelah disubmit, flag akan keluar Jarkom2023{qu3ryyyyying_043051_QiDxQlCzRjD_15_fun}
![dokumentasi-flagno8](https://i.ibb.co/dfRn1w4/dokumentasi-flagno8.jpg)

9. Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
- Langkah pertama masukkan kueri “ip.src==10.51.40.1 && ip.dst!=10.39.55.34”
- Setelah memasukan queri dan menemukan jawaban di masukan ke nc untuk mendapatkan flagnya  Jarkom2023{y3s_its_RlSjOjSiNlQ_qu3ry1ng}
![dokumentasi-flagno9](https://i.ibb.co/p3YntMw/dokumentasi-flagno9.jpg)


10. Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
- Ketikan filter “telnet” untuk dimasukan.  jika kita memasukan filter 'telnet' melihat hanya paket-paket yang terkait dengan sesi Telnet, termasuk permintaan masuk, perintah yang dikirim oleh pengguna, dan respon dari sistem atau perangkat jarak jauh tersebut.
- Setelah itu kita klik kanan untuk follow TCP Stream. untuk menemukan jawaban yang akan dimasukan untuk jawaban nc.
![dokumentasi-flagno10](https://i.ibb.co/61FXjxc/dokumentasi-flagno10.jpg)

























