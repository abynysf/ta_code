# Perbandingan Model FinBERT dan VADER dalam Analisis Sentimen Pasar Saham

**Mahasiswa**: Muhammad Abyan Farras Yusuf (22/506156/SV/22088)

**Mitra**: Advisorlauren Co., Ltd.

## Deskripsi Proyek

Penelitian ini membandingkan performa model FinBERT dan VADER dalam analisis sentimen keuangan berbasis media sosial untuk mendukung pengambilan keputusan investasi. Hasil penelitian diintegrasikan dengan indikator teknikal (EMA, RSI, MACD) dan divisualisasikan melalui dashboard real-time.

## 📚 Documentation

- **[System Design & Architecture](TWITTER_INTEGRATION_SYSTEM_DESIGN.md)** - Complete technical architecture documentation with diagrams
- **[Testing Guide](TESTING_GUIDE.md)** - Step-by-step testing instructions
- **[Quick Start](QUICKSTART.md)** - Get started in 5 minutes
- **[Setup Summary](PROJECT_SETUP_SUMMARY.md)** - Complete setup guide
- **[Notebook Explanations](NOTEBOOK_EXPLANATIONS.md)** - Jupyter notebook documentation

## Tech Stack

- **Frontend**: React.js + Vite
- **Backend**: Python + FastAPI
- **Data Pipeline**: Scrapy/Twitter API, yfinance
- **Models**: HuggingFace Transformers (FinBERT), VADER Sentiment Analyzer
- **Database**: PostgreSQL
- **Deployment**: Docker, AWS
- **Evaluation**: scikit-learn (accuracy, precision, recall, F1-score, confusion matrix)

## Struktur Proyek

```
ta_code/
├── backend/                 # FastAPI backend application
│   ├── app/
│   │   ├── api/            # API endpoints
│   │   ├── models/         # Database models
│   │   ├── services/       # Business logic
│   │   │   ├── sentiment/  # Sentiment analysis services
│   │   │   ├── technical/  # Technical indicators
│   │   │   └── data/       # Data processing services
│   │   ├── database/       # Database connections
│   │   ├── utils/          # Utility functions
│   │   └── config/         # Configuration
│   ├── tests/              # Backend tests
│   └── requirements.txt
├── frontend/               # React + Vite dashboard
│   ├── src/
│   ├── public/
│   └── package.json
├── scripts/                # Standalone scripts
│   ├── data_collection/   # Twitter/news scraping
│   ├── preprocessing/     # Data cleaning & preparation
│   └── evaluation/        # Model evaluation scripts
├── data/                   # Data storage
│   ├── raw/               # Raw scraped data
│   ├── processed/         # Cleaned data
│   └── models/            # Saved model weights
├── notebooks/              # Jupyter notebooks for experiments
├── docs/                   # Documentation
└── docker-compose.yml      # Docker orchestration
```

## Setup

### Backend

```bash
cd backend
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env  # Configure environment variables
uvicorn app.main:app --reload
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Database

```bash
docker-compose up -d postgres
```

## Fitur Utama

1. **Analisis Sentimen Ganda**: Perbandingan FinBERT vs VADER
2. **Indikator Teknikal**: EMA, RSI, MACD
3. **Dashboard Real-time**: Visualisasi sentimen dan harga saham
4. **Evaluasi Model**: Metrics komprehensif (accuracy, precision, recall, F1)
5. **Data Pipeline**: Otomatis scraping dan processing

## Roadmap

- [ ] Setup project structure
- [ ] Implement FinBERT sentiment analysis
- [ ] Implement VADER sentiment analysis
- [ ] Build data scraping pipeline
- [ ] Implement technical indicators
- [ ] Create FastAPI endpoints
- [ ] Build React dashboard
- [ ] Model evaluation & comparison
- [ ] Deployment setup

## Lisensi

Academic Research Project
