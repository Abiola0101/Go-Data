# GoData Vehicle Classification Project

This project is part of a data science initiative to analyze and classify vehicle data from Go Auto’s dealership listings using machine learning techniques. The goal is to **predict the transmission type (Automatic or Manual)** for vehicles based on various listing features and to explore the business value of such predictions for dealerships.

---

## Project Objective

To build and evaluate a **binary classification model** that can determine whether a vehicle has an **automatic** or **manual** transmission using data scraped from Canadian Black Book (CBB) APIs and compiled by the Business Intelligence team.

This project aims to:
- Enhance business insights through machine learning
- Improve dealership efficiency by automating listing classification
- Demonstrate real-world ML application with model explainability and deployment

---

## Dataset Description

The dataset contains **30 days of active and sold vehicle listings** across Go Auto dealerships in Edmonton.

### Key Features:
- Year, Make, Model
- Mileage
- Price
- Vehicle Trim and Category
- Dealership Name
- Exterior/Interior Colors
- Transmission Type (Target Variable)


## Exploratory Data Analysis (EDA)

The EDA phase focused on:
- Identifying class imbalance in transmission types
- Feature correlations with transmission (e.g., price, mileage, trim)
- Cleaning missing values and standardizing categorical features
- Visualizing trends using boxplots, histograms, and seaborn pairplots

---

## Machine Learning Model

### Model Used:
- **Random Forest Classifier**

### Model Iteration:
- Base model vs. tuned models with hyperparameters
- Cross-validation with accuracy and F1-score as evaluation metrics

### Final Results:
```
Accuracy: ~0.92
Precision: 0.91 (Manual), 0.93 (Automatic)
Recall: 0.86 (Manual), 0.96 (Automatic)
F1-Score: 0.89 (Manual), 0.94 (Automatic)
```

---

## Model Explainability

Model explainability was performed using two approaches:

### SHAP (SHapley Additive Explanations):
- Summary plots for global feature importance
- Force plots for local interpretation

### LIME (Local Interpretable Model-Agnostic Explanations):
- Instance-level insights for business interpretability
- Useful for dealership decision-making

---

## Deployment

### Flask API for Predictions:
- Built an endpoint to **predict transmission type**
- Accepts JSON payloads and returns model predictions
- Easy to integrate into web apps or dealer dashboards

---

## Potential Use Cases

- Auto-classification of vehicle listings
- Enhanced filters and search on dealership websites
- Predictive tagging for online vehicle marketplaces
- Dealership performance analysis based on inventory patterns

---

## Project Structure

```
godata/
├── data/                    # Raw and cleaned datasets
├── models/                  # Saved Random Forest model
├── notebooks/               # EDA, modeling, SHAP/LIME explainability
├── app.py                   # Flask API for deployment
├── requirements.txt         # Project dependencies
├── README.md                # Project overview and documentation
```

---

## Installation & Setup

1. Clone the repo:
```bash
git clone https://github.com/yourusername/godata.git
cd godata
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the Flask API locally:
```bash
python app.py
```

---

## Future Improvements

- Add Streamlit or Looker Studio dashboard for dealership users
- Integrate vehicle image classification using computer vision
- Include more dealerships and expand to other cities
- Schedule daily retraining with new listings

---

