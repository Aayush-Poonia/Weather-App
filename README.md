# 🌦️ Weather App Using API

A simple Python project that fetches and displays the **current weather of any city** using a weather API.  
This project demonstrates how to work with **APIs, HTTP requests, and JSON data in Python**.

---

## 📌 Features

- Get **real-time weather information**
- Shows **temperature, humidity, and weather condition**
- Uses a **free weather API**
- Simple **command-line interface**
- Beginner-friendly Python project

---

## 🛠️ Technologies Used

- Python
- Requests Library
- OpenWeatherMap API
- JSON Data Handling

---

## 📂 Project Structure

```
weather-app
│
├── Weather_app.py
└── README.md
```

---

## ⚙️ Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Aayush-Poonia/weather-app.git
```

### 2️⃣ Navigate to the project folder

```bash
cd weather-app
```

### 3️⃣ Install required library

```bash
pip install requests
```

---

## 🔑 Get API Key

1. Go to https://openweathermap.org  
2. Create a free account  
3. Generate your API key  
4. Replace the API key in the Python script

Example:

```python
api_key = "YOUR_API_KEY"
```

---

## ▶️ How to Run the Project

Run the Python file:

```bash
python Weather_app.py
```

Enter the city name when prompted.

Example:

```
Enter city name: Delhi
```

Output:

```
Weather Information
-------------------
City: Delhi
Temperature: 31 °C
Humidity: 42 %
Condition: clear sky
```

---

## 💻 Example Code

```python
import requests

api_key = "YOUR_API_KEY"

city = input("Enter city name: ")

url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}&units=metric"

response = requests.get(url)
data = response.json()

if data["cod"] == 200:
    temp = data["main"]["temp"]
    humidity = data["main"]["humidity"]
    weather = data["weather"][0]["description"]

    print("\nWeather Information")
    print("---------------------")
    print("City:", city)
    print("Temperature:", temp, "°C")
    print("Humidity:", humidity, "%")
    print("Condition:", weather)

else:
    print("City not found")
```

---

## 📖 What I Learned

- Working with REST APIs
- Sending HTTP requests in Python
- Parsing JSON responses
- Handling user input
- Displaying formatted output

---

## 🚀 Future Improvements

- Add weather icons
- Create a GUI version using Tkinter
- Build a web app using Flask
- Add multiple city search
- Implement better error handling

---

## 👨‍💻 Author

**Aayush Poonia**

- Cybersecurity Enthusiast  
- Web Developer  
- Python Developer  

GitHub:  
https://github.com/Aayush-Poonia
