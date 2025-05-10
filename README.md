# Basic-Heater-Control-System
# Heater Control System – Design Document
https://wokwi.com/projects/430578880299072513
### 👤 Candidate: Kunal  
### 📅 Date: 2025-05-10  

---

### 📌 Objective
To design and implement a basic embedded heater control system that turns a heater (simulated with an LED) ON/OFF based on real-time temperature readings from a DHT22 sensor.

---

### 🧰 1. Minimum Sensors Required
- **DHT22 Temperature Sensor**
  - Measures temperature and humidity.
  - Single-wire digital communication.
  - Easy to interface with Arduino using `DHT.h`.

---

### 🔗 2. Communication Protocol
- **Single-wire digital (DHT22 protocol)**
- **Justification:**
  - Lightweight and efficient for temperature monitoring.
  - Requires only 1 data pin + pull-up resistor.
  - Compatible with Arduino and supported by the `DHT.h` library.

---

### 🧱 3. Block Diagram

```
[DHT22 Sensor]
     |
     | (DATA)
     v
[Arduino UNO] -----> [LED]  ← Simulates Heater
     |
     v
[Serial Monitor] ← Logs temperature & state


```

---

### 🔮 4. Future Roadmap
- **Overheat Protection:** Force shutdown when temperature > 50°C.
- **Multiple Heating Profiles:** Low/Medium/High thresholds.
- **BLE Integration:** Advertise current state to mobile.
- **Display Module:** OLED/LCD to show real-time temperature.
- **RTOS Integration:** Use FreeRTOS for scheduling tasks cleanly.
