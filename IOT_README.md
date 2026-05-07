# 🌱 IoT Sensor Systems — ESP32, MQTT & Cloud Visualization
**Gaukhar Assyrzhanova** | IIoT-2401 | Astana IT University

A collection of IoT engineering projects built on the **ESP32 microcontroller**, integrating real-world sensors, cloud dashboards (**ThingsBoard**), and automated alerting via **Telegram Bot API**. All prototypes were simulated in **Wokwi** and programmed in **C++ (Arduino framework)**.

---

## 🛠 Tools & Technologies
| Tool | Purpose |
|------|---------|
| ESP32 DevKit V1/V4 | Edge computing, Wi-Fi, MQTT publishing |
| C++ (Arduino IDE) | Firmware development |
| MQTT / PubSubClient | Lightweight IoT data transmission |
| ThingsBoard Cloud | Real-time dashboard & data visualization |
| Wokwi | Hardware simulation environment |
| Python | Metrological modeling & data analysis |
| Telegram Bot API | Push notifications & hazard alerts |

---

## 📁 Projects

---

### 🌾 Project 1 — AquaGuard: Precision Agriculture Monitoring System
**File:** `AquaGuard_Report.pdf`
**Authors:** Assyrzhanova Gaukhar & Kanatova Dariya

**What it does:**
An IoT-based smart irrigation system that monitors soil and environmental conditions in real time and makes automated watering decisions.

**Sensors & Components:**
- DHT22 — ambient temperature & humidity
- Capacitive soil moisture sensors (×2, simulated via potentiometers) — volumetric water content at two depths
- LDR (BH1750 target) — illuminance measurement
- DS1307 RTC — telemetry timestamps
- Relay module — controls water pump
- LCD2004 I2C (20×4) — local status display
- Tactile push button — simulates rain forecast input

**Key Features:**
- Automated irrigation algorithm: activates pump when soil is dry, suppresses when rain is forecast
- MQTT telemetry published every 5 seconds to ThingsBoard (JSON with 8 keys)
- ThingsBoard dashboard: gauge widgets, time-series chart, pump/LED status cards
- Telegram Bot push notifications via HTTPS for critical events
- Wokwi simulation with full circuit validation

**Tech Stack:** ESP32 · C++ · MQTT · ThingsBoard · Wokwi · DHT22 · Relay · Telegram Bot API

---

### 🏠 Project 2 — Smart Home Environmental Monitoring System
**File:** `SmartHome_Report.pdf`

**What it does:**
An indoor environmental monitoring prototype for smart home automation. Continuously collects multi-sensor data, streams it to the cloud, and triggers automated safety alerts.

**Sensors & Components:**
- DHT22 — temperature (±0.5°C) & humidity (±5% RH)
- PIR sensor — motion detection (pyroelectric effect)
- Photoresistor (LDR) — illuminance via 12-bit ADC mapping
- MQ-series gas sensor — combustible gas detection with digital threshold output

**Key Features:**
- 3-layer IoT architecture: Perception → Network → Application
- MQTT publish every 5 seconds with JSON telemetry payload
- ThingsBoard real-time dashboard with all sensor streams
- Telegram Bot REST API alert when gas concentration exceeds safe threshold
- `isnan()` data integrity validation — retains last valid state on sensor read error
- Power consumption analysis: ~391.6 mA peak (ESP32 + MQ heater + DHT22 + PIR)

**Tech Stack:** ESP32 · C++ · MQTT · ThingsBoard · Telegram Bot API · PIR · MQ Gas Sensor

---

### 🌡 Project 3 — Industrial Sensor Selection & Characterization
**File:** `IndustrialSensors_Report.pdf`
**Authors:** Assyrzhanova Gaukhar & Kanatova Dariya

**What it does:**
Comparative analysis of three industrial temperature sensors to evaluate metrological parameters: sensitivity, noise, and response time. Integrates Python modeling with ESP32 data acquisition.

**Sensors Compared:**
| Sensor | Type | Interface | Key Advantage |
|--------|------|-----------|---------------|
| DHT22 | Digital capacitive | Single-wire | Low cost, humidity combo |
| DS18B20 | Semiconductor IC | 1-Wire bus | High precision, noise-resistant |
| NTC Thermistor | Passive analog | ADC (Steinhart-Hart eq.) | Fast response, ultra-low cost |

**Methodology:**
1. **Wokwi simulation** — GPIO config, ADC resolution, I2C/1-Wire buses
2. **Python metrological modeling** — response time, dynamic noise, nonlinearity from datasheets
3. **IIoT integration** — JSON telemetry via MQTT to ThingsBoard for real-time comparison

**Tech Stack:** ESP32 · C++ · Python · MQTT · ThingsBoard · Wokwi · DS18B20 · NTC Thermistor

---

## 📊 Skills Demonstrated
- **IoT system design** — full stack from sensors to cloud
- **ESP32 firmware** in C++ (Arduino framework)
- **MQTT protocol** — publish/subscribe, JSON payloads, ThingsBoard integration
- **Sensor integration** — analog (ADC), digital (1-Wire, I2C), capacitive
- **Cloud dashboards** — ThingsBoard gauge, time-series, telemetry widgets
- **Automated alerting** — Telegram Bot via REST API
- **Python** — metrological data modeling and analysis
- **Wokwi simulation** — hardware prototyping without physical components
- **Technical documentation** — structured engineering reports with error analysis

---

## 👩‍💻 About
**Gaukhar Assyrzhanova**
Industrial Engineering (IIoT) Student — Astana IT University
Academic Mobility: Hochschule Schmalkalden, Germany (2025)

📧 gokass111@gmail.com | 🔗 [LinkedIn](https://linkedin.com/in/gaukhar-assyrzhanova)
