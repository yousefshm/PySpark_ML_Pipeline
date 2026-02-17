# 🚗 PySpark End-to-End Fuel Consumption Pipeline

![Python](https://img.shields.io/badge/Python-3.7%2B-blue)
![PySpark](https://img.shields.io/badge/Apache%20Spark-PySpark-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📖 Project Overview
This project demonstrates the construction of a scalable **Machine Learning Pipeline** using **Apache Spark (PySpark)** to predict vehicle fuel efficiency (MPG). 

Unlike standard notebooks, this project focuses on **Data Engineering best practices**, including building a robust ETL process, automating feature engineering via a pipeline, and implementing model persistence for production deployment.

**Dataset Source:** [UCI Machine Learning Repository - Auto MPG Data Set](https://archive.ics.uci.edu/ml/datasets/auto+mpg)

---

## 🛠️ Key Features
* **Scalable ETL:** Ingests raw CSV data, cleans missing values, handles duplicates, and standardizes schema using Spark DataFrames.
* **Advanced Feature Engineering:**
    * **StringIndexer:** Handles categorical data (Origin).
    * **VectorAssembler:** Combines features into a single vector.
    * **StandardScaler:** Normalizes features to ensure model stability across different scales (e.g., Weight vs. Cylinders).
* **ML Pipeline Automation:** Wraps all transformation and modeling steps into a single `Pipeline` object, preventing data leakage and ensuring reproducibility.
* **Model Persistence:** Saves the trained pipeline to disk (`fuel_consumption_model`) for future inference without retraining.

---

## 📊 Model Performance
The Linear Regression model was trained on 70% of the data and evaluated on 30% unseen test data.

| Metric | Value | Description |
| :--- | :--- | :--- |
| **R-Squared ($R^2$)** | **0.79** | The model explains 79% of the variance in fuel consumption. |
| **RMSE** | **3.39** | On average, predictions deviate by ~3.39 MPG from actual values. |

---

## 📂 Project Structure

├── data/
│   └── mpg-raw.csv              # Raw dataset
├── output/
│   └── mpg-cleaned.parquet      # Processed data (Parquet format)
├── fuel_consumption_model/      # Saved Pipeline Model artifacts
├── ML_Pipeline_Project.ipynb    # Main Jupyter Notebook
└── README.md                    # Project Documentation

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/PySpark-Fuel-Efficiency-Pipeline.git](https://github.com/YourUsername/PySpark-Fuel-Efficiency-Pipeline.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install pyspark findspark pandas matplotlib
    ```
3.  **Run the Notebook:**
    Launch Jupyter Notebook and execute `ML_Pipeline_Project.ipynb`.

---

## 👨‍💻 Author
**Yousef Almotawea** Data Engineer | IBM Certified | CDMP
[https://www.linkedin.com/in/yousef-almotawea-cdmp%C2%AE-730003238/]

---

## 📜 Acknowledgements
This project is based on a guided lab from the **IBM Data Engineering Professional Certificate**. I have significantly refactored the code to follow industry standards, including modular pipeline construction, added visualizations, and model persistence capabilities.
