# 📊 Survival Analysis: Prediksi Umur Startup Indonesia

Proyek ini melakukan analisis survival untuk memprediksi **berapa lama startup di Indonesia dapat bertahan hidup** sebelum mengalami *pivot* atau *kebangkrutan*. Data digunakan dari sumber sekunder (dummy atau DSInnovate-style), dianalisis menggunakan Python dan pustaka `lifelines`.

---

## 🔍 Tujuan

- Mengestimasi **probabilitas bertahan hidup** startup dari waktu ke waktu
- Mengidentifikasi **faktor-faktor yang memengaruhi risiko bangkrut atau pivot**
- Membandingkan performa model survival: **Kaplan-Meier, Cox, Exponential, dan Weibull**
- Memprediksi **median survival time** untuk startup baru berdasarkan profil mereka

---

## 📦 Isi Proyek

- `Survival_analysis.ipynb` → Notebook utama untuk preprocessing, model fitting, dan visualisasi
- `startup_data_fixed.csv` → Dataset startup Indonesia (simulasi dummy)
- `README.md` → Dokumentasi proyek

---

## 📈 Metodologi

### ✅ Data Features:
- `founded_year`, `end_year`, `status`
- `funding_amount`, `num_employees`
- `sector`, `location`, `founder_background`

### ✅ Model Survival yang Digunakan:
| Model             | Tipe            | Tujuan                                                   |
|------------------|------------------|-----------------------------------------------------------|
| Kaplan-Meier     | Non-parametrik   | Estimasi survival curve umum dan per kategori            |
| Log-Rank Test    | Statistik uji    | Uji signifikansi antar kelompok (lokasi, sektor, dll.)   |
| Cox Proportional | Semi-parametrik  | Mengukur pengaruh variabel terhadap risiko               |
| Exponential AFT  | Parametrik       | Prediksi dengan asumsi hazard konstan                    |
| Weibull AFT      | Parametrik       | Prediksi dengan hazard rate fleksibel (meningkat/menurun)|

---

## 🔑 Temuan Utama

- **Median survival startup** sekitar **6.5 tahun**
- Startup dengan **founder latar belakang tech** memiliki risiko bangkrut/pivot **lebih rendah** (Cox model)
- **Pendanaan** dan **jumlah karyawan** tidak signifikan secara statistik dalam model yang diuji
- **Model terbaik**: *Weibull AFT*, karena fleksibel dan memiliki AIC & likelihood terbaik

---

## 📚 Tools & Library

- Python (Jupyter/Google Colab)
- `lifelines` for survival models
- `pandas`, `matplotlib`, `seaborn`

---


## 💡 Catatan Tambahan

    Dataset yang digunakan adalah versi simulasi. Untuk riset lanjutan, disarankan menggunakan dataset asli (misalnya dari DSInnovate, Crunchbase, DailySocial).

    Model dapat dikembangkan lebih lanjut dengan memasukkan fitur-fitur seperti: revenue, burn rate, investor quality, product-market fit, dll.

---
## 🧠 Author

Nofie Iman
Universitas Gadjah Mada
LinkedIn

---
## 📄 License

MIT License – feel free to fork, modify, and use this for your own analysis or thesis.


---

