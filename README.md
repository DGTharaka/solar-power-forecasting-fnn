# ☀️ Hourly Solar PV Power Forecasting using Feedforward Neural Networks (FNN)

This project implements a **Feedforward Neural Network (FNN)** for accurate **hour-ahead solar PV power forecasting** using advanced time-series feature engineering.

---

## 📌 Objective

- Predict next-hour solar PV power output
- Capture temporal patterns using engineered features
- Provide a fast and reliable forecasting model for grid operation and energy management

---

## 🧠 Key Techniques

### Temporal Feature Engineering
- Hour, day, month, day-of-week  
- Cyclical encoding using sine & cosine transforms  
- Solar position half-sine curve (daylight behavior)

### Historical Memory Features
- Lag values (up to 72 hours)
- Rolling statistics (mean, min, max, median, std)
- Exponential Moving Averages (EMA)

---

## 🏗️ Model Architecture

Feedforward Neural Network with:

| Layer | Neurons | Dropout |
|------|--------|---------|
| Dense 1 | 1024 | 0.30 |
| Dense 2 | 512 | 0.25 |
| Dense 3 | 256 | 0.20 |
| Dense 4 | 128 | 0.15 |
| Dense 5 | 64  | 0.10 |
| Dense 6 | 32  | 0.05 |
| Output | 1 | — |

**Activation:** Swish  
**Loss:** Huber  
**Optimizer:** Adam  
**Residual skip connection** for improved training stability

---

## 📊 Evaluation Metrics

- R² Score  
- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)  
- Mean Squared Error (MSE)  

Performance achieved:
- **R² > 0.99**
- **Normalized error < 5%**

---

