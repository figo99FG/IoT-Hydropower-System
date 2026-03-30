# Advanced Hydropower Monitoring System — Arduino IoT

A physical **Arduino-based IoT system** that monitors a small-scale hydropower setup in real time. Sensors measure water flow, water level, temperature, and soil moisture — with servo-controlled valve automation and live OLED readouts. Data is published to Arduino IoT Cloud for remote monitoring.

Built as a group hardware project at Middlesex University London.

---

## ⚡ What It Does

- Monitors critical hydropower parameters in real time using physical sensors
- Automatically controls a servo-actuated water valve based on sensor thresholds
- Displays live readings on an OLED screen mounted on the device
- Publishes all data to Arduino IoT Cloud for remote dashboards and alerts
- Compares IoT vs M2M approaches — demonstrating why IoT enables superior scalability and remote control

---

## 🛠️ Hardware

| Component | Model / Type | Purpose |
|---|---|---|
| Microcontroller | Arduino Uno MKR WIFI 1010 | Central processing + Wi-Fi connectivity |
| Ultrasonic sensor | HC-SR04 | Water level measurement |
| Temperature sensor | DS18B20 | Water temperature monitoring |
| Soil moisture sensor | Capacitive | Moisture level at turbine site |
| Water flow sensor | YF-S201 | Flow rate measurement |
| OLED display | 128×64 I2C | Live local readout |
| Servo motor | SG90 | Valve automation (open/close) |
| Water pump | Mini submersible | Simulates hydro flow |
| Turbine generator | Micro generator | Power generation simulation |

---

## ☁️ Cloud Platform

- **Arduino IoT Cloud** — device registration, variable sync, remote dashboard
- **MQTT** — communication protocol between device and cloud
- **Wi-Fi (MKR WIFI 1010)** — wireless connectivity for cloud publishing

---

## 📐 System Architecture

```
[Water Flow Sensor]──┐
[Ultrasonic Sensor]──┤
[Temp Sensor]────────┼──→ Arduino MKR WIFI 1010 ──→ Arduino IoT Cloud
[Soil Moisture]──────┤         │                        (dashboard + alerts)
                     │         ↓
                     │   [OLED Display]
                     │   (live readings)
                     │
                     └──→ [Servo Valve]
                          (auto-control)
```

---

## ⚙️ How It Works

1. Sensors read environmental data every N seconds
2. Arduino processes readings and checks against defined thresholds
3. If water level exceeds threshold → servo closes valve automatically
4. All readings displayed on OLED in real time
5. Data published to Arduino IoT Cloud via MQTT over Wi-Fi
6. Cloud dashboard shows live graphs and can trigger remote alerts

---

## 📊 Monitored Parameters

| Parameter | Sensor | Unit |
|---|---|---|
| Water level | Ultrasonic (HC-SR04) | cm |
| Flow rate | YF-S201 | L/min |
| Temperature | DS18B20 | °C |
| Soil moisture | Capacitive | % |
| Valve state | Servo output | Open / Closed |

---

## 📚 Concepts Demonstrated

- Physical sensor integration and calibration
- IoT vs M2M communication comparison
- Cloud-connected embedded systems
- Event-driven actuator control
- Real-time data visualisation on constrained hardware
- Wireless protocol usage (MQTT over Wi-Fi)

---

## 👥 Team

Group hardware build and demo — Middlesex University London

**Module**: IoT Systems — Middlesex University London

---

## 👤 Author Contact

**Figo Figo** — BSc Networking & Security, Middlesex University London  
🌐 [figo.me.uk](https://figo.me.uk) · 💼 [LinkedIn](https://www.linkedin.com/in/figo-figo-1204642b2)
