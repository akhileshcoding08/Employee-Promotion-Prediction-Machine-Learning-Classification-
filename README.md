# 🏆 Employee Promotion Prediction — Machine Learning Classification

Predicting whether an employee is likely to be promoted using demographic, performance, and work-related features which built to help HR teams move from manual, time-consuming promotion reviews to a faster, data-driven process.

---

## 📌 Overview

A company wants to identify which employees are likely to get promoted based on their work performance, experience, working hours, projects handled, salary, education level, and other employee-related factors.

The HR department currently evaluates promotions manually, which is time-consuming and may lead to biased decisions. This project builds a **Machine Learning classification model** that predicts whether an employee will be promoted or not - using **Logistic Regression**, **K-Nearest Neighbors (KNN)**, and **Support Vector Machine (SVM)**, then compares their performance.

---

## 📂 Dataset

**File:** `Employee Promotion.xlsx`
**Size:** 2,010 records × 11 columns (2,000 unique records after removing duplicates)

| Column | Description |
|---|---|
| `Age` | Age of the employee |
| `Salary` | Current salary of the employee |
| `Experience` | Total years of work experience |
| `Hours_Per_Week` | Average working hours per week |
| `Projects_Handled` | Number of projects handled |
| `Performance_Score` | Performance rating/score |
| `Gender` | Gender of the employee |
| `Department` | Department the employee belongs to |
| `Education` | Highest education qualification |
| `Work_Mode` | Remote / Hybrid / On-site |
| `Promotion` | **Target** — Promoted (1) or Not Promoted (0) |

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas**, **NumPy** — data manipulation
- **Matplotlib**, **Seaborn** — visualization
- **Scikit-learn** — preprocessing, modeling, evaluation
- **Jupyter Notebook**

---

## ⚙️ Project Workflow

1. Import libraries and load the dataset (`pandas.read_excel`)
2. Initial inspection — `shape`, `info()`, `describe()`
3. Remove duplicate rows
4. Handle missing values — numeric columns filled with **median**, categorical columns filled with **mode**
5. Visualize outliers with **boxplots**
6. Explore feature relationships with a **correlation heatmap**
7. Encode categorical columns with **LabelEncoder**
8. Split into features (`X`) and target (`y = Promotion`)
9. Scale features with **StandardScaler**
10. Train/test split — 80% / 20% (`random_state=42`)
11. Train three models: **Logistic Regression**, **KNN**, **SVM**
12. Evaluate with **accuracy**, **precision**, **recall**, and **F1-score**
13. Compare models and select the best performer

---

## 📊 Results

| Model | Accuracy | Precision (Promoted) | Recall (Promoted) | F1-score (Promoted) |
|---|---|---|---|---|
| Logistic Regression | 89.75% | 0.47 | 0.71 | 0.57 |
| K-Nearest Neighbors (KNN) | 89.25% | 0.39 | 0.73 | 0.51 |
| **Support Vector Machine (SVM)** | **91.50%** | **0.56** | **0.78** | **0.65** |

🏅 **Best model: SVM**, with the highest accuracy and F1-score for the "Promoted" class — the metric that matters most on this imbalanced dataset.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook / JupyterLab

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/employee-promotion-prediction.git
cd employee-promotion-prediction

# 2. (Optional) Create a virtual environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook Employee_Promotion_Classification_Model.ipynb
```

> Make sure `Employee Promotion.xlsx` is placed in the project's root directory before running the notebook.

---

## 📁 Repository Structure

```
employee-promotion-prediction/
│
├── Employee_Promotion_Classification_Model.ipynb   # Main analysis notebook
├── Employee Promotion.xlsx                          # Dataset
├── README.md                                        # Project overview
├── requirements.txt                                 # Python dependencies
└── .gitignore
```

---

## 🔮 Future Improvements

- Handle class imbalance (SMOTE / class weighting) to boost minority-class recall
- Hyperparameter tuning with `GridSearchCV`
- Try Random Forest / XGBoost / ensemble methods
- Add SHAP-based feature importance for explainability
- Deploy as a simple Streamlit/Flask web app
- Use k-fold cross-validation for more robust evaluation

---
