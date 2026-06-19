# 🏠 House Price Predictor
### End-to-End Machine Learning Project | Housing Prices Dataset

![Status](https://img.shields.io/badge/Status-Complete-green)
![Phase](https://img.shields.io/badge/Phase-5%20Summary-blue)
![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Project Overview

Real estate buyers and sellers often rely on guesswork or outdated comparisons to estimate a property's fair value. This project builds a **regression model that predicts house prices based on property features** such as size, number of rooms, location, and amenities.

**Dataset:** [Housing Prices Dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset) — 545 real-world housing records from Kaggle.

---

## 🗂️ Project Structure

```
house-price-prediction/
│
├── analysis.ipynb        ✅ Complete (Tasks 1-5)
├── Housing.csv           ✅ Dataset
├── summary.docx          ✅ Executive Report
├── summary.md            ✅ Markdown Report
├── README.md             ✅ Documentation
└── charts/               ✅ Visualization Exports
```

---

## 📊 Dataset

| Property | Value |
|---|---|
| Source | [Kaggle — Housing Prices Dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset) |
| Rows used | 545 properties |
| Features | 12 input features |
| Target | `price` (USD) |
| Data Quality | 100% clean (No missing values) |

### Feature Dictionary

| Column | Type | Description |
|---|---|---|
| `price` | Target | The sale price of the house |
| `area` | Int | Total square footage of the house |
| `bedrooms` | Int | Number of bedrooms |
| `bathrooms` | Int | Number of bathrooms |
| `stories` | Int | Number of floors |
| `mainroad` | Binary | 1 = near main road, 0 = not |
| `guestroom` | Binary | 1 = has guestroom, 0 = not |
| `basement` | Binary | 1 = has basement, 0 = not |
| `hotwaterheating` | Binary | 1 = has hot water heating, 0 = not |
| `airconditioning` | Binary | 1 = has AC, 0 = not |
| `parking` | Int | Number of parking spaces |
| `prefarea` | Binary | 1 = in preferred area, 0 = not |
| `furnishingstatus`| Categorical| Furnished, Semi-Furnished, Unfurnished |

---

## 🗺️ Project Roadmap

### Phase 1 — Data Loading & Exploration ✅
- Loaded CSV using Pandas.
- Inspected first 10 rows and dataset shape (545x13).
- Identified target (`price`) and feature columns.

### Phase 2 — Data Cleaning ✅
- Verified zero missing values.
- Removed duplicates.
- **One-Hot Encoding:** Converted categorical text (Yes/No, Furnishing Status) into numeric form for the model.

### Phase 3 — Model Building ✅
- Split data into **80% Training** and **20% Testing** sets.
- Trained **Linear Regression** (Baseline).
- Trained **Random Forest Regressor** (Comparison).

### Phase 4 — Visualization ✅
- **Price Distribution:** Histogram showing the spread of house values.
- **Correlation Heatmap:** Identifying which features relate most strongly to price.
- **Actual vs Predicted:** Scatter plot to visualize model accuracy.

---

## 📈 Results

| Model | R² Score | Performance |
|---|---|---|
| **Linear Regression** | **0.7668** | **Best Model** |
| Random Forest | 0.6334 | Lower Accuracy |

**Why did Linear Regression win?**
In this dataset, the relationship between features like `area` and `price` is predominantly linear. The Random Forest model, while powerful, likely overfitted or struggled with the relatively small sample size (545 rows), whereas the simpler Linear Regression model captured the core trends more effectively.

---

## 💡 Key Learnings

- **Space is King:** Total `area` is the strongest predictor of house price.
- **Luxury Premiums:** Adding `airconditioning` and being in a `prefarea` (preferred area) significantly boosts property valuation.
- **Simplicity Wins:** For smaller, clean datasets with clear linear trends, complex models like Random Forest aren't always better than standard Linear Regression.
- **Encoding Matters:** Converting "Yes/No" to "1/0" is essential for computers to process human-readable categories.

---

## 🎯 Interview Talking Points

- *"The dataset was small but high-quality, allowing for a clear comparison between linear and non-linear models."*
- *"I used One-Hot Encoding to handle categorical variables like furnishing status, ensuring the model could interpret all features."*
- *"Linear Regression achieved an R² of 0.7668, meaning it explains nearly 77% of the price variance."*
- *"I found that area, bathrooms, and air conditioning were the top three most influential features for pricing."*

---

## 🧰 Tech Stack

| Tool | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Visualization |
| `seaborn` | Heatmaps and distribution plots |
| `scikit-learn` | Machine learning models and evaluation |

---

## ⚙️ Setup & Run

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/house-price-prediction.git
cd house-price-prediction

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# 3. Run the analysis
jupyter notebook analysis.ipynb
```

---

## 📄 License

MIT License — free to use, modify, and share.

---

*Built by Puskar Ghosal — Data Science Portfolio Project*
