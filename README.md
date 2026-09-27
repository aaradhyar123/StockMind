# MarketMind

**Stock Price Trend Prediction using LSTM Networks** — a full-stack web app that fetches historical stock data, trains/serves an LSTM model, and visualizes short-horizon price trend predictions.

> ⚠️ Educational project. Not financial advice.

## Docs

- [Problem Statement](docs/PROBLEM_STATEMENT.md)
- [Solution](docs/SOLUTION.md)
- [Architecture](docs/ARCHITECTURE.md)
- [Antigravity project context](CONTEXT.md) — read this first if you're an agent working in this repo

## Quick start

### 1. Backend

```bash
cd backend
python -m venv venv && source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt

# Train a model for a ticker (creates backend/data/<TICKER>_lstm.h5)
python train_model.py --ticker AAPL --epochs 25

# Run the API
uvicorn app.main:app --reload --port 8000
```

API docs will be live at `http://localhost:8000/docs`.

### 2. Frontend

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173`.

## Project structure

See [CONTEXT.md](CONTEXT.md#3-repository-layout).

## Tech stack

Python · TensorFlow/Keras · FastAPI · React · Vite · Recharts · yfinance

## Status

MVP scaffold — single-ticker trend prediction, no auth, SQLite for caching.

## License

MIT 
