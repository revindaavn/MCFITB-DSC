# 📊 LOMBA_DSC_MCF_ITB

Proyek ini berisi notebook untuk melakukan pemodelan dan prediksi data klaim asuransi, meliputi:

- Claim Frequency
- Claim Severity
- Total Claim

File utama yang digunakan dalam project ini adalah:

```
LOMBA_DSC_MCF_ITB.ipynb
```

---

## 🛠️ Requirements

Pastikan sudah menginstall:

- Python 3.9+
- Jupyter Notebook / JupyterLab

### 📦 Library yang Dibutuhkan

```
pandas
numpy
matplotlib
scikit-learn
xgboost
lightgbm
```

Install semua dependency dengan:

```bash
pip install pandas numpy matplotlib scikit-learn xgboost lightgbm
```

Jika menggunakan Google Colab:

```python
!pip install xgboost lightgbm
```

---

## 📂 Struktur Folder

Pastikan struktur folder seperti berikut:

```
project_folder/
│
├── LOMBA_DSC_MCF_ITB.ipynb
├── data_train.csv
├── data_test.csv
└── README.md
```

Dataset harus berada di folder yang sama dengan notebook (jika dijalankan secara lokal).

---

## ▶️ Cara Menjalankan Notebook

### 🔹 Opsi 1: Local (Jupyter Notebook)

Masuk ke folder project:

```bash
cd project_folder
```

Jalankan Jupyter:

```bash
jupyter notebook
```

Buka file:

```
LOMBA_DSC_MCF_ITB.ipynb
```

Jalankan semua cell:

```
Kernel → Restart & Run All
```

---

### 🔹 Opsi 2: Google Colab

1. Upload file `.ipynb`
2. Upload dataset (`data_train.csv`, `data_test.csv`)
3. Sesuaikan path file (biasanya `/content/`)
4. Jalankan cell dari atas ke bawah

---

## ⚙️ Alur Notebook

Notebook dijalankan secara berurutan dengan tahapan:

1. Import Library  
2. Load Dataset  
3. Feature Engineering (lag feature, rolling mean, dll)  
4. Training Model:
   - Model Frequency
   - Model Severity
5. Forecast Periode Agustus–Desember 2025  
6. Generate File Submission  

---

## 📈 Mengubah Periode Forecast

Untuk mengubah periode prediksi, ubah bagian berikut pada notebook:

```python
pd.date_range('2025-08-01','2025-12-01',freq='MS')
```

Sesuaikan tanggal awal dan akhir sesuai kebutuhan.

---

## 📄 Output

Setelah seluruh cell berhasil dijalankan, akan dihasilkan file:

```
submission.csv
```

Format file submission:

```
id,value
2025_08_Claim_Frequency,xxx
2025_08_Claim_Severity,xxx
2025_08_Total_Claim,xxx
...
```

File ini siap untuk diupload ke sistem kompetisi.

---

## 🧠 Troubleshooting

### ❌ ModuleNotFoundError
Install library yang belum tersedia menggunakan:

```bash
pip install nama_library
```

### ❌ FileNotFoundError
Pastikan:
- Nama file dataset benar
- Path file sesuai

### ❌ Feature mismatch saat prediksi
Pastikan fitur saat training dan forecasting identik.

---

## 🏁 Selesai

Jika semua langkah dilakukan dengan benar, notebook akan menghasilkan file submission tanpa error dan siap digunakan untuk kompetisi.
