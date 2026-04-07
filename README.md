# BPJS DIAGNOSTIC ANALYSIS: OPERATIONAL, FINANCIAL, AND POLICY EVALUATION DASHBOARD

> Proyek ini adalah sebuah dashboard analitik strategis yang dirancang untuk mengevaluasi efisiensi operasional, keberlanjutan finansial, dan dinamika kepesertaan dari sistem Jaminan Kesehatan Nasional (JKN/BPJS) berdasarkan analisis diagnosis pasien rawat inap tingkat lanjut dari tahun 2014-2018. Proyek ini bertujuan untuk mengungkap potensi "kebocoran" dana asuransi, merumuskan strategi preventif berdasarkan tren penyakit, serta memberikan rekomendasi kebijakan berbasis data (data-driven policy recommendations).

> Full Project Repository : https://github.com/bagaskara0506/BPJS_Inpatient_Analytics.git
> Analysis data sources : https://data.bpjs-kesehatan.go.id/bpjs-portal/action/dataset-list.cbi?page=2&filter=&kategori=

---

# Tech Stack & Tools

- **Data Visualization & Analytics:** Microsoft Power BI
- **Data Transformation (ETL):** Power Query
- **Data Modeling & Calculation:** DAX (Data Analysis Expressions)

---

# 3 Pilar Pertanyaan Bisnis (Business Questions)

## Pilar 1: Operasional & Mutu Klinis (Clinical Operations)

Fokus pada apa yang terjadi di dalam fasilitas kesehatan dan pola penyakit pasien secara makro.

1. **Top Disease Trends & Volume Analytics :** Apa saja diagnosa penyakit dengan jumlah admisi (kunjungan rawat inap) tertinggi secara kumulatif selama 5 tahun terakhir (2014-2018)?

2. **Emerging Threats (Penyakit Baru) :** Diagnosis apa saja yang berstatus sebagai "Penyakit Baru" di setiap tahunnya? (Indikator: Penyakit yang masuk ke dalam daftar Top 100 pada tahun berjalan, namun tidak terdapat pada daftar Top 100 di tahun persis sebelumnya).

**Key Insights (Temuan) :**

- **Dominasi Penyakit Endemis & Gaya Hidup :** Admisi rawat inap tertinggi selama 5 tahun didominasi oleh penyakit terkait sanitasi dan gaya hidup. Typhoid Fever (Tipes) dan Dyspepsia (Asam Lambung/Maag) menempati puncak tertinggi secara kumulatif hingga menyentuh jutaan kasus.

- **Dinamika Penyakit Baru :** Terdapat fluktuasi kemunculan "Penyakit Baru" setiap tahunnya. Meskipun secara volume jumlahnya masih berada di bawah prevalensi penyakit lama, tren fluktuasi ini tetap menjadi indikator penting dalam pergeseran pola kesehatan masyarakat.

**Actionable Recommendations (Tindakan) :**

- **Shift to Preventive (Optimalisasi & Insentif FKTP) :** Melalui kolaborasi dengan Kemenkes, BPJS perlu menggeser fokus penanganan Typhoid dan Dyspepsia ke Faskes Tingkat Pertama (Puskesmas/Klinik) lewat kampanye promotif dan preventif. Selain itu, pemberian insentif khusus dari BPJS bagi FKTP yang berhasil menekan angka rujukan Top 10 Diagnosa ini sangat direkomendasikan. Kasus ini idealnya bisa dicegah di fase awal sehingga tidak terekskalasi menjadi layanan FKRTL (Rawat Inap) yang berbiaya jauh lebih besar.

- **Alokasi Kapasitas Dinamis (Resource Forecasting) :** Menggunakan data tren historis ini, pihak RS dapat melakukan forecasting untuk mengantisipasi ketersediaan ranjang (Bed Occupancy Rate), stok obat/cairan infus, serta kesiapan alat medis pada musim-musim di mana kasus Top 10 (seperti Typhoid atau Dengue) biasanya memuncak.

