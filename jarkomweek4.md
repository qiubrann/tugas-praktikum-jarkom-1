## **Laporan Jaringan Komputer WEEK 4** 

NAMA : ANANDHAKA GHIBRAN MAS NIM : 103072400135 

## **DNS** 

Tujuan Praktikum : 

1. Mahasiswa dapat menginvestigasi cara kerja DNS menggunakan Wireshark 

## **NSLOOKUP** 

1. Jalankan nslookup untuk mendapatkan alamat IP dari server web di Asia. Berapa alamat IP server tersebut? 

Jawab : IP : 2404.6800.4003.c02.5e.142.250.4.94 

2. Jalankan nslookup agar dapat mengetahui server DNS otoritatif untuk universitas di Eropa Jawab : menggunakkan universitas oxford 

3. Jalankan nslookup untuk mencari tahu informasi mengenai server email dari Yahoo! Mail melalui salah satu server yang didapatkan di pertanyaan nomor 2. Apa alamat IP-nya? Jawab : pada mta5.am0.yahoodns.net salah satu ip nya adalah : 67.195.204.79 

## **IPCONFIG** 

IPCONFIG/ALL : 

IPCONFIG/DISPLAYDNS 

## **Tracing DNS dengan Wireshark** 

Filter tracing DNS sesuai dengan IPaddress : 

Filter DNS : 

## Soal : 1. Cari pesan permintaan DNS dan balasannya. Apakah pesan tersebut dikirimkan melalui UDP atau TCP? Jawab : Pesan DNS dikirim menggunakan UDP (User Datagram Protocol), bukan TCP. 

2. Apa port tujuan pada pesan permintaan DNS? Apa port sumber pada pesan balasannya? Jawab : Port tujuan pada pesan permintaan DNS adalah 53, sedangkan port sumber pada pesan balasan juga 53. 

## 3. Pada pesan permintaan DNS, apa alamat IP tujuannya? Apa alamat IP server DNS lokal anda (gunakan ipconfig untuk mencari tahu)? Apakah kedua alamat IP tersebut sama? 

**==> picture [144 x 12] intentionally omitted <==**

**----- Start of picture text -----**<br>
Jawab : Ya, sama 182.8.64.11<br>**----- End of picture text -----**<br>


4.Periksa pesan permintaan DNS. Apa “jenis” atau ”type” dari pesan tersebut? Apakah pesan permintaan tersebut mengandung ”jawaban” atau ”answers”? Jawab : Jenis (type) dari pesan DNS adalah A (Address Record), yang digunakan untuk meminta alamat IP dari suatu domain. Pesan permintaan DNS tidak mengandung jawaban (answers), karena hanya berisi 

**==> picture [131 x 12] intentionally omitted <==**

**----- Start of picture text -----**<br>
permintaan ke server DNS.<br>**----- End of picture text -----**<br>


4. Periksa pesan balasan DNS. Berapa banyak ”jawaban” atau ”answers” yang terdapat di dalamnya? Apa saja isi yang terkandung dalam setiap jawaban tersebut? Jawab : Ada 7 jawaban (answers) 

## 5. Perhatikan paket TCP SYN yang selanjutnya dikirimkan oleh host Anda. Apakah alamat IP 

pada paket tersebut sesuai dengan alamat IP yang tertera pada pesan balasan DNS? Jawab : Alamat IP pada paket TCP SYN adalah 2606:4700::6810... (IPv6), sedangkan alamat IP pada hasil DNS sebelumnya adalah IPv4 (misalnya 74.xxx.xxx.xxx). Oleh karena itu, kedua alamat IP tersebut tidak sama, karena sistem dapat menggunakan IPv6 atau IPv4 tergantung konfigurasi jaringan. 

