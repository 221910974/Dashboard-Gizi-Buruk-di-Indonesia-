# Pembangunan Dashboard Gizi Buruk di Indonesia Menggunakan Tableau
 
 Hady Rizaldy Gunawan (221910974, 3SD1, 19)
 
 UAS Visualisasi Data
  
I.	LATAR BELAKANG

Hingga saat ini, gizi buruk masih menjadi masalah utama kesehatan yang menarik perhatian banyak masyarakat luas. Di negara berkembang tercatat bahwa sepertiga dari populasi balita yang ada di negaranya mengalami gizi buruk. Hal ini tentunya akan berdampak buruk bagi suatu negara, karena jika bayi yang mengalami gizi buruk dibiarkan bertahan hingga dewasa mereka akan beresiko mengalami perkembangan kognitif yang buruk dan reproduktivitas yang rendah (Smith dan Haddad, 2000). Selain itu gizi buruk juga dapat menyebabkan kematian, keadaan ini cukup mengakhawatirkan bagi suatu negara dikarenakan anak adalah generasi penerus bangsa.
Di Indonesia jumlah kasus gizi buruk pada tahun 2012 sebanyak 42.702 kasus kurang lebih mengalami penurunan sebesar 14%, namun dalam beberapa tahun terakhir penurunannya sangat landai (Kementrian Kesehatan RI, 2013). Meskipun mengalami penurunan secara nasional, namun secara regional terdapat beberapa provinsi yang tercatat memiliki angka gizi buruk yang cukup tinggi. Provinsi tersebut diantaranya adalah Jawa Tengah, Jawa Timur dan Nusa Tenggara Timur. Walaupun begitu masalah gizi buruk ini merupakan isu kesehatan yang harus terus diwaspadai dan ditangani secara maksimal. Untuk memaksimalkan penanganan gizi buruk, perlu diketahui faktor-faktor yang mempengaruhi gizi buruk. 

II.	METODE PENELITIAN

Metode penelitian yang akan digunakan untuk pembangunan dashboard gizi di Indonesia adalah metode eksperimen dengan beberapa tahapan. Data yang akan digunakan untuk pembuatan dashboard adalah data mengenai gizi yang bersumber dari Profil Kesehatan Indonesia Tahun 2020 dan website Kementrian Kesehatan Republik Indonesia.
Penelitian ini akan dilakukan dengan beberapa tahapan, dimulai dari studi literatur mengenai gizi, dashboard dan implementasi menggunakan tableau. Selanjutnya mempersiapkan data yang dibutuhkan dan melalui tahap ETL dan data validation. Setelah datanya valid dan sesuai dengan kebutuhan user, maka akan akan dilanjutkan ketahapan akhir yaitu visualisasi dan pembuatan dashboard.

III.	HASIL DAN PEMBAHASAN

Bagian ini menguraikan hasil dari proses ekstraksi dari datasource dan pengolahannya terkait gizi di Indonesia, sehingga nantinya didapati output berupa visualisasi yang nantinya akan dibentuk menjadi dashboard.

A.	Pengolahan Data

Sumber data (datasource) yang digunakan dalam penelitian ini berupa data terkait gizi di Indonesia. Datasource dibentuk dalam format excel yang mana datanya diperoleh dari Profil Kesehatan Indonesia Tahun 2020 dan Website Kementrian Kesehatan Republik Indonesia. Data ini memiliki 10 variable, meliputi Setelah data diperoleh, masukan data gizi di Indonesia dalam format excel

B.	Eksekusi Data

Tahapan ini memperlihatkan proses eksekusi dari datasource atau sumber data awal menggunakan platform tableau.
1.	Proses input atau memasukan data dan proses read atau membaca data yang akan diproses yang masih berupa format excel.
2.	Setelah itu koneksi data ke platform tableau, yaitu menghubungkan datasource ke platform tableau. 
3.	Selanjutnya melakukan proses pengolahan beserta proses analisis data dari data gizi berdasarkan variabel yang ditentukan. 

C.	Visualisasi Data Gizi 

