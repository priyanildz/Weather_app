<!-- <div align="center">

# <img src="https://img.icons8.com/fluency/48/partly-cloudy-day.png" width="36"/> Weather App

**A clean, minimal weather web application built with Python & Flask**

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.x-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![OpenWeatherMap](https://img.shields.io/badge/OpenWeatherMap-API-orange?style=for-the-badge&logo=openweathermap&logoColor=white)](https://openweathermap.org/api)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

[Live Demo](#live-demo) &nbsp;·&nbsp; [Features](#features) &nbsp;·&nbsp; [Getting Started](#getting-started) &nbsp;·&nbsp; [Screenshots](#screenshots)

</div>

---

## Overview

Weather App is a lightweight Flask web application that fetches real-time weather data for any city in the world using the OpenWeatherMap API. Enter a city name and instantly get the current temperature, humidity, wind speed, weather condition, and local date/time — all in a clean, card-based UI.

---

## Screenshots

> _Add screenshots to the `assets/` folder and update these paths._

| Home Screen | Weather Result |
|:-----------:|:--------------:|
| ![Home](assets/screenshot-home.png) | ![Result](assets/screenshot-result.png) |

---

## Live Demo

> _Deploy to a platform like Render, Railway, or Vercel and paste your URL below._

[![Live Demo](https://weather-app-043d.onrender.com)](#)

---

## Features

- **City Search** — Look up current weather for any city worldwide
- **Real-Time Data** — Pulls live data from the OpenWeatherMap API
- **Temperature Display** — Shows temperature in Celsius (converted from Kelvin)
- **Weather Details** — Humidity, wind speed, weather condition, and weather icon
- **Local Date & Time** — Displays the city's local date and time using the timezone offset
- **Error Handling** — Clear messages for invalid cities or missing/invalid API keys
- **Responsive UI** — Centered card layout that works across screen sizes

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Python 3, Flask |
| Templating | Jinja2 |
| Styling | Custom CSS |
| Weather Data | OpenWeatherMap REST API |
| Environment Config | python-dotenv |
| Production Server | Gunicorn |

---

## Project Structure

```
weather_app/
├── app.py                  # Flask application & route logic
├── requirements.txt        # Python dependencies
├── .env                    # Local environment variables (not committed)
├── .env.example            # Environment variable template
├── .gitignore
├── static/
│   └── style.css           # App stylesheet
├── templates/
│   └── index.html          # Main HTML template (Jinja2)
└── assets/                 # Screenshots for README
    ├── screenshot-home.png
    └── screenshot-result.png
```

---

## Getting Started

### Prerequisites

- Python 3.8 or higher
- A free [OpenWeatherMap API key](https://openweathermap.org/api)

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/priyanildz/Weather_app.git
cd Weather_app
```

**2. Create and activate a virtual environment**

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Configure your API key**

```bash
cp .env.example .env
```

Open `.env` and replace the placeholder with your actual key:

```env
OPENWEATHER_API_KEY=your_openweather_api_key_here
```

> Get a free API key at [openweathermap.org/api](https://openweathermap.org/api). New keys may take up to 2 hours to activate.

**5. Run the application**

```bash
python app.py
```

Open your browser and navigate to `http://127.0.0.1:5000`

---

## Usage

1. Enter a city name in the search box (e.g., `Mumbai`, `London`, `New York`)
2. Click **Get Weather**
3. View the current temperature, humidity, wind speed, condition, and local time for that city

---

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENWEATHER_API_KEY` | Your OpenWeatherMap API key | Yes |

---

## Deployment

To deploy with Gunicorn (production):

```bash
gunicorn app:app
```

For platforms like **Render** or **Railway**, set the start command to `gunicorn app:app` and add `OPENWEATHER_API_KEY` as an environment variable in the platform dashboard.

---

## API Reference

This app uses the [OpenWeatherMap Current Weather API](https://openweathermap.org/current):

```
GET https://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}
```

**Data used from the response:**

| Field | Description |
|-------|-------------|
| `main.temp` | Temperature in Kelvin (converted to °C) |
| `main.humidity` | Humidity percentage |
| `wind.speed` | Wind speed in m/s |
| `weather[0].description` | Weather condition text |
| `weather[0].icon` | Weather icon code |
| `dt` + `timezone` | Unix timestamp + offset for local time |

---

## Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">

Made with <img src="https://img.icons8.com/fluency/16/like.png"/> by [priyanildz](https://github.com/priyanildz)

</div> -->

<!-- 
<div align="center">

# <img src="https://img.icons8.com/fluency/48/partly-cloudy-day.png" width="36"/> Weather App

**A clean, minimal real-time weather web application built with Python & Flask**

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.x-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![OpenWeatherMap](https://img.shields.io/badge/OpenWeatherMap-API-orange?style=for-the-badge&logo=openweathermap&logoColor=white)](https://openweathermap.org/api)
[![Gunicorn](https://img.shields.io/badge/Gunicorn-Production-499848?style=for-the-badge&logo=gunicorn&logoColor=white)](https://gunicorn.org)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

[🌐 Live Demo](#-live-demo) &nbsp;·&nbsp; [✨ Features](#-features) &nbsp;·&nbsp; [🚀 Getting Started](#-getting-started) &nbsp;·&nbsp; [📸 Screenshots](#-screenshots) &nbsp;·&nbsp; [🤝 Contributing](#-contributing)

</div>

---

## 📖 Overview

**Weather App** is a lightweight Flask web application that fetches real-time weather data for any city in the world using the [OpenWeatherMap API](https://openweathermap.org/api). Enter any city name and instantly get the current temperature, humidity, wind speed, weather condition, and local date/time — all rendered in a clean, card-based UI with weather icons.

---

## 🌐 Live Demo

<div align="center">

[![Live Demo](https://img.shields.io/badge/🌤️_Live_Demo-Open_App-2196F3?style=for-the-badge)](https://weather-app-043d.onrender.com)

</div>

> The app is hosted on [Render](https://render.com). It may take **10–15 seconds** to load on first visit if the instance has been idle (free tier cold start).

---

## 📸 Screenshots

| Home Screen | Weather Result |
|:-----------:|:--------------:|
| ![Home Screen](assets/home.png) | ![Weather Result](assets/output.png) |

---

## ✨ Features

- 🔍 **City Search** — Look up current weather for any city worldwide
- 🌡️ **Real-Time Temperature** — Displays temperature in °C (converted from Kelvin via OpenWeatherMap)
- 💧 **Humidity & Wind** — Shows humidity percentage and wind speed in m/s
- 🕐 **Local Date & Time** — Calculates and displays the city's local time using the API timezone offset
- 🌤️ **Weather Icons** — Pulls live condition icons directly from OpenWeatherMap CDN
- ⚠️ **Error Handling** — Clear messages for invalid city names, missing API keys, or rejected credentials
- 📱 **Responsive UI** — Centered card layout that adapts across different screen sizes
- ⚙️ **Production Ready** — Configured with Gunicorn for deployment on cloud platforms

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Backend** | Python 3, Flask |
| **Templating** | Jinja2 |
| **Styling** | Custom CSS (linear gradient, card layout) |
| **Weather Data** | OpenWeatherMap Current Weather REST API |
| **Environment Config** | python-dotenv |
| **Production Server** | Gunicorn |
| **Hosting** | Render |

---

## 📁 Project Structure

```
15_weather_app/
├── app.py                  # Flask application & all route logic
├── requirements.txt        # Python dependencies
├── .env                    # Local environment variables (not committed)
├── .env.example            # Environment variable template for new contributors
├── .gitignore              # Ignores .env, __pycache__, *.pyc
├── static/
│   └── style.css           # App stylesheet (gradient background, card UI)
├── templates/
│   └── index.html          # Main Jinja2 HTML template
└── assets/                 # Screenshots used in this README
    ├── home.png
    └── output.png
```

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+** installed on your machine
- A free **OpenWeatherMap API key** — [sign up here](https://openweathermap.org/api)

> ⏱️ New API keys can take up to **2 hours** to activate after registration.

---

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/priyanildz/Weather_app.git
cd Weather_app
```

**2. Create and activate a virtual environment**

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Configure your API key**

```bash
cp .env.example .env
```

Open `.env` and replace the placeholder with your actual key:

```env
OPENWEATHER_API_KEY=your_openweather_api_key_here
```

**5. Run the application**

```bash
python app.py
```

Open your browser and navigate to **[http://127.0.0.1:5000](http://127.0.0.1:5000)**

---

## 🧭 Usage

1. Enter a city name in the search box — e.g., `Mumbai`, `London`, `New York`, `Tokyo`
2. Click **Get Weather**
3. View the live weather card showing:
   - 🌡️ Current temperature in °C
   - 💧 Humidity percentage
   - 💨 Wind speed in m/s
   - 🌤️ Weather condition with icon
   - 🕐 City's local date and time

---

## 🔑 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENWEATHER_API_KEY` | Your personal OpenWeatherMap API key | ✅ Yes |

---

## 🌍 API Reference

This app uses the [OpenWeatherMap Current Weather Data API](https://openweathermap.org/current):

```
GET https://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}
```

**Data fields used from the response:**

| Field | Usage |
|-------|-------|
| `main.temp` | Temperature in Kelvin → converted to °C |
| `main.humidity` | Humidity percentage |
| `wind.speed` | Wind speed in m/s |
| `weather[0].description` | Weather condition text |
| `weather[0].icon` | Icon code for the condition image |
| `dt` + `timezone` | Unix timestamp + offset to compute local time |
| `name` | City name as confirmed by the API |

---

## ☁️ Deployment

### Deploy with Gunicorn (production server)

```bash
gunicorn app:app
```

### Deploy on Render

1. Push your code to GitHub
2. Go to [render.com](https://render.com) → **New Web Service**
3. Connect your GitHub repo
4. Set the **Start Command** to:
   ```
   gunicorn app:app
   ```
5. Add `OPENWEATHER_API_KEY` as an **Environment Variable** in the Render dashboard
6. Deploy — your app will be live at a `*.onrender.com` URL

> The same steps work for **Railway** and similar platforms.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. **Fork** this repository
2. **Create** a new feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Commit** your changes:
   ```bash
   git commit -m "Add: your feature description"
   ```
4. **Push** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a **Pull Request** against the `main` branch

Please make sure your code is clean and tested before submitting.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — feel free to use, modify, and distribute it.

---

<div align="center">

Made with ❤️ by [priyanildz](https://github.com/priyanildz)

⭐ If you found this useful, consider giving the repo a star!

</div> -->

<div align="center">

# <img src="https://img.icons8.com/fluency/48/partly-cloudy-day.png" width="40"/> Weather App

### Real-Time Weather Intelligence • Minimal UI • Production Ready

<p>
A lightweight and scalable weather web application that delivers real-time weather insights for any city worldwide using a clean and responsive interface.
</p>

<br/>

<a href="https://weather-app-043d.onrender.com" target="_blank">
  <img src="https://img.shields.io/badge/Live%20Application-Open-1E88E5?style=for-the-badge&logo=google-chrome&logoColor=white" />
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-Backend-000000?style=for-the-badge&logo=flask&logoColor=white"/>
<img src="https://img.shields.io/badge/OpenWeatherMap-API-F57C00?style=for-the-badge&logo=openweathermap&logoColor=white"/>
<img src="https://img.shields.io/badge/Gunicorn-Production-499848?style=for-the-badge&logo=gunicorn&logoColor=white"/>
<img src="https://img.shields.io/badge/License-MIT-2E7D32?style=for-the-badge"/>

</div>

---

## Overview

**Weather App** is a minimal yet powerful Flask-based web application that fetches and displays real-time weather data using the OpenWeatherMap API.

It focuses on simplicity, performance, and clarity — delivering accurate weather information in a clean card-based interface without unnecessary complexity.

---

## Screenshots

<div align="center">

| Home Interface | Weather Output |
|---------------|----------------|
| <img src="assets/home.png" width="400"/> | <img src="assets/output.png" width="400"/> |

</div>

---

## Key Features

- Real-time weather data for any city worldwide  
- Temperature conversion (Kelvin to Celsius)  
- Displays humidity, wind speed, and conditions  
- Dynamic weather icons from API  
- Local time calculation using timezone offset  
- Clean and responsive UI design  
- Robust error handling (invalid city, API issues)  
- Production-ready deployment using Gunicorn  

---

## Technology Stack

<div align="center">

| Category | Technology |
|----------|-----------|
| Backend | <img src="https://img.icons8.com/color/20/python.png"/> Python |
| Framework | <img src="https://img.icons8.com/ios-filled/20/000000/flask.png"/> Flask |
| Templating | <img src="https://img.icons8.com/ios-filled/20/code.png"/> Jinja2 |
| Styling | <img src="https://img.icons8.com/color/20/css3.png"/> CSS |
| API | <img src="https://img.icons8.com/color/20/cloud.png"/> OpenWeatherMap |
| Environment | <img src="https://img.icons8.com/color/20/settings.png"/> python-dotenv |
| Server | <img src="https://img.icons8.com/ios-filled/20/server.png"/> Gunicorn |
| Hosting | <img src="https://img.icons8.com/color/20/cloud.png"/> Render |

</div>

---

## Project Structure

```
15_weather_app/
├── app.py
├── requirements.txt
├── .env
├── .env.example
├── .gitignore
├── static/
│   └── style.css
├── templates/
│   └── index.html
└── assets/
    ├── home.png
    └── output.png
```

---

## Getting Started

### Prerequisites

- Python 3.8 or higher  
- OpenWeatherMap API key  

---

### Installation

```bash
git clone https://github.com/priyanildz/Weather_app.git
cd Weather_app
```

```bash
python -m venv venv
```

```bash
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

```bash
pip install -r requirements.txt
```

---

### Environment Setup

```bash
cp .env.example .env
```

Update `.env`:

```env
OPENWEATHER_API_KEY=your_api_key_here
```

---

### Run Application

```bash
python app.py
```

Open:

```
http://127.0.0.1:5000
```

---

## Usage Flow

1. Enter a city name  
2. Submit request  
3. View:
   - Temperature  
   - Humidity  
   - Wind speed  
   - Weather condition  
   - Local time  

---

## API Integration

```
GET https://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}
```

### Data Used

- Temperature  
- Humidity  
- Wind Speed  
- Weather Description  
- Weather Icon  
- Timezone Offset  

---

## Deployment

### Production Server

```bash
gunicorn app:app
```

### Render Deployment

- Create new web service  
- Connect repository  
- Set start command:

```
gunicorn app:app
```

- Add environment variable:

```
OPENWEATHER_API_KEY
```

---

## Contributing

1. Fork the repository  
2. Create a feature branch  
3. Commit your changes  
4. Push to GitHub  
5. Open a pull request  

---

## License

This project is licensed under the MIT License.

---

<div align="center">

Developed by  
<strong>priyanildz</strong>

</div>