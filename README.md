# Depression Risk Prediction — Educational Machine Learning Project

This project demonstrates an end-to-end **binary classification pipeline** for predicting depression risk using student-related data.  
It is designed as an **educational notebook**, focusing on data analysis, evaluation methodology, threshold selection, and probability calibration.

---

## Project objectives

The main goals of this project are to:

- Perform **Exploratory Data Analysis (EDA)** on a real-world dataset
- Build and compare **Random Forest** and **Gradient Boosting** models
- Handle **class imbalance** appropriately
- Select an **optimal decision threshold** using mathematical criteria
- **Calibrate predicted probabilities** for better interpretability
- Perform manual predictions using custom input data

---

## Dataset

- File: `dataset.csv`
- Each row represents a student.
- Features include demographic, academic, lifestyle, and stress-related variables.
- Target variable:
  - `Depression = 0` → not at risk
  - `Depression = 1` → at risk

Please ensure that the dataset file name and path match the one defined in the notebook.

---

## Methodology

The notebook follows a structured machine learning workflow:

### 1. Data exploration
- Dataset inspection (`shape`, `info`, `describe`)
- Missing values and duplicate checks
- Target distribution analysis
- Feature distributions
- Correlation analysis

### 2. Data preparation
- Feature–target separation
- Identification of numeric and categorical variables
- One-hot encoding using `ColumnTransformer`
- Consistent preprocessing with `Pipeline`

### 3. Model training
- Random Forest with class balancing
- Gradient Boosting
- Fair comparison using identical preprocessing

### 4. Model evaluation
- Validation with multiple metrics:
  - Accuracy, Precision, Recall, F1-score
  - ROC-AUC and Precision–Recall AUC
- ROC and Precision–Recall curves
- Confusion matrices

### 5. Threshold selection
- Mathematical optimization using:
  - Maximum F1-score
  - Youden’s J statistic
- Threshold sweep analysis

### 6. Probability calibration
- Sigmoid (Platt scaling)
- Isotonic regression
- Evaluation with calibration curves and Brier score

### 7. Final evaluation
- Unbiased evaluation on a held-out test set
- Comparison of calibrated vs non-calibrated models

### 8. Manual prediction
- Manual insertion of feature values
- Prediction of depression risk probability
- Final classification using the selected threshold

---

## Key concepts demonstrated

- Proper train / validation / test splitting
- Avoiding data leakage with pipelines
- Handling imbalanced datasets
- Threshold optimization beyond the default 0.5
- Difference between ranking performance and probability calibration
- Model interpretability via feature importance

---

## Requirements

Main Python libraries used:
- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

All analysis is performed inside a Jupyter Notebook.

---

## How to run the project

1. Place `dataset.csv` in the same directory as the notebook.
2. Open the notebook in Jupyter.
3. Run the cells sequentially from top to bottom.
4. Modify the **manual prediction** section to test custom inputs.

---

## Disclaimer

This project is intended for **educational purposes only**.  
It is **not a medical diagnostic tool** and must not be used for clinical decision-making.

---

## License

MIT License

Copyright (c) 2026 @stacktrap

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Author

@stacktrap
