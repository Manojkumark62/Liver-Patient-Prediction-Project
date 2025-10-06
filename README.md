***Liver Patient Prediction***

**Overview:**

This project aims to predict whether a patient has liver disease based on clinical attributes such as bilirubin levels, enzyme counts, and protein ratios. The dataset used is the Indian Liver Patient Dataset, which contains medical records of patients. The analysis follows a structured data science workflow including data loading/cleaning, exploratory data analysis (EDA), model building/evaluation, and feature importance analysis.
The project is implemented in a Jupyter Notebook (Liver_Patient_Prediction.ipynb) using Python. Machine learning models like Logistic Regression, Random Forest, and XGBoost are trained and evaluated, with Random Forest showing the best performance.
Dataset

**Features:**

Age

Gender

Total_Bilirubin

Direct_Bilirubin

Alkaline_Phosphotase

Alamine_Aminotransferase

Aspartate_Aminotransferase

Total_Proteins

Albumin

Albumin_and_Globulin_Ratio


Target: Binary classification (1: Liver disease, 2: No liver disease; remapped to 0/1 in the code for modeling).

Size: 570 entries.

Imbalance: The dataset is imbalanced (more patients with liver disease), handled using SMOTE oversampling.


**Requirements:**

pandas

numpy

matplotlib

seaborn

scikit-learn

imbalanced-learn

xgboost


The notebook includes all steps: data loading, cleaning, EDA visualizations, model training, evaluation, and feature importance.

**Project Structure:**

Liver_Patient_Prediction.ipynb: Main Jupyter Notebook with code, explanations, and visualizations.

**Data Loading & Cleaning:**

Load dataset from CSV.

Rename columns for clarity.

Handle missing values (e.g., fill median for Albumin_and_Globulin_Ratio).

Encode categorical features (Gender: Male=1, Female=0).

Remap Target (2 → 0 for no disease).


**Exploratory Data Analysis (EDA):**

Count plots for Target and Gender.

Correlation heatmap.

Histograms and boxplots for feature distributions.

Pairplots and scatter plots for relationships.


**Data Preprocessing:**

Split data into train/test (80/20).
Standardize features using StandardScaler.
Handle class imbalance with SMOTE.


**Model Building & Evaluation:**

Models trained: Logistic Regression, Random Forest, XGBoost.

Metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC, Confusion Matrix.


**Feature Importance:**

Visualized for Random Forest and XGBoost (e.g., bar plots showing top features like Total_Bilirubin, Alkaline_Phosphotase).


**Conclusion:**

Random Forest outperforms others with balanced metrics.
Logistic Regression has high precision but low recall (misses many cases).
XGBoost provides good balance but lower ROC-AUC.
This model can aid in early liver disease detection for clinical decision-making.


**Results:**

Best Model: Random Forest (Accuracy: 73%, F1-Score for disease class: 0.81).
Key Insights: Features like bilirubin levels and enzyme counts are highly important for prediction.
Visualizations are embedded in the notebook for better understanding.
