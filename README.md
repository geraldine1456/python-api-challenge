# 📊 Python API Challenge

## 📌 Overview

This project leverages the power of APIs to explore how weather changes with latitude. Using Python, Jupyter Notebook, and data from the OpenWeatherMap and Geoapify APIs, the analysis addresses a fundamental data science question:

> ❓ *What is the weather like as we approach the equator?*

The project is broken into two parts:

- **Part 1: WeatherPy** – Visualizing weather conditions across 600+ cities.
- **Part 2: VacationPy** – Finding ideal vacation spots based on user-defined weather criteria.

---

## 🌍 Part 1: WeatherPy

WeatherPy pulls current weather data for over 600 cities worldwide using OpenWeatherMap’s API. The analysis focuses on the relationship between **latitude** and key weather metrics.

### 🔍 Key Analyses

- Latitude vs. **Max Temperature**
- Latitude vs. **Humidity**
- Latitude vs. **Cloudiness**
- Latitude vs. **Wind Speed**

Each variable is further analyzed by:

- **Northern Hemisphere (Latitude ≥ 0)**
- **Southern Hemisphere (Latitude < 0)**

### 📈 Linear Regression Plots

Using SciPy’s `linregress`, regression lines and R² values are included to quantify relationships. For example, temperature shows a **strong correlation** with latitude — confirming that it gets hotter closer to the equator.

---

## 🏖️ Part 2: VacationPy

In this section, ideal vacation destinations are identified based on specific weather criteria. Cities are filtered using the following conditions:

- Max Temperature: **20°C – 28°C**
- Wind Speed: **< 4.5 m/s**
- Cloudiness: **0%**

Once filtered, the **Geoapify API** is used to locate the **nearest hotel** to each city. These destinations are visualized on an interactive **humidity-based map**, with hover labels showing city, country, and hotel name.

---

## 📂 Repository Structure

```
python-api-challenge/
│
├── WeatherPy/
│   ├── WeatherPy.ipynb         # Weather data collection and analysis
│   ├── VacationPy.ipynb        # Vacation filtering & map visualization
|   ├── output\_data/           # Saved city weather data, Scatter plots figures      
|   ├── api\_keys.py            # Contains API keys (ignored via .gitignore)
|
├── .gitignore                  # Ensures sensitive files aren't pushed
└── README.md                   # Project summary and instructions

```

---

## 🧰 Technologies Used

- **Python**  
  Libraries: `pandas`, `matplotlib`, `requests`, `json`, `scipy`
- **Jupyter Notebook**
- **OpenWeatherMap API**
- **Geoapify API**
- **Citipy** – for finding the nearest city to given coordinates
- **Git & GitHub** – for version control

---

## ⚙️ How to Use

### 1. **Clone the Repository**

```bash
git clone https://github.com/geraldine1456/python-api-challenge.git
cd python-api-challenge
```

### 2. **Install Required Libraries**

```bash
pip install pandas matplotlib requests scipy jupyter
```

### 3. **Get Your API Keys**

* **OpenWeatherMap API**: [Sign up here](https://openweathermap.org/api)
* **Geoapify API**: [Sign up here](https://www.geoapify.com/)

### 4. **Create `api_keys.py` File**

In the root of the project, create a file named `api_keys.py` and add:

```python
weather_api_key = "your_openweathermap_api_key"
geoapify_key = "your_geoapify_api_key"
```

> ✅ Make sure `api_keys.py` is listed in `.gitignore` to keep your keys secure.

### 5. **Launch Jupyter Notebook**

```bash
jupyter notebook
```

Navigate to the appropriate folder and open:

* `WeatherPy/WeatherPy.ipynb` to run the weather analysis
* `VacationPy/VacationPy.ipynb` to find ideal vacation spots

---

## ✅ Summary

This project demonstrates how to:

* Collect real-time weather and location data using APIs
* Clean and analyze geographic datasets
* Visualize trends and patterns with plots and regression
* Integrate multiple APIs (OpenWeatherMap + Geoapify)
* Make data-driven decisions for travel planning

---
