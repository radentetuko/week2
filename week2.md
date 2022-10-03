# Materi Week 2

## 1. JavaSripct Dasar - Scope & Function

- ### **Scope**

  Variabel JavaScript hanya memiliki dua scope. Terdapat dua jenis variabel scope yang ada di JavaScript yaitu **Global Variable** dan **Local Variable**.

  - #### **Local Variable**

    Variable local scope atau variable fungsi lokal adalah variabel yang dideklarasikan di dalam fungsi pada JavaScript. Variabel lokal hanya dapat diakses dari dalam fungsi tersebut. Oleh karena itu, kita tidak dapat menjangkau mereka dari fungsi lain di dokumen kita.

    ```javascript
    // dibagian ini variabel 'makanan' tidak dapat diakses

    function simpleFunction() {
      var makanan = "Bakso";

      // jika variabel 'makanan' ditaruh di dalam sini maka variabel 'makanan' dapat diakses
    }
    ```

  - #### **Global Variable**

    Semua variabel yang dibuat di luar fungsi disebut variabel global JavaScript. Objek semacam itu dapat diakses di seluruh situs web. Variabel global memiliki cakupan JavaScript global. Semua fungsi dapat mengaksesnya di seluruh halaman web:

    ```javascript
    var makanan = "Bakso";
    // disini kamu bisa menggunakan variabel 'makanan'

    function simpleFunction() {
      // disini kamu bisa menggunakan variabel 'makanan'
    }
    ```

