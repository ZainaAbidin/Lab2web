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
