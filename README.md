<div align="center">

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

</div>