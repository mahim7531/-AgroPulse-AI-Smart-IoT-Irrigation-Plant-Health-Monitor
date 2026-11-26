AgroPulse AI — Reusable Dashboard & AI Krishi Report Prompt

Copy and paste the prompt below whenever you want to recreate or expand this exact dashboard:

Build a responsive, modern web dashboard for AgroPulse AI — Smart IoT Irrigation & Plant Health Monitor (ESP32_PLANT_01) with a clean light/dark mode toggle, agricultural emerald/teal/sky color palette, and interactive live simulation, plus user authentication (Login & Registration) and ESP32 Device Key security.

0. Authentication & Access Control (Login, Registration & Device Security)

Farmer / User Login & Registration Modal/Screen: Clean sign-in and registration views supporting Email / Phone + Password, farmer name, and assigned device ID (ESP32_PLANT_01), with show/hide password toggle, form validation, and quick Demo Farmer Login option for fast testing.

Session / JWT & Protected Actions: Display the logged-in farmer's profile pill/badge in the header with a Logout button. Gate sensitive actions (such as toggling Manual Override / Relay Pump, changing moisture thresholds, or generating AI Krishi Reports) behind authenticated session state (Bearer token) while allowing clean error/toast feedback if unauthenticated.

ESP32 Device Authentication (x-device-key): Include configuration/documentation notes for authenticating incoming POST /api/telemetry requests from ESP32_PLANT_01 using a secret device API key header (x-device-key) so unauthorized requests are rejected.

1. Top Navigation Bar

Brand logo & title: AgroPulse AI (v2.4 IoT) with subtitle Smart IoT Irrigation & Plant Health Monitor.

Live device badge for ESP32_PLANT_01 showing online status and Wi-Fi RSSI (-58 dBm).

Controls for Live Sim: ON/PAUSED, manual Sync button, Dark/Light Mode toggle, and Farmer Account / Login / Logout status.

2. Top 4 KPI Sensor Cards

Soil Moisture: Large percentage value (42%), hourly delta, status badge (Slightly Dry / Optimal Moisture / High Saturation), crop optimal range, and animated progress bar.

Air Temperature (DHT11): Value in °C (28.4°C), trend indicator, and calculated Heat Index.

Air Humidity (DHT11): Percentage (64%), VPD readout, and status badge.

Rule-Based AI Health & Reservoir: Dynamic health badge (Mild Water Stress / Healthy Optimal / Critical Dry Stress / Heat Stress Risk / Overwatered) plus water tank percentage (78%) and a Refill Tank button.

3. Irrigation & Relay Control Panel (GPIO 26)

Switch between AI Auto-Irrigation and Manual Override.

Interactive submersible DC pump card with animated pump icon, ON/OFF badge, Start Pump / Stop Pump toggle, and a 15s irrigation countdown bar that increases soil moisture (+1.5% per tick) and slightly lowers tank level.

Moisture threshold range slider (30%–70%) that triggers auto-watering when moisture drops below the threshold in Auto mode.

4. AI Krishi Advisory Report Generator (Telemetry + Leaf Image)

Language toggle supporting বাংলা (Bangla) and English.

Crop selector dropdown (Tomato, Paddy / Dhan, Green Chili, Potato) paired with a custom crop text input and a Generate AI Krishi Report button with a scan overlay animation.

Leaf Photo Capture / Upload: Allows snapping a photo via camera or uploading a leaf image from the device, shows a thumbnail preview with a remove button, and combines leaf visual diagnosis (chlorosis/yellowing, brown spots/blight, or healthy green) with live soil moisture, temperature, and humidity in the generated farmer report.

Bottom summary strip showing 24h Avg Moisture, 24h Avg Temp, and Health Score (/ 100).

5. 24-Hour Telemetry Chart & HTTP POST Event Logs

Interactive SVG trend chart for Soil %, Temp °C, and Humidity % with hover crosshair and floating tooltip.

Live event log table displaying timestamp, device ID (ESP32_PLANT_01), soil moisture, temp/humidity, pump state, and HTTP status (200 OK).
