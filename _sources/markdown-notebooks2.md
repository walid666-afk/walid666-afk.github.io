## 3. **MENGAMBIL DATA DARI MYSQL DATABASE**

> **MySQL** atau dibaca My Sequel merupakan sebuah **Database** Management System atau sering disingkat DBMS yang dijalankan menggunakan perintah SQL (Structured Query Language) yang populer digunakan untuk pembuatan aplikasi berbasis website.

​			Untuk pengambilan database dari MySQL database tidaklah sulit, untuk aplikasi yang harus kita install tentunya  Power BI dan juga MySQL database, disini saya menggunakan XAMPP, untuk langkah-langkahnya adalah sebagai berikut.


- Pertama-tama disini kita running dulu XAMPP, selanjutnya kita bisa buka phpMyAdmin, dan kita buat database baru, disini saya beri nama "pendatairis", ini sebagai contoh data yang akan kita ambil nantinya, selanjutnya disini kita bisa import data yang akan kita gunakan.

  ![](https://github.com/walid666-afk/Pendata/blob/main/ss/Screenshot%20(91).png?raw=true)

- Disini kita sudah memiliki data yang sudah kita import tadi, selanjutnya disini kita bisa pindah ke aplikasi Power BI, selanjutnya kita pilih menu GET DATA, dan pilih MORE.

  ![](https://github.com/walid666-afk/Pendata/blob/main/ss/Screenshot%20(59).png?raw=true)

- Selanjutnya kita bisa memilih bentuk database yang kita ingin ambil, disini kita MySQL database, lalu klik connect.

  ![](https://github.com/walid666-afk/Pendata/blob/main/ss/Screenshot%20(92).png?raw=true)

- Langkah selanjutnya kita bisa isi kolom server dengan server dari MySQl yang kita gunakan beserta portnya, yaitu(localhost:3306) dan pada kolom database kita isikan nama database yang sudah kita buat tadi (pendatairis) lalu kita klik oke.

  ![](https://github.com/walid666-afk/Pendata/blob/main/ss/Screenshot%20(94).png?raw=true)

- Selanjutnya kita liat pada menu sebelah kanan, kita pindah dari windows ke database, selanjutnya kita isikan kolom username dengan (root), untuk password bisa kita kosongkan, lalu klik connect.

  ![](https://github.com/walid666-afk/Pendata/blob/main/ss/Screenshot%20(95).png?raw=true)

- Dan disini akan keluar database yang kita inginkan, kita bisa centang untuk memilihnya, dan kita klik load, dan database telah selesai diambil, dan untuk menampilkan data terdapat nama data tersebut di sebelah kan, dan kita bisa centang semua kotak yang ada.

  ![](https://github.com/walid666-afk/Pendata/blob/main/ss/Screenshot%20(96).png?raw=true)

