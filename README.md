# Jawaban soal
## 1.
<img width="1920" height="1080" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/39450f98-522c-49d2-bc61-c59548794e05" />

## 2.
`h1 { ... }`
Pendeklarasian ini menggunakan selektor elemen, artinya semua elemen `<h1>` yang ada di dalam halaman web akan mendapatkan gaya (style) yang sama. Aturan ini bersifat global, sehingga berlaku untuk setiap `<h1>` tanpa memandang lokasinya. Misalnya, jika ada `<h1>` di bagian header, intro, atau footer, semuanya akan otomatis mengikuti style yang ditentukan. Dengan kata lain, `h1 { ... }` cocok digunakan ketika kita ingin memberikan tampilan seragam untuk semua judul utama pada halaman.

`intro h1 { ... }`
Pendeklarasian ini lebih spesifik karena menggunakan kombinasi selektor ID dan elemen. Aturan hanya berlaku untuk `<h1>`yang berada di dalam elemen dengan `id="intro"`. Jadi, kalau ada beberapa `<h1>` di halaman, hanya `<h1>` di dalam area #intro yang terpengaruh, sedangkan `<h1>` lain tetap menggunakan aturan berbeda atau gaya default. Selektor ini berguna ketika kita ingin memberikan gaya khusus pada judul tertentu di dalam sebuah bagian halaman, tanpa memengaruhi `<h1>` lainnya.

## 3.
Jika ada deklarasi CSS internal, eksternal, dan inline untuk elemen yang sama, maka yang akan ditampilkan oleh browser adalah deklarasi dengan prioritas tertinggi. Urutan prioritasnya seperti ini:

1. Inline CSS → Paling kuat, karena ditulis langsung di dalam elemen HTML dengan atribut style="".
2. Internal CSS → Ditulis di dalam tag <style> pada file HTML yang sama.
3. Eksternal CSS → Ditulis di file .css terpisah lalu dipanggil dengan <link>.

Jadi, jika ketiga deklarasi itu ada pada elemen yang sama, maka yang tampil di browser adalah style dari inline CSS, kecuali ada aturan khusus seperti penggunaan !important pada internal/eksternal, yang bisa mengubah prioritas.

**Inline CSS**
Prioritas tertinggi karena ditulis langsung di elemen HTML.
```
<h1 style="color: red;">Hello World</h1>
```

**internal**
Prioritas lebih rendah dibanding inline. Jika keduanya ada, browser akan membaca urutan terakhir.
```
<style>
  h1 { color: green; } /* Internal */
</style>
```

**eksternal**
```
/* style.css (Eksternal) */
h1 { color: blue; }
```

## 4.
Jika pada sebuah elemen HTML terdapat ID dan Class sekaligus, lalu keduanya memiliki deklarasi CSS masing-masing, maka style yang ditampilkan di browser adalah style dari ID. Hal ini karena dalam hirarki prioritas CSS, ID selector lebih kuat (specificity lebih tinggi) dibandingkan Class selector.

***Misalnya, ada elemen berikut:***
```
<p id="paragraf-1" class="text-paragraf">Ini contoh paragraf.</p>
```

***Kemudian didefinisikan CSS:***
```
.text-paragraf {
  color: blue;   /* Class */
}

#paragraf-1 {
  color: red;    /* ID */
}
```

Meskipun elemen tersebut memiliki Class dengan warna biru, browser akan menampilkan teks paragraf berwarna merah, karena aturan dari ID #paragraf-1 mengalahkan aturan dari Class .text-paragraf.

Dengan demikian, dapat disimpulkan bahwa ketika sebuah elemen memiliki ID dan Class bersamaan, deklarasi CSS ID yang akan ditampilkan di browser, kecuali ada aturan khusus seperti penggunaan !important yang bisa mengubah prioritas.




# penjelasan dari setiap langkah praktikum beserta screenshotnya.

## 1. Membuat dokumen HTML
<img width="1920" height="1080" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/dcc17909-2acf-4d41-b1e6-97d0151270cb" />
Halaman web pada gambar tersebut menampilkan hasil dari penggunaan HTML dasar dengan penerapan internal dan inline CSS. Struktur halaman terdiri dari judul besar “CSS Internal dan Inline CSS”, tautan menuju materi CSS dasar, sebuah heading “Hello World”, serta paragraf yang berisi penjelasan tentang pembelajaran HTML dan CSS di mata kuliah Pemrograman Web di Universitas Pelita Bangsa. Selain itu, terdapat tautan tambahan “Informasi selengkapnya” yang mengarahkan pengguna pada informasi lebih lanjut. Tampilan masih sederhana karena berfokus pada pengenalan dasar penggunaan tag-tag HTML serta CSS.

