# Weather App

Simple Flask weather app using OpenWeather API.

## Run Locally

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Create `.env` file in project root:

```env
OPENWEATHER_API_KEY=your_openweather_api_key
```

3. Start app:

```bash
py app.py
```

Open http://127.0.0.1:5000

## Deploy On Render

1. Push your latest code to GitHub.
2. In Render, click **New +** -> **Web Service**.
3. Connect your GitHub repo and select this project.
4. Use these settings:

```text
Runtime: Python 3
Build Command: pip install -r requirements.txt
Start Command: gunicorn app:app
```

5. In service environment variables, set:

```env
OPENWEATHER_API_KEY=your_new_active_openweather_key
```

6. Deploy.

After deploy, open your Render URL and search city weather.

## Notes

- `.env` is ignored by git via `.gitignore`.
- Keep API keys secret and never commit real keys.
