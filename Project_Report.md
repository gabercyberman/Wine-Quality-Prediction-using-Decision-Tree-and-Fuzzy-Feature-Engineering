# Wine Quality Prediction Project
## Machine Learning with Decision Tree & Fuzzy Features

---

### 1. Project Overview
This project aims to predict the quality of wine (red and white) based on physicochemical features using machine learning. The core model is a Decision Tree classifier, and we enhance the feature set with fuzzy logic membership functions for selected features.

---

### 2. Dataset Description
- **Source:** UCI Machine Learning Repository (Wine Quality Data Set)
- **Files Used:**
  - `winequality-red.csv`
  - `winequality-white.csv`
- **Features:**
  11 physicochemical properties (e.g., alcohol, sulphates, citric acid, etc.)
  + `type` column (added: 0 for white, 1 for red)
- **Target:**
  `quality` (integer score from 3 to 9)

---

### 3. Data Preparation & Cleaning
- **Loading:** Both CSV files are loaded and combined into a single DataFrame.
- **Cleaning:**
  - Checked for missing values (none found).
  - Removed duplicate rows.
  - Converted wine type to numeric (0/1).
- **Result:** Clean, combined dataset ready for analysis.

---

### 4. Exploratory Data Analysis (EDA)
- **Visualizations:**
  - Distribution of wine quality for both types.
  - Correlation matrix between features.
- **Findings:**
  - Most wines are rated between 5 and 7.
  - Some features (like alcohol) show correlation with quality.

---

### 5. Data Preprocessing
- **Splitting:** Data split into training (80%) and test (20%) sets.
- **Scaling:** All numeric features scaled using Min-Max Scaler.

---

### 6. Feature Engineering: Fuzzy Features
- **Selected Features:** `alcohol` and `sulphates`.
- **Fuzzy Memberships:** For each, created three fuzzy features (`low`, `medium`, `high`) using triangular membership functions.
- **Result:** 6 new fuzzy features added to the feature set.

---

### 7. Model Training & Hyperparameter Tuning
- **Model:** DecisionTreeClassifier (scikit-learn)
- **Optimization:**
  - Used Hill-Climbing to find the best `max_depth` for the tree.
- **Visualization:** Plotted the final decision tree.

---

### 8. Evaluation
- **Metrics Reported:**
  - Accuracy
  - Precision (weighted)
  - Recall (weighted)
  - Confusion Matrix
- **Performance:**
  The model’s performance was evaluated on the test set and metrics were reported.

---

### 9. Conclusions & Recommendations
- **Fuzzy features** improved the representation of numeric variables and may help the model distinguish quality levels more flexibly.
- **Decision Tree** is interpretable and allows for easy visualization of decision paths.
- **Possible Improvements:**
  - Try other models (e.g., Random Forest, SVM).
  - Use more advanced feature engineering or ensemble methods.
  - Tune more hyperparameters for better accuracy.

---

### 10. How to Run the Project
1. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Open and run `Wine_Quality_Corrected.ipynb` in Jupyter Notebook.
3. Make sure the folder `wine+quality` with both CSV files is in the project directory.

---

### 11. Files Structure
- `Wine_Quality_Corrected.ipynb`: The main notebook with all steps and code.
- `wine+quality/`: Folder containing the dataset CSVs.
- `requirements.txt`: Required Python packages.
- `README.md`: Project instructions.

---
