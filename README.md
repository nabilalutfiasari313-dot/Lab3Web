# Laporan Praktikum 3: CSS Dasar

Repositori ini dibuat untuk memenuhi tugas praktikum mata kuliah **Pemrograman Web** di **Universitas Pelita Bangsa**. Modul ini membahas mengenai dasar-dasar *Cascading Style Sheets (CSS)*, aturan penulisan, serta penggunaan selector.

---

## Identitas Mahasiswa
* **Nama:** Nabila Lutfia Sari
* **NIM:** 312510040
* **Kelas / Program Studi:** Teknik Informatika - Universitas Pelita Bangsa

---

## Tujuan Praktikum
1. Mahasiswa mampu memahami konsep dasar CSS.
2. Mahasiswa mampu memahami aturan penulisan pada CSS (Internal, Eksternal, dan Inline).
3. Mahasiswa mampu memahami selector sebagai pengontrol CSS (Element, ID, dan Class Selector).
4. Mahasiswa mampu membuat pengaturan dan styling CSS pada dokumen HTML.

---

## Langkah-Langkah Praktikum dan Hasil Screenshot

### 1. Membuat Dokumen HTML (`lab2_css_dasar.html`)
Membuat struktur dasar dokumen HTML yang mencakup tag `header`, `nav`, dan `div` dengan ID tertentu.
* **Hasil Tampilan:**
  ![Tampilan HTML Dasar](./<img width="959" height="478" alt="langkah1" src="https://github.com/user-attachments/assets/ca092590-1214-440e-8cea-12e774f68299" />)

### 2. Menambahkan CSS Internal
Menambahkan tag `<style>` di dalam bagian `<head>` dokumen HTML untuk mengatur gaya elemen dasar seperti *font-family*, *header*, dan tag `h1`.
* **Hasil Tampilan:**
  ![Tampilan CSS Internal](./<img width="958" height="469" alt="langkah2" src="https://github.com/user-attachments/assets/4aec4856-2fcc-4d8a-9c4f-a7ae50e9523d" />
)

### 3. Menambahkan Inline CSS
Menambahkan atribut `style` secara langsung pada tag paragraf `<p>` untuk mengatur perataan teks dan warna font.
* **Hasil Tampilan:**
  ![Tampilan Inline CSS](./<img width="958" height="469" alt="langkah3" src="https://github.com/user-attachments/assets/c5f62291-8fa6-4208-8356-920041186e64" />
)

### 4. Membuat CSS Eksternal (`style_eksternal.css`)
Membuat file CSS terpisah untuk mengatur tampilan menu navigasi (`nav`), warna latar belakang hijau, serta efek *hover*.
* **Hasil Tampilan:**
  ![Tampilan Eksternal CSS](./<img width="958" height="467" alt="langkah4" src="https://github.com/user-attachments/assets/2d9c6b4c-661e-4d42-9baa-64601ca8082a" />)

### 5. Menambahkan CSS Selector (ID & Class Selector)
Menggunakan **ID Selector (`#intro`)** untuk kotak pengantar dan **Class Selector (`.button`, `.btn-primary`)** untuk tombol interaktif.
* **Hasil Tampilan:**
  ![Tampilan Selesai Selector](./<img width="959" height="470" alt="langkah5" src="https://github.com/user-attachments/assets/06f4d466-5f53-429c-9f04-378a03becbc3" />
)

## Validasi CSS (W3C Validator)
Kode CSS pada file `style_eksternal.css` telah diuji melalui W3C CSS Validation Service dan dinyatakan valid tanpa error (*No Error Found*).
* **Bukti Validasi:**
  ![Validasi W3C CSS](./<img width="955" height="457" alt="Screenshot 2026-10-10 185728" src="https://github.com/user-attachments/assets/b3d9fcd9-5908-4c27-8b57-342cd386b422" />)

---

## Struktur File Repositori
```text
Lab3Web/

│
├── lab2_css_dasar.html       # File utama dokumen HTML
├── style_eksternal.css       # File stylesheet terpisah
├── langkah1.png              # Screenshot langkah 1
├── langkah2.png              # Screenshot langkah 2
├── langkah3.png              # Screenshot langkah 3
├── langkah4.png              # Screenshot langkah 4
├── langkah5.png
├── validasicss               # Screenshot langkah 5
└── README.md                 # Laporan praktikum

```
---

## Jawaban Pertanyaan & Tugas

**1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.**

Jawaban:

Eksperimen telah dilakukan pada file stylesheet dengan menambahkan serta mengubah beberapa atribut CSS (seperti warna latar belakang, batas elemen, ukuran teks, dan warna hover pada menu navigasi). Hasil penerapan perubahan atribut CSS tersebut dapat dilihat pada screenshot tampilan web pada Langkah 5 (Gambar 6: CSS ID dan Class Selector).

**2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!**

Jawaban:

* **h1 {...} (Element Selector)**: Berlaku secara global untuk semua elemen tag h1 yang ada di dalam dokumen HTML tanpa memandang lokasinya.

* **#intro h1 {...} (Descendant / Contextual Selector)**: Hanya berlaku khusus untuk elemen h1 yang berada di dalam elemen utama dengan id="intro". Elemen h1 lainnya di luar elemen #intro tidak akan terkena gaya tersebut.

**3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!**

Jawaban:

* **Deklarasi yang ditampilkan:** Inline CSS.
  
* **Penjelasan:** Aturan CSS bersifat bertingkat (*cascading*). Gaya yang ditulis langsung pada atribut `style` di dalam elemen HTML memiliki tingkat prioritas tertinggi, sehingga mengalahkan CSS internal dan eksternal.
  
* **Contoh:** 
  Jika pada CSS eksternal ditulis `p { color: blue; }` dan CSS internal `p { color: green; }`, tetapi pada tag HTML ditulis `<p style="color: red;">Teks</p>`, maka teks yang muncul di browser akan berwarna **merah**.

---

**4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! (`<p id="paragraf-1" class="text-paragraf">`)**

**Jawaban:**
* **Deklarasi yang ditampilkan:** Deklarasi dari **ID Selector (`#paragraf-1`)**.
  
* **Penjelasan:** Berdasarkan aturan spesifisitas CSS, ID Selector memiliki bobot nilai yang lebih tinggi dibandingkan Class Selector, sehingga aturan pada ID akan menimpa aturan pada Class.
  
* **Contoh:**
  Jika di dalam CSS terdapat aturan `#paragraf-1 { color: red; }` dan `.text-paragraf { color: green; }`, maka elemen `<p id="paragraf-1" class="text-paragraf">` akan menampilkan teks berwarna **merah**.
