
# 🌡️ Air Temperature Forecasting using Deep Learning and Statistical Models

## 🏆 Overview
This project aims to accurately forecast air temperature using a combination of classical statistical methods and modern deep learning architectures. The models were evaluated based on metrics like MAE, RMSE, and MAPE to identify the most effective approach.

---

## 📂 Dataset
- Historical air temperature data with associated timestamps
- Preprocessed to handle missing values, format inconsistencies, and time-series structure

---

## 🔍 Data Preprocessing
- ❌ Removed missing values
- ⏰ Converted timestamp column to datetime index
- 📉 Scaled features using `MinMaxScaler` to normalize the range
- 📈 Converted series into supervised format using time lags
- 🧪 Train-test split with sequence windows

---

## ⚙️ Models Implemented

### 📈 Classical Time Series Models
- **ARIMAX**
- **SARIMAX**

### 🤖 Deep Learning Models
- **LSTM (Long Short-Term Memory)**
- **GRU (Gated Recurrent Units)**
- **N-BEATS (Neural Basis Expansion)**

---

## 📊 Model Performance Summary

| **Model**   | **MAE ↓** | **RMSE ↓** | **MAPE ↓** | **Comments**                            |
|-------------|-----------|------------|------------|-----------------------------------------|
| **LSTM**    | 0.0925    | 0.1174     | —          | ✅ Best performer overall                |
| **GRU**     | 0.0949    | 0.1184     | —          | Close to LSTM, slightly behind          |
| **N-BEATS** | 0.455     | 0.514      | 1.60%      | Visually smooth, weaker metrics         |
| **SARIMAX** | 0.5135    | 0.6412     | —          | Outperformed ARIMAX                     |
| **ARIMAX**  | 0.671     | 0.8123     | —          | ❌ Worst performance                     |

---

## 🛠 Tech Stack

- **Python**
- **Pandas**, **NumPy** for data manipulation
- **Matplotlib**, **Seaborn** for visualizations
- **TensorFlow / Keras** for LSTM, GRU, N-BEATS
- **statsmodels** for ARIMAX, SARIMAX
- **sklearn** for preprocessing and evaluation metrics

---

## 📉 Visualizations

- Training vs Validation Loss Curves  
- Time Series Predictions vs Actuals  
- Residual Analysis  
- Autocorrelation and Partial Autocorrelation Plots  
- Confusion Matrix (for classification framing, if applied)  

---

## ✅ Key Takeaways

- Deep learning models (especially LSTM) outperform statistical baselines for this dataset.
- Proper data scaling and sequence preparation are critical for deep learning success.
- N-BEATS offered smooth predictions but didn’t beat LSTM/GRU on MAE/RMSE.

---

## 🚀 Future Work

- Hyperparameter tuning using Bayesian or grid search
- Explore attention-based models like **Transformer for Time Series**
- Try hybrid models combining SARIMA + LSTM
- Deploy model using Flask or Streamlit dashboard for live forecasting

---

## 📝 License
This project is licensed under the MIT License.

---

## 🙌 Credits

- [TensorFlow](https://www.tensorflow.org/)
- [Keras](https://keras.io/)
- [Statsmodels](https://www.statsmodels.org/)
- [N-BEATS Paper](https://arxiv.org/abs/1905.10437)
- Open-source time series datasets

