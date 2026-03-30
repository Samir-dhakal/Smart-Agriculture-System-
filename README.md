# Smart-Agriculture-System-
# 🌾 Smart Agriculture System for Crop Recommendation using AI
### Weather + Soil Data Powered Intelligent Crop Advisory System

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![ML](https://img.shields.io/badge/ML-Random%20Forest-green.svg)
![Flask](https://img.shields.io/badge/Backend-Flask-lightgrey.svg)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)
![Phase](https://img.shields.io/badge/Current%20Phase-Phase%201-brightgreen.svg)

---

## 📌 Project Overview

The **Smart Agriculture System** is an AI-powered crop recommendation application that helps farmers make data-driven decisions by analyzing real-time **weather conditions** and **soil parameters**. Instead of relying on guesswork or tradition, farmers can input their soil data and location to receive an instant, accurate crop recommendation powered by Machine Learning.

> *"When farmers grow smarter, the nation grows stronger — and AI is the bridge that gets us there."*

---

## 🚨 Problem Statement

> Farmers across India lack an intelligent and accessible system that recommends the most suitable crop based on real-time weather conditions and soil parameters — resulting in poor crop yield, excessive resource wastage, and severe economic loss for farming communities.

### Key Problems Identified:
| Problem | Description |
|--------|-------------|
| ❌ Wrong Crop Selection | Farmers plant crops based on habit rather than soil suitability |
| 🌦️ Unpredictable Weather | Climate change disrupts traditional seasonal farming knowledge |
| 🧪 Poor Soil Management | Unknown N, P, K, pH levels cause fertilizer waste and soil damage |
| 📵 No Smart Tools | Rural farmers have zero access to AI-based advisory systems |

---

## 🎯 Objectives

**Objective 1 — Data Foundation**
> Collect and preprocess real-world weather data (temperature, humidity, rainfall) and soil data (Nitrogen, Phosphorus, Potassium, pH) to build a clean, reliable, and balanced training dataset.

**Objective 2 — AI Model Development**
> Train and evaluate a supervised ML classification model using Random Forest that accurately recommends the best-suited crop with a target accuracy above 95%.

**Objective 3 — Accessible Deployment**
> Build a simple, user-friendly web interface where farmers can enter soil readings, auto-fetch live weather data by city name, and receive an instant crop recommendation with confidence score.

---

## 🌍 Societal Benefits

- 🌾 **Higher Farmer Income** — Right crop = better yield = more profit per season
- 💧 **Resource Conservation** — Reduces water, fertilizer, and pesticide waste by up to 30%
- 🇮🇳 **National Food Security** — Supports India's sustainable agricultural growth goals
- 📱 **Digital Inclusion** — Makes AI accessible to rural and uneducated farmers
- 🌱 **Eco-Friendly Farming** — Prevents soil degradation and promotes biodiversity

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| Source | [Kaggle — Crop Recommendation Dataset](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset) |
| Size | 2200 rows × 8 columns |
| Crop Classes | 22 crops (Rice, Wheat, Maize, Mango, Cotton, etc.) |
| Type | Supervised Learning — Fully Labeled |

### Input Features:
| Feature | Description | Unit |
|---------|-------------|------|
| N | Nitrogen content in soil | mg/kg |
| P | Phosphorus content in soil | mg/kg |
| K | Potassium content in soil | mg/kg |
| Temperature | Average temperature | °C |
| Humidity | Relative humidity | % |
| pH | Soil pH value | 0–14 |
| Rainfall | Annual rainfall | mm |
| **Label** | **Recommended Crop (Output)** | — |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | Python 3.8+ |
| ML Library | Scikit-learn |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Weather API | OpenWeatherMap API |
| Web Framework | Flask |
| Frontend | HTML, CSS, Bootstrap |
| Dataset Source | Kaggle |

---

## 🤖 ML Models Evaluated

| Model | Accuracy |
|-------|---------|
| Random Forest | 99.3% ✅ Selected |
| Naive Bayes | 99.5% |
| SVM | 97.7% |
| Decision Tree | 90.2% |

**Why Random Forest?**
- Handles both numerical and categorical data
- Resistant to overfitting
- Works well on small to medium datasets
- Provides feature importance scores
- Fast prediction (under 1 second)

---

## ⚙️ How It Works

```
[Farmer Inputs Data]
        |
        |-----> [Soil Parameters (Manual Form)]
        |       N, P, K, pH
        |
        |-----> [Weather API (Auto-Fetched)]
                Temperature, Humidity, Rainfall
                        |
                        v
            [Data Preprocessing Layer]
            Feature Scaling + Encoding
                        |
                        v
            [Trained Random Forest Model]
                        |
                        v
            [Output: Crop Recommendation]
            "Best Crop: Rice (Confidence: 94.2%)"
```

---

## 📁 Project Structure

```
smart-agriculture-ai/
│
├── dataset/
│   └── crop_recommendation.csv       # Kaggle dataset
│
├── model/
│   ├── train_model.py                # Model training script
│   ├── random_forest_model.pkl       # Saved trained model
│   └── scaler.pkl                    # Saved StandardScaler
│
├── app/
│   ├── app.py                        # Flask web application
│   ├── templates/
│   │   ├── index.html                # Input form page
│   │   └── result.html               # Recommendation output page
│   └── static/
│       ├── css/style.css             # Stylesheet
│       └── images/                   # UI images
│
├── notebooks/
│   ├── EDA.ipynb                     # Exploratory Data Analysis
│   └── Model_Training.ipynb          # ML model training notebook
│
├── requirements.txt                  # Python dependencies
├── README.md                         # Project documentation
└── .env                              # API keys (not pushed to GitHub)
```

---

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
pip
OpenWeatherMap API Key (free at openweathermap.org)
```

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/smart-agriculture-ai.git
cd smart-agriculture-ai
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Set up your API key**
```bash
# Create a .env file in the root directory
echo "WEATHER_API_KEY=your_openweathermap_api_key_here" > .env
```

**4. Train the model**
```bash
python model/train_model.py
```

**5. Run the web application**
```bash
python app/app.py
```

**6. Open in browser**
```
http://localhost:5000
```

---

## 📦 Requirements

```
flask
scikit-learn
pandas
numpy
matplotlib
seaborn
requests
python-dotenv
joblib
```

Install all at once:
```bash
pip install flask scikit-learn pandas numpy matplotlib seaborn requests python-dotenv joblib
```

---

## 📈 Project Phases

| Phase | Title | Status |
|-------|-------|--------|
| 🔵 Phase 1 | Problem Identification | ✅ Complete |
| 🟡 Phase 2 | Dataset Collection & Preprocessing | 🔄 In Progress |
| 🔴 Phase 3 | Methodology & Results | ⏳ Upcoming |
| 🟣 Phase 4 | Poster Presentation | ⏳ Upcoming |

---

## 📋 Phase 1 — Problem Identification (Completed ✅)

- [x] Problem clearly identified and formally stated
- [x] 3 measurable project objectives defined
- [x] Real-world societal benefits documented across 5 dimensions
- [x] 3 possible solutions analyzed and evaluated
- [x] Final technical approach selected with clear justification
- [x] Project scope defined and feasibility confirmed

---

## 🔮 Future Scope

- 📡 **IoT Integration** — Automatic soil data collection via IoT sensors
- 📱 **Mobile App** — Android/iOS app with offline functionality
- 🗣️ **Regional Languages** — Support for Tamil, Hindi, Telugu interfaces
- 🌿 **Extended Recommendations** — Add fertilizer and pesticide suggestions
- 🛰️ **Satellite Imagery** — Large-scale farm monitoring using satellite data

---

## 👥 Team

| Role | Name |
|------|------|
| Developer | [Samir Dhakal ] |
| Developer | [Aayusha Kuikel] |
| Developer | [Ayush Pandey] |
| Institution | [SRM Institute Of Science And Technology] |
| Department | [Computer Techonlogies ] |
| Academic Year | 2025–26 |

---

## 📄 License

This project is developed for academic purposes under the **Application Development** course.

---

## 🙏 Acknowledgements

- [Kaggle](https://www.kaggle.com) — For the Crop Recommendation Dataset
- [OpenWeatherMap](https://openweathermap.org) — For the free Weather API
- [Scikit-learn](https://scikit-learn.org) — For ML model libraries
- All farmers of India 🌾 — The true inspiration behind this project

---

*Smart Agriculture System — Empowering Farmers with AI* 🌾🤖
