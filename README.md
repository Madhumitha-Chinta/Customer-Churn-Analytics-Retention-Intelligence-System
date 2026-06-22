# Customer Churn Analytics & Retention Intelligence System

An end-to-end Machine Learning and Business Intelligence solution designed to analyze customer behavior, predict churn risk, and identify the principal drivers of customer attrition. Built using **Python**, **scikit-learn**, and **Streamlit**.

---

## Features

- **Key Performance Indicators (KPIs)**:
  - **Total Customers**: Monitored volume of the customer base.
  - **Churn Rate**: Real-time percentage of customers who have churned.
  - **Revenue Loss**: Direct financial impact calculated from monthly charges of churned customers.
- **Interactive Visualizations (Plotly)**:
  - **Churn Distribution**: Uncover overall churn ratios.
  - **Contract vs. Churn**: Analyze how contract structures (Month-to-month, One-year, Two-year) correlate with customer retention.
  - **Monthly Charges vs. Churn**: Outlier-aware boxplots depicting monthly spending ranges for churned vs. active customers.
  - **Sidebar Filter**: Real-time dashboard filtering by contract type.
- **Predictive Churn Simulator**:
  - Predict real-time customer churn probability and risk status (🔴 High Risk, 🟡 Medium Risk, 🟢 Low Risk) based on key customer metrics.
- **Model Explainability**:
  - Horizontal bar charts displaying scikit-learn model feature importances, demonstrating which factors (e.g., tenure, charges, contract type) contribute most to customer attrition.

---

## 🛠️ Tech Stack

- **Frontend / Dashboard**: [Streamlit](https://streamlit.io/)
- **Data Visualization**: [Plotly Express](https://plotly.com/python/)
- **Data Engineering**: [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/)
- **Machine Learning**: [scikit-learn](https://scikit-learn.org/)
- **Model Serialization**: [joblib](https://joblib.readthedocs.io/)

---

##  Model Performance

The predictive model is built using a **Random Forest Classifier** trained on the Telco Customer Churn dataset.

### Evaluation Metrics
| Metric | Score |
| :--- | :--- |
| **Accuracy** | `76.08%` |
| **Precision** | `55.96%` |
| **Recall** | `45.31%` |
| **F1 Score** | `50.07%` |

### Classification Report
```text
              precision    recall  f1-score   support

           0       0.82      0.87      0.84      1036
           1       0.56      0.45      0.50       373

    accuracy                           0.76      1409
   macro avg       0.69      0.66      0.67      1409
weighted avg       0.75      0.76      0.75      1409
```

---

##  Project Structure

```
├── .gitignore              # Git exclusions (venv, caches, etc.)
├── requirements.txt        # Python dependency specifications
├── README.md               # Project documentation
├── app/
│   └── main.py             # Streamlit Dashboard application
├── data/
│   ├── Telco-Customer-Churn.csv  # Raw dataset
│   ├── cleaned_churn.csv         # Cleaned customer data
│   └── model_data.csv            # Preprocessed feature-store dataset
├── models/
│   ├── churn_model.pkl           # Trained Random Forest model binary
│   └── encoder_mappings.pkl      # Serialized label encoders
└── notebooks/
    ├── download_data.py          # Data ingestion script
    ├── data_understanding.py     # Initial data profiling and exploration
    ├── data_cleaning.py          # Cleaning duplicates and filling nulls
    ├── eda.py                    # Exploratory Data Analysis & visual plots
    ├── preprocessing.py          # Categorical encoding & feature selection
    └── model_training.py         # Model training & serialization pipeline
```

---

##  Getting Started

### Prerequisites
Make sure you have **Python 3.8+** installed on your system.

### Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd "Customer Churn Analytics & Retention Intelligence System"
   ```

2. **Create and activate a virtual environment**:
   * **Windows**:
     ```bash
     python -m venv .venv
     .venv\Scripts\activate
     ```
   * **macOS/Linux**:
     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

To launch the Streamlit dashboard locally, run the following command in your terminal:
```bash
streamlit run app/main.py
```

The application will automatically launch in your default web browser at **`http://localhost:8501`**.

---

## 🔗 How to Post to GitHub

Initialize your repository and push to GitHub using the commands below:

1. **Initialize Git**:
   ```bash
   git init
   ```
2. **Stage files for commit**:
   ```bash
   git add .
   ```
3. **Commit your files**:
   ```bash
   git commit -m "Initial commit: End-to-end churn prediction and analytics system"
   ```
4. **Link to your GitHub remote repository**:
   ```bash
   git branch -M main
   git remote add origin <YOUR_GITHUB_REPOSITORY_URL>
   ```
5. **Push to main branch**:
   ```bash
   git push -u origin main
   ```
