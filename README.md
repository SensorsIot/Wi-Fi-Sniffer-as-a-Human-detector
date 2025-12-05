# Wi-Fi Sniffer as a Human Detector

[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/SensorsIot/Wi-Fi-Sniffer-as-a-Human-detector)](https://github.com/SensorsIot/Wi-Fi-Sniffer-as-a-Human-detector/stargazers)
[![YouTube](https://img.shields.io/badge/YouTube-Video-red?logo=youtube)](https://www.youtube.com/watch?v=fmhjtzmLrg8)

![ESP8266](https://img.shields.io/badge/ESP8266-Supported-green?logo=espressif)
![Arduino](https://img.shields.io/badge/Arduino-Compatible-00979D?logo=arduino)
![MQTT](https://img.shields.io/badge/MQTT-Enabled-purple?logo=eclipsemosquitto)

Detect human presence by sniffing Wi-Fi probe requests from smartphones and other devices.

📺 **Video Tutorial:** https://www.youtube.com/watch?v=fmhjtzmLrg8

## 📦 Dependencies

Install using the Library Manager in Arduino IDE:

| Library | Description |
|---------|-------------|
| [ESP8266](https://github.com/esp8266/Arduino) | ESP8266 board support |
| [ArduinoJson](https://arduinojson.org/) | JSON serialization |
| [PubSubClient](https://pubsubclient.knolleary.net) | MQTT client |

## ⚙️ Configuration

Before uploading, update these settings:

### 📡 MQTT Settings (`mqtt.h`)

```cpp
mqttServer = "192.168.0.100";  // Your MQTT broker IP
MQTT_USERNAME = "admin";        // Your MQTT username
MQTT_KEY = "admin";             // Your MQTT password
```

### 📶 WiFi Settings (`WiFi_Sniffer.ino`)

```cpp
mySSID = "your-wifi-name";
MyPassword = "your-wifi-password";
```

### 🔌 Serial Monitor

The default baud rate is **115200**. Make sure your Serial Monitor matches this setting.

> 💡 **Tip:** If you're using older hardware that requires a different baud rate, change `Serial.begin(115200);` in the sketch to your preferred speed (e.g., `9600`).

## 📬 MQTT Topics

| Topic | Description |
|-------|-------------|
| `Sniffer/#` | All sniffer data is published under this topic |

## 🔴 Node-RED Integration

A sample Node-RED flow is included in `Node-red Flow.txt`.

To import:
1. Open Node-RED
2. Menu → Import → Clipboard
3. Paste the contents of the flow file