Setelah dilakukannya penginputan data ke tableau, akan dilanjutkan dengan proses visualisasi dari tiap-tiap variable yang diinginkan. 
1)	Peta Sebaran Gizi
     Disini kita akan menampilkan peta sebaran gizi di Indonesia seperti terlihat pada gambar . Peta ini menampilkan jumlah gizi-gizi yang ada d Indonesia pada setiap provinsi. Jumlah tersebut akan terlihat ketika users meletakkan kursor ke bagian dari peta. 
    
     ![image](https://user-images.githubusercontent.com/100757750/174733268-d8ac87a0-ab4f-492b-85b3-08724ec5d0b1.png)

     Untuk pembuatannya, klik variable provinsi yang sudah dalam bentuk Geographical Role ( state ) dan tahan geser masukan kedalam Rows, kemudian masukkan variable gizi buruk, kurang, sedang dan lebih ke dalam sheet sehingga nanti akan mincul jumlah gizi menurut provinsi. Tidak lupa kita masukan juga variable provinsi ke dalam filter untuk memfilter data agar tidak terjadi double counting. Kemudian Show me untuk menampilkan Maps yang sesuai dengan data yang akan divisualisasikan.
2)	Total Balita, Stunting, Wasting, dan Underweight
     Untuk memberi informasi kepada users disini kita membuat total dari balita dan kategori gizi buruk yang ada di Indonesia.
   
     ![image](https://user-images.githubusercontent.com/100757750/174743868-16e6854c-bf3e-4d17-8352-4d0fbf071828.png)

    Cara menampilkan total tersebut cukup mudah, yaitu dengan cara klik dan tahan variable yang diinginkan yaitu total balita, stunting, wasting, dan underweight kemudian pindahkan ke kolom Marks paling bawah. Setelah itu ubah variable yang awalnya dari Detail menjadi Teks. 
3)	Peta Sebaran  Stunting, Wasting, dan Underweight
     Selain peta sebaran gizi di Indonesia, users juga dapat melihat peta sebaran dari kategori gizi buruk yang ada di Indonesia yaitu Stunting, Wasting, dan Underweight. Peta akan terlihat ketika users mengklik jumlah dari Stunting, Wasting, ataupun Underweight. Jika sudah di klik users akan dibawa ke laman yang berisi peta sebaran.
    
    ![image](https://user-images.githubusercontent.com/100757750/174732543-263c4484-4f0d-4c54-8a77-f5d2b4f11b5f.png)

     Cara membuatnya sama dengan cara membuat peta sebaran gizi, yaitu dengan klik dan tahan variable provinsi yang sudah dalam bentuk Geographical Role ( state ) dan tahan geser masukan kedalam Rows, kemudian masukkan variable Stunting, Wasting, dan Underweight ke sheets. Kemudian Show me untuk menampilkan Maps yang sesuai dengan data yang akan divisualisasikan.
4)	Gizi Buruk per Provinsi
     Disini users akan diperlihatkan keadaan gizi buruk perprovinsi. Users dapat melihat jumlah gizi buruk dari masing-masing provinsi dengan cara mengarahkan kursor ke tabel yang tersedia kemudian secara langsung,  users juga dapat melihat provinsi mana yang memiliki jumlah gizi buruk paling banyak dengan cara melihat warna gelap pada tabel yang tersedia.
     
     ![image](https://user-images.githubusercontent.com/100757750/174744399-ef001b6e-0b86-47dd-be2e-121e1608f460.png)
     
     Untuk menampilkan table pada gambar adalah dengan cara menggunakan variable provinsi dan gizi buruk. Kemudian Shows Me untuk memilih visualisasi sesuai gambar di atas.
5)	Faktor yang Mempengaruhi Gizi Buruk
     Kemudian pada dashboard juga akan ditampilkan faktor-faktor yang mempengaruhi gizi buruk. Faktor-faktor tersebut nantinya dapat dipilih oleh users, terdapat 10 faktor yang dapat dipilih users. Faktor tersebut akan divisualisasikan dalam bentuk bar chart yang menampilkan persentase faktor dari setiap  provinsi.
    
    ![image](https://user-images.githubusercontent.com/100757750/174732016-0db8d815-ca8f-4c76-be9b-2c12cf6c1b86.png)

     Pembuatan visualisasi factor-faktor yang mempengaruhi gizi buruk dilakukan dengan cara menarik variable provinsi ke dalam Columns dan variable factor- factor yang dibentuk melalui Create Calculated Field ke dalam Rows.  Setelah itu Show me untuk menampilkan bar chart yang sesuai dengan data yang akan divisualisasikan.
6)	Kategori Gizi Buruk
     Selanjutnya adalah visualisasi kategori gizi buruk, pada visualisasi ini melibatkan variable provinsi dan kategori gizi buruk yaitu Stunting, Wasting, dan Underweight. Users dapat memilih kategori mana yang ditampilkan. Visualisasi dibuat dalam bentuk bar chart yang menampilkan jumlah dari tiap kategori.
     
     ![image](https://user-images.githubusercontent.com/100757750/174731551-81862636-4568-489d-bf63-2a8ae8454a11.png)
     
     Untuk pembuatannya dilakukan dengan cara memasukan variable provinsi ke dalam Rows dan kategori gizi buruk yang sudah dibentuk melalui Create Calculated Field ke dalam Columns. Setelah itu Show me untuk menampilkan bar chart yang sesuai dengan data yang akan divisualisasikan.

D.	Pembuatan Dashboard

Dashboard dibuat dengan menggabungkan semua visualisasi yang telah dibentuk. Dashboard berisikan jumlah balita, stunting, wasting, dan underweight. Selain itu juga terdapat peta sebaran gizi di Indonesia, gizi buruk per provinsi. Factor yang mempengaruhi gizi buruk dan kategori gizi buruk per provinsi. Hal lain yang terdapat pada dashboard ini adalah Ketika users meng klik jumlah stunting, wasting ataupun underweight maka akan muncul peta sebaran dari kategori yang di klik.

![image](https://user-images.githubusercontent.com/100757750/174743112-2f157af5-53ed-4896-9f8d-04309ecd606b.png)

Dashboard yang dirancang dengan rapi dan terorganisasi dapat berperan dalam mempercepat penyampaian  informasi dan memudahkan  pengambilan keputusan. Berikut merupakan  link tableau dashboard Gizi Buruk Balita di Indonesia Tahun 2020 (https://public.tableau.com/app/profile/hady.rizaldy.gunawan/viz/GiziBurukBalitadiIndonesia/Dashboard?publish=yes ).

V.	KESIMPULAN

Data gizi buruk yang digunakan dari Profil Kesehatan Indonesia dan website  Kemenkes ternyata dapat divisualisasikan dengan baik dan sistematis menggunakan platform tableau. Dashboard yang baik dan dirancang dengan rai, sistematis, dan terorganisasi dapat mempercepat penyampaian informasi dan memudahkan pengambilan keputusan.
