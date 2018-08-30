# JASA-TANI
![N|Solid](https://raw.githubusercontent.com/muhammadrofiq/JasaTani/master/app/testlogo.png)



JASA-TANI Merupakan aplikasi penyewaan traktor pertanian berbasis android. Aplikasi ini dikembangkan untuk memudahkan petani dalam mencari penyedia jasa peminjaman alat serta memudahkan penyedia jasa dalam memenejemen usahanya. Aplikasi ini dibagi menjadi dua bagian, yaitu aplikasi untuk petani dan penyedia jasa. Namun saat ini hanya tersedia aplikasi penyedia saja. Berikut usercase yang kami buat pada aplikasi ini : 

![N|Solid](https://raw.githubusercontent.com/muhammadrofiq/JasaTani/master/app/Untitled%20Diagram(2).png)


  - Kami memberikan model haar cascade dalam bentuk XML yang dihasilkan melalui process pelatihan yang cukup lama
  - Model KNN yang kami berikan hanya model sederhana yang kami latih menggunakan beberapa tipe font plat nomor. 

# The Features!
  - main.py, merupakan program inti untuk mendeteksi karakter pada platnomor
  - Single-cap, pengguna dapat melakukan capturing image menggunakan camera laptop kemudian image tersebut dieksekusi menggunakan main.py
  - Program ini dapat terkoneksi ke arduino 


untuk saat ini program koneksi ke arduino sedang tidak diaktifkan.



### Tech

project ini menggunakan beberapa teknologi, yaitu:

* Python 
* Opencv python 

### Diagram

Ada beberapa tahapan yang dilakukan program ini untuk mengenali karakter pada plat nomor kendaraan.
![](http://i1250.photobucket.com/albums/hh532/qwense/Alur%20OCR_zpsxhx7su2w.jpg)

* Image input yang diproses akan disegmentasi atau diambil bagian **platnomornya saja** menggunakan model harcascade yang telah dibuat
* Setelah gambar terfokus pada bagian platnomor saja dilakukanlah **praprocessing**, dengan memaksimalkan kontras dan penghalusan citra dengan gaussian blur.
* Langkah selanjutnya adalah mendeteksi karakter yang terdapat pada plat nomor kendaraan. program ini mendeteksi **seluruh kontur** pada citra.
* Kontur yang telah didapatkan akan di **filter** dengan menyaring kontur yang benar benar memiliki **karakteristik seperti huruf dan angka** kemudian mengelompokannya sesuai dengan kemiripan ukuran dengan karakter lain.

Berikut ini merupakandiagram dari fungsi automation gate.
![](http://i1250.photobucket.com/albums/hh532/qwense/Alur%20Gate%20Automization_zpslzhzepyo.jpg)

Jika anda ingin mengkoneksikan project ini ke arduino, berikut skema arduino yang di perlu di buat.
![](http://i1250.photobucket.com/albums/hh532/qwense/Skema%20arduino_zpsj9wrke9m.png)
### Installation


Install Opencv python mengikuti petunjuk ini:
[installation guide](https://www.pyimagesearch.com/2015/06/22/install-opencv-3-0-and-python-2-7-on-ubuntu/)
Clone atau download project OCR-WKWK dan extract.
Masuk kedalam directory src dan jalankan program single-cap.py
```sh
$ cd src
$ workon cv
$ python single-cap.py
```

### Notes
Program ini dibuat diatas sistem operasi linux, sehingga ada kemungkinan beberapa fungsi ada yang tidak berjalan pada sistem operasi lain. 

License
----

Ga ada.


