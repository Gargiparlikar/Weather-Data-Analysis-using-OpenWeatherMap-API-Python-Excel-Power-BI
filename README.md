# Weather-Data-Analysis-using-OpenWeatherMap-API-Python-Excel-Power-BI


### 📊 **Overview**
This project focuses on collecting, analyzing, and visualizing **real-time weather data** from the **OpenWeatherMap API** using **Python**.  
It provides live updates of temperature, humidity, pressure, and other weather parameters for multiple cities, performs trend analysis using Pandas, and visualizes results through Matplotlib and Seaborn.

---

### ⚙️ **Key Features**
- 🔗 Integrated **OpenWeatherMap API** to fetch real-time weather and forecast data.  
- 🧮 Processed and analyzed data using **Pandas** for temperature, humidity, and pressure insights.  
- 🔁 Automated hourly data updates using Python’s `schedule` module.  
- 📈 Created visualizations with **Matplotlib** and **Seaborn** for trends and correlations.  
- 💾 Exported analyzed data into **Excel/CSV files** for reporting and record-keeping.  
- 🔍 Performed analytical insights such as:
  - Hottest & Coldest Cities  
  - Correlation between Temperature, Humidity, and Pressure  
  - Weather Condition Frequency Distribution  
  - Forecast Trends for the Next 5 Days  

---

### 🧠 **Tech Stack**
| Layer | Tools / Technologies |
|--------|----------------------|
| **Programming Language** | Python |
| **API Source** | OpenWeatherMap API |
| **Libraries** | Pandas, Requests, Matplotlib, Seaborn, Schedule, OpenPyXL |
| **Data Format** | Excel / CSV |

---

🔄 Workflow
1. API Data Collection

Fetched temperature, humidity, visibility, windspeed

Handled API token & errors

2. Data Cleaning

Converted units

Removed invalid records

Filled missing info

3. Analysis

Temp trends

Humidity variation

Weather condition classification

4. Dashboard

Multi-city comparison

Forecast charts

Parameter correlations

✔ Run the Script
python weather_api_fetch.py

# DASHBOARD PREVIEW
![Weather Data Analysis Project Screenshot](https://github.com/Gargiparlikar/Weather-Data-Analysis-using-OpenWeatherMap-API-Python-Excel-Power-BI/blob/main/Screenshot%202025-12-01%20132158.png)

🧾 Key Insights

Coastal areas have 10–15% higher humidity

Temperature correlates strongly with windspeed
---

### 💻 **Example Python Code Snippets**

**Fetch Real-Time Weather Data**
```python
params = {"q": city, "appid": API_KEY, "units": "metric"}
response = requests.get(BASE_URL, params=params)
data = response.json()

record = {
    "City": city,
    "Temperature (°C)": data["main"]["temp"],
    "Humidity (%)": data["main"]["humidity"],
    "Pressure (hPa)": data["main"]["pressure"],
    "Wind Speed (m/s)": data["wind"]["speed"],
    "Weather": data["weather"][0]["main"],
    "Time": datetime.now().strftime("%Y-%m-%d %H:%M:%S")
}
---



