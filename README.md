# 🌦️ Rain Prediction in Australia — Deep Learning Models Comparison

This project aims to predict **whether it will rain tomorrow in Australia** using advanced **deep learning techniques**.  
The dataset contains 10 years of daily weather observations from the **Australian Bureau of Meteorology**, available on [Kaggle](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package).

The study compares the performance of four neural network architectures — **MLP, 1D-CNN, LSTM**, and **TabTransformer** — to identify the most effective model for short-term rainfall prediction.

---

## 📘 Project Overview

Rain prediction is a critical task in meteorology that affects agriculture, disaster management, and daily life.  
This project uses historical weather data to predict the binary variable `RainTomorrow` (`Yes` or `No`), indicating whether rainfall exceeding 1mm will occur on the next day.

---

## 🧠 Models Implemented

| Model | Description | Key Strength |
|--------|--------------|---------------|
| **MLP (Multi-Layer Perceptron)** | Baseline feedforward network using fully connected layers. | Captures nonlinear relationships. |
| **1D-CNN (Convolutional Neural Network)** | Learns local feature interactions across input variables. | Efficient and less prone to overfitting. |
| **LSTM (Long Short-Term Memory)** | Sequence-based model capturing temporal dependencies in weather data. | Ideal for time-series patterns. |
| **TabTransformer** | Attention-based model using embeddings and transformer encoder blocks. | Handles categorical-numerical mix effectively. |

Each model was trained independently using the same preprocessed dataset and compared on key performance metrics such as **Accuracy, Precision, Recall, F1-score,** and **AUC**.

---

## 📊 Dataset Information

**Dataset:** [Rain in Australia - Kaggle](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package)  
**Records:** ~145,460  
**Features:** 23 meteorological variables  
**Time Period:** 2007–2017  
**Target Variable:** `RainTomorrow` (Yes/No)  
**Imbalance:** Only ~22% of samples are “Yes” → handled using **Random Oversampling**.

---

## 🧹 Data Preprocessing and Feature Engineering

The preprocessing pipeline included:
- **Balance the dataset:** Oversample the minority class
- **Missing value handling:** Median for numeric, “Missing” placeholder for categorical.  
- **Outlier removal:** IQR-based filtering to eliminate extreme values.  
- **Feature scaling:** Standardization using `StandardScaler`.  
- **Encoding:** One-Hot Encoding for MLP/CNN/LSTM, Label Encoding for TabTransformer.  
- **Temporal feature extraction:** Derived `Month`, `DayOfWeek`, and `Season` from `Date`.  
- **Correlation filtering:** Removed features with correlation > 0.9 to avoid redundancy.  
- **Class imbalance correction:** Balanced classes via oversampling.

---

## ⚙️ Model Training Workflow

1. Load and clean dataset  
2. Perform feature engineering and scaling  
3. Train 4 separate models  
4. Evaluate using Accuracy, Precision, Recall, F1-score, AUC  
5. Compare performance and visualize results  

---

## 🧩 Evaluation Metrics

- **Accuracy**  
- **Precision**  
- **Recall (Sensitivity)**  
- **F1-score**  
- **ROC-AUC**  
- **Confusion Matrix**

These metrics ensure fair comparison across models, especially considering dataset imbalance.

---

## 🖼️ Visualizations

Include the following visualizations in the `notebooks/` or `results/` folder:
- Class distribution before and after balancing  
- Feature correlation heatmap  
- Feature importance or SHAP values (optional)  
- Model performance comparison bar charts  

---

## 🚀 How to Run

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/Rain-Prediction-Australia.git
cd Rain-Prediction-Australia
```
### 2️⃣ Clone the repository
```bash
pip install -r requirements.txt
```
### 3️⃣ Run the 4 model files seperately
```bash
#example
python tab_transformer.py
```
---

## 📈 Results Summary

| Model          | Accuracy | Precision | Recall   | F1-Score | Key Obeservations      |
| -------------- | -------- | --------- | -------- | -------- | -------- |
| MLP            | 81.95%     | 56.81%      | 81.35%     | 66.90%     | Strong baseline, High recall, Low precision.     |
| 1D-CNN         | 82.58%     | 82.34%      | 82.97%     | 82.67%     | Best balance     |
| LSTM           | 76.62%     | 78.82%      | 82.13%     | 77.71%     | Learn pattern across sequential data     |
| TabTransformer | 84.55% | 76.26%  | 81.87% | 78.96% | Effectively captures interactions between numeric and categorical weather features |

---

## Members

- IT22111906 - Marambe R.T
- IT22122414 - Sembukuttiarachchi J.S
- IT22112514 - Fernando M.L.A
- IT22105134 - D.P.S Ranasinghe
