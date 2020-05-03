# SoalShiftSISOP20_modul4_D08

05111840000001 KANA REKHA

05111740000169	MUHAMMAD FARHAN HAYKAL

- [SoalShiftSISOP20_modul4_D08](#soalshiftsisop20modul4d08)
	- [Soal 1](#soal-1)
	- [Soal 4](#soal-4)
	
## Soal 1
* Pertama jalannya program itu memanggil fungsi fuse di main-nya . Didalam parameter terdapat Xmp_oper yang merujuk pada deklarasi struct . 
* Didalam struct tersebut ada xmp_getattr (untuk mengambil path file) , xmp_readdir(membaca direktori), xmp_mknod(membuat file) , xmp_mkdir (membuat direktori ), xmp_unlink (menghapus file ), xmp_rmdir (menghapus direktori) , xmp_rename (mengganti nama file/direktori) , xmp_truncate (edit file) , xmp_open (buka file/direktori) , xmp_read (baca file/direktori) , xmp_write (menulis ke file ) , decryptV1 untuk proses dekripsi , encryptV1 untuk proses enkripsi .
* Mendefinisikan direktori yang akan di mount yang ditampung ke variable dir_path dan mendefinisikan caesar chipnya.Selanjutnya mengarah ke xmp_getattr yang membawa parameter path . Kemudian membandingkan path dengan fungsi strncmp dengan 6 karakter dan /encv1_ .Apabila benar maka akan memanggil fungsi decryptV1 yaitu untuk dekripsi nama path file.
* Pada fungsi decryptV1 membawa parameter src yang berisi nama path file .Kemudian menghitung panjang path filenya yang ditampung ke variable len.Melakukan looping sampai len dan apabila bertemu '/'  akan berhenti dan mendapat akan titik mulai untuk dekripsinya dan '.' maka akan berhenti dan akan memutuskan ekstensi karena ekstensi tidak akan di dekripsi. Kemudian melakukan looping lagi dengan i dimulai dari titik start yang didapat tadi sampai len , Lalu didalam looping tersebut saat nama path bertemu dengan '/' maka akan diabaikan dan dilanjutkan dengan menghitung caesar character dan melakukan perulangan yang didalamnya melakuka proses dekripsi. 
* Pada funsgi encryptV1 membawa parameter src yang bersini nama path file . proses melakukan enkripsi kurang lebih sama dengan dekripsi yang berbeda pada karakter-karakter akan direplace dengan index - key (10)
* Pada funsgi readdir terdapat fungsi filler yang berfungsi untuk saat proses enkripsi telah selesai fungsi tersebut yang akan mengisi ke direktori mount.
## Soal 4
* Mendefinisikan fs.log yang ditampung pada variable log_path.
* fp = fopen (log_path, "a+") disini berfungsi untuk jika file fs.log itu belum dibuat maka akan dibuat ,  dan kita akan membuka file untuk membaca dan menambahkan isi ke dalam file tsb (menambahkan tulisan di akhir file)
* Kemudian akan mengambil time dan mengekstractnya . Kemudian menampungnya ke variabel time .
* Untuk levelnya ada 2 yaitu WARNING hanya untuk unlink dan rmdir .Selain itu termasuk kedalam INFO . 
* Pada fungsi unlink dan rmdir itu akan mempassing level WARNING. Selain fungsi itu akan mempassing level INFO.



