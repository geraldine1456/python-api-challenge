# python-api-challenge

## 📊 Overview

This project leverages the power of APIs to explore how weather changes with latitude. Using Python, Jupyter Notebook, and data from the OpenWeatherMap and Geoapify APIs, the analysis answers a fundamental data science question:

> ❓ *What is the weather like as we approach the equator?*

The project is broken into two parts:
- **Part 1: WeatherPy** – Visualizing weather conditions across 600+ cities.
- **Part 2: VacationPy** – Finding ideal vacation spots based on user-defined weather criteria.

---

## 🧰 Technologies Used

- Python (Pandas, Matplotlib, Requests, JSON, SciPy)
- Jupyter Notebook
- OpenWeatherMap API
- Geoapify API
- Citipy (for generating nearest cities by coordinates)
- Git & GitHub for version control
---


## 🌍 Part 1: WeatherPy

WeatherPy pulls current weather data for over 500 cities worldwide using OpenWeatherMap’s API. The analysis focuses on the relationship between **latitude** and key weather metrics.

### 🔍 Key Analyses:
- Latitude vs. **Max Temperature**
- Latitude vs. **Humidity**
- Latitude vs. **Cloudiness**
- Latitude vs. **Wind Speed**

Each variable is further split and analyzed across:
- **Northern Hemisphere (Latitude ≥ 0)**
- **Southern Hemisphere (Latitude < 0)**

### 📈 Linear Regression Plots

Using SciPy’s `linregress`, regression lines and R² values are included to quantify relationships. For example, temperature shows a **strong correlation** with latitude — confirming that it gets hotter closer to the equator.

---

## 🏖️ Part 2: VacationPy

In this section, ideal vacation destinations are identified based on specific weather criteria. Cities are filtered using the following example conditions:

- Max Temperature: **21°C – 27°C**
- Wind Speed: **< 4.5 m/s**
- Cloudiness: **0%**

Once filtered, the **Geoapify API** is used to locate the **nearest hotel** to each city. These destinations are visualized on an interactive **humidity-based map**, with hover labels showing city, country, and hotel name.

---

## 📂 Repository Structure

```

python-api-challenge
│
├── WeatherPy/
│   ├── WeatherPy.ipynb         # Main analysis notebook
│   ├── VacationPy.ipynb        # Vacation filtering & map visualization
│   ├── output\_data.csv        # Saved city weather data and scatter plot figures
│   ├──api\_keys.py             # Contains API keys (ignored via .gitignore)
|
├── .gitignore                  # Ensures sensitive files aren't pushed
└── README.md                   # Project summary

```

## ✅ Summary

This project demonstrates how to:
- Collect real-time data using APIs
- Clean and analyze geographic weather data
- Visualize trends and patterns using plots and regression
- Integrate multiple APIs (OpenWeatherMap + Geoapify)
- Make data-driven decisions for travel planning

---

