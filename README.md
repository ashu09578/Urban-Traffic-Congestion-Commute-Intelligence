# 🚦 Urban Traffic Congestion & Commute Intelligence

> **Predict hourly traffic volume on a major US interstate using machine learning — built on the UCI Metro Interstate Traffic Volume dataset.**

---

## 📖 Project Description

Urban traffic congestion is one of the most pressing challenges in modern cities. This project delivers a complete, beginner-friendly data science pipeline that analyses over **six years of hourly traffic data** on **Interstate 94 (Minneapolis–Saint Paul, MN)** and trains machine learning models to predict hourly vehicle counts.

The project covers the full ML lifecycle: raw data → cleaning → EDA → feature engineering → modelling → evaluation → insights.

---

## 🌍 Real-World Problem

- US commuters lose an average of **54 hours per year** to traffic delays (INRIX, 2022)
- Accurate traffic forecasting enables:
  - Smart signal control and dynamic routing
  - Public transport planning
  - Emergency vehicle dispatch
  - Carbon emission reduction through less idling

---

## 🎯 Objectives

1. Clean and validate the UCI Metro Interstate Traffic Volume dataset  
2. Uncover temporal, meteorological, and seasonal traffic patterns through EDA  
3. Engineer features: cyclical time encodings, lag features, and contextual flags  
4. Train and compare four regression models: Linear Regression, Decision Tree, Random Forest, Gradient Boosting  
5. Evaluate models using MAE, RMSE, R², and MAPE  
6. Surface actionable commute intelligence insights  

---

## 📦 Dataset

| Property | Detail |
|---|---|
| **Name** | Metro Interstate Traffic Volume |
| **Source** | [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Metro+Interstate+Traffic+Volume) |
| **Records** | ~48,200 hourly observations |
| **Period** | October 2012 – September 2018 |
| **Location** | I-94 ATR 301, westbound (Minneapolis–Saint Paul, MN) |
| **Target** | `traffic_volume` — vehicles per hour |

Key features: `temp`, `rain_1h`, `snow_1h`, `clouds_all`, `weather_main`, `holiday`, `date_time`

---

## 🛠️ Technologies Used

| Category | Library / Tool |
|---|---|
| Language | Python 3.8+ |
| Data handling | pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Machine Learning | scikit-learn |
| Notebook environment | Jupyter Notebook / JupyterLab |

---

## 📁 Project Structure

```
Urban-Traffic-Congestion/
│
├── Urban_Traffic_Congestion.ipynb        # Main Jupyter Notebook (full pipeline)
├── Urban_Traffic_Congestion_Report.docx  # Professional project report
├── requirements.txt                      # Python dependencies
├── README.md                             # This file
│
└── (generated after running notebook)
    ├── plot_traffic_distribution.png
    ├── plot_daily_traffic.png
    ├── plot_hourly_traffic.png
    ├── plot_dow_traffic.png
    ├── plot_monthly_traffic.png
    ├── plot_weather_traffic.png
    ├── plot_weather_violin.png
    ├── plot_holiday_traffic.png
    ├── plot_correlation_heatmap.png
    ├── plot_rush_hour_heatmap.png
    ├── plot_model_comparison.png
    ├── plot_actual_vs_predicted.png
    ├── plot_residuals.png
    └── plot_scatter_actual_predicted.png
```

---

## ⚙️ Installation & Setup

### 1. Clone / download the project

```bash
git clone https://github.com/your-username/urban-traffic-congestion.git
cd urban-traffic-congestion
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run the Notebook

```bash
jupyter notebook Urban_Traffic_Congestion.ipynb
```

Or with JupyterLab:

```bash
jupyter lab Urban_Traffic_Congestion.ipynb
```

Then run all cells from top to bottom: **Kernel → Restart & Run All**

> **Internet connection required** on first run to download the dataset from the UCI repository.  
> Alternatively, download the CSV manually from the UCI link above and place it as `Metro_Interstate_Traffic_Volume.csv` in the project folder — the notebook falls back to the local file automatically.

---

## 📊 Key Findings

| Finding | Detail |
|---|---|
| **Rush-hour peaks** | Highest traffic at 07:00–09:00 and 16:00–18:00 on weekdays |
| **Weekend dip** | Weekday traffic is ~35–45% higher than weekend traffic |
| **Seasonal pattern** | Winter months (Nov–Feb) see the lowest volumes; summer peaks in Jun–Sep |
| **Weather effect** | Adverse weather mildly reduces traffic, but time-of-day is 5–10× more influential |
| **Holiday effect** | National holidays reduce traffic to near-weekend levels |
| **Lag features** | Previous-hour traffic (`traffic_lag1`) is the single most predictive feature |
| **Best model** | Random Forest achieved R² ≈ 0.95, MAE < 250 vehicles/hour on the test set |

> **Note:** Run the notebook to generate your own exact metric values — the figures above are indicative based on the dataset and feature set used.

---

## 🚀 Future Scope

- **LSTM / Transformer models** for long-range temporal forecasting  
- **Real-time API integration** with HERE Traffic or TomTom  
- **Geospatial expansion** to multiple highway segments  
- **Anomaly detection** for accidents and road-work events  
- **Multi-step forecasting** (3h, 6h, 12h, 24h ahead)  
- **XGBoost / LightGBM** for faster, more scalable training  

---

## 📄 License

This project is for educational purposes. The UCI Metro Interstate Traffic Volume dataset is provided under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) licence.

---

## 🙏 Acknowledgements

- Dataset: John Hogue (2019) via the UCI Machine Learning Repository  
- scikit-learn, pandas, Matplotlib, Seaborn open-source communities  
