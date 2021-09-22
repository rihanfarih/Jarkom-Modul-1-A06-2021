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

## Soal 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")  

## Soal 8
Cari paket yang menunjukan pengambilan file dari FTP tersebut!  
  
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
4. **Langkah keempat:** Melakukan ekstrak dengan password yang telah didapatkan. sebagai beriut:
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
## Soal 12
## Soal 13
## Soal 14
## Soal 15

