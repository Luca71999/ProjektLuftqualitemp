#  Luftqualitäts- & Temperaturmesser (ESP32)

Ein selbstgebautes IoT-Messgerät zur Erfassung von **Temperatur**, **Luftfeuchte** und **Luftqualität (VOC / eCO₂)**  
mit **ESP32**, **BME680** und **OLED-Display**.  
Die Messwerte werden lokal angezeigt und können **live über WLAN** in einer eigenen App oder Weboberfläche abgerufen werden.

Ziel des Projekts ist es, **möglichst viel Hardware und Software selbst zu entwickeln** – vom Sensor bis zur App.


## 📌 Features

- 🌡️ Temperaturmessung
- 💧 Luftfeuchtigkeit
- 🌫️ Luftqualität (VOC / eCO₂)
- 🖥️ Lokale Anzeige auf OLED (SSD1306)
- 📡 WLAN-Anbindung (ESP32)
- 🔄 Live-Datenübertragung (geplant: MQTT / REST)
- 📱 Eigene App / Web-Frontend (geplant)
- 🖨️ 3D-gedrucktes Gehäuse


## 🧱 Hardware

| Komponente | Beschreibung |
|-----------|-------------|
| ESP32 Dev Board | Mikrocontroller mit WLAN |
| BME680 | Temperatur, Luftfeuchte, Luftdruck, VOC |
| OLED Display | 0.96" SSD1306 (128×64, I²C) |
| Breadboard & Jumper | Prototyping |
| USB-Netzteil | Stromversorgung |
| 3D-Drucker | Gehäuse |


## 🔌 Schaltung (I²C)

Alle Komponenten teilen sich denselben I²C-Bus:

| ESP32 Pin | Funktion |
|----------|----------|
| 3V3 | Versorgung |
| GND | Masse |
| GPIO21 | SDA |
| GPIO22 | SCL |


## 🧠 Software-Stack

- **PlatformIO** (VS Code)
- **Arduino Framework (ESP32)**
- **C++**
- Geplant:
  - MQTT (Mosquitto)
  - Backend (z. B. FastAPI / Node.js)
  - App oder Web-Frontend


## 📁 Projektstruktur

```text
air-quality-monitor/
├── src/
│   └── main.cpp        # Hauptprogramm
├── lib/                # Eigene Module (Sensor, Display, WLAN)
├── include/
├── platformio.ini      # Board- & Build-Konfiguration
└── README.md
