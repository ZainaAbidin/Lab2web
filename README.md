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
Pada tampilan HTML yang ditunjukkan pada gambar, terlihat bahwa halaman web masih menampilkan gaya bawaan dari browser karena belum diterapkan aturan CSS tambahan. Judul utama “CSS Internal dan Inline CSS” muncul dengan ukuran besar sesuai tag `<h1>,` sedangkan teks Inline CSS ditampilkan miring karena menggunakan tag `<i>`. Tepat di bawahnya terdapat tiga tautan navigasi, yaitu “CSS Dasar”, “CSS Eksternal”, dan “HTML Dasar”, yang tampil berwarna biru dan bergaris bawah sesuai default hyperlink.

Pada bagian isi, terdapat heading kedua “Hello World” yang juga menggunakan tag <h1>, lalu diikuti paragraf penjelasan. Dalam paragraf tersebut, kata “Pemrograman Web” dicetak tebal menggunakan tag `<b>`, sementara “Universitas Pelita Bangsa” dicetak miring dengan tag `<i>`. Setelah itu, ada tautan tambahan “Informasi selengkapnya.” yang tampil dengan gaya standar link, yaitu biru bergaris bawah.

Secara keseluruhan, struktur halaman HTML sudah terbentuk dengan baik karena mencakup header, navigasi, dan konten utama. Namun tampilannya masih sederhana, dengan latar belakang putih dan teks hitam. Hal ini terjadi karena CSS belum diterapkan. Jika ditambahkan aturan CSS, tampilan web bisa dibuat lebih menarik, misalnya dengan pewarnaan background, pengaturan tipografi, pemberian jarak antar elemen, serta desain link agar terlihat seperti tombol interaktif.
