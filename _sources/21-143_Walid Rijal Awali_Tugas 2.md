# Cara mengumpulkan database menggunakan 

# Microsoft Power BI

----

​				Microsoft [Power BI](https://www.microsoft.com/en-us/download/details.aspx?id=58494) adalah software intelligence bisnis buatan Microsoft yang memungkinkan Anda untuk mengolah data lebih detail dan menampilkannya dengan grafis yang lebih interaktif. Microsoft Power BI dapat memvisualisasikan data yang telah Anda masukkan atau data yang sudah terkoneksi oleh sistem ketiga. Anda juga bisa mengontrol dan memantau data Anda dengan mudah.

​				Pada aplikasi ini, disini juga dapat mengumpulkan beberapa data dari beberapa sumber, seperti file type CSV, Postgresql, MySql database, dan masih banyak lagi, untuk saat ini disini kita akan membahas bagaimana cara mengambil data dari excel, Postgresql, dan juga MySql database.

1. ## 1. **MENGAMBIL DATA DARI DATA BERFORMAT CSV**

   > Comma Separated Values atau CSV adalah suatu format data dalam basis data di mana setiap record dipisahkan dengan tanda koma (, ) atau titik koma. Selain sederhana, format ini dapat dibuka dengan berbagai text-editor seperti Notepad, Wordpad, ataupun Microsoft Excel.

   ​			Untuk pengambilan database berbentuk CSV sangatlah mudah, untuk aplikasi yang harus kita install tentunya  Power BI, untuk langkah-langkahnya adalah sebagai berikut.

   -  Pertama-tama pastikan anda memiliki data yang ingin kita pindah, disini saya menggunakan data [iris](https://gist.github.com/netj/8836201) dan juga aplikasi yang dibutuhkan.

     <img src="ss\Screenshot (60).png" style="zoom:20%;" />

   - Langkah kedua disini kita buka aplikasi Power BI, dan kita klik GET DATA, lalu pilih more.

     <img src="ss\Screenshot (59).png" style="zoom:20%;" />

   - Selanjutnya kita bisa memilih bentuk database yang kita ingin ambil, disini kita pilih bentuk data teks/csv, lalu klik connect.

     <img src="ss\Screenshot (61).png" style="zoom:20%;" />

   - Langkah selanjutnya kita bisa pilih file yang sudah kita siapkan tadi dan klik open.

     <img src="ss\Screenshot (62).png" style="zoom:20%;" />

   - Selanjutnya kita bisa klik load data tersebut.

     <img src="ss\Screenshot (63).png" style="zoom:20%;" />

   - Dan data sudah tersimpan di dalam aplikasi Power BI, dan untuk menampilkan data terdapat nama data tersebut di sebelah kan, dan kita bisa centang semua kotak yang ada.

     <img src="ss\Screenshot (64).png" style="zoom:20%;" />

2. ## 2. **MENGAMBIL DATA DARI POSTGRESQL**

   > PostgreSQL adalah database yang banyak digunakan pada[ web app](https://www.postgresql.org/download/), aplikasi mobile, dan aplikasi analytics. Itulah kenapa aplikasi yang membutuhkan pengolahan data yang lebih kompleks akan lebih cocok menggunakan postgreSQL.

   ​			Untuk pengambilan database dari PostgreSQL sangatlah mudah, untuk aplikasi yang harus kita install tentunya PostgreSQL dan juga Power BI, dan juga kita membutuhkan ElephantSQL dimana digunakan untuk hosting database untuk PostgreSQL, disini kita akan melakukan 2 cara mengambilan database, yang pertama yaitu dari local data dan juga database yang berada di server dari ElephantSQL, untuk langkah-langkahnya adalah sebagai berikut.

   ### 1. Pengambilan database dari local data PostgreSQL

   - Pertama-tama, disini kita harus membuat server di PGADMIN, dengan cara kita klik kanan pada server, setelah itu kita klik REGISTER dan kita pilih SERVER, disini saya beri nama "localpendatb".

     <img src="ss\Screenshot (68).png" style="zoom:20%;" />

   - Setelah itu disni kita buat database dengan cara klik kanan pada menu DATABASE, dan kita pilih menu CREATE, lalu pilih DATABASE, disini saya beri nama "databaseiris" lalu klik save.

     <img src="ss\Screenshot (75).png" style="zoom:20%;" />

   - Untuk menambahkan data, bisa menggunakan perintah creat table, disini kita  klik kanan pada database yang sudah kita buat tadi, lalu kita pilih menu QUERY TOOL.

     <img src="ss\Screenshot (66).png" style="zoom:25%;" />

   - Untuk perintah yang digunakan, kalian dapat mengcopy perintah dibawah untuk memudahkan, kita tempelkan pada bagian sebelah kanan, dan selanjutnya kita bisa klik RUN.

     <img src="ss\Screenshot (69).png" style="zoom:20%;" />

     ```
     CREATE TABLE iris(
       sepal_l FLOAT,
       sepal_w FLOAT,
       petal_l FLOAT,
       petal_w FLOAT,
       class   VARCHAR(20)
     );
     
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.5,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.0,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.7,3.2,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.1,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.6,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.9,1.7,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.4,1.4,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.4,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.4,2.9,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.7,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.4,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.0,1.4,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.3,3.0,1.1,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,4.0,1.2,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,4.4,1.5,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.9,1.3,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.5,1.4,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,3.8,1.7,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.8,1.5,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.4,1.7,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.7,1.5,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.6,1.0,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.3,1.7,0.5,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.4,1.9,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.0,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.4,1.6,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,3.5,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,3.4,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.7,3.2,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.1,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.4,1.5,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,4.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,4.2,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.2,1.2,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,3.5,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.4,3.0,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.4,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.5,1.3,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.5,2.3,1.3,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.4,3.2,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.5,1.6,0.6,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.8,1.9,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.0,1.4,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.8,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.2,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.3,3.7,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.3,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.0,3.2,4.7,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,3.2,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.1,4.9,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.3,4.0,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,2.8,4.6,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.8,4.5,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,3.3,4.7,1.6,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,2.4,3.3,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.6,2.9,4.6,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,2.7,3.9,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,2.0,3.5,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.9,3.0,4.2,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.2,4.0,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.9,4.7,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.9,3.6,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.1,4.4,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,3.0,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,4.1,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,2.2,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.5,3.9,1.1,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.9,3.2,4.8,1.8,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.8,4.0,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.5,4.9,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.8,4.7,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.9,4.3,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.6,3.0,4.4,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.8,2.8,4.8,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.0,5.0,1.7,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.9,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.6,3.5,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.4,3.8,1.1,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.4,3.7,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,3.9,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.7,5.1,1.6,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.0,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,3.4,4.5,1.6,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.1,4.7,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.3,4.4,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,3.0,4.1,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.5,4.0,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.6,4.4,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,3.0,4.6,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.6,4.0,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,2.3,3.3,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.7,4.2,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,3.0,4.2,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.9,4.2,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,2.9,4.3,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,2.5,3.0,1.1,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.8,4.1,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,3.3,6.0,2.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,5.1,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.1,3.0,5.9,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.9,5.6,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.0,5.8,2.2,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.6,3.0,6.6,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,2.5,4.5,1.7,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.3,2.9,6.3,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,2.5,5.8,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.2,3.6,6.1,2.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.2,5.1,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.7,5.3,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.8,3.0,5.5,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.5,5.0,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.8,5.1,2.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,3.2,5.3,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.0,5.5,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,3.8,6.7,2.2,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,2.6,6.9,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.2,5.0,1.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.2,5.7,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.8,4.9,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,2.8,6.7,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.7,4.9,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.3,5.7,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.2,3.2,6.0,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,2.8,4.8,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,3.0,4.9,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.8,5.6,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.2,3.0,5.8,1.6,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.4,2.8,6.1,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.9,3.8,6.4,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.8,5.6,2.2,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.8,5.1,1.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.6,5.6,1.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,3.0,6.1,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,3.4,5.6,2.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,3.1,5.5,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,3.0,4.8,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.1,5.4,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.1,5.6,2.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.1,5.1,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,5.1,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.8,3.2,5.9,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.3,5.7,2.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.0,5.2,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.5,5.0,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.0,5.2,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,3.4,5.4,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.9,3.0,5.1,1.8,'Iris-virginica');
     ```

     

   - Dan database yang kita buat sudah selesai, kita bisa melihatnya di menu SCHEMAS, lalu pilih menu TABLE, dan klik kanan pada table yang sudah kita buat tadi, klik kanan pada table tersebut dan pilih menu VIEW/EDIT DATA. jika belum keluar data table yang sudah kita buat tadi kalian bisa refresh dengan klik kanan pada menu database yang dibuat tadi.

     <img src="ss\Screenshot (70).png" style="zoom:20%;" />

   - Selanjutnya untuk mengambil database tersebut kita klik GET DATA lagi pada menu di aplikasi Power BI, kita pilih menu MORE.

     <img src="ss\Screenshot (59).png" style="zoom:20%;" />

   - Setelah itu kita pilih di bagian DATABASE, dan kita pilih PostgreSQL database, lalu kita klik connect.

     <img src="ss\Screenshot (71).png" style="zoom:20%;" />

   - Setelah itu disini kita bisa isi kolom server beserta portnya (localhost:5432), dan juga kita isikan kolom database dengan nama yang kita buat tadi (databaseiris), lalu kita klik oke.

     <img src="ss\Screenshot (72).png" style="zoom:20%;" />

   - Dan disini akan keluar database yang kita inginkan, kita bisa centang untuk memilihnya, dan kita klik load, dan database telah selesai diambil, untuk menampilkannya kita bisa menggunakan cara yang sama seperti diatas.

     <img src="ss\Screenshot (73).png" style="zoom:20%;" />

   ### 2. Pengambilan database dari online data PostgreSQL di ElephantSQL

   - Pertama-tama disini kita buat akun ElephantSQL terlebih dahulu, disini saya mencontohkan dengan ElephantSQL untuk menyimpan datanya secara online, setelah selesai kita bisa pilih menu di profile, lalu kita klik CREATE NEW TEAM, disini saya beri nama "Pendata B".

     <img src="ss\Screenshot (78).png" style="zoom:20%;" />

   - Selanjutnya disini kita bisa klik "create" untuk membuat instance.

     <img src="ss\Screenshot (83).png" style="zoom:20%;" />

   - Kita dapat isikan kolom name dan juga tag seperti contoh dibawah ini.

     <img src="ss\Screenshot (80).png" alt="Screenshot (80)" style="zoom:20%;" />

   - Lalu kita disini bisa memilih berbagai region yang ditampilkan.

     <img src="ss\Screenshot (81).png" alt="Screenshot (81)" style="zoom:20%;" />

   - Setelah itu kita bisa klik "create instance".

     <img src="ss\Screenshot (82).png" alt="Screenshot (82)" style="zoom:20%;" />

   - Selanjutnya akan tampil instance yang kita buat tadi dan kita bisa mengkliknya, dan akan keluar beberapa details dari instance yang sudah kita buat seperti gambar dibawah ini.

     <img src="ss\Screenshot (84).png" alt="Screenshot (84)" style="zoom:20%;" />

     <img src="ss\Screenshot (85).png" style="zoom:20%;" />

     

   - Selanjutnya kita pindah ke aplikasi Power BI lagi, disini kita harus membuat server untuk ElephantSQL di PGADMIN, berbeda dari diatas, pertama kita klik kanan pada menu SERVER, lalu kita pilih menu REGISTER dan klik pada menu SERVER.

     <img src="ss\Screenshot (68).png" style="zoom:20%;" />

     <img src="ss\Screenshot (76).png" style="zoom:20%;" />

   - Setelah langkah diatas kita bisa liat pada kolom connection, pada kolom hostname, kita bisa isikan server yang terdapat pada ElephantSQL, lalu kita klik save. 

     <img src="ss\Screenshot (86).png" style="zoom:20%;" />

     <img src="ss\Screenshot (85).png" style="zoom:20%;" />

   - Setelah selesai disini kita tidak perlu membuat databese, karena akan terbuat otomatis database sesuai dengan nama di kolom User & Default database pada ElephantSQL, kita bisa scroll kebawah dan mencarinya.

     <img src="ss\Screenshot (87).png" style="zoom:20%;" />

   - Untuk menambahkan data, kita bisa menggunakan perintah creat table, disini kita  klik kanan pada database yang sudah kita buat tadi, lalu kita pilih menu QUERY TOOL.

     <img src="ss\Screenshot (66).png" style="zoom:25%;" />

   - Untuk perintah yang digunakan, kalian dapat mengcopy perintah dibawah untuk memudahkan, kita tempelkan pada bagian sebelah kanan, dan selanjutnya kita bisa klik RUN.

     <img src="ss\Screenshot (69).png" style="zoom:20%;" />

     ```
     CREATE TABLE iris(
       sepal_l FLOAT,
       sepal_w FLOAT,
       petal_l FLOAT,
       petal_w FLOAT,
       class   VARCHAR(20)
     );
     
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.5,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.0,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.7,3.2,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.1,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.6,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.9,1.7,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.4,1.4,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.4,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.4,2.9,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.7,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.4,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.0,1.4,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.3,3.0,1.1,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,4.0,1.2,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,4.4,1.5,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.9,1.3,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.5,1.4,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,3.8,1.7,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.8,1.5,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.4,1.7,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.7,1.5,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.6,1.0,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.3,1.7,0.5,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.4,1.9,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.0,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.4,1.6,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,3.5,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,3.4,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.7,3.2,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.1,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.4,1.5,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,4.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,4.2,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.2,1.2,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,3.5,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,3.1,1.5,0.1,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.4,3.0,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.4,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.5,1.3,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.5,2.3,1.3,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.4,3.2,1.3,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.5,1.6,0.6,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.8,1.9,0.4,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.8,3.0,1.4,0.3,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,3.8,1.6,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.6,3.2,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.3,3.7,1.5,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,3.3,1.4,0.2,'Iris-setosa');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.0,3.2,4.7,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,3.2,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.1,4.9,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.3,4.0,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,2.8,4.6,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.8,4.5,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,3.3,4.7,1.6,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,2.4,3.3,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.6,2.9,4.6,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.2,2.7,3.9,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,2.0,3.5,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.9,3.0,4.2,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.2,4.0,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.9,4.7,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.9,3.6,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.1,4.4,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,3.0,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,4.1,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,2.2,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.5,3.9,1.1,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.9,3.2,4.8,1.8,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.8,4.0,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.5,4.9,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.8,4.7,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.9,4.3,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.6,3.0,4.4,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.8,2.8,4.8,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.0,5.0,1.7,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.9,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.6,3.5,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.4,3.8,1.1,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.4,3.7,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,3.9,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.7,5.1,1.6,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.4,3.0,4.5,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,3.4,4.5,1.6,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.1,4.7,1.5,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.3,4.4,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,3.0,4.1,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.5,4.0,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.5,2.6,4.4,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,3.0,4.6,1.4,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.6,4.0,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.0,2.3,3.3,1.0,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.7,4.2,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,3.0,4.2,1.2,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.9,4.2,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,2.9,4.3,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.1,2.5,3.0,1.1,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.8,4.1,1.3,'Iris-versicolor');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,3.3,6.0,2.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,5.1,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.1,3.0,5.9,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.9,5.6,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.0,5.8,2.2,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.6,3.0,6.6,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (4.9,2.5,4.5,1.7,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.3,2.9,6.3,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,2.5,5.8,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.2,3.6,6.1,2.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.2,5.1,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.7,5.3,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.8,3.0,5.5,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.7,2.5,5.0,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.8,5.1,2.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,3.2,5.3,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.0,5.5,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,3.8,6.7,2.2,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,2.6,6.9,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,2.2,5.0,1.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.2,5.7,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.6,2.8,4.9,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,2.8,6.7,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.7,4.9,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.3,5.7,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.2,3.2,6.0,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,2.8,4.8,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,3.0,4.9,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.8,5.6,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.2,3.0,5.8,1.6,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.4,2.8,6.1,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.9,3.8,6.4,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,2.8,5.6,2.2,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.8,5.1,1.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.1,2.6,5.6,1.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (7.7,3.0,6.1,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,3.4,5.6,2.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.4,3.1,5.5,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.0,3.0,4.8,1.8,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.1,5.4,2.1,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.1,5.6,2.4,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.9,3.1,5.1,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.8,2.7,5.1,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.8,3.2,5.9,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.3,5.7,2.5,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.7,3.0,5.2,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.3,2.5,5.0,1.9,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.5,3.0,5.2,2.0,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (6.2,3.4,5.4,2.3,'Iris-virginica');
     insert into iris(sepal_l, sepal_w, petal_l, petal_w, class) values (5.9,3.0,5.1,1.8,'Iris-virginica');
     ```

     

   - Dan database yang kita buat sudah selesai, kita bisa melihatnya di menu SCHEMAS, lalu pilih menu TABLE, dan klik kanan pada table yang sudah kita buat tadi, klik kanan pada table tersebut dan pilih menu VIEW/EDIT DATA. jika belum keluar data table yang sudah kita buat tadi kalian bisa refresh dengan klik kanan pada menu database yang dibuat tadi.

     <img src="ss\Screenshot (70).png" style="zoom:20%;" />

   - Selanjutnya untuk mengambil database tersebut kita klik GET DATA lagi pada menu di aplikasi Power BI, kita pilih menu MORE.

     <img src="ss\Screenshot (59).png" style="zoom:20%;" />

   - Setelah itu kita pilih di bagian DATABASE, dan kita pilih PostgreSQL database, lalu kita klik connect.

     <img src="ss\Screenshot (71).png" style="zoom:20%;" />

   - Setelah itu disini kita bisa isi kolom server dengan alamat server yang terdapat pada ElephantSQL (mel.db.elephantsql.com), dan juga kita isikan kolom database dengan nama database yang kita punya tadi (tazcfpqb), lalu kita klik oke.

     <img src="ss\Screenshot (88).png" style="zoom:20%;" />

   - Dan disini akan keluar database yang kita inginkan, kita bisa centang untuk memilihnya, dan kita klik load, dan database telah selesai diambil, untuk menampilkannya kita bisa menggunakan cara yang sama seperti diatas.

     <img src="ss\Screenshot (89).png" style="zoom:20%;" />

   ## 3. **MENGAMBIL DATA DARI MYSQL DATABASE**

> **MySQL** atau dibaca My Sequel merupakan sebuah **Database** Management System atau sering disingkat DBMS yang dijalankan menggunakan perintah SQL (Structured Query Language) yang populer digunakan untuk pembuatan aplikasi berbasis website.

​			Untuk pengambilan database dari MySQL database tidaklah sulit, untuk aplikasi yang harus kita install tentunya  Power BI dan juga MySQL database, disini saya menggunakan XAMPP, untuk langkah-langkahnya adalah sebagai berikut.

-  Pertama-tama disini kita running dulu XAMPP, selanjutnya kita bisa buka phpMyAdmin, dan kita buat database baru, disini saya beri nama "pendatairis", ini sebagai contoh data yang akan kita ambil nantinya, selanjutnya disini kita bisa import data yang akan kita gunakan.

  <img src="ss\Screenshot (91).png" style="zoom:20%;" />

- Disini kita sudah memiliki data yang sudah kita import tadi, selanjutnya disini kita bisa pindah ke aplikasi Power BI, selanjutnya kita pilih menu GET DATA, dan pilih MORE.

  <img src="ss\Screenshot (59).png" style="zoom:20%;" />

- Selanjutnya kita bisa memilih bentuk database yang kita ingin ambil, disini kita MySQL database, lalu klik connect.

  <img src="ss\Screenshot (92).png" style="zoom:20%;" />

- Langkah selanjutnya kita bisa isi kolom server dengan server dari MySQl yang kita gunakan beserta portnya, yaitu(localhost:3306) dan pada kolom database kita isikan nama database yang sudah kita buat tadi (pendatairis) lalu kita klik oke.

  <img src="ss\Screenshot (94).png" style="zoom:20%;" />

- Selanjutnya kita liat pada menu sebelah kanan, kita pindah dari windows ke database, selanjutnya kita isikan kolom username dengan (root), untuk password bisa kita kosongkan, lalu klik connect.

  <img src="ss\Screenshot (95).png" style="zoom:20%;" />

- Dan disini akan keluar database yang kita inginkan, kita bisa centang untuk memilihnya, dan kita klik load, dan database telah selesai diambil, dan untuk menampilkan data terdapat nama data tersebut di sebelah kan, dan kita bisa centang semua kotak yang ada.

  <img src="ss\Screenshot (96).png" style="zoom:20%;" />

