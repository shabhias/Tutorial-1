# MODULE 1

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




# MODULE 3


## Reflection

1. Explain what principles you apply to your project!
    
   - SRP, memisahkan antara CarController yang pada awalnya ada di ProductController
   - OCP, menambahkan metode update pada model agar pemanggilan metode lebih umum pada repository
   - ISP, memisahkan interface productService dan juga carService agar moduleritas lebih baik dibandingkan menggabungkan keduanya menjadi satu.Pendekatan ini dapat meningkatkan efisiensi dalam mengimplementasikan metode abstrak dan struktur kode menjadi lebih fleksibel.
   - DIP, Pada CarRepository, saya mengganti objek dari CarServiceImpl yang merupakan kelas konkret menjadi CarService yang merupakan antarmuka, agar mengurangi atau menghilangkan hubungan antar komponen-komponen kelas konkret yang dapat disebut sebagai decoupling.
   
2. Explain the advantages of applying SOLID principles to your project with examples.
    - SRP, kode menjadi lebih terorganisir dengan cara memisahkan dependency tiap kelas, memudahkan pemahaman dan komunikasi antar pengembang.
    - OCP, dapat meningkatkan fleksibilitas dan meminimalkan dampak perubahan.
    - LSP, dapat mengurangi ketergantungan antar kelas
    - ISP, dapat memungkinkan polimorfisme yang lebih baik dan mengurangi ketergantungan antar kelas.
    - DIP, dapat mengurangi dampak perubahan pada satu bagian kode terhadap bagian kode lainnya.

    

3. Explain the disadvantages of not applying SOLID principles to your project with examples.
    - Jika tidak mengikuti DIP dan OCP, dapat mengakibatkan keterikatan yang kuat antara controller dan implementasi. Hal ini dapat menghasilkan testing yang buruk dan sulit untuk beralih antara implementasi untuk testing.
    - Kesulitan dalam memahami dan memelihara kode karena tidak menerapkan SRP sehingga banyak tanggung jawab oleh controller, repository, atau model. 
    - Jika tidak mengikuti ISP dan LSP, basis kode terikat erat dan kurang fleksibel karena antarmuka, abstraksi, atau kelas dasar dengan metode maupun dependensi yang tidak perlu.


   
# MODULE 4

## Reflection

1. Reflect based on Percival (2017) proposed self-reflective questions (in “Principles and Best Practice of Testing” submodule, chapter “Evaluating Your Testing Objectives”), whether this TDD flow is useful enough for you or not. If not, explain things that you need to do next time you make more tests.
   - Saya memastikan bahwa kode yang dibuat sudah memiliki tes fungsional agar bisa meyakinkan bahwa aplikasi saya sudah berfungsi. Namun, untuk meningkatkan keakuratan pengujian, saya perlu memastikan tes saya mencakup semua kasus yang diuji
   - Tes yang saya buat, memastikan saya untuk melakukan refaktor kode dan juga saya mempertimbangkan jika diperlukan unit test tambahan bergantung pada kebutuhan. 
   - Saya berusaha memperbaiki tes secara teratur untuk memastikan tes berjalan dengan baik. Namun saya terus mencari cara agar dapat mendeteksi bug secara efisien.

2. You have created unit tests in Tutorial. Now reflect whether your tests have successfully followed F.I.R.S.T. principle or not. If not, explain things that you need to do the next time you create more tests.
   - Saya sudah membagi test menjadi functional test dan unit test yang mempunyai dependency yang berbeda. Dan memfokuskan setiap tes memiliki fokus masing-masing.
   - Tes saya sudah dirancang untuk berjalan secepat mungkin dengan mencari cara untuk meningkatkan efisiensi dan kecepatan tes.
   - Menerapkan teknik mock, setUp, tearDown, dll agar terhindar dari duplikasi
   - Menggunaka teknik Test Double pada saat fungsi saya membutuhkan fungsi lain.
   - Pengujian mencakup semua happy path dan unhappy path dan memperhatikan tiap tes mencakup semua kasus yang mungkin terjadi. 




