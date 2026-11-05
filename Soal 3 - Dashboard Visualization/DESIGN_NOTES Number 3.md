DESIGN NOTES & DASHBOARD DOCUMENTATION Company: PT Sinar Niaga Nusantara Project: Executive & Regional Sales Performance Dashboard

1. Target Users & KPI Selection Dashboard ini dirancang untuk melayani dua persona pengguna dengan kebutuhan spesifik:  
* Board of Directors (Direksi) \- Overview Page:  
  * Kebutuhan: Ingin melihat kesehatan perusahaan secara keseluruhan dalam waktu kurang dari 5 menit tanpa harus membuka manual buku panduan.  
  * KPI Utama: Total Revenue, Gross Profit, Gross Margin (persen), dan Average Discount Rate (dibandingkan dengan tahun lalu / YoY).  
  * Alasan: Sesuai permintaan BOD agar tampil sederhana dan sesuai permintaan Head of Sales agar angka pendapatan utama diletakkan di bagian paling atas dengan ukuran besar.  
* Regional Sales Managers (RSM) \- Detail Page:  
  * Kebutuhan: Ingin membandingkan performa wilayahnya dengan wilayah lain serta tahun lalu untuk mencari area yang perlu perhatian khusus.  
  * KPI Utama: Revenue & Gross Profit per Region, Breakdown Channel (Online vs Offline), dan Kategori Produk Penunjang.  
  * Alasan: Memungkinkan manajer regional melakukan evaluasi operasional secara mendalam dan adil antar-region.  
2. Data Preparation & Assumptions  
* Sumber Data: Menggunakan dataset bersih dari folder Soal 1 (sales\_transactions\_raw.csv).  
* Periode Fiskal (FY): Ditetalkan dari 1 September hingga 31 Agustus (FY2025: 1 Sep 2024 sampai 31 Aug 2025; FY2026: 1 Sep 2025 sampai 31 Aug 2026).  
* Asumsi Utama:  
  * Perhitungan Revenue menggunakan rumus: qty dikali unit\_price dikali (1 minus discount).  
  * Perhitungan Gross Profit menggunakan rumus: revenue dikurangi cost.  
  * Pembersihan kategori produk dilakukan untuk menyatukan variasi penulisan (contoh: Laptop, laptop, LAPTOP diseragamkan menjadi Laptop).  
3. Key Design Decisions & Clarity Principles  
* Layout Terstruktur: Dibagi menjadi 2 halaman terpisah (Halaman 1 untuk Direksi, Halaman 2 untuk Regional Manager) untuk menghindari informasi yang terlalu padat.  
* Pemilihan Warna Fungsional: Menggunakan warna netral (abu-abu dan putih) sebagai latar belakang, warna biru korporat untuk metrik positif, dan warna merah atau oranye terang hanya untuk menandakan penurunan Gross Profit atau anomali diskon tinggi.  
* Menghindari Grafik Rumit: Tidak menggunakan diagram 3D atau pie chart dengan banyak irisan. Menggunakan kartu angka besar, diagram batang horizontal untuk perbandingan region, dan grafik garis untuk tren bulanan.  
4. Four Key Business Insights (Visible Directly from Dashboard)  
* Penurunan Profitabilitas Global: Total Gross Profit perusahaan merosot tajam dari \-Rp 1,87 Miliar pada FY2025 menjadi \-Rp 6,43 Miliar pada FY2026 akibat lonjakan rata-rata diskon yang tidak terkontrol hingga 55,3 persen.  
* Kanibalisasi Diskon Channel Online: Channel Online mencatatkan tingkat diskon yang sangat tinggi sehingga menggerus margin keuntungan produk-produk utama hingga bernilai negatif.  
* Anomali Kategori IT (Laptop & Smartphone): Kontributor pendapatan terbesar seperti Laptop dan Smartphone mengalami kerugian margin yang parah di FY2026 akibat penetapan harga jual di bawah modal (COGS).  
* Stabilitas Kategori Pendukung: Kategori Peralatan Kantor dan ATK tetap konsisten menyumbang margin positif (+21 persen hingga \+23 persen), menjadi penyeimbang yang sehat bagi portofolio produk perusahaan.

