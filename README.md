# end-to-end-data-science-project-python
Training data science skills: From data cleaning to a machine learning model

# End-to-End Data Science Project: From Data Cleaning to Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Google Colab](https://img.shields.io/badge/Platform-Google%20Colab-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## Overview

This project demonstrates a complete end-to-end data science workflow, 
covering the full pipeline from raw data ingestion through to a trained 
and evaluated machine learning model. The work is divided across three 
tasks using two independent datasets, each targeting a different stage 
of the data science process.

The project was completed as part of the Predictive Analytics and Machine 
Learning using Python module at Berlin School of Business and Innovation 
(BSBI), MSc Data Analytics programme.

---

---

## Tasks Covered

### Task 1 — Data Cleaning and Exploratory Data Analysis
- Loaded Dataset 1 (1375 rows, 5 features: X1, X2, X3, X4, Label)
- Performed systematic data quality checks:
  - Detected and removed **25 duplicate rows**
  - Dropped **1 missing value** in the Label column
  - Detected and removed **93 outliers** using the IQR method
  - Final clean dataset: **1256 rows**
- Conducted EDA and uncovered a key distributional difference:
  - **X1** — bimodal, approximately symmetrical (skewness = -0.16)
  - **X4** — unimodal, left-skewed (skewness = -0.84)

---

### Task 2 — Probability Metrics and Impurity Measures
- Calculated class probabilities from the clean dataset:
  - P(Class 0) = 0.5756
  - P(Class 1) = 0.4244
- Computed **Gini Impurity = 0.4886** (close to maximum of 0.5)
- Computed **Entropy = 0.9834** (close to maximum of 1.0)
- Established **baseline misclassification rate = 42.44%**

---

### Task 3 — Regression Modelling
- Loaded Dataset 2 independently (1000 rows, 2 columns: t and f(t))
- Visualised data to identify an exponential decay pattern
- Selected **Exponential Regression** based on visual and mathematical evidence
- Fitted model using `scipy.optimize.curve_fit`
- Final equation: **f(t) = 44.3999 × e^(-0.7868 × t)**
- Model evaluation:
  - **R² Score = 0.9946** (exceptionally strong fit)
  - **RMSE = 35.99**
- Identified three underlying trends:
  - f(t) decreases by **54.5%** for every 1 unit increase in t
  - **Asymptotic behaviour** — f(t) approaches but never reaches zero
  - Smooth and consistent decay with minimal random variation

---

## Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.x | Core programming language |
| Pandas | Data loading, cleaning and manipulation |
| NumPy | Numerical computations |
| Matplotlib | Data visualisation |
| Seaborn | Statistical visualisation |
| SciPy | Exponential regression model fitting |
| Scikit-learn | Model evaluation metrics (R², RMSE) |
| Google Colab | Development environment |

---

## Key Findings

- Raw data is rarely clean — this project encountered duplicates, 
  missing values and outliers before any analysis could begin
- Visual inspection of data before modelling is critical — the scatter 
  plot directly guided the choice of exponential regression over linear 
  or polynomial alternatives
- Both Gini Impurity (0.4886) and Entropy (0.9834) confirmed the 
  classification dataset is highly mixed, setting a meaningful 
  performance benchmark for future modelling
- The exponential model achieved an R² of 0.9946, demonstrating that 
  the right model choice produces near-perfect results

---

## Datasets

| Dataset | Used In | Link |
|---------|---------|------|
| Dataset 1 | Tasks 1 and 2 | [Access here](https://drive.google.com/file/d/1o2zNGpyc7llWJCPbf6RXCJuweYCfrvnt/view?usp=sharing) |
| Dataset 2 | Task 3 | [Access here](https://drive.google.com/file/d/1wJj-Cy5f5KmVEmD8KQH6ncup2JHNGSxn/view?usp=sharing) |

---

## How to Run

1. Open the notebook in Google Colab
2. Run all cells from top to bottom
3. Datasets load automatically via Google Drive links
4. All outputs, plots and results will generate in sequence

---

## Author

**Zee**
MSc Data Analytics — Berlin School of Business and Innovation (BSBI)
Berlin, Germany

---

## Acknowledgements

This project was completed as part of the Predictive Analytics and 
Machine Learning using Python module, issued by Dr. habil. Gregor 
Tkachov at BSBI in partnership with the University for the Creative 
Arts (UCA).