- **Sistem Peringatan Dini (Early Warning) Penyakit Baru :** Walaupun volumenya belum mendominasi, BPJS harus menjadikan data Penyakit Baru ini sebagai radar kewaspadaan. Perlu dilakukan analisis lanjutan terkait akar penyebabnya (misal : faktor perubahan iklim, pergeseran pola hidup, atau demografi) agar BPJS dan Kemenkes dapat merancang intervensi preventif yang tepat sasaran sebelum penyakit tersebut mewabah dan membebani kas JKN.

## Pilar 2: Evaluasi Finansial & Efisiensi (Financial Sustainability)

Fokus pada kebocoran dana asuransi akibat pelayanan yang berulang.

1. **Targeted Readmission Rate Analysis :** Berapa persentase kunjungan berulang (Readmission Rate) khusus pada kelompok Penyakit Kronis dan Katastropik(Diabetes, Hipertensi, Jantung Koroner, Gagal Ginjal, Kanker, TB, dll) ?
   Analisis ini difilter secara spesifik pada 39 kode awalan ICD-10 Penyakit Kronis dan Katastropik, seperti E10, E11, I10, I20, I21, I22, I23, I24, I25, Z95, I60, I61, I62, I63, I64, G40, J45, J44, M32, D66,D67, D56, E05, E03, C53, C50, C91, C92, C93, C94, C95, N18, Z49, K74, A15, A16, Z21, B20, F20.

- **Tujuan Bisnis :** Menemukan penyakit kronis mana yang paling banyak menyedot dana JKN akibat pasien yang terus kembali dirawat inap, sehingga BPJS bisa merancang intervensi dini (subsidi obat jalan, telemedicine, atau insentif klinik Prolanis/PRB) untuk menekan angka readmission tersebut.

**Key Insights (Temuan) :**

- **Disease level :** Pasien Penyakit Kronis & Katastropik memiliki tingkat readmission 42,41% sepanjang 5 tahun.

- **Temuan paling kritis:** Hereditary factor VIII deficiency (Hemofilia A) memiliki tingkat readmission hingga 90,68%, disusul Beta Thalassemia (83,62%). Artinya, 9 dari 10 pasien hemofilia pasti akan kembali dirawat inap, menyedot dana JKN secara berulang tanpa henti.

**Actionable Recommendations (Tindakan) :**

- **Intervensi Khusus Thalassemia & Hemofilia :** Buat kebijakan seperti bank darah untuk pengadaan suplai darah agar stok selalu siap untuk penanganan Thalassemia yang membutuhkan transfusi darah dan penggunaan obat biosimiliar yang fungsinya sama persis untuk mengganti obat biologis (Paten) yang biayanya lebih mahal.

- **Perkuat Program Rujuk Balik (PRB) & Telemedicine :** Untuk menekan biaya tanpa harus mengorbankan kualitas layanan, BPJS harus memperkuat program PRB yang sudah ada dengan menambahkan fitur telemedicine untuk pasien kronis agar selalu dalam pantauan dan tetap menerima pelayanan seperti visit rawat inap tetapi posisinya dirumah dan visit dilakukan virtual. Untuk distribusi obat pasien pihak BPJS berkolaborasi dengan faskes (RS) dapat bekerja sama dengan jasa logistik untuk pengantaran obat langsung ke rumah pasien untuk mengurangi intensitas kunjungan pasien dan megurangi beban operational RS serta mendukung program kesehatan dari bpjs untuk kemudahan pasien.

## Pilar 3: Kepesertaan & Kebijakan Publik (Membership & Public Policy)

Fokus pada stabilitas jumlah pasien yang dirawat dan implikasinya terhadap status kepesertaan.

1. **Membership Fluctuation (Volatilitas Peserta per Diagnosa) :** Bagaimana tren naik-turunnya jumlah peserta (pasien unik) setiap tahunnya dari 2014 hingga 2018 berdasarkan diagnosisnya?

