# ⚡ EV Charge & Vehicle Demand Prediction 🚗🔋

A Machine Learning project focused on predicting Electric Vehicle (EV) charging demand and vehicle usage trends using historical and environmental data. This prediction helps optimize charging infrastructure, energy consumption, and city planning for EV-friendly environments.

![EV](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-blue)
![Python](https://img.shields.io/badge/Python-3.10%2B-yellow)
![License](https://img.shields.io/github/license/rishu12-xyz/EV-Charge-Vehicle-Demand-Prediction)

---

## 📌 Table of Contents

- [🔍 Project Overview](#-project-overview)
- [📂 Project Structure](#-project-structure)
- [🔧 Installation](#-installation)
- [📊 Dataset Description](#-dataset-description)
- [🧠 Model Training](#-model-training)
- [📈 Results and Evaluation](#-results-and-evaluation)
- [🖥️ Streamlit Web App](#️-streamlit-web-app)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🔍 Project Overview

This project aims to forecast the **charging demand and vehicle count** at electric charging stations using regression and time-series models. By analyzing usage patterns, time of day, temperature, and other environmental factors, the project predicts:
- Number of EVs likely to arrive at a station
- Total expected energy demand

✅ **Use Cases**:
- Optimizing energy distribution
- Reducing grid stress
- Improving public EV infrastructure

---

## 📂 Project Structure

```bash
EV-Charge-Vehicle-Demand-Prediction/
│
├── 📁 data/                 # Raw and cleaned dataset files
├── 📁 models/               # Trained model files (.pkl)
├── 📁 notebooks/            # Jupyter notebooks for EDA, training
├── 📁 app/                  # Streamlit app and frontend
│   └── app.py              # Main Streamlit script
│
├── model_training.py        # Model training script
├── demand_predictor.py      # Reusable prediction functions
├── requirements.txt         # Required Python packages
└── README.md                # You're reading it now
```

---

## 🔧 Installation

1. **Clone the repository**

```bash
git clone https://github.com/rishu12-xyz/EV-Charge-Vehicle-Demand-Prediction.git
cd EV-Charge-Vehicle-Demand-Prediction
```

2. **Create a virtual environment (optional)**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

---

## 📊 Dataset Description

The dataset includes:

| Feature              | Description                                 |
|----------------------|---------------------------------------------|
| `Timestamp`          | Date and time of data entry                 |
| `Temperature`        | Ambient temperature at that time            |
| `Humidity`           | Relative humidity                          |
| `EV_Charging_Count`  | Number of EVs connected to charging         |
| `Total_kWh`          | Energy consumed by chargers (in kWh)        |
| `Day_of_Week`        | Weekday encoded (0=Monday, ..., 6=Sunday)   |
| `Hour_of_Day`        | Hour of the day (0–23)                      |

📁 Sample datasets available in `data/` folder.

---

## 🧠 Model Training

Models used:
- **Linear Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **ARIMA (for Time Series forecast)**

Training is done using `model_training.py`. To retrain the model:

```bash
python model_training.py
```

It will output:
- Trained `.pkl` model file
- Evaluation metrics (R², MAE, RMSE)
- Feature importance graphs

---

## 📈 Results and Evaluation

✅ Best Performing Model: **XGBoost Regressor**

| Metric         | Value     |
|----------------|-----------|
| R² Score       | 0.92      |
| MAE            | 3.1       |
| RMSE           | 4.8       |

📉 Residual plots and feature importance visualizations are available in `notebooks/`.

---

## 🖥️ Streamlit Web App

The project includes an interactive web application built with **Streamlit**.

### 🚀 To Run the App:

```bash
cd app
streamlit run app.py
```

The app allows:
- Input of custom values (temperature, time, etc.)
- Real-time prediction of EV charging demand
- Display of visual trends and stats

---

## 🤝 Contributing

Contributions are welcome! Here's how:
- ⭐ Star this repo
- Fork and clone
- Create a new branch: `git checkout -b feature-name`
- Commit your changes
- Push to your branch: `git push origin feature-name`
- Submit a Pull Request (PR)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 📫 Contact

**Rishikesh Pandit**  
📧 rtechist@gamil.com 
🔗 [LinkedIn](https://www.linkedin.com/in/rishikesh-pandit/) | [GitHub](https://github.com/rishu12-xyz)

---

> *“Powering the future, one prediction at a time.”*
