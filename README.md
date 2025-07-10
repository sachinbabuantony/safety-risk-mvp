# Construction Site Safety Risk Predictor (MVP)

This project predicts the likelihood of safety incidents at a construction site based on historical incidents, environmental factors, equipment usage, and more. It provides actionable risk alerts and recommendations.

## Features
- User inputs site data and past incident logs via web form
- AI model predicts incident risk score for next period
- Dashboard displays risk level and recommendations
- Easily retrain model with new data (edit `main_dataset.csv` and run `train_model.py`)

## Tech Stack
- **Frontend:** React
- **Backend:** FastAPI (Python)
- **ML:** scikit-learn

## Getting Started

### 1. Backend Setup
```bash
cd backend
python -m venv venv
venv\Scripts\activate  # On Windows
pip install -r requirements.txt  # Or install: fastapi uvicorn scikit-learn pandas joblib
python train_model.py  # Train model on main_dataset.csv
python -m uvicorn app:app --reload  # Start backend
```

### 2. Frontend Setup
```bash
cd frontend
npm install
npm start
```

### 3. Usage
- Open [http://localhost:3000](http://localhost:3000) in your browser.
- Fill out the form and click "Predict Risk".
- To retrain, edit `backend/main_dataset.csv` and rerun `python train_model.py`.

## Deployment
- Backend: Railway, Render, or Heroku
- Frontend: Vercel, Netlify, or GitHub Pages

---

**For questions or contributions, open an issue or pull request!** 