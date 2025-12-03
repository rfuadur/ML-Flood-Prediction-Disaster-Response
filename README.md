# Machine Learning-Based Flood Prediction for Disaster Preparedness and Response

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-green)

**Repository Link:** [https://github.com/rfuadur/ML-Flood-Prediction-Disaster-Response](https://github.com/rfuadur/ML-Flood-Prediction-Disaster-Response)

## 📌 Project Overview
Floods are among the deadliest natural disasters, causing significant damage to infrastructure and human lives. Traditional hydrological models often struggle to capture the complex interactions between environmental factors.

This project explores the application of **Machine Learning (ML)** techniques to predict flood events and enhance disaster preparedness. By leveraging historical meteorological data, river flow measurements, and land use patterns, we developed models to identify patterns preceding flooding events, providing timely alerts to mitigate risks.

## 👥 Authors
* **MD Fuadur Rahman Mollah** - CSE, BRAC University
* **Alvee Ishraque** - CSE, BRAC University
* **MD Shahadat Hossain Shamim** - CSE, BRAC University

## 📂 Dataset Details
The study utilizes a dataset combining environmental and urban features to assess flood threats.

* **Original Size:** 5,050 records.
* **Final Size (After Cleaning):** 4,800 records.
* **Features:**
    * `Rainfall_mm`: Precipitation levels.
    * `River_Level_m`: River water levels.
    * `Soil_Moisture_%`: Soil saturation levels.
    * `Flood_Risk`: Target variable (Categorical).
    * `Evacuation_Required`: Target variable (Binary).

## ⚙️ Methodology & Preprocessing
To ensure model accuracy, the following preprocessing steps were applied:

1.  **Feature Selection:** Removed the `City` column as it showed minimal contribution to risk prediction.
2.  **Data Cleaning:** * Handled missing values (`NaN`) in `Soil_Moisture_%` and `River_Level_m`.
    * Discarded records with missing `Rainfall_mm` data.
3.  **Encoding:** Applied **One-Hot Encoding** to the `Flood_Risk` variable to convert it into a numeric format suitable for ML algorithms.

## 🧠 Models Implemented
We trained and evaluated five distinct machine learning algorithms:

* **Random Forest (RF):** An ensemble of decision trees using bagging to reduce overfitting.
* **Decision Tree (DT):** A baseline classifier using top-down partitioning.
* **AdaBoost:** An ensemble boosting method that adjusts weights for misclassified samples.
* **K-Nearest Neighbors (KNN):** A non-parametric method classifying based on neighbor proximity.
* **Support Vector Machine (SVM):** A classifier that finds the optimal hyperplane to separate classes.

## 📊 Results & Performance
The models were evaluated on a 20% test set using **Accuracy** and **F1 Score**.

| Model | Accuracy | F1 Score | Notes |
| :--- | :--- | :--- | :--- |
| **AdaBoost** | **53.50%** | 34.0% | **Highest Accuracy** achieved in the study. |
| **KNN** | 51.25% | **51.0%** | **Best F1 Score**; balanced precision/recall. |
| **Random Forest**| 52.19% | 34.0% | Strong baseline but prone to class imbalance issues. |
| **SVM** | 50.21% | 50.0% | Struggled with class imbalance (predicted "No Flood" often). |
| **Decision Tree**| 48.96% | 26.4% | Lowest performance due to overfitting. |

### Key Findings
* **AdaBoost** proved to be the most accurate model overall.
* **KNN** and **SVM** provided better F1 scores, indicating they may be more reliable for datasets where the balance between identifying flood vs. non-flood events is critical.
* Class imbalance remains a challenge, suggesting future work could benefit from synthetic sampling techniques (e.g., SMOTE).

## 🚀 How to Run the Project
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/rfuadur/ML-Flood-Prediction-Disaster-Response.git](https://github.com/rfuadur/ML-Flood-Prediction-Disaster-Response.git)
    ```
2.  **Navigate to the directory:**
    ```bash
    cd ML-Flood-Prediction-Disaster-Response
    ```
3.  **Install necessary libraries:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```
4.  **Launch the Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    *Open the `.ipynb` file to view the training and testing process.*

## 📄 License
This project is open-source and available for educational and research purposes.
