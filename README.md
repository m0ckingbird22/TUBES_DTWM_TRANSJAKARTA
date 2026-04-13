# Tugas Besar DWH - Transportasi Umum Jakarta

## Anggota Kelompok

| Nama                  | NIM         | Role                             |
| --------------------- | ----------- | -------------------------------- |
| Muhammad Afiq Aqhdaq  | 24110300008 | Data Architect & Schema Designer |
| Dhafi Ihza Al Kahfi   | 24110300031 | Data Engineer / ETL Developer    |
| Muhammad Nabil Alviro | -           | Data Analyst & Visualizer        |

## Setup Environment

```bash
# 1. Clone repo
git clone https://github.com/xxx/Tubes_DWH_TransportasiJakarta.git
cd Tubes_DWH_TransportasiJakarta

# 2. Buat virtual environment
python -m venv venv

# Windows
venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Setup credentials
cp .env.example .env
# Edit .env dan isi dengan API key & project ID kamu
# Taruh credentials.json (service account Google Cloud) di root folder
```

## Struktur Folder

```
├── notebook/
│   └── tubes_dwh_jakarta_transit.ipynb
├── data/
│   ├── gtfs/          ← Source 1: GTFS data
│   ├── manual/        ← Source 2: Tarif & info operasional
│   └── gmaps/         ← Source 3: Google Maps API results
├── schema/
│   └── star_schema.png
├── assets/
│   ├── screenshots/
│   └── demo/
├── laporan/
│   └── Laporan_TUBES1.pdf
├── .gitignore
├── .env.example
├── requirements.txt
└── README.md
```

## Cara Run Notebook

```bash
jupyter notebook notebook/tubes_dwh_jakarta_transit.ipynb
```

Run semua cell dari atas ke bawah secara berurutan.

## Catatan

- File `.env` dan `credentials.json` **TIDAK** di-commit ke GitHub
- Data GTFS di `data/gtfs/` perlu di-download manual dari data.jakarta.go.id
- Data Google Maps di `data/gmaps/` perlu di-generate via API
