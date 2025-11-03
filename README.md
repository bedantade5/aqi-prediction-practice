# AQI Prediction Practice

Practicing various machine learning models to predict daily Air Quality Index (AQI) using a Kaggle dataset.

## 🎯 Project Goal

The goal of this project is to build and evaluate a machine learning model that can predict the air quality **Status** (e.g., 'Good', 'Moderate', 'Unhealthy') based on the date and country. This is treated as a **classification problem**.

## 💾 Dataset

This project uses the **AQI - Air Quality Index Scheduled Daily Update** dataset from Kaggle.

* **Source:** [https://www.kaggle.com/datasets/azminetoushikwasi/aqi-air-quality-index-scheduled-daily-update](https://www.kaggle.com/datasets/azminetoushikwasi/aqi-air-quality-index-scheduled-daily-update)

## 🛠️ Methodology

A full end-to-end machine learning workflow was performed:

1.  **Data Loading:** The `data_date.csv` file was loaded using Pandas.
2.  **Data Cleaning:** All rows with missing values (`dropna()`) were removed.
3.  **Feature Engineering:**
    * The `Date` column was split into `Year`, `Month`, and `Day` to be used as numerical features.
    * The categorical `Country` column was one-hot encoded using `pd.get_dummies()`.
4.  **Target Encoding:**
    * The `Status` column (our target) was converted from text to numerical categories (e.g., 0, 1, 2) using `LabelEncoder`.
5.  **Model Training & Comparison:**
    * The data was split into an 80:20 training and testing set.
    * **Seven different models** were trained and evaluated to compare their performance.
    * A `StandardScaler` was applied to the data for distance-based models (KNN) to test the effect of feature scaling.

## 📈 Results

The final comparison of all models yielded a clear leaderboard. The `RandomForestClassifier` provided the highest accuracy "out of the box."

### Final Model Leaderboard

| Model | Accuracy |
| :--- | :--- |
| **Random Forest** | **75.82%** |
| KNN (Scaled) | 74.74% |
| XGBoost | 72.91% |
| Decision Tree | 70.58% |
| Logistic Regression | 67.97% |
| KNN (Unscaled) | 58.02% |
| AdaBoost | 57.13% |


## 🚀 How to Run

1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/aqi-prediction-practice.git](https://github.com/your-username/aqi-prediction-practice.git)
    cd aqi-prediction-practice
    ```
2.  Create a `data/` folder and place the `data_date.csv` file inside it.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn xgboost matplotlib seaborn
    ```
4.  Run the Jupyter Notebook.
    *(Note: You may need to update the file path in the notebook from `/kaggle/input/...` to `data/data_date.csv`.)*