## 2. Mendeklarasikan CSS Internal
<img width="1920" height="1080" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/d3a61c15-3b3f-458d-b370-97aff7a34fba" />
Kode HTML tersebut menggunakan CSS internal yang ditulis langsung di dalam tag <style> pada bagian <head>. Dengan pendekatan ini, styling hanya berlaku untuk halaman yang sama. Pada contoh tersebut, beberapa elemen dasar diberikan gaya sederhana, misalnya teks di dalam <header> diberi warna biru tua, link di dalam <nav> diberi warna hijau tua dengan jarak antar-link, dan paragraf pada bagian #intro dibuat lebih rapi dengan margin tambahan. Selain itu, tombol yang dibuat menggunakan class .button diberi latar belakang biru, teks putih, serta sudut membulat agar terlihat lebih menarik, dan ketika diarahkan kursor (hover), warnanya berubah menjadi lebih gelap.

Penerapan CSS internal seperti ini cocok digunakan untuk latihan atau proyek sederhana karena mudah dibaca dan dipahami. Namun, jika halaman web semakin besar, biasanya digunakan CSS eksternal agar lebih terorganisir. Dalam contoh ini, fokus utamanya adalah mengenalkan bagaimana CSS bekerja untuk mengatur tampilan teks, link, dan tombol dengan cara yang sangat sederhana. Dengan begitu, mahasiswa dapat melihat langsung perbedaan tampilan saat menggunakan CSS dibandingkan hanya dengan HTML biasa.

## 3. Menambahkan Inline CSS
<img width="1920" height="1080" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/f5719579-5dfb-4a46-a1fd-542954e52817" />
Internal CSS adalah cara menuliskan kode CSS di dalam tag <style> pada bagian <head> sehingga aturan gaya bisa dipakai berulang kali pada beberapa elemen sekaligus, sedangkan Inline CSS ditulis langsung pada atribut style di tiap elemen HTML sehingga efeknya hanya berlaku untuk elemen tersebut saja. Dengan internal CSS, pengaturan tampilan lebih terstruktur dan mudah dikelola, sementara inline CSS biasanya dipakai untuk perubahan cepat atau styling khusus yang sifatnya spesifik. Keduanya sama-sama valid, tapi praktik terbaik adalah memaksimalkan internal (atau eksternal) CSS agar kode tetap rapi, dan inline CSS hanya digunakan bila benar-benar diperlukan.

## 4. Membuat CSS Eksternal
<img width="1920" height="1080" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/503066a3-6a3c-4402-bc30-0dbafc51c2e5" />
Eksternal CSS adalah metode penulisan kode CSS yang dipisahkan dari file HTML dan ditempatkan dalam file khusus dengan ekstensi .css, kemudian dihubungkan ke HTML menggunakan tag <link> di dalam bagian <head>. Cara ini sangat membantu menjaga struktur kode tetap rapi karena gaya tampilan bisa diatur secara terpusat dan dapat digunakan kembali oleh banyak halaman web sekaligus. Dengan eksternal CSS, pengembang web lebih mudah melakukan perubahan tampilan hanya dengan mengedit satu file, tanpa perlu membuka dan mengubah setiap halaman HTML satu per satu.

## 5. Menambahkan CSS Selector
<img width="1920" height="1080" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/8c060c38-0da6-4aa8-b5fa-a6f16d7fd576" />
Kode CSS eksternal di atas berfungsi untuk memberikan tampilan yang lebih rapi dan menarik pada halaman web dengan pengaturan terstruktur. Bagian awal melakukan reset dasar pada elemen body dengan menghilangkan margin bawaan, menentukan jenis huruf Arial atau sans-serif, serta memberi warna latar belakang abu-abu terang dan teks berwarna gelap agar nyaman dibaca. Header diberi warna hijau dengan teks putih dan rata tengah untuk menonjolkan judul. Navigasi diatur menggunakan latar belakang hitam, teks putih tebal, serta efek transisi warna hijau saat kursor diarahkan pada link, sehingga lebih interaktif. Bagian intro dibuat lebih fokus dengan memberi padding, lebar maksimal, margin tengah, latar putih, sudut membulat, serta bayangan halus agar terlihat seperti card modern. Sementara itu, tombol dirancang berbentuk kotak dengan sudut membulat, warna dasar hijau, teks putih, dan efek hover berupa perubahan warna hijau lebih gelap, sehingga terlihat profesional dan responsif saat digunakan.
