# Intelligent Cloud-Based Air Quality Alert System - Dashboard

React (Vite) dashboard for the ESP32 + MQ135 + AWS project.

## Run locally
    npm install
    npm run dev

## Build and deploy (Netlify)
    npm run build        # output goes to dist/
Drag the `dist` folder onto Netlify, or connect the repo (netlify.toml is included).

## Demo mode vs live mode
- No `.env` file: DEMO mode. Sensor and cloud services are simulated in the browser.
- Copy `.env.example` to `.env` and set `VITE_API_URL` to your API Gateway URL: LIVE mode.
  The endpoint must return JSON such as {"adc": 1093} or {"aqi": 134}.
## Structure
- src/lib/aqi.js               formulas, thresholds, AQI categories
- src/hooks/useAirQuality.js   simulator, persistence timer, LED/buzzer logic, history, log
- src/components/              one file per dashboard section
- src/styles.css               all styling

http://aish-rid-aqdd-051580166213-ap-southeast-2-an.s3-website-ap-southeast-2.amazonaws.com/


