# 🚨 911 Emergency Calls — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=flat&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-9cf?style=flat)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)

An end-to-end exploratory data analysis of **99,492 real 911 emergency calls** from Montgomery County, Pennsylvania. This project was built as a data science capstone and extended with deeper EDA to uncover patterns in emergency response data.

---

## 📊 Project Overview

This notebook explores when, where, and why people call 911 — uncovering time patterns, geographic hotspots, seasonal trends, and anomaly spikes hidden in the data.

**Dataset:** [Montgomery County 911 Calls — Kaggle](https://www.kaggle.com/mchirico/montcoalert)  
**Records:** 99,492 emergency calls  
**Time Period:** 2015 – 2020  
**Location:** Montgomery County, PA, USA

---

## 🔍 What's Inside

### Part 1 — Capstone (Guided Analysis)
| Topic | Description |
|-------|-------------|
| Data Setup | Load, inspect, and understand the dataset |
| Basic Questions | Top ZIP codes, townships, and unique call titles |
| Feature Engineering | Extract `Reason`, `Hour`, `Month`, `Day of Week` from raw columns |
| Time Series | Daily call volume trends split by EMS / Fire / Traffic |
| Heatmaps | Call frequency by Hour×Day and Month×Day using Seaborn |

### Part 2 — Extended EDA (Deep Dive)
| Topic | Description |
|-------|-------------|
| Data Quality | Missing value audit across all columns |
| Top Sub-Types | Most common specific emergencies per department (EMS / Fire / Traffic) |
| Hour of Day | 24-hr call rhythm with annotated peak hour |
| Day of Week | Weekday vs weekend breakdown by reason |
| Seasonal Patterns | Winter / Spring / Summer / Fall call distribution |
| Anomaly Detection | Spike days identified using 2σ threshold above daily mean |
| Geographic Hotspots | Hexbin density maps using lat/lng — one per reason |
| Peak Hour Heatmaps | EMS sub-types × hour and Traffic sub-types × day |
| Key Insights | Summary table of 7 major findings |

---

## 📸 Sample Visualizations

> Run the notebook to generate all plots. Key visuals include:
> - 📈 Daily call volume time series with spike annotations
> - 🗺️ Geographic density maps (EMS / Fire / Traffic)
> - 🔥 Heatmaps of call frequency by hour, day, and month
> - 📊 Grouped bars comparing call volume across seasons and days

---

## 🧰 Tech Stack

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, feature engineering |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualizations and heatmaps |

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/BestBow/911-calls-eda.git
cd 911-calls-eda
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Download the dataset
Get `911.csv` from [Kaggle](https://www.kaggle.com/mchirico/montcoalert) and place it in the root folder.

### 4. Run the notebook
```bash
jupyter notebook 911_Calls_Extended_EDA.ipynb
```

---

## 💡 Key Findings

1. **EMS dominates** — nearly 49% of all 911 calls, led by vehicle accidents and cardiac emergencies
2. **Rush hour is the most dangerous time** — call volume peaks at 4–5 PM across all reasons
3. **Weekdays are busier** — Traffic and EMS drop on weekends; Fire holds steady
4. **Winter drives more calls** — January spikes likely from weather-related accidents and heating emergencies
5. **Anomaly spikes are detectable** — certain dates see >2σ surges, likely tied to major weather events
6. **Geography is concentrated** — emergency density clusters around the Lower Merion and Norristown corridors
7. **2–5 AM is the quietest window** — consistent across all reasons and all days of the week

---

## 📁 Project Structure

```
911-calls-eda/
│
├── 911_Calls_Extended_EDA.ipynb   # Main notebook
├── 911.csv                        # Dataset (download from Kaggle)
└── README.md                      # This file
```

---

## 📄 License

This project is open source under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- Dataset provided by [Mike Chirico](https://www.kaggle.com/mchirico) on Kaggle
- Capstone project structure from [Pierian Data](https://github.com/Pierian-Data/Python-for-Data-Science-and-Machine-Learning-Bootcamp)