6. Halaman web yang sebelumnya anda akses (http://www.ietf.org) memuat beberapa gambar. Apakah host Anda perlu mengirimkan pesan permintaan DNS baru setiap kali ingin mengakses suatu gambar? 

Jawab : Tidak, host tidak perlu mengirimkan permintaan DNS baru setiap kali mengakses suatu gambar. Hal ini karena alamat IP dari domain tersebut sudah disimpan dalam DNS cache, sehingga dapat langsung digunakan tanpa perlu melakukan query DNS kembali. 

## **Pengambilan paket NSLOOOKUP pada** ~~SS~~ **www.mit.edu** 

**==> picture [28 x 10] intentionally omitted <==**

**----- Start of picture text -----**<br>
Soal :<br>**----- End of picture text -----**<br>


1. Apa port tujuan pada pesan permintaan DNS? Apa port sumber pada pesan balasan DNS? Jawab : Port tujuan pada permintaan DNS adalah 53, dan port sumber pada balasan DNS juga 53. 

2. Ke alamat IP manakah pesan permintaan DNS dikirimkan? Apakah alamat IP tersebut merupakan default alamat IP server DNS lokal Anda? Jawab : Ya, sama Pesan permintaan DNS dikirim ke alamat IP 182.8.64.11. Berdasarkan hasil ipconfig, alamat IP tersebut merupakan DNS server lokal yang digunakan. Oleh karena itu, kedua alamat IP tersebut sama. 

3. Periksa pesan permintaan DNS. Apa ”jenis” atau ”type” dari pesan tersebut? Apakah pesan tersebut mengandung ”jawaban” atau ”answers”? Jawab : Jenis pesan DNS adalah A (Address Record). Pesan permintaan tidak mengandung jawaban (answers), karena hanya berisi permintaan 

## alamat IP. A WiFi - ao x File Edit View Go Capture Analyze Statistics Telephony Wireless Tools Help 4040 MBBB RL eVTSFsRBaacaeas Wi ip.adar== 192.168.1.57 Goey+ No. Time Source Destination Protoco Lengti Info = **65** 89 **43** .04253.1238 **5** 4...57.. **192.168.1.57** 239182 **.** 255.255.2508.64.11 DNSSSDP 21271 M-SEARCHStandard query* HTTP/1.1@x3@3e HTTPS www.mit.edu | 660 43.1241715.._192.168.1.57 182.8.64.11 DNS 71 Standard query @xb320 AAAA www.mit.edu = 661 43.1244648.. 192.168.1.57 182.8.64.11 DNS 71 Standard query @xb4f7 A www.mit.edu = | 662 43.1315333.. 192.168.1.57 182.8.64.11 DNS 71 Standard query @xdebd AAAA www.mit.edu — H 663 43.1317214.. 192.168.1.57 182.8.64.11 DNS 71 Standard query @x4cb3 A www.mit.edu =I Hl 664 43.1327857.. 192.168.1.57 182.8.64.11 DNS 71 Standard query @x13ac HTTPS www.mit.edu = **H** l **66** 56 **43.13** 30167..31555.. **192.168.1.57 182.8.64.11 DNS 71 Standard query @x** 528b@9be **A** AAAwww.mit.eduwww.mit.edu 4 Hl 667 43.2544996.. 182.8.64.11 192.168.1.57 DNS 203 Standard query response @xb32@ AAAA www.mit.edu CNAME www.mit.edu.edgekey.net CNAME e9566.dscb.akamaiedge.net A || 668669 43.2544996..43.2546139.. 182.8.64.11182.8.64.11 192.168.1.57192.168.1.57 DNSDNS 203203 StandardStandard queryquery responseresponse @x528bOxdebd AAAAAAAA www.mit.eduwww.mit.edu CNAMECNAME www.mit.edu.edgekey.netwww.mit.edu.edgekey.net CNAMECNAME e9566.dscb.akamaiedge.nete9566.dscb.akamaiedge.net ‘aA——} iH 670671 43.2546139..43.2546139.. 182.8.64.11182.8.64.11 192.168.1.57192.168.1.57 DNSDNS 225225 StandardStandard queryquery responseresponse @x13ac0x303e HTTPSHTTPS www.mit.eduwww.mit.edu CNAMECNAME www.mit.edu.edgekey.netwww.mit.edu.edgekey.net CNAMECNAME e9566.dscb.akamaiedge.nete9566.dscb.akamaiedge.net [|-—4 Jei 673672 43.2546139...43.2546139.. 182.8.64.11182.8.64.11 192.168.1.57192.168.1.57 DNSDNS 163163 StandardStandard queryquery responseresponse Oxb4f7@x4cb3 AA www.mit.eduwww.mit.edu CNAMECNAME www.mit.edu.edgekey.netwww.mit.edu.edgekey.net CNAMECNAME e9566.dscb.akamaiedge.nete9566.dscb.akamaiedge.net AA 23—J2 | 674 43.2546139.. 182.8.64.11 192.168.1.57 DNS 163 Standard query response @x@9be A www.mit.edu CNAME www.mit.edu.edgekey.net CNAME e9566.dscb.akamaiedge.net A a 4 677 43.2557838.. 192.168.1.57 13.35.1.10 TCeP 54 59294 » 443 [FIN, ACK] Seq=2 Ack=1 Win=255 Len=0 > = [Stream Packet Number: 1] ie bc bd 84 23 db 9a 24 b2 b9 af cf 7d 08 0@ 45 00 #-$ }--E » [Timestamps] 00 39 56 f7 00 00 80 11 2b c8 cO a8 O1 39 bb O8 ov + 9 UDP payload (29 bytes) 40 Ob f6 f6 00 35 00 25 48 e0 b4 £7 0100 00 01 @---5:-%H ~ Domain Name System (query) @2@ 00 02 OO 02 OO 03 77 77 77 O3 Gd 69 74 3 65 w ww-mit-e Transaction ID: @xb4f7 64 75 00 08 @1 00 01 du ~ Flags: @x@10@ Standard query Q... .22. sees sees = Response: Message is a query -000 0... .... .... = Opcode: Standard query (0) sees 0:0. eee «e+. = Truncated: Message is not truncated sees seed sees ses. = Recursion desired: Do query recursively seve eeee Ose eeee = Zi reserved (0) sees sees 2220 4... = Non-authenticated data: Unacceptable Questions: 1 Answer RRs: @ Authority RRs: @ Additional RRs: @ ~ Queries > www.mit.edu: type A, class IN [Response In: 673 4> @GB wireshark_Wi-FiZ187M3.pcapng Packets: 1455 - Displayed: 349 (24.0%) -Dropped: 0 (0.0%) Profile: Default 4. Periksa pesan balasan DNS. Berapa banyak ”jawaban” atau “answers” yang terdapat di dalamnya. Apa saja isi yang terkandung dalam setiap jawaban tersebut? Jawab : Jumlah jawaban pada balasan DNS adalah 3.Isi jawaban berupa alamat IP (A record) dan/atau alias domain (CNAME). 

## **NSLOOKUP -type=NS mit.edu 8.8.8.8** 

Soal : 

1. Ke alamat IP manakah pesan permintaan DNS dikirimkan? Apakah alamat IP tersebut merupakan default alamat IP server DNS lokal Anda? Jawab : Pesan permintaan DNS dikirim ke alamat IP 8.8.8.8. 

Alamat IP tersebut bukan merupakan DNS server lokal, karena DNS lokal yang digunakan adalah 182.8.64.11. 

Hal ini terjadi karena perintah nslookup secara eksplisit menggunakan DNS server Google (8.8.8.8). Perbedaan ini disebabkan karena penggunaan parameter tambahan pada perintah nslookup yang mengarahkan query ke DNS server tertentu (8.8.8.8), bukan ke DNS lokal secara default. 

2. Periksa pesan permintaan DNS. Apa ”jenis” atau ”type” dari pesan tersebut? Apakah pesan tersebut mengandung ”jawaban” atau ”answers”? Jawab : Jenis pesan DNS adalah NS (Name Server). 

Pesan permintaan tidak mengandung jawaban (answers), karena hanya berupa permintaan ke server DNS. 

3. Periksa pesan balasan DNS. Apa nama server MIT yang diberikan oleh pesan balasan? Apakah pesan balasan ini juga memberikan alamat IP untuk server MIT tersebut? Jawab : Pesan balasan DNS memberikan beberapa nama server milik MIT, seperti use2.akam.net dan asia2.akam.net. 

Pesan balasan ini tidak selalu memberikan alamat IP secara langsung, melainkan hanya nama 

**==> picture [60 x 9] intentionally omitted <==**

**----- Start of picture text -----**<br>
server DNS.<br>**----- End of picture text -----**<br>


## **NSLOOKUP** ~~ee~~ **www.aiit.or.kr bitsy.mit.edu** 

## Soal : 

1. Ke alamat IP manakah pesan permintaan DNS dikirimkan? Apakah alamat IP tersebut merupakan default alamat IP server DNS lokal Anda? Jawab : Pesan permintaan DNS dikirim ke alamat IP 53. Alamat tersebut bukan merupakan DNS server lokal, karena DNS lokal yang digunakan adalah 182.8.64.11. 

**==> picture [373 x 12] intentionally omitted <==**

**----- Start of picture text -----**<br>
Hal ini terjadi karena query diarahkan ke server DNS tertentu (bitsy.mit.edu).<br>**----- End of picture text -----**<br>


2. Periksa pesan permintaan DNS. Apa ”jenis” atau ”type” dari pesan tersebut? Apakah pesan tersebut mengandung ”jawaban” atau ”answers”? Jawab : Jenis pesan DNS adalah A (bitsy.mit.edu). Pesan permintaan tidak mengandung jawaban (answers), karena hanya berisi permintaan alamat IP. 

3. Periksa pesan balasan DNS. Berapa banyak ”jawaban” atau “answers” yang terdapat di dalamnya. Apa saja isi yang terkandung dalam setiap jawaban tersebut? Jawab : Jumlah jawaban pada pesan balasan DNS adalah 1. 

**==> picture [286 x 12] intentionally omitted <==**

**----- Start of picture text -----**<br>
Setiap jawaban berisi alamat IP dari domain www.aiit.or.kr<br>**----- End of picture text -----**<br>


