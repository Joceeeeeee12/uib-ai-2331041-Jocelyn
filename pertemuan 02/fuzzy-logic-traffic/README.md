## Deskripsi Singkat Project
Project ini merupakan implementasi logika fuzzy untuk menganalisis tingkat kemacetan lalu lintas berdasarkan data dari variabel antrian kendaraan, waktu tunggu, dan tingkat kedatangan kendaraan. Dengan menggunakan sistem inferensi fuzzy, model ini membantu menentukan tingkat kepadatan lalu lintas (Traffic Level) secara dinamis berdasarkan kondisi input yang berubah-ubah.

## Tujuan
Tujuan dari project ini adalah untuk mensimulasikan bagaimana logika fuzzy dapat digunakan dalam pengambilan keputusan pada sistem lalu lintas, khususnya dalam memperkirakan **tingkat kemacetan** dan mengatur **perpanjangan waktu lampu hijau (Green Extension)** agar lalu lintas menjadi lebih efisien.

## Cara Kerja Logika Fuzzy
Logika fuzzy digunakan karena mampu menangani data yang bersifat **tidak pasti atau samar (uncertain)**, seperti istilah "antrian panjang", "waktu tunggu sedang", atau "kedatangan kendaraan tinggi".
Setiap variabel input didefinisikan dengan **membership function** untuk mengubah nilai numerik menjadi himpunan fuzzy (short, medium, long, dsb.).
Kemudian, aturan fuzzy (**fuzzy rules**) diterapkan untuk menghubungkan input dengan output menggunakan operator logika seperti **AND (∧)** dan **OR (∨)**.
Hasil akhirnya adalah **defuzzifikasi**, yaitu mengubah hasil fuzzy menjadi nilai numerik yang merepresentasikan **Traffic Level**.

## Data yang Digunakan
Dataset (`traffic-data.csv`) berisi beberapa parameter utama kondisi lalu lintas:
* **Queue_Length** : Panjang antrian kendaraan (0–10 satuan)
* **Waiting_Time** : Lama waktu tunggu kendaraan di lampu merah (0–30 detik)
* **Arrival_Rate** : Tingkat kedatangan kendaraan (0–15 kendaraan per satuan waktu)

## Input dan Output Sistem
| Jenis        | Variabel        | Domain | Fungsi Keanggotaan  |
| ------------ | --------------- | ------ | ------------------- |
| **Input 1**  | Queue_Length    | 0–10   | Short, Medium, Long |
| **Input 2**  | Waiting_Time    | 0–30   | Short, Medium, Long |
| **Input 3**  | Arrival_Rate    | 0–15   | Low, Medium, High   |
| **Output 1** | Green_Extension | 0–20   | Short, Medium, Long |
| **Output 2** | Traffic_Level   | 0–1    | Low, Medium, High   |

## Hasil
Hasil simulasi menunjukkan nilai **Traffic Level** yang dihitung secara otomatis berdasarkan kombinasi dari tiga input utama. Distribusi output divisualisasikan menggunakan grafik histogram dan scatter plot untuk melihat hubungan antara masing-masing variabel input terhadap tingkat kemacetan yang dihasilkan.

## Kesimpulan Singkat
Model fuzzy ini menunjukkan bagaimana pendekatan berbasis logika fuzzy dapat digunakan untuk membantu pengambilan keputusan dalam sistem lalu lintas secara adaptif dan realistis. Sistem dapat dikembangkan lebih lanjut untuk diterapkan pada kontrol lampu lalu lintas otomatis di persimpangan jalan.
