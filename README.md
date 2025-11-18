# ⚙️ Machine Predictive Maintenance Classification

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

An end-to-end machine learning application designed to predict industrial machine failures before they occur. Utilizing a **Random Forest Classifier**, this tool analyzes sensor data (temperature, torque, rotational speed) to classify equipment status, enabling proactive predictive maintenance strategies.



## 🔗 Quick Links
* **📓 Google Colab Notebook:** [View Code & Analysis](https://colab.research.google.com/)
* **📂 Kaggle Dataset:** [View Dataset Source](https://www.kaggle.com/) 

## 📊 Project Overview
Predictive maintenance is a critical technique in modern industry to reduce downtime and maintenance costs. This project leverages a synthetic dataset of **10,000 data points** to simulate real-world sensor readings.

**Key Capabilities:**
* **Real-time Classification:** Predicts "Failure" or "No Failure" instantly based on user inputs.
* **Interactive Interface:** Built with Streamlit for easy parameter adjustment.
* **Robust Modeling:** Uses Random Forest to handle complex interactions between features like Tool Wear and Torque.


## 🗂️ Dataset Description
The dataset consists of **10,000 rows** and **14 features**, reflecting real predictive maintenance scenarios.

| Feature | Description |
| :--- | :--- |
| **UID** | Unique identifier (1 to 10,000). |
| **ProductID** | Quality variant (L/M/H) with a serial number. |
| **Air Temperature [K]** | Normalized to standard deviation of 2K around 300K. |
| **Process Temperature [K]** | Normalized to std dev of 1K, added to Air Temp + 10K. |
| **Rotational Speed [rpm]** | Calculated from 2860W power with noise. |
| **Torque [Nm]** | Distributed around 40 Nm (No negative values). |
| **Tool Wear [min]** | Quality variants H/M/L add 5/3/2 mins of wear. |
| **Machine Failure** | Target Label (0 = No Failure, 1 = Failure). |

> **⚠️ Important Note:** The dataset contains two targets. Care was taken during training to avoid **data leakage** by excluding the secondary target variable from the feature set.



## 🧠 Model Details
* **Algorithm:** Random Forest Classifier.
* **Reasoning:** Chosen for its ability to handle both numerical and categorical data, prevent overfitting through ensemble learning, and capture non-linear relationships between sensor readings.
* **Training:** Trained on a synthetic dataset mirroring real industrial physics.



## 🛠️ Installation & Usage

### Prerequisites
Ensure you have **Python 3.x** installed.

