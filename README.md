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

### 📈 **Data Flow**
1. **Fetch Live Weather Data** from OpenWeatherMap API.  
2. **Store Data** in Excel files (`weather_data/`).  
3. **Perform Analysis** using Pandas for temperature and humidity trends.  
4. **Visualize Results** using Matplotlib & Seaborn charts.  
5. **Automate Updates** every hour using the Schedule library.

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
