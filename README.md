# **🌦️ AI-weather-forecast**

## **🚀 Project Overview**

Accurate weather forecasting is essential for agriculture, disaster management, and daily planning.

**Features include:**

- Temperature
- Humidity
- Wind Speed
- Rainfall
- Pressure

---

## **👥 Members**

- IT22111906 - Marambe R.T
- IT22122414 - Sembukuttiarachchi J.S
- IT22112514 - Fernando M.L.A
- IT22105134 - D.P.S Ranasinghe

---

## **📂 Project Structure**

```
AI-weather-forecast/
│
├── 1D_CNN.ipynb # CNN-based model for weather forecasting
├── Tab_Transformer.ipynb # Transformer-based model
├── Dataset_balancing.ipynb # Balances dataset using oversampling
├── weatherAUS 2.csv # Original dataset
├── weatherAUS_updated.csv # Balanced dataset
└── README.md # Project documentation
```

---

## **⚙️ Setup Instructions**

### 1. **Clone the repository**

```bash
git clone https://github.com/your-username/AI-weather-forecast.git
cd AI-weather-forecast
```

---

### 2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate #for linux/mac
venv\Scripts\activate #for windows
```

---

### 3. **Install dependencies**

```bash
pip install -r requirements.txt
```

or

```bash
pip install pandas numpy scikit-learn matplotlib tensorflow torch
```

---

## **📊 Dataset Information**

- Source: WeatherAUS dataset
- Features include:
  Temperature, Humidity, Wind Speed, Rainfall, and Pressure
- Balanced version: weatherAUS_updated.csv

---

## **🧩 Models Implemented**

| Model          | Description                                             |
| :------------- | :------------------------------------------------------ |
| 1D CNN         | Extracts temporal patterns in sequential weather data   |
| TabTransformer | Uses attention mechanisms for tabular data prediction   |
| Oversampling   | Balances dataset to improve model fairness and accuracy |

---

## **🧠 How to Run the Notebooks**

1. Open the .ipynb files in Google Colab or Jupyter Notebook.

2. Upload the dataset files (weatherAUS 2.csv or weatherAUS_updated.csv).

3. Run all cells in sequence to train and evaluate the models.

4. View accuracy, confusion matrix, and prediction visualizations.

---

## **📜 License**

This project is licensed under the MIT License — feel free to use and modify it for your learning or research purposes.

---
