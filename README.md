# 💧 Water Resource Monitoring & Prediction

This project uses a combination of **remote sensing data (NDWI)** and **climate data (Rainfall, Temperature)** to monitor and predict water conditions in a specific region of **Jharkhand, India** using **LSTM, Prophet**, and **rule-based classification**.

---

## 🚀 Project Objectives

- Analyze historical NDWI, Rainfall, and Temperature data (2010–2024)
- Forecast:
  - NDWI using LSTM
  - Rainfall & Temperature using Prophet
- Classify upcoming water conditions (Flood, Drought, Normal)
- Enable user-driven forecasting (by year/month input)
- Visualize water condition trends over time

---

## 🗺️ Study Region

- **Location**: Jharkhand, India (near Ranchi or Hazaribagh)
- **Coordinates**: Longitude `85.324`, Latitude `23.344`
- **Area**: Circular buffer of 5 km radius

---

## 📊 Datasets Used

| Dataset Type | Source | Duration |
|--------------|--------|----------|
| NDWI (Monthly Average) | CSV Format | Jan 2010 – Dec 2024 |
| Rainfall (mm) | CSV Format | Jan 2010 – Jan 2024 |
| Temperature (Tmax & Tmin in °C) | CSV Format | Jan 2010 – Jan 2024 |

---

## ⚙️ Technologies

- Python (Google Colab)
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `keras`, `prophet`
- Models:
  - **LSTM** for NDWI time-series forecasting
  - **Prophet** for Rainfall & Temperature forecasting
  - Rule-based logic for **Flood/Drought/Normal** classification

---

## 🧪 Methodology

1. **Data Preprocessing**  
   - Clean & merge NDWI and climate data  
   - Handle missing values, normalize inputs

2. **Exploratory Data Analysis (EDA)**  
   - Time series plots  
   - Histograms, KDE plots, Boxplots  
   - Heatmaps (correlation)

3. **Forecasting**
   - `LSTM` for NDWI (Monthly)
   - `Prophet` for Rainfall, Tmax, Tmin (Monthly)

4. **Classification Logic**  
   Based on NDWI & Rainfall thresholds:
if NDWI < -0.15 and Rainfall < 50 mm → Drought
if NDWI > -0.17 and Rainfall > 200 mm → Flood
else → Normal



5. **Future Prediction Interface**  
- User enters number of months (e.g., 20)  
- Model displays future predictions with water condition labels

---

## 📈 Example Output

Date | NDWI | Rainfall(mm) | Condition
2024-12-01 | -0.16 | 4.4 | Drought
2025-01-01 | -0.16 | 20.1 | Drought
2025-06-01 | -0.16 | 201.4 | Flood
2025-08-01 | -0.16 | 358.9 | Flood


## 📌 Features

- 📅 Interactive user input (months/year)
- 📉 Forecasts extend beyond 2024
- 📊 Visualizations for predicted conditions
- ✅ Highly accurate time series predictions using deep learning & Prophet


## ✅ Conclusion

This project demonstrates a powerful integration of **satellite data**, **machine learning**, and **climate forecasting** to enable **early flood/drought detection** in water-vulnerable regions like Jharkhand.



## 🤝 Contributing

Open for contributions:
- Better classification models
- Deployment as a web dashboard
- Geo-visualization integrations

---

## 📬 Contact

**Author:** Subhadra Bhattacharyya  
📧 Email: subhadrabhattacharyya7@gmail.com
🌐 Location: India  
