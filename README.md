# AQI Prediction Practice

Practicing various machine learning models to predict daily Air Quality Index (AQI) using a Kaggle dataset.

## 🎯 Project Goal

The goal of this project is to build and evaluate a machine learning model that can predict the air quality **Status** (e.g., 'Good', 'Moderate', 'Unhealthy') based on the date and country. This is treated as a **classification problem**.

## 💾 Dataset

This project uses the **AQI - Air Quality Index Scheduled Daily Update** dataset from Kaggle.

* **Source:** [https://www.kaggle.com/datasets/azminetoushikwasi/aqi-air-quality-index-scheduled-daily-update](https://www.kaggle.com/datasets/azminetoushikwasi/aqi-air-quality-index-scheduled-daily-update)

To run this project, please download the `data_date.csv` file from the link above and place it in a `data/` folder.

## 🛠️ Project Status & Methodology

This project is currently a work in progress.

1.  **Data Loading:** The `data_date.csv` file is loaded.
2.  **Exploratory Data Analysis (EDA):** Initial checks for null values and data types are performed.
3.  **Feature Engineering:**
    * The `Date` column is split into `Year`, `Month`, and `Day` to be used as numerical features.
    * The categorical `Country` column is one-hot encoded.
4.  **Target Variable:**
    * The `Status` column (our target) is converted from text to numerical categories using `LabelEncoder`.
5.  **Model Training:**
    * The data is split into an 80:20 training and testing set.
    * A baseline **Decision Tree Classifier** is trained.

## 📈 Current Results

The initial Decision Tree Classifier achieved an accuracy of **~70.58%** on the test set.

Future steps will involve:
* Trying other classification models (e.g., Random Forest, Gradient Boosting).
* Performing hyperparameter tuning to improve accuracy.
* Conducting a more in-depth feature analysis.

## 🚀 How to Run

1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/aqi-prediction-practice.git](https://github.com/your-username/aqi-prediction-practice.git)
    cd aqi-prediction-practice
    ```
2.  Create a `data/` folder and place the `data_date.csv` file inside it.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn
    ```
4.  Run the Jupyter Notebook.
    *(Note: You may need to update the file path in the notebook from `/kaggle/input/...` to `data/data_date.csv`.)*
