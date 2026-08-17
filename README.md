# CodeAlpha_Disease-Prediction-From-Medical-Data


## Objective
Predict the possibility of disease (breast cancer diagnosis: malignant vs. benign) from structured patient diagnostic data.

## Approach
Four classification algorithms are trained and compared.
- SVM
- Logistic Regression
- Random Forest
- XGBoost

## Project Structure
```
CodeAlpha_DiseasePrediction/
├── Disease_Prediction_Model.ipynb   <- Main notebook (run this)
├── dataset/
│   └── breast_cancer_data.csv       <- Generated when the notebook runs
├── models/
│   ├── svm.pkl                      <- Best trained model (auto-named)
│   ├── scaler.pkl
│   └── feature_columns.pkl
├── images/
│   ├── class_distribution.png
│   ├── correlation_heatmap.png
│   ├── feature_distributions.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── feature_importance.png
│   └── model_comparison.png
├── README.md
├── requirements.txt
└── .gitignore
```

## Dataset
This project uses the **Wisconsin Breast Cancer Diagnostic Dataset** — the exact "Breast Cancer (UCI ML Repository)" dataset named in the task brief. It's real clinical data: 569 patients, 30 diagnostic features computed from digitized images of breast mass cell nuclei (radius, texture, perimeter, smoothness, concavity, etc.). It ships built into scikit-learn (`sklearn.datasets.load_breast_cancer`), so the notebook runs fully offline with zero manual download.

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook Disease_Prediction_Model.ipynb
```

## Results
| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| SVM | 0.982 | 0.986 | 0.986 | 0.986 | 0.995 |
| Logistic Regression | 0.982 | 0.986 | 0.986 | 0.986 | 0.995 |
| Random Forest | 0.947 | 0.958 | 0.958 | 0.958 | 0.994 |
| XGBoost | 0.956 | 0.947 | 0.986 | 0.966 | 0.992 |

## Disclaimer
This is an internship project, **not** a certified diagnostic tool. It should never be used for actual medical decisions — real clinical deployment would require regulatory approval, much larger and more diverse patient data, and validation by medical professionals.

## Author
Deval Patel