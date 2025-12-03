# ML-Flood-Prediction-Disaster-Response
A comparative study of machine learning models (Random Forest, AdaBoost, KNN, SVM, Decision Tree) to predict flood risks and evacuation requirements using meteorological and hydrological data. Achieved 53.5% accuracy with AdaBoost and 51% F1-score with KNN.
# Machine Learning-Based Flood Prediction for Disaster Preparedness

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Libraries](https://img.shields.io/badge/Libraries-Scikit--Learn%20%7C%20Pandas%20%7C%20NumPy-orange)

## 📌 Project Overview
Floods are among the deadliest natural disasters, threatening infrastructure and human lives. [cite_start]This project leverages Machine Learning (ML) to enhance disaster preparedness by predicting flood events[cite: 7]. [cite_start]By analyzing meteorological and hydrological data, this system aims to provide timely alerts to mitigate risks and improve community resilience[cite: 11].

## 📂 Dataset
[cite_start]The dataset originally contained **5,050 records** with the following features[cite: 48]:
* **Rainfall_mm**: Amount of rainfall.
* **River_Level_m**: Water level of the river.
* **Soil_Moisture_%**: Percentage of moisture in the soil.
* **City**: Location data (Removed during preprocessing).
* **Flood_Risk**: Categorical risk level (Target Variable 1).
* **Evacuation_Required**: Binary requirement for evacuation (Target Variable 2).

## ⚙️ Data Preprocessing
To prepare the data for training, the following steps were taken:
1.  [cite_start]**Feature Selection**: The `City` column was removed as it contributed minimally to flood risk prediction[cite: 49].
2.  [cite_start]**Handling Missing Values**: Rows with missing values in `Rainfall_mm`, `River_Level_m`, and `Soil_Moisture_%` were removed[cite: 50, 51].
3.  [cite_start]**Encoding**: One-Hot Encoding was applied to the `Flood_Risk` variable to convert categorical data into a numeric format[cite: 52].
4.  [cite_start]**Final Shape**: The cleaned dataset used for training comprised **4,800 records** and **7 features**[cite: 53].

## 🧠 Models Implemented
[cite_start]We evaluated five different machine learning algorithms to find the optimal model for this specific task[cite: 57]:

1.  [cite_start]**Random Forest**: An ensemble method using bootstrapped subsets to reduce overfitting[cite: 58].
2.  [cite_start]**Decision Tree**: A top-down partitioning strategy[cite: 62].
3.  [cite_start]**AdaBoost (Adaptive Boosting)**: Iteratively adjusts weights of misclassified samples to reduce bias and variance[cite: 65].
4.  [cite_start]**K-Nearest Neighbors (KNN)**: Classifies data points based on the majority vote of their neighbors[cite: 67].
5.  [cite_start]**Support Vector Machine (SVM)**: Finds the optimal hyperplane to separate classes[cite: 70].

## 📊 Results & Analysis
[cite_start]The models were evaluated using **Accuracy** and **F1 Score** on a 20% test set[cite: 75, 76].

| Model | Accuracy (%) | F1 Score (%) | Key Observation |
| :--- | :--- | :--- | :--- |
| **AdaBoost** | **53.5%** | 34.0% | [cite_start]Highest Accuracy achieved[cite: 92, 111]. |
| **KNN** | 51.25% | **51.0%** | [cite_start]Best balance between precision and recall (Best F1 Score)[cite: 92, 111]. |
| **Random Forest** | 52.19% | 34.0% | [cite_start]Strong baseline performance but required tuning[cite: 86]. |
| **SVM** | 50.21% | 50.0% | [cite_start]Struggled with class imbalance (predicted "No Flood" for all cases)[cite: 105]. |
| **Decision Tree** | 48.96% | 26.4% | [cite_start]Prone to overfitting[cite: 79]. |

### Conclusion
[cite_start]While **AdaBoost** achieved the highest overall accuracy, **KNN** demonstrated the most balanced performance (F1 Score) for identifying positive flood risks[cite: 111]. The project highlights the challenge of class imbalance in real-world disaster datasets.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/ML-Flood-Prediction.git](https://github.com/your-username/ML-Flood-Prediction.git)
