# E-Commerce Analytics Dashboard

Proyek analisis data e-commerce menggunakan dataset transaksi September 2016 – Agustus 2018.
Dashboard dibuat menggunakan **Streamlit** untuk menyampaikan hasil analisis secara interaktif.

---

## 📌 Deskripsi Proyek

Dashboard ini dibuat untuk menganalisis performa platform e-commerce berdasarkan data transaksi yang telah dibersihkan. Analisis dilakukan untuk memahami pola pertumbuhan bisnis, perilaku pelanggan, serta preferensi metode pembayaran.

**Pertanyaan yang dijawab:**
1. Bagaimana tren jumlah transaksi bulanan selama September 2016 – Agustus 2018?
2. Bagaimana segmentasi pelanggan berdasarkan metode RFM (Recency, Frequency, Monetary)?
3. Metode pembayaran apa yang paling dominan dan bagaimana rata-rata nilainya?

---

## 📁 Struktur Folder

```
Submission/
├── Projek.ipynb                          # Jupyter Notebook analisis data
├── requirements.txt                      # Library yang digunakan
├── README.md                             # Dokumentasi proyek
└── dashboard/
    ├── Dashboard.py                      # File utama Streamlit
    ├── orders_clean.csv                  # Dataset orders (sudah dibersihkan)
    └── orders_payments_clean(Merge).csv  # Dataset payments (sudah dibersihkan)
```

---

## 📊 Ringkasan Insight

### Gathering Data
Dataset terdiri dari dua file CSV hasil merge dari dataset e-commerce Brazil (Olist):
- `orders_clean.csv` — berisi data transaksi pelanggan
- `orders_payments_clean(Merge).csv` — berisi data metode dan nilai pembayaran

### Assessing Data
- Ditemukan missing values pada beberapa kolom timestamp yang kemudian ditangani
- Tidak ditemukan data duplikat yang signifikan
- Tipe data disesuaikan, terutama kolom `order_purchase_timestamp` dikonversi ke datetime

### Cleaning Data
- Missing values pada kolom yang tidak krusial diisi atau dihapus
- Kolom timestamp dikonversi ke format datetime
- Outlier pada `payment_value` tidak dihapus karena mencerminkan variasi transaksi yang valid

### Explanatory Analysis
1. **Tren Transaksi** — Transaksi tumbuh dari 1 order (Sep 2016) hingga puncak 7.288 order (Nov 2017), kemudian stabil di 6.000–7.000/bulan pada 2018.
2. **Segmentasi RFM** — Mayoritas pelanggan (56%) berada di segmen Others. Best Customer hanya 1,6% namun memiliki rata-rata Monetary tertinggi (R$ 405,64).
3. **Metode Pembayaran** — Credit card mendominasi dengan 74.584 transaksi dan rata-rata nilai R$ 162,24. Voucher memiliki rata-rata nilai terendah di R$ 62,45.

---

## 🚀 Cara Menjalankan Dashboard (Local)

### 1. Clone Repository
```bash
git clone https://github.com/vviper14/fundamental-analisis-data.git
cd fundamental-analisis-data
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Jalankan Dashboard
```bash
cd dashboard
streamlit run Dashboard.py
```

### 4. Buka di Browser
Streamlit akan otomatis membuka browser di:
```
http://localhost:8501
```

---

## 🌐 Link Dashboard Online

https://khusus-app-gttwtjers8mhhyjpnvreea.streamlit.app/

---

## 📦 Requirements

```
streamlit==1.41.0
pandas==2.2.2
plotly==5.24.1
```

---

## 👤 Identitas

| | |
|---|---|
| **Nama** | Suroso Aditya Wibowo |
| **ID Dicoding** | CDCC184D6Y1024 |
| **Email** | *(isi email kamu)* |