# basis-data-praktikum1
## 1. Membuat database dengan nama: latihan2
    CREATE DATABASE latihan2;
![Screenshot_12](https://user-images.githubusercontent.com/115523263/231242104-fb519d60-d96d-415a-8a73-ecdc0e1c76e6.png)
## 2. gunakan database latihan2 untuk membuat table
    USE latihan2;
![Screenshot_13](https://user-images.githubusercontent.com/115523263/231245280-dc6bd7d6-6260-47cc-846f-2c6448313573.png)
##  menampilkan basis data yang ada pada server database MySQL
    SHOW databases;
![image](https://user-images.githubusercontent.com/115523263/231242670-e0bff32d-6804-4313-bd96-a18150f325bb.png)
## 3. Membuat tabel mahasiswa di dalam database latihan2
    CREATE TABLE mahasiswa (nama VARCHAR(100), alamat TEXT);
![image](https://user-images.githubusercontent.com/115523263/231243220-2e0a72f9-670b-4a49-97c7-3f712aeca14c.png)
## 4. menambahkan kolom keterangan (varchar 15)
    ALTER TABLE mahasiswa ADD COLUMN keterangan varchar(15);
![image](https://user-images.githubusercontent.com/115523263/231243708-d0a7ec73-e904-442e-8f49-752056c3d0d4.png)
## 5. menambahkan kolom id (int 11) di awal sebagai kolom pertama
    ALTER TABLE mahasiswa ADD COLUMN id int(11) First;
![image](https://user-images.githubusercontent.com/115523263/231244263-7449bd92-eef8-4c07-bc5e-111690b4c392.png)
## 6. menambahkan kolom phone (varchar 15) setelah kolom alamat
    ALTER TABLE mahasiswa ADD COLUMN phone varchar(15) after alamat;
![image](https://user-images.githubusercontent.com/115523263/231246166-28524698-798f-4127-b267-0aebae0da76f.png)
## 7. Mengubah tipe data kolom id menjadi char(11)
    ALTER TABLE mahasiswa MODIFY COLUMN id VARCHAR(11);
![image](https://user-images.githubusercontent.com/115523263/231246536-adacbf4f-18f7-4821-bdb6-d4cb9b1ab854.png)
## 8. Mengubah nama kolom phone menjadi hp (varchar 20)
    ALTER TABLE mahasiswa CHANGE COLUMN phone hp varchar(20);
![image](https://user-images.githubusercontent.com/115523263/231246893-680bd7f0-e2db-4b99-8b47-87ed3affbc31.png)
## 9. Menambahkan kolom email setelah kolom hp
    ALTER TABLE mahasiswa ADD COLUMN email text after hp;
![image](https://user-images.githubusercontent.com/115523263/231247303-142a16b9-a867-47ee-a7d2-16ba0ec1bf7c.png)
## 10. Menghapus kolom keterangan dari tabel
    ALTER TABLE mahasiswa DROP keterangan;
![image](https://user-images.githubusercontent.com/115523263/231247588-6969997b-a60a-4c30-85a9-b1c551771d9d.png)
## 11. Mengganti nama tabel yang awal nya mahasiswa menjadi data_mahasiswa
    ALTER TABLE mahasiswa RENAME data_mahasiswa;
![image](https://user-images.githubusercontent.com/115523263/231247936-f0d01d51-9ac4-4737-afef-a6f047d5b3a2.png)
## 12. Mengganti nama field id menjadi nim
    ALTER TABLE data_mahasiswa CHANGE COLUMN id nim varchar(11);
![image](https://user-images.githubusercontent.com/115523263/231248295-9da63f6d-5b33-4c9b-853e-fbed86cad8aa.png)
## 13. Menjadikan nim sebagai PRIMARY KEY
    ALTER TABLE data_mahasiswa ADD PRIMARY KEY(nim);
![image](https://user-images.githubusercontent.com/115523263/231248699-5c4c329f-e8d0-429b-ac50-da83f09d69c3.png)
## 14. Menjadikan kolom email sebagai UNIQUE KEY
    ALTER TABLE data_mahasiswa ADD CONSTRAINT email unique KEY(email);
![image](https://user-images.githubusercontent.com/115523263/231249008-7cb9aada-4dc8-4f6e-ac53-a7bc0d7c976b.png)
# hasil output akhir
![image](https://user-images.githubusercontent.com/115523263/231250722-09c04d0f-7580-407e-8331-90b465f590b5.png)
# evaluasi
- Apa yang di maksud dengan int (11)? 

Int(11) bermaksud sebagai sebuah data yang menggunakan jenis data Integer dengan panjang karakter sebanyak 11. Ini berarti bahwa jenis data Int(11) digunakan untuk merepresentasikan nilai bilangan bulat dengan panjang maksimal 11 karakter.
- apa yang dimaksud dengan kolom Null yang berisi yes dan no

Jika kita menggunakan perintah desc untuk melihat struktur tabel, kita akan menemukan kolom Null yang berisi Yes dan No. Apabila nilai pada kolom Null adalah No, itu berarti data yang tersedia harus diisi atau diinputkan. Sebaliknya, jika nilai pada kolom Null adalah Yes, itu berarti data yang tersedia tidak perlu diisi atau diinputkan dan dapat dikosongkan.