- ### **Function**

  Fungsi adalah sub-program yang bisa digunakan kembali baik di dalam program itu sendiri, maupun di program yang lain.

  - #### 4 Cara menggunakan Function

    1. Membuat Fungsi dengan Cara Biasa

       Cara ini paling sering digunakan, terutama buat yang baru belajar Javascript.

       ```javascript
       function namaFungsi() {
         console.log("Hello World!");
       }
       ```

    2. Membuat Fungsi dengan Ekspresi

       Kita menggunakan variabel, lalu diisi dengan fungsi.

       ```javascript
       var namaFungsi = function () {
         console.log("Hello World!");
       };
       ```

    3. Membuat Fungsi dengan Tanda Panah

       Cara ini sering digunakan di kode Javascript masa kini, karena lebih sederhana. Akan tetapi sulit dipahami bagi pemula. Fungsi ini mulai muncul pada standar ES6.

       ```javascript
       var namaFungsi = () => {
         console.log("Hello World!");
       };

       // atau seperti ini (jika isi fungsi hanya satu baris):
       var namaFungsi = () => console.log("Hello World!");
       ```

    4. Membuat Fungsi dengan Kostruktor

       Cara ini sebenarnya tidak direkomendasikan oleh Developer Mozilla, karena terlihat kurang bagus. Soalnya body fungsinya dibuat dalam bentuk string yang dapat mempengaruhi kinerja engine javascript.

       ```javascript
       var namaFungsi = new Function('console.log("Hello World!");');
       ```

  - #### Perbedaan Parameter dan Argument

    Parameter adalah syarat input yang harus dimasukkan ke dalam suatu fungsi dan dideklarasikan bersama dengan deklarasi fungsi. Sementara argument adalah nilai yang dimasukan ke dalam suatu fungsi, sesuai dengan persyaratan parameter, di mana argument dituliskan bersamaan dengan pemanggilan fungsi.

    Contoh :

    ```javascript
    function operasiPerkalian(angka1, angka2) {
      return angka1 * angka2;
    }

    console.log(operasiPerkalian(2, 6)); // Output: 12;
    ```

    Penjelasan :

    - **angka1 & angka2** adalah parameter.
    - **2 & 6** adalah argument.

  - #### Menampilkan data di console

    Browser pada umumnya mempunyai tab console yang bisa digunakan untuk menampilkan data console.log dari kode JavaScript. Untuk mengaktifkan tab console di Chrome, bisa dilakukan dengan pilih menu View -> Developer -> Developer Tools atau dengan tekan tombol F12 atau kombinasi tombol Ctrl-Shift-I

    ![Console](https://www.javascripttutorial.net/wp-content/uploads/2019/12/web-development-tool-console-tab.png)

    Apa gunanya _console.log_ ini? Dengan console.log, output dari variabel atau operasi yang kita masukkan tidak akan kelihatan di halaman website dan hanya bisa tampil di tab console. Dengan begitu, output tersebut tidak akan mengganggu tampilan website kamu.

    console.log juga sering digunakan developer ketika mau debug/investigasi kesalahan di kode yang ditulis.

## 2. Data Type Built in Prototype & Method

- ### Tipe Data

  Tipe data ada 2 jenis, primitif dan non primitif

  1. Tipe Data Primitif

     - string
     - Number
     - BigInt
     - Boolean
     - undefined
     - Null
     - Symbol

  2. Tipe Data Non-primitif
     - Object
     - Array

  - string - deretan karakter yang diapit oleh sepasang tanda kutip;
  - number - bilangan bulat, pecahan, dan lain-lain;
  - boolean - nilai benar dari sebuah pernyataan yang dituliskan sebagai true atau false;
  - null - sebuah nilai yang berarti kosong atau menunjuk pada nilai yang tidak ada;
  - undefined - berbeda dari null, undefined menandakan kondisi variabel yang belum diberi sebuah nilai. Jadi pernyataan "nilai variabel itu adalah undefined" sebenarnya kurang tepat, sebab variabelnya memang tidak mempunyai sebuah nilai;
  - symbol - sebuah nilai unik yang dihasilkan tiap kali kita memanggil fungsi Symbol(). Nilai unik ini memiliki beberapa kegunaan seperti memberi nomor identifikasi unik dan berperan sebagai nama properti unik sebuah objek;
  - object - sebuah kumpulan pasangan properti dan nilai. Seperti objek dalam kehidupan sehari-hari saja. Misalnya objek Apel memiliki properti warna dengan nilai merah.

- ### Objek Math

  Objek Math adalah objek yang berisi fungsi-fungsi matematika dan beberapa konstanta untuk melakukan perhitungan matematika seperti sin, cos, tan, eksponen, akar kuadrat, dll.

  - Fungsi Trigonometri di Javascript

    Trigonometri adalah cabang ilmu matematika yang mempelajari tentang sudut dan panjang pada segitiga.

    Nah, di objek Math terdapat fungsi-fungsi untuk menghitung trigonometri.

    Misalkan kita ingin menghitung nilai sin, cos dan tan dari 10, maka pada program kita bisa tulis seperti ini:

    ![trigonometri](https://www.petanikode.com/img/js/math/trigono.avif)

  - Fungsi Logaritma, Pangkat, dan Eksponensial di Javascript

    Logaritma adalah operasi matematika yang merupakan kebalikan (atau invers) dari eksponen atau pemangkatan. 2

    Objek Math di Javascript juga menyediakan fungsi log() untuk logaritma dan pow() untuk pemangkatan.

    ![logaritma](https://www.petanikode.com/img/js/math/log.avif)

    Kemudian untuk menghitung eksponensial, kita dapat menggunakan fungsi exp().

    Contoh:

    ![logaritma](https://www.petanikode.com/img/js/math/exp.avif)

  - Fungsi Pembulatan di Javascript

    Apabila kita membutuhkan bilangan bulat (integer), kita bisa gungakan fungsi pembulatang di objek Math.

    Ada beberapa fungsi yang sering digunakan:

    1. floor() membulatkan ke bawah;
    2. round() membulatkan ke yang terdekat, bisa ke bawah dan ke atas;
    3. ceil() membulatkan ke atas.

    Contoh:

    ![logaritma](https://www.petanikode.com/img/js/math/pembulatan.avif)

  - Fungsi Akar di Javascript

    Untuk fungsi akar kuadrat kita bisa menghitungnya dengan fungsi sqrt().

    contoh :

    1[akar](https://www.petanikode.com/img/js/math/sqrt.avif)

    Untuk akar kubik kita bisa gunakan fungsi cbrt().

    Contoh :

    ![akar](https://www.petanikode.com/img/js/math/cbrt.avif)

    untuk akar n atau nth root, kita bisa akali dengan menggunakan fungsi pow().

    ![akar](https://www.petanikode.com/img/js/math/nth.avif)

  - Fungsi Random dan Mutlak di Javascript

    Fungsi random adalah fungsi yang mengahilkan nilai acak antara 0.0 sampai 1.0.

    ![Random](https://www.petanikode.com/img/js/math/random.avif)

    Fungsi mutlak adalah fungsi yang menghasilkan nilai mutlak atau absolute.

    Contoh:

    ```javascript
    var x = Math.abs(-2);
    ```

    Variabel x akan bernilai 2, karena fungsi abs() akan selalu memberikan nilai mutlak atau positif.

  - Fungsi Minimum dan Maksimum di Javascript

    Fungsi minimum dan maksimum adalah fungsi untuk menentukan nilai paling kecil dan paling besar pada sekumpulan nilai.

    Fungsi ini bisa kita berikan input berupa urutan bilangan.

    Apabila kita ingin memberikan input array, maka array tersebut harus kita pecah isinya.

    Contoh:

    ![minmax](https://www.petanikode.com/img/js/math/minmax.avif)

  - Konstanta di objek math

    Selain menyediakan fungsi-fungsi matematika, objek Math juga menyediakan konstanta seperti PI, E, LN10, dll. yang bisa kita manfaatkan untuk perhitungan rumus tertentu.

    ```javascript
    Math.E; // returns Euler's number
    Math.PI; // returns PI
    Math.SQRT2; // returns the square root of 2
    Math.SQRT1_2; // returns the square root of 1/2
    Math.LN2; // returns the natural logarithm of 2
    Math.LN10; // returns the natural logarithm of 10
    Math.LOG2E; // returns base 2 logarithm of E
    Math.LOG10E; // returns base 10 logarithm of E
    ```

## 3. DOM JavaScript

DOM merupakan singkatan dari Document Object Model.

Artinya, dokumen (HTML) yang dimodelkan dalam sebuah objek.

- ### Mengkases Elemen Tertentu dengan DOM

  Objek document adalah model dari dokumen HTML. Objek ini berisi kumpulan fungsi dan atribut berupa objek dari elemen HTML

  Apabila kita ingin mengakses elemen yang spesifik, terdapat beberapa fungsi yang bisa digunakan:

  - getElementById() fungsi untuk memilih elemen berdasarkan atribut id.
  - getElementByName() fungsi untuk memilih elemen berdasarkan atribut name.
  - getElementByClassName() fungsi untuk memilih elemen berdasarkan atribut class.
  - getElementByTagName() fungsi untuk memilih elemen berdasarkan nama tag.
  - getElementByTagNameNS() fungsi untuk memilih elemen berdasarkan nama tag.
  - querySelector() fungsi untuk memilih elemen berdasarkan query.
  - querySelectorAll() fungsi untuk memilih elemen berdasarkan query.

Fungsi-fungsi di atas cukup sering digunakan untuk mengakses elemen tertentu.

Contoh:

Misalkan kita punya kode HTML seperti ini:

```javascript
<div id="tutorial"></div>
```

Maka untuk memilih element tersebut di Javascript, kita bisa gunakan fungsi getElementByI() seperti ini:

```javascript
// memilih elemen dengan id 'tutorial'
var tutorial = document.getElementById("tutorial");
```

Variabel tutorial akan menjadi sebuah objek DOM dari elemen yang kita pilih.
