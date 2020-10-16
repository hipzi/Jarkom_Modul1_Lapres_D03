# Jarkom_Modul1_Lapres_D03

 - Display Filter :
	 * <a href="#soal-1">soal 1 </a>
	 * <a href="#soal-2">soal 2 </a>
	 * <a href="#soal-3">soal 3 </a>
     * <a href="#soal-4">soal 4 </a>
     * <a href="#soal-5">soal 5 </a>
     * <a href="#soal-6">soal 6 </a>
     * <a href="#soal-7">soal 7 </a>
     * <a href="#soal-8">soal 8 </a>
     * <a href="#soal-9">soal 9 </a>
     * <a href="#soal-10">soal 10 </a>
 - Capture Filter :
	 * <a href="#soal-11">soal 11 </a>
	 * <a href="#soal-12">soal 12 </a>
	 * <a href="#soal-13">soal 13 </a>
     * <a href="#soal-14">soal 14 </a>
     * <a href="#soal-15">soal 15 </a>

## Display Filter
<justify>
<a id="soal-1"></a>
<p></p>
1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"! 
<p></p>
<code> http.host == "testing.mekanis.me" </code>

![1.1](img/1-1.png)
<p></p>
<code> Klik kanan -> Follow -> Http Stream </code>

![1.2](img/1-2.png)
</justify>

<justify>
<a id="soal-2"></a>
<p></p>
2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
<p></p>
<code> file → export object → http → cari jpg → nemu download gambarnya </code>

![2.1](img/2.png)
</justify>

<justify>
<a id="soal-3"></a>
<p></p>
3. Cari username dan password ketika login di "ppid.dpr.go.id"!
<p></p>
<code> http.host == "ppid.dpr.go.id" and http.request.method==POST </code>

![3.1](img/3.png)
</justify>

<justify>
<a id="soal-4"></a>
<p></p>
4. Temukan paket dari web-web yang menggunakan basic authentication method!
<p></p>
<code> http.authbasic </code>

![4.1](img/4-1.png)
![4.2](img/4-2.png)
</justify>

<justify>
<a id="soal-5"></a>
<p></p>
5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
<p></p>
<code> http.host == "aku.pengen.pw" </code>

![5.1](img/5-1.png)
![5.2](img/5-2.png)
<p>
<b>Urutan T568B</b> <br>
Urutan ke 1 : Putih Orange RD+ (data terima+) <br>
Urutan ke 2 : Orange RD- (data terima-) <br>
Urutan ke 3 : Putih Hijau TD+ (data kirim +) <br>
Urutan ke 4 : Biru NC (tidak dipakai) <br>
Urutan ke 5 : Putih Biru NC (tidak dipakai) <br>
Urutan ke 6 : Hijau TD- (data kirim -) <br>
Urutan ke 7 : Putih Coklat NC (tidak dipakai) <br>
Urutan ke 8 : Coklat NC (tidak dipakai) <br>
</p>
</justify>

<justify>
<a id="soal-6"></a>
<p></p>
6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
<p></p>
<code> ftp-data : buat cari zip dan zipkey.txt </code>
<p></p>
<code> ftp.request.arg == "Answer.zip" </code>

![6.1](img/6-1.png)
<p></p>
<code> ftp.request.arg == "zipkey.txt" </code>

![6.2](img/6-2.png)
<p></p>
<p>pass : hey997400323051</p>
<p></p>
<code> Klik kanan -> follow -> tcp stream -> save data berupa raw -> save as sesuai format file </code>

![6.3](img/6-3.png)
</justify>

<justify>
<a id="soal-7"></a>
<p></p>
7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
<p></p>
<code> ftp-data contains "Yes.pdf" </code>

![7.1](img/7-1.png)
<p></p>
<code> Klik kanan -> follow -> tcp stream -> save data berupa raw -> save as sesuai format file </code>

![7.2](img/7-2.png)
</justify>

<justify>
<a id="soal-8"></a>
<p></p>
8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
<p></p>
<code> ftp.response.arg == "Microsoft FTP Service" </code>

![8.1](img/8-1.png)

<p></p>
<code> ftp.request.command==RETR && ip.dst == 198.246.117.106 </code>

![8.2](img/8-2.png)
</justify>

<justify>
<a id="soal-9"></a>
<p></p>
9. Cari username dan password ketika login FTP pada localhost!
<p></p>
<code> ftp.request.command==USER || ftp.request.command==PASS </code>

![9.1](img/9.png)
</justify>

<justify>
<a id="soal-10"></a>
<p></p>
10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46" 
<p></p>
<code> frame contains "application/pdf" </code>

![10.1](img/10.png)
</justify>

## Capture Filter

<justify>
<a id="soal-11"></a>
<p></p>
11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
<p></p>
<code> port 21 → loopback (soalnya ftp soal ini pake yang lokal) </code>

![11.1](img/11.png)
</justify>

<justify>
<a id="soal-12"></a>
<p></p>
12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
<p></p>
<code> src port 80 → wlo1(wifi) </code>

![12.1](img/12.png)
</justify>

<justify>
<a id="soal-13"></a>
<p></p>
13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
<p></p>
<code> dst port 443 → wlo1(wifi) </code>

![12.1](img/13.png) 
</justify>

<justify>
<a id="soal-14"></a>
<p></p>
14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
<p></p>
<code> ifconfig </code>

![14.1](img/14-1.png)
<p></p>
<code> src host 192.168.1.2 </code>

![14.1](img/14-2.png)
</justify>

<justify>
<a id="soal-15"></a>
<p></p>
15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
<p></p>
<code> dst host monta.if.its.ac.id → wlo1(wifi) </code>

![15.1](img/15.png)
</justify>