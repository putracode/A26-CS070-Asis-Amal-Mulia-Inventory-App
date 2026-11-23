# Asis Amal Mulia Inventory App
> **Digitalisasi Manajemen Inventaris dan Penjualan Toko Seragam Asis Amal Mulia Family**  
> *Program Capstone Asah 2026 (Led by Dicoding, Supported by GoTo)*  
> **ID Tim:** A26-CS070 | **Bidang UMKM:** Retail

---

## 1. Anggota Tim & Pembagian Peran (6 Orang)

| No | Nama Anggota | ID Peserta | Learning Path | Tanggung Jawab Utama |
| :-: | :--- | :---: | :--- | :--- |
| 1 | **Saputra** | `ae009b6y1631` | Next-Gen AI Engineer | Model Prediksi Stok Penjualan (Forecasting), FastAPI, Chatbot Gemini & Deploy Hugging Face |
| 2 | **Nadia Rahya Harahap** | `ae009b6x1314` | Next-Gen AI Engineer | Smart Insight, FastAPI, Chatbot Gemini & Deploy Hugging Face |
| 3 | **Adam Himawan** | `ds009b6y0030` | Data Science Specialist | EDA, Visualisasi & Insight, Dasbor Streamlit |
| 4 | **Reza Prasetiyo Syahputra** | `ds009b6y1550` | Data Science Specialist | Data Wrangling (Digitalisasi Nota), Data Dictionary & Dataset Siap Latih |
| 5 | **Daffi Arvyn Prakasa** | `fs009b6y0399` | AI Full-Stack Developer | Frontend React, Login, Integrasi AI & Deploy |
| 6 | **Muhammad Rahardian Baihaqi** | `fs222b6y1236` | AI Full-Stack Developer | Backend REST API Express, Database PostgreSQL & Validasi |

---

## 2. Struktur Monorepo

```text
asis-inventory-app/
├── frontend/               # [Full-Stack] React + Vite + Tailwind CSS — Deploy Vercel
├── backend/                # [Full-Stack] Node.js + Express REST API, PostgreSQL + Prisma, JWT + bcrypt — Deploy Railway
├── data-science/           # [Data Science] Data Wrangling, Data Dictionary, EDA & Dasbor Streamlit
├── ai-service/             # [Next-Gen AI] FastAPI, Forecasting, Data Insight & Chatbot Gemini — Deploy Hugging Face Spaces
├── docs/                   # [Semua] API Contract, ERD Database, Data Dictionary & Panduan Pengguna
├── .gitignore              # Unified Git ignore rules (Node.js + Python + Secrets)
└── README.md               # Dokumentasi utama proyek
```

---

## 3. Strategi Kolaborasi (Branching Strategy)

* **`main`**: Kode stabil dan teruji yang siap digunakan untuk demo dan penilaian akhir *(Protected Branch)*.
* **`dev`**: Branch integrasi harian tempat seluruh fitur dari 3 peran digabungkan.
* **Feature Branches (`feat/*`)**: Dibuat dari `dev` untuk tiap tugas
  <!-- * Full-Stack: `feat/fe-login`, `feat/fe-stock-transaction`, `feat/be-auth-jwt`, `feat/be-stock-api`
  * Data Science: `feat/ds-data-wrangling`, `feat/ds-eda-dashboard`
  * Next-Gen AI: `feat/ai-forecasting`, `feat/ai-data-insight`, `feat/ai-chatbot` -->

---

## 4. Alur Kerja Kontrak API (Contract-First)
Seluruh skema data request dan response disepakati pada dokumen [`docs/api-contract.md`](docs/api-contract.md) bersama [`docs/data-dictionary.md`](docs/data-dictionary.md) sejak Minggu 1, memungkinkan Frontend, Backend, Data Science, dan AI Service bekerja secara paralel dengan data contoh (mock) tanpa saling menunggu.
