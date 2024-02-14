"# tutorial-1" 

## Reflection 1

Setelah menggunakan Spring Boot, saya mengalami berbagai manfaat, 
di antaranya mempermudah pengembangan aplikasi Java dengan cepat dan efisien.

Dengan menerapkan prinsip clean code, yaitu memastikan setiap fungsi memiliki 
dependency yang jelas dalam melaksanakan tugasnya, serta melakukan penulisan 
kode yang bersih dan terdokumentasi dengan baik dengan mengurangi penulisan komentar 
yang tidak perlu jika kode sudah cukup jelas, pengelolaan kode menjadi lebih efisien 
dan lebih mudah dipahami oleh pembaca.

Saya mengalami beberapa kesalahan, salah satunya adalah mendapatkan error ketika membuka 
page localhost. Ini terjadi saat saya memilih dependencies (Thymeleaf) yang ada di spring 
initializer. Solusinya adalah ketelitian dalam memilih semua dependencies yang dibutuhkan.
git c
## Reflection 2

- Dengan menerapkan unit testing, saya merasa lebih percaya dengan code saya. Jika ada error 
atau kesalahan code, kita menjadi tau fungsi apa yang terjadi error. Namun, suatu kode akan 
baik atau berhasil tergantung dengan akurasi unit-test yang dibuat. 

Jumlah unit test yang dibuat dalam suatu kelas tergantung pada kompleksitasnya. Sebaiknya 
kita menguji semua kondisi atau fungsionalitas yang berbeda.

Ada beberapa hal yang dapat memastikan unit-test cukup untuk memverifikasi program,
satunya adalah dengan code coverage untuk megukur sejauh mana kode kita telah diuji. Semakin
tinggi code average, semakin tinggi kemungkinan kita telah menguji sebagian besar kode. Namun, 
code average tidak menjamin 100% bahwa kita telah menguji semua kemungkinan kasus dan logika dalam
kode. 

Setelah menerapkan clean code pada CreateProductFunctionalTest.java saya memiliki beberapa isu yaitu 
duplikasi kode, Solusinya dengan mengekstraksi kode yang sama ke dalam metode utilitas dan memanggilnya 
dari metode tersebut. Isu ini juga bisa menjadi pertimbangan untuk membuat rangkaian functional test baru 
yang mirip dengan yang sudah ada. 



"# tutorial-2"


## Reflection 1

- Tidak diperlukannya modifier pada class dan metode pengujian JUnit5

Pada JUnit5, seharusnya class dan metode pengujian memiliki visibilitas default atau package-private Penggunaan modifier public pada class atau metode tidak direkomendasikan karena dapat mengakibatkan akses yang tidak diinginkan dan mengganggu isolasi pengujuan.


Solusi: Untuk mengubah visibilitas class atau metode pengujian, kita perlu menghapus kata kunci public atau protected sehingga menggunakan modifier default atau package-private.

-  Tidak diperlukannya import yang tidak diperlukan

Adanya unnecessary import dalam kode dapat menyebabkan berbagai masalah, seperti meningkatkan kompleksitas kode, memperlambat proses kompilasi, dan membuat kode sulit dipahami Oleh karena itu, penting untuk menghapus import yang tidak diperlukan dan hanya menambahkan import yang benar-benar diperlukan dalam kode kita.


Solusi: Untuk menghapus import yang tidak diperlukan, kita perlu melakukan pengecekan secara manual dan menghapus import yang tidak digunakan. Selain itu, kita juga perlu menambahkan import yang benar-benar diperlukan dalam kode kita.


## Reflection 2

Mengganti penggunaan injeksi @Autowired dengan menginisialisasi class secara langsung

Framework dependensi Spring menggunakan anotasi @Inject dan @Autowired untuk melakukan dependency injection Namun, penggunaan injeksi seperti ini dapat menyebabkan masalah terkait mutabilitas dan behavior yang tidak dapat diprediksi.


Solusi: Untuk menghindari masalah tersebut, kita dapat mengganti objek yang menggunakan injeksi @Autowired dengan menginisialisasi class secara langsung.












