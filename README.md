# Fake News Detector

## Overview

A machine learning-based system that classifies news articles as **real or fake** using a **Multinomial Naive Bayes** model.

The project provides a simple web interface where users can enter news text and receive a prediction with confidence scores, along with a FastAPI-based API.

---

# Features

- Real-time news classification:
  -  Real News
  -  Fake News

- Confidence score and prediction probabilities.

- User-friendly web interface for testing news articles.

- Prediction logging and model performance monitoring.

- Monthly reports for analyzing predictions.

- Tracking low-confidence predictions for review.

---

# Machine Learning Model

- **Algorithm:** Multinomial Naive Bayes

- **Accuracy:** 87.2%

- **Classes:**
  - Fake
  - Real

Model files:

```
models/
├── fake_news_classifier_v20251120_2200.pkl
└── model_metadata_v20251120_2200.json
```

---

# 🛠️ Technologies Used

## Backend
- Python
- FastAPI

## Machine Learning
- Scikit-learn
- Pandas
- NumPy
- NLTK

## Frontend
- HTML
- CSS
- JavaScript

---

#  Project Structure

```
fake_news_project/

├── app/
│   ├── main.py
│   ├── model_utils.py
│   ├── logging_utils.py
│   └── config.py

├── models/
│   └── trained model files

├── static/
│   ├── index.html
│   ├── script.js
│   └── styles.css

├── logs/
└── requirements.txt
```

---

#  API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Display web interface |
| POST | `/predict` | Classify news text |
| GET | `/monthly-report` | View monthly report |
| GET | `/critical-cases` | View low-confidence cases |
| GET | `/model-info` | View model information |

---

#  How To Run

## 1. Install Requirements

```bash
pip install -r requirements.txt
```

## 2. Run the Server

```bash
uvicorn app.main:app --reload --loop asyncio
```

## 3. Open Application

Open your browser and visit:

```
http://127.0.0.1:8000
```

---

#  Screenshots

## Web Interface 

![Fake News Detector Screenshot](screenshots/screenshot.png)