- **Asumsi Bisnis & Mitigasi Risiko :** Fluktuasi (terutama penurunan tajam jumlah peserta pada penyakit tertentu) dapat menjadi indikator bahwa banyak pasien yang status kepesertaannya berubah menjadi Non-Aktif (menunggak premi) sehingga tidak bisa mengakses rawat inap.

**Key Insights (Temuan) :**

- **Decline in membership :** Total peserta setiap tahunnya mengalami peningkatan, tetapi sejak tahun 2016 peningkatan tersebut mengalami penurunan dibanding peningkatan tahun sebelumnya.

- **Ketimpangan (Mismatch) :** Beban rumah sakit naik drastis, tapi penambahan peserta baru melambat. Ini mengindikasikan bahwa sistem JKN lebih banyak melayani orang sakit (yang sudah ada), namun kesulitan merekrut orang sehat baru untuk mensubsidi silang, atau tingginya angka peserta mandiri yang Non-Aktif (menunggak premi).

**Actionable Recommendations (Tindakan) :**

- **Peralihan ke PBI :** Pihak BPJS bekerjasama dengan kementrian sosial untuk reaktivasi peserta non-aktif yang berhak agar tanggungannya dialihkan ke APBD/APBN sehingga meningkatkan premi bpjs.

- **Ekspansi Agresif Segmen Pekerja Sehat :** Strategi "jemput bola" untuk mendaftarkan Pekerja Penerima Upah (PPU) dari sektor UMKM dan pekerja informal. Suntikan peserta sehat ini sangat krusial untuk menyeimbangkan Risk Pooling (subsidi silang) agar kas BPJS tidak jebol akibat tingginya biaya dari Pilar 2 tadi.

- **Program Retensi & Autodebet :** Terapkan skema pembayaran autodebet yang lebih masif atau insentif pembayaran di muka bagi peserta mandiri untuk menekan angka tunggakan.

---

## Proses pembersihan & penggabungan data dengan power query (ETL (Extract, Transform, Load))

1. Memasukan seluruh data ke power query
2. Menghapus kolom yang tidak diperlukan
3. Menghapus baris yang tidak diperlukan
4. Mendeklarasikan baris header
5. Menghapus kolom yang tidak diperlukan
6. Membuat kolom baru untuk tahun
7. Menyesuikan type data pada kolom tahun
8. Menggabungkan seluruh data menjadi satu tabel dengan append query dan menamai master data dengan Master_RITL_2014_2018

---

## PEMBUATAN METRIK BISNIS (DAX MEASURES & COLUMNS)

### Measure:

1. Readmission Rate % : Presentase kunjungan berulang (Readmission) dibandingkan dengan total peserta unik (pasien unik) untuk setiap diagnosis penyakit.
2. Total Admisi : Jumlah total seluruh kunjungan rawat inap (admisi) dari tahun 2014 sampai 2018.
3. Total Peserta : Jumlah total peserta unik (pasien unik) yang dirawat inap dari tahun 2014 sampai 2018.
4. Total Readmission : Jumlah total kunjungan berulang (Readmission) dari tahun 2014 sampai 2018, Pembandingannya Total Admisi dikurangi Total Peserta, karena setiap peserta unik pasti memiliki minimal 1 admisi, sehingga sisanya adalah kunjungan berulang (Readmission).
5. Peserta Tahun Lalu : Naik turunnya jumlah peserta unik (pasien unik) dibandingkan dengan tahun sebelumnya, dengan rumus: Total Peserta Tahun Berjalan dikurangi Total Peserta Tahun Sebelumnya.
6. Pertumbuhan Peserta YoY % : Pertumbuhan jumlah peserta unik (pasien unik) dibandingkan dengan tahun sebelumnya, dengan rumus: (Total Peserta Tahun Berjalan dikurangi Total Peserta Tahun Sebelumnya) dibagi Total Peserta Tahun Sebelumnya, lalu dikalikan 100 untuk mendapatkan persentase. (menggunakan fungsi DIVIDE untuk menghindari error pembagian dengan nol jika Total Peserta Tahun Sebelumnya adalah nol).
7. Status Penyakit : Labeling status diagnosa, jika tahunnya 2014 maka akan diberi label "Data Dasar 2014" karena tidak memiliki pembanding di tahun sebelumnya, jika diatas 2014 labeling akan dibuat jika di tahun sekarang ada peserta yang diagnosanya di tahun sebelumnya tidak ada peserta maka dikatergorikan "Penyakit Baru", jika di tahun sekarang ada peserta yang diagnosanya di tahun sebelumnya juga ada peserta maka dikategorikan "Penyakit Lama".
8. Total Penyakit Baru : Jumlah total diagnosa penyakit yang berstatus "Penyakit Baru"
9. Total Penyakit Lama : Jumlah total diagnosa penyakit yang berstatus "Penyakit Lama"

