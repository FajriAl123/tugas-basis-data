# tugas-basis-data
1. Buat sebuah database dengan nama latihan2!
``` 
CREATE DATABASE latihan1;
```
![WhatsApp Image 2023-04-11 at 07 56 33 (1)](https://user-images.githubusercontent.com/130415622/231028730-22999e91-917a-495e-b20b-7ca80f1af188.jpeg)

!![bdatas 1](https://user-images.githubusercontent.com/130415622/231029748-563f8f68-11e6-4f8d-8723-b30cabb9e3ed.png)



2. Buat sebuah tabel dengan nama biodata (nama, alamat) didalam
database latihan1!
```
CREATE TABLE siswa (nama VARCHAR(100), alamat TEXT);
```
!![bdatas 2](https://user-images.githubusercontent.com/130415622/231029784-29771d94-6080-4bc4-ab03-c091c14c7b22.png)



3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom
terakhir!
```
ALTER TABLE siswa ADD COLUMN keterangan varchar(15) AFTER alamat;
```
!![bdatas 3](https://user-images.githubusercontent.com/130415622/231029817-3bda2989-5232-494a-b05b-395af65a4f23.png)



4. Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
```
ALTER TABLE siswa ADD COLUMN id int(11) First;
```
!![bdatas 4](https://user-images.githubusercontent.com/130415622/231029846-2177fc4b-e3b3-482e-b53e-20af1587613f.png)



5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah
kolom alamat!
```
ALTER TABLE siswa ADD COLUMN phone varchar(15) after alamat;
```
!![bdatas 5](https://user-images.githubusercontent.com/130415622/231029910-58e061b7-53ff-4897-91e3-9b168bd0a196.png)



6. Ubah tipe data kolom id menjadi char(11)!
```
ALTER TABLE siswa MODIFY COLUMN id VARCHAR(11);
```
!![bdatas 6](https://user-images.githubusercontent.com/130415622/231029936-6d4312ac-0e74-459a-b768-c9e748fe00d8.png)



7. Ubah nama kolom phone menjadi hp (varchar 20)!
```
ALTER TABLE siswa CHANGE COLUMN phone hp varchar(20);
```
!![bdatas 7](https://user-images.githubusercontent.com/130415622/231029968-55127ccf-60f8-45ca-9180-380dbf6fe13f.png)



8. Tambahkan kolom email setelah kolom hp
```
ALTER TABLE siswa ADD COLUMN email text after hp;
```
!![bdatas 8](https://user-images.githubusercontent.com/130415622/231029995-41bf23e9-b426-4a2a-84de-5982c59c6f46.png)



9. Hapus kolom keterangan dari tabel!
```
alter table siswa drop keterangan;
```
!![bdatas 9](https://user-images.githubusercontent.com/130415622/231030024-dc445e22-e3ae-41a2-bd1a-f7ac4d7ad8dd.png)



10. Ganti nama tabel menjadi data_mahasiswa!
```
alter table siswa rename data_mahasiswa;
```
!![bdatas 10](https://user-images.githubusercontent.com/130415622/231030067-6ba665f1-196b-4c7d-acda-7779c5edef10.png)



11. Ganti nama field id menjadi nim!
```
ALTER TABLE data_mahasiswa CHANGE COLUMN id nim varchar(11);
```
!![bdatas 11](https://user-images.githubusercontent.com/130415622/231030092-16241c48-9a06-430c-8cf1-a1a3fa05aa26.png)



12. Jadikan nim sebagai PRIMARY KEY!
```
ALTER TABLE data_mahasiswa ADD PRIMARY KEY(nim);
```
!![bdatas 12](https://user-images.githubusercontent.com/130415622/231030127-c015e67a-486d-4a0f-bc46-16ca2fd06194.png)



13. Jadikan kolom email sebagai UNIQUE KEY
```
ALTER TABLE data_mahasiswa ADD CONSTRAINT email unique KEY(email);
```
!![bdatas 13](https://user-images.githubusercontent.com/130415622/231030159-22372933-5d02-47de-8d5e-5aa560552dbf.png)



14. Hasil akhir

!![bdatas 13](https://user-images.githubusercontent.com/130415622/231030221-18264b65-c20d-4d85-8754-0933237746ab.png)



# Evaluasi dan pertanyaan
1. Apa maksud dari int (11)?
```
int (11) nunjukkan bahwa kolom memiliki tipe data bilangan bulat (integer) dengan ukuran 11 digit 
```

2. Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang
berisi Yes dan No. Apa maksudnya ?
```
Jika kolom "Null" adalah "YES", itu berarti kolom tersebut diizinkan untuk memiliki nilai NULL.

Jika kolom "Null" adalah "NO", maka kolom tersebut tidak diizinkan untuk memiliki nilai NULL
```
