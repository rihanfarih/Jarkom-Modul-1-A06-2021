# Jarkom-Modul-1-A06-2021
Repository untuk laporan resmi praktikum Jarkom 2021 - A06


- Muh. Nur Fajrin Amiruddin (05111940000005)
- Rihan Farih Bunyamin (05111940000165)
- Lathifa Itqonina Mardiyati(05111940000176)

## Soal 1
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!   
  
Untuk mengetahui webserver yang digunakan, langkah yang dapat digunakan sebagai berikut:
1. **Langkah pertama :**   melakukan filter dengan  ``http.host == ichimarumaru.tech``  
2. **Langkah ke dua :**  klik kanan salah satu paket > follow > HTTP Stream maka akan memunculkan pop up halaman baru yang didalamnya terdapat informasi bahwa web server yang digunakan adalah **nginx/1.18.0 (Ubuntu)**. Rincian tersebut didapatkan berdasarkan informasi sebagai berikut:   
![image9](https://user-images.githubusercontent.com/55240758/134283868-f37eb43c-9d17-439c-848a-12111fbe0c11.png)
  
## Soal 2
Temukan paket dari web-web yang menggunakan basic authentication method!    
  
Untuk mengetahui paket dari web, maka filter yang digunakan adalah ``http.authbasic`` dimana paket yang ditemukan berdasarkan file.pcap yang diberikan sebagai berikut :  
![image13](https://user-images.githubusercontent.com/55240758/134284634-e3a8204a-a0c0-43cd-bd3f-63dc1ddf4e1e.png)

## Soal 3
Ikuti perintah di basic.ichimarumaru.tech! username dan password bisa didapatkan dari file .pcapng!
    
Untuk mengakses website tersebut dibutuhkan username dan password, langkah yang dapat digunakan sebagai berikut :    
1. **Langkah pertama :** Melakukan filter dengan ``http.host == basic.ichimarumaru.tech ``  
2. **Langkah kedua :** Klik salah satu paket untuk mengetahui informasi username dan password dengan melakukan expand opsi Hypertext Transfer Protocol>Authorization. Maka didapatkan _credentials_ yang secara urut berupa username dan password. Sebagai berikut :  
![image21](https://user-images.githubusercontent.com/55240758/134285205-8a95978f-4e31-4d50-a338-8de9a89bdf78.png)  

Maka setelah itu gunakan username dan password yang telah didapat untuk mengakses websitenya, Pada web tersebut terdapat soal mengenai urutan kabel T-568A. Jawabannya ada dalam screenshot dibawah ini :
![image6](https://user-images.githubusercontent.com/55240758/134285553-19b9f4a6-4a79-4735-b379-7e85a18c8113.png)

## Soal 4  
Temukan paket mysql yang mengandung perintah query select!    

Untuk mendapatkan paket tersebut, yakni dengan melakukan filter menggunakan ``mysql contains “select”``. Maka paket yang akan didapatkan sebagai berikut :  
![image7](https://user-images.githubusercontent.com/55240758/134285870-bf987ff5-8256-455b-9422-542d65321b22.png)  

## Soal 5
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password  bisa didapat dari **query insert** pada table users dari file .pcap!  

Untuk melakukan login dibutuhkan username dan password, langkah yang dapat digunakan sebagai berikut :  
1. **Langkah pertama :** Untuk mendapatkan username dan password dapat dilakukan dengan melakukan filter menggunakan ``insert.query``.  
2. **Langkah kedua :** klik salah satu paket untuk mengetahui rincian informasi mengenai username dan password dengan melakukan expand MySQL Protocol> Request Command Query. Sebagai berikut :  
![image15](https://user-images.githubusercontent.com/55240758/134286234-e17521b9-4542-402b-b0f9-2a0a4b37d807.png)

Maka setelah itu gunakan username dan password yang telah didapat untuk melakukan login website, Pada web tersebut terdapat soal mengenai urutan kabel T-568B. Jawabannya ada dalam screenshot dibawah ini :    
![image10](https://user-images.githubusercontent.com/55240758/134286408-a232f558-1c52-4fd7-b5ca-4cf90af80eeb.png) 

## Soal 6
Cari username dan password ketika melakukan login ke FTP Server!  
untuk menjawabnya, gunakan filter ``ftp.request.command == USER || ftp.request.command == PASS``

![image11](https://lh3.googleusercontent.com/e0GwIr98us2da5AJs56nbJKpHXLrUfqPe5Vc9MXO29Awbcst9OMV39_TS-GpwZGz2TBogfW5waEPAogOmTv1t_pFQSY5864zcGh7UCmxPVU2VEggTfPaHyGbzn84jVa3E1L6fGKj=s0) 
## Soal 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf") 
untuk menjawabnya langkah yang dilakukan sebagai berikut:
1. gunakan ``frame contains "Real.pdf" `` untuk mencari filenya ![image12](https://lh3.googleusercontent.com/M6uWGfR8QPcOuKaVurzC8D1-x1ezOlmjYFcxzUBHN4EMfpWAuBHuDokYWDYiEsI4UhFcJackCFKc0Vuyxqcmddwfwk7ynklRtTrGtcnPNyLcDwaOOzTGWU6sMP5_XLgPo-EcgzTu=s0) 
2. lalu follow TCP stream (ganti ke raw) dan save jadi .zip ![image13](	https://lh5.googleusercontent.com/Fxvsa80S4monR059D32731ifJF13_Lqgsu3E_I_cWzh1lFsLdtENcstEepSM_fqyYKBDNGW60myG81_6n6sx0X7IvXlpm6O9NKjrnvCFdsxdmQb0THkPrA7ZxGEwaARvmoBIIza4=s0) 
3. Buka lah filenya ![image14](	https://lh6.googleusercontent.com/iEFa0eYUOo9iv2pV5HyDUt61x7dxxq9y6jLnP37JwiGMjOqKl9wQpotn3BxqjHKe4jHTaC8-lQU7m-8yiQ8vyuWnK-xLX5pCbGRtHdyjGOrbyvpLSXx9RcjKgCFqqeJmo187GT5W=s0) 

## Soal 8
Cari paket yang menunjukan pengambilan file dari FTP tersebut!  

untuk menjawabnya , gunakan ```ftp.request.command == stor``` untuk mencari perintah pengambilan file dari FTP
![image15](https://lh3.googleusercontent.com/pplsYsIsDwLjdltavqNioWg__i8INfE0Svm3lEgpuw_e3mGf2ChATPC76ITLwxD0vH10Z6gt44w99iuezzmvfhjugu6jbGc3_bO9sU7JTuswAa-WB9oO6i15aJacrxRsMT6qvGSK=s0) 

  
## Soal 9
Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut !.  

Berdasarkan perintah soal, langkah yang dapat digunakan sebagai berikut :  
1. **Langkah pertama :** Mencari paket "secret.zip" dengan melakukan filtering menggunakan ``ftp-data``. Maka akan ditampilkan paket-paket apa saja yang menuju FTP sebagai berikut:  ![image12](https://user-images.githubusercontent.com/55240758/134286871-5d43cea8-2434-47b9-86f7-5a6ed0e3e805.png)
2. **Langkah kedua :** Untuk menyimpan file tersebut pilih salah satu paket "secret.zip", klik kanan paket yang telah dipilih > follow > TCP Stream. Kemudian wireshark akan memunculkan halaman sebagai berikut :  
![image23](https://user-images.githubusercontent.com/55240758/134288847-ab5aad33-da5a-4de6-9258-287a1992901e.png) Berdasarkan tampilan tersebut langkah selanjutnya yaitu pada opsi Show Data > Raw, kemudian simpan dengan menekan tombol Save As.  
3. **Langkah ketiga :** Setelah file disimpan dalam bentuk raw, untuk membukanya dilakukan langkah ekstrak berkas yang mana terdapat password untuk melakukannya. Untuk itu berdasarkan informasi yang telah didapat pada no. 10 yaitu password dapat diakses pada file bernama "bukanapaapa.txt". Maka terlebih dahulu mencari paket atau file tersebut dengan melakukan fiter ``ftp-data.command contains "bukanapaapa.txt"``.  Dimana password dapat dilihat dengan melakukan expand pada opsi Line-based text data.
![image3](https://user-images.githubusercontent.com/55240758/134290010-d93c5302-49b5-44f6-855c-1e5a069b337f.png)
Adapun cara lain untuk mengetahui password yakni dengan melakukan klik kanan paket > follow > TCP stream untuk mengetahui isi teks pada file bukanapapa.txt yang berupa password sebagai berikut :  
![image20](https://user-images.githubusercontent.com/55240758/134290558-cc0a3dc0-de23-49ae-8870-c957b3a3708e.png)  
4. **Langkah keempat:** Melakukan ekstrak dengan password yang telah didapatkan sebagai berikut:
![image26](https://user-images.githubusercontent.com/55240758/134290730-77838511-7a11-49b6-8197-e3390bda7a82.png)  
Maka dengan begitu file dapat dibuka dan berisi sebagai berikut :  ![image16](https://user-images.githubusercontent.com/55240758/134290921-3f27fc6a-84b4-4ad7-b431-9057bb7fd65f.png)

## Soal 10
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!


Langkah yang dapat digunakan sebagai berikut:  
1. **Langkah pertama:** mencari terlebih dahulu paket history.txt pada hasil filter menggunakan ``ftp-data``.
![image12](https://user-images.githubusercontent.com/55240758/134286871-5d43cea8-2434-47b9-86f7-5a6ed0e3e805.png)
  
2. **Langkah kedua:** klik kanan salah satu paket > follow > TCP Stream untuk melihat isi paket sebagai berikut. Dimana pada command bash tersebut terdapat informasi bahwa password berada pada file bukanapapa.txt untuk membuka file zip. Sehingga langkah selanjutnya sama dengan soal no.9.
![image19](https://user-images.githubusercontent.com/55240758/134286891-d2183f73-f381-443e-8fb8-79a8965a2b5a.png)

## Soal 11
 Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!   
 Gunakan wireshark filter expression: ``src port 80``
 ![image20](https://lh3.googleusercontent.com/TkdBiFXSVPUOvZB1Z5bbCHoIN1sIGl7BL5KLCK2aj_QOaAFEQdL_hEkdnQXTTn4rk56Zwu4NskitvyLR-OEns-YOw64NupUzvBk8_f62RmWXRqh3KRHQvIsbJbGCRnT-RYd0adjz=s0)

## Soal 12
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!  
Gunakan wireshark filter expression: ``port 21``
![image21](https://lh4.googleusercontent.com/FQIvEAA63C5qR4npXrz1vbYLMnGTyqpjKLHE1KxQ_S5xqEivMkXirgo2zGV4wl5-i76EskG8N5WHyI_tuFBYQSMKN5uviDE52-ws5NVb-qVBxIRd4TgY493L6Czovxw0XfcWxtfj=s0)

## Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

Gunakan wireshark filter expression: ``dst port 443``
![image18](https://user-images.githubusercontent.com/73771452/134446260-23b394c5-9fe5-40bf-92dd-8a4f1fe3d602.png)

## Soal 14
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!

Gunakan wireshark filter expression: ``dst host kemenag.go.id``
![image11](https://user-images.githubusercontent.com/73771452/134446510-04183bf8-9eae-47b0-aee5-2317015f337c.png)

## Soal 15
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Langkah yang dapat digunakan sebagai berikut:  
1. **Langkah pertama:** Buka Command Prompt dengan cara menekan tombol 'Windows' dan 'R' secara bersamaan atau buka melalui Start menu kemudian ketik Run untuk mengecek ip.
2. **Langkah kedua:** Ketik 'ipconfig' kemudian tunggu beberapa saat sampai command prompt menunujukkan IP Configuration dari perangkat yang digunakan.
3. **Langkah pertama:** Kemudian masukkan ip tersebut dan gunakan wireshark filter expression: ``src net 192.168.1.6``
![image25](https://user-images.githubusercontent.com/73771452/134446192-9d8876c7-a4c7-420b-8d20-a6e73f193332.png)
