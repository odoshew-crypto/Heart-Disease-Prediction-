-This project applies Machine Learning classification models to predict whether a patient has heart disease based on medical features. The goal is to assist in early detection using data-driven insights.

-Problem Type: Classification
Target Variable:
0 → No Heart Disease
1 → Heart Disease Present Dataset

-The dataset contains patient medical records such as:
Age
Sex
Chest pain type
Blood pressure
Cholesterol levels
Maximum heart rate

-Source: Kaggle
Tools 
Python
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn Project Structure
Heart-Disease-Prediction/
│
├── data/
│   └── heart.csv
│
├── notebooks/
│   └── eda.ipynb
│   └── model_training.ipynb
│
├── images/
│   ├── heatmap.png
│   ├── confusion_matrix.png
│
├── src/
│   └── model.py
│
├── README.md
├── requirements.txt
└── main.py
- Exploratory Data Analysis (EDA)
 Correlation Heatmap

A correlation heatmap was used to understand relationships between features and the target variable.

Insight:
Helps identify which medical features are strongly linked to heart disease.
 Model Building
Models used:
Logistic Regression (baseline mode)
 Model Evaluation
 Confusion Matrix
Used to evaluate classification performance by comparing predictions vs actual results.
from sklearn.metrics import confusion_matrix
import seaborn as sns
import matplotlib.pyplot as plt
cm = confusion_matrix(y_test, y_pred)
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues')
plt.title("Confusion Matrix")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.show()
Results
-Model	Accuracy
Logistic Regression	85%

 Best Model: Random Forest Classifier

- Visualizations
Correlation Heatmap

(Add image in GitHub: images/heatmap.png)

 Confusion Matrix
