## Deskripsi Singkat Project
Project ini merupakan implementasi logika fuzzy untuk menentukan **tingkat kualitas film (Movie Quality)** berdasarkan beberapa faktor yang memengaruhi, yaitu **rating IMDb**, **tahun rilis**, dan **jumlah suara penonton (IMDb Votes)**. Dengan pendekatan fuzzy logic, sistem ini mampu menilai kualitas film secara fleksibel dan tidak kaku seperti perhitungan matematis biasa, sehingga hasilnya lebih menyerupai cara berpikir manusia.

# Tujuan
Tujuan utama dari project ini adalah untuk membangun **model penilaian kualitas film** menggunakan logika fuzzy yang dapat:

1. Mengklasifikasikan film ke dalam kategori kualitas **Low**, **Medium**, atau **High**.
2. Memberikan **skor kualitas (Movie Quality Score)** berdasarkan kombinasi beberapa parameter utama.
3. Menyediakan hasil analisis yang dapat digunakan untuk memahami tren kualitas film dari data IMDb.

### **Cara Kerja Logika Fuzzy**

Logika fuzzy digunakan karena mampu menangani data yang bersifat **subjektif dan tidak pasti**, seperti istilah “film lama tapi bagus” atau “rating sedang tapi populer”.
Proses fuzzy berjalan melalui beberapa tahap:

1. **Fuzzifikasi:** mengubah nilai numerik (seperti rating atau jumlah votes) menjadi derajat keanggotaan fuzzy (low, medium, high).
2. **Inferensi:** menerapkan aturan logika fuzzy (fuzzy rules) untuk menggabungkan input menjadi keputusan.
3. **Defuzzifikasi:** mengubah hasil fuzzy menjadi nilai numerik yang merepresentasikan kualitas film (0–10).

Contoh aturan fuzzy:

* Jika *IMDb Rating* **tinggi** dan *Jumlah Votes* **banyak**, maka *Kualitas Film* **tinggi**.
* Jika *IMDb Rating* **rendah** atau *Jumlah Votes* **sedikit**, maka *Kualitas Film* **rendah**.
* Jika *IMDb Rating* **sedang** dan *Tahun Rilis* **modern**, maka *Kualitas Film* **sedang**.

---

### **Data yang Digunakan**

Dataset (`data.csv`) berisi informasi film yang telah dibersihkan, dengan atribut utama sebagai berikut:

* **imdbAverageRating** : skor penilaian film dari IMDb (0–10)
* **releaseYear** : tahun rilis film
* **imdbNumVotes** : jumlah pengguna yang memberikan suara
* **title** : judul film

---

### **Input dan Output Sistem**

| Jenis       | Variabel        | Domain              | Fungsi Keanggotaan            |
| ----------- | --------------- | ------------------- | ----------------------------- |
| **Input 1** | IMDb Rating     | 0–10                | Low, Medium, High             |
| **Input 2** | Release Year    | (min_year–max_year) | Classic, Modern, Contemporary |
| **Input 3** | Number of Votes | 0–max_votes         | Few, Average, Many            |
| **Output**  | Movie Quality   | 0–10                | Low, Medium, High             |

---

### **Hasil dan Analisis**

Sistem menghasilkan kolom baru bernama **`movie_quality_score`** dan **`movie_quality_category`** yang menunjukkan nilai dan kategori kualitas film berdasarkan hasil fuzzy logic.
Beberapa hasil visualisasi yang dibuat antara lain:

* **Distribusi Skor Kualitas Film** → menunjukkan sebaran nilai kualitas pada semua film.
* **Diagram Batang Kategori Film** → menunjukkan jumlah film dalam kategori *Low*, *Medium*, dan *High*.

Selain itu, data film dengan skor tertinggi disimpan ke dalam file **`top-movies.csv`** untuk analisis lebih lanjut.

---

### **Kesimpulan Singkat**

Dengan logika fuzzy, sistem ini dapat menilai kualitas film dengan pendekatan yang **lebih fleksibel dan realistis** dibandingkan metode konvensional. Model ini mempertimbangkan kombinasi beberapa faktor — tidak hanya rating, tetapi juga tahun rilis dan jumlah penonton — untuk menghasilkan penilaian yang lebih mendekati persepsi manusia terhadap kualitas film.

---

Apakah kamu ingin saya bantu ubah versi ini jadi **versi singkat satu paragraf** (misalnya untuk ditulis di slide presentasi atau README GitHub)?
