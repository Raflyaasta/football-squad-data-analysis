# ⚽ Analisis Demografi & Efisiensi Performa Skuad Sepak Bola

Oleh: Rafly Asta Nurdian | Mahasiswa Statistika & Data Enthusiast  
Tools: Microsoft Excel (PivotTable, PivotChart, Uji Korelasi Pearson)  
Sumber Data: Dataset Kaggle (Premier League 2024-2025 Data)

---

## 1. Latar Belakang & Objektif
Dalam dunia sepak bola modern, manajemen skuad yang efektif sangat bergantung pada data. Proyek ini bertujuan untuk mengeksplorasi dataset statistik ratusan pemain sepak bola guna memahami struktur tim, distribusi usia, serta menguji hipotesis terkait korelasi umur dan alokasi menit bermain.

Tujuan Analisis:
1. Menganalisis distribusi skuad berdasarkan usia dan menit bermain per posisi.
2. Mengidentifikasi profil usia klub (Studi Kasus: Klub termuda).
3. Menguji hipotesis korelasi statistik antara usia dan menit bermain.

---

## 2. Persiapan & Pembersihan Data (Data Cleaning)
Data mentah berformat CSV dari Kaggle memerlukan penyesuaian agar siap dianalisis:
* Mengatasi Error Tipe Data: Saat melakukan agregasi awal, Excel memunculkan error `#DIV/0!` karena kolom numerik (`Playing Time_Min`) terbaca sebagai format teks (*String*).
* Solusi: Menggunakan fitur Text-to-Columns untuk mengonversi tipe data teks menjadi angka mutlak (*Number*). Langkah ini krusial untuk memastikan rumus matematika dan PivotTable berjalan akurat tanpa anomali.

---

## 3. Hasil Analisis & Visualisasi

### A. Beban Kerja Pemain Berdasarkan Posisi
Menggunakan **PivotTable** untuk menganalisis total dan rata-rata menit bermain berdasarkan posisi (Bek, Gelandang, Penyerang, Kiper).

<img width="920" height="686" alt="Screenshot 2026-03-01 195213" src="https://github.com/user-attachments/assets/10bb71a4-a119-44d6-8f9a-ff9a5efd4e8a" />


**Insight:**
* Secara kumulatif, posisi **Midfielder / Gelandang (MF)** mencatat total menit bermain tertinggi di liga, yaitu mencapai **235.634 menit**. 
* Ketika dianalisis secara rata-rata individu, posisi **Midfielder (MF)** dan **Defender (DF)** menjadi pemain dengan beban kerja (menit bermain) paling tinggi. Hal ini wajar mengingat kedua posisi ini adalah tulang punggung formasi yang paling banyak menguras stamina dan jarang dirotasi di tengah pertandingan dibandingkan penyerang.

### B. Distribusi Usia Skuad & Profil Klub
Menganalisis komposisi umur untuk melihat tren regenerasi pemain di liga.

<img width="1156" height="395" alt="Screenshot 2026-03-01 195239" src="https://github.com/user-attachments/assets/58ddc34a-7dfb-4703-88e4-453e7f76f01c" />

<img width="1011" height="431" alt="Screenshot 2026-03-01 195227" src="https://github.com/user-attachments/assets/801dc0bd-3242-42a1-9051-a9a577f0fe1b" />

<img width="1048" height="639" alt="Screenshot 2026-03-01 195252" src="https://github.com/user-attachments/assets/4d752c7a-ffed-4ab1-9cd1-0c9c95c442ca" />


**Insight:**
* Liga didominasi oleh pemain dalam rentang **usia 20-24 tahun (205 pemain)** dan **usia 25-29 tahun (204 pemain)**. 
* **Temuan Khusus:** Dari seluruh tim yang dianalisis, **Chelsea** tercatat sebagai klub dengan rata-rata usia pemain paling muda, menunjukkan strategi manajemen yang berfokus pada investasi talenta jangka panjang.

### C. Korelasi Antara Usia dan Menit Bermain
Menghitung koefisien korelasi Pearson (`=CORREL`) antara variabel `Age` (Usia) dan `Playing Time_Min` (Menit Bermain).

<img width="855" height="451" alt="Screenshot 2026-03-01 195311" src="https://github.com/user-attachments/assets/36359b05-409b-4ca7-9506-56bdc1b0f8f4" />


**Insight:**
* **Hasil Uji Statistik:** Uji korelasi Pearson menghasilkan angka **0,196942**. Angka korelasi positif yang lemah ini membuktikan bahwa hubungan usia dan menit bermain bersifat **non-linear** (bukan berarti semakin tua/muda pasti semakin sering main).
* **Tren Starter (Starting XI):** Analisis lebih lanjut menunjukkan bahwa pemain yang rutin menjadi *starter* tersebar secara merata pada rentang **usia 20 hingga 34 tahun**. Ini mengindikasikan bahwa pelatih lebih mengutamakan performa aktual dan kebugaran dibandingkan sekadar metrik umur semata.

---

## 4. Kesimpulan Akhir
Manajemen menit bermain dan komposisi sebuah skuad sepak bola sangat terukur. Data membuktikan bahwa Gelandang dan Bek adalah mesin utama tim dengan menit bermain tertinggi. Selain itu, dengan dominasi pemain usia 20-29 tahun dan korelasi usia-menit bermain yang rendah (0,19), terbukti bahwa kesempatan bermain di level tertinggi didorong oleh efisiensi performa di lapangan, bukan senioritas umur.