### Column:

1. Kategori Penyakit : Berisi daftar ICD X dengan kode 3 huruf pertama yang terkategori sebagai penyakit Kronis, Katastropik, Berbiaya Tinggi, Lainnya (39 kode ICD X yang sudah disebutkan sebelumnya masuk ke dalam kategori Kronis/Katastropik/Berbiaya Tinggi, sedangkan kode ICD X lainnya masuk ke dalam kategori Lainnya).
2. Kategori Finansial : Berisi label "Chronic and Catastrophic" untuk 39 kode ICD X yang sudah disebutkan sebelumnya, sedangkan kode ICD X lainnya akan diberi label "Others".

---

## VISUALISASI & INTERPRETASI INSIGHT

### Page Pilar 1: Operasional & Mutu Klinis (Clinical Operations) :

1. Top 10 Penyakit Penyumbang Rawat Inap Tertinggi (Bar Chart)
2. Tren Admission & Volume per Tahun (Line Chart)
3. Emerging Threats (Table - List Diagnoses)
4. Total Old & New Diagnoses (Clustered Column Chart)

![Dashboard Clinical Operations](<dashboard/IMG/Pilar%201%20Operasional%20&%20Mutu%20Klinis%20(Clinical%20Operations).jpg>)

### Page Pilar 2: Evaluasi Finansial & Efisiensi (Financial Sustainability) :

1. Readmissions Analysis of Chronic-Catastrophic (Clustered Bar Chart - visual untuk melihat dari 39 kelompok penyakit kronis & katastropik tersebut, mana yang persentase rawat inap ulangnya paling parah)
2. Trend Readmission Rate per Tahun (Line Chart)

![Dashboard Financial Sustainability](<dashboard/IMG/Pilar%202%20Evaluasi%20Finansial%20&%20Efisiensi%20(Financial%20Sustainability).jpg>)

### Pilar 3: Kepesertaan (Membership Fluctuation)

1. Volatilitas Peserta & Pertumbuhan YoY (Line and clustered column chart)
2. Komposisi Kategori Penyakit (Kronis vs Lainnya) pada Fluktuasi Peserta

![Dashboard Membership Fluctuation](<dashboard/IMG/Pilar%203%20Kepesertaan%20dan%20Kebijakan%20Publik%20(Membership%20Fluctuation).jpg>)

### Excutive Summary Page (Halaman Ringkasan Eksekutif) :

1. Total Members, Total Admission, Readmission Rate (KPI Cards)
2. Top 10 Diagnoses by Admission (Bar Chart)
3. Readmission Rate of Chronic-Catastrophic Diseases (Clustered Bar Chart)
4. Trend total patients per year (Line Chart)
5. Total membership growth YoY (Line and clustered column chart)

![Dashboard Excutive Summary](dashboard/IMG/Executive%20Summary.jpg)

_Created by [https://www.linkedin.com/in/satria-bagaskara/] | Data Analyst_
