# 🌫️ IoT Air Quality Monitoring System

A smart IoT-based system using ESP32, DHT22, and MQ2 gas sensor to monitor temperature, humidity, and gas concentration levels. The data is sent live to a ThingSpeak cloud dashboard for visualization and historical analysis.

---

## 📋 Intern Details

- **👨‍💼 Name:** Mohammed Abdul Ali Nabeel
- **🎓 Intern ID:** CITS0D781
- **🏢 Company:** CodTech IT Solutions
- **🌐 Domain:** Internet of Things (IoT)
- **📅 Internship Duration:** 4 Weeks
- **🧑‍🏫 Mentor:** Neela Santhosh

---

## 📦 Components Used

| Component      | Description                          |
|----------------|--------------------------------------|
| ESP32          | Wi-Fi-enabled microcontroller        |
| DHT22          | Temperature and Humidity sensor      |
| MQ2            | Gas sensor (LPG, CO, smoke, methane) |
| Jumper Wires   | For direct connections               |
| ThingSpeak     | Cloud dashboard for data monitoring  |

> ⚠️ **Note**: Breadboard was not used. All components were connected directly using jumper wires.

---

## 🔧 Circuit Connections
<img width="1066" height="585" alt="image" src="https://github.com/user-attachments/assets/593c0058-fb62-4b25-b4d3-34202af28bf3" />

## OUTPUT
<img width="1266" height="830" alt="image" src="https://github.com/user-attachments/assets/8b41026a-e6a8-447d-acb6-8e2a21a2b4d7" />
<img width="1303" height="416" alt="image" src="https://github.com/user-attachments/assets/43ae5511-47f4-419d-9b32-25621fc2e48f" />



### DHT22
| Pin  | ESP32 Pin |
|------|-----------|
| VCC  | 5V        |
| GND  | GND       |
| DATA | GPIO 15   |

### MQ2
| Pin  | ESP32 Pin |
|------|-----------|
| VCC  | 5V        |
| GND  | GND       |
| AO   | GPIO 34   |

---

## 📲 ThingSpeak Setup

1. Create a channel at [thingspeak.com](https://thingspeak.com).
2. Add 3 fields:
   - Field 1: Temperature
   - Field 2: Humidity
   - Field 3: Gas Level
3. Copy your:
   - **Channel ID**
   - **Write API Key**

Update the following in the code:

```cpp
unsigned long channelID = YOUR_CHANNEL_ID;
const char* writeAPIKey = "YOUR_WRITE_API_KEY";
