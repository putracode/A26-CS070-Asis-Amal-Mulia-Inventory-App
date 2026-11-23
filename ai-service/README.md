# AI Service (Forecasting, Data Insight & Chatbot) — Asis Amal Mulia Inventory App
> **Learning Path:** Next-Gen AI Engineer  
> **Program:** Capstone Asah 2026 (Led by Dicoding, Supported by GoTo) — **ID Tim:** `A26-CS070`

Layanan kecerdasan buatan berbasis **FastAPI** untuk **Toko Seragam Asis Amal Mulia Family** yang di-deploy pada **Hugging Face Spaces**. Mencakup tiga kapabilitas utama: (1) pemodelan prediksi penjualan (*sales forecasting*) dan rekomendasi jumlah *restock* menjelang musim tahun ajaran baru, (2) pengolahan otomatis *Data Insight* bisnis, serta (3) asisten AI (*chatbot*) berbasis **Gemini API** untuk menjawab pertanyaan ketersediaan stok dan informasi produk secara instan.


## 1. Cakupan Fitur & Hasil Kerja 

| Fitur / Hasil Kerja | Kategori | Indikator Keberhasilan | PIC |
| :--- | :---: | :--- | :---: |
| **1. Prediksi Penjualan (*Sales Forecasting*)** | Wajib | Melakukan *preprocessing* dataset dari tim DS, melatih serta membandingkan minimal 2 model ML, memilih model dengan *error* terendah (MAE, RMSE, MAPE), dan mendokumentasikan hasil perbandingannya di README. | Saputra |
| **2. Modul Data Insight** | Wajib | Mengolah data transaksi menjadi ringkasan produk terlaris, tren penjualan, dan pergerakan stok secara akurat tanpa perhitungan manual. | Nadia |
| **3. REST API FastAPI (Online)** | Wajib | Menyajikan model prediksi dan modul *insight* melalui REST API yang di-deploy secara online di Hugging Face Spaces dengan respons cepat (< 5 detik) dan stabil. | Saputra & Nadia |
| **4. Asisten AI / Chatbot** | Wajib | Saputra & Nadia |


## 2. Spesifikasi Endpoint FastAPI
> Kontrak payload lengkap dengan tim Backend terdokumentasi pada [`../docs/api-contract.md`](../docs/api-contract.md).

| Method & Endpoint | Fungsi Utama |
| :--- | :--- | :---: |
| `POST /api/v1/forecast` | Menerima data histori & parameter produk/periode, mengembalikan hasil prediksi penjualan dan rekomendasi jumlah *restock* |
| `POST /api/v1/insights` | Menerima data transaksi dari Backend dan mengembalikan agregasi produk terlaris, tren penjualan, serta pergerakan stok |
| `POST /api/v1/chat` | Menerima pertanyaan pengguna beserta konteks stok terkini dari Backend, menyusun prompt, dan memanggil Gemini API |

<!-- ## 3. Panduan Menjalankan Secara Lokal

### Prasyarat
* **Python** versi 3.11

### Langkah Instalasi
1. Masuk ke direktori `ai-service`:
   ```bash
   cd ai-service
   ```
2. Buat dan aktifkan *virtual environment*:
   ```bash
   python -m venv .venv
   # Windows (PowerShell):
   .\.venv\Scripts\Activate.ps1
   # macOS / Linux:
   source .venv/bin/activate
   ```
3. Salin `.env.example` menjadi `.env` dan isi kunci konfigurasi:
   ```bash
   cp .env.example .env
   ```
   Isi `.env`:
   ```env
   GEMINI_API_KEY="masukkan_api_key_gemini"
   AI_SERVICE_API_KEY="kunci_internal_ai_service"
   MODEL_PATH="models/best_forecast_model.joblib"
   ```
4. Instal seluruh dependensi:
   ```bash
   pip install -r requirements.txt
   ```
5. Jalankan server FastAPI secara lokal:
   ```bash
   uvicorn app.main:app --reload --port 8000
   ```
6. Buka dokumentasi interaktif Swagger UI di browser:
   * `http://localhost:8000/docs` -->
