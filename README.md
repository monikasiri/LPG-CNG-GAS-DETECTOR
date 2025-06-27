### **Project Summary**
---
This project detects LPG/CNG gas leakage and fire using sensors. It gives alerts via a buzzer, LCD, and servo motor, and also sends emergency messages to a Telegram chat using WiFi.

### **Abstract**
---
The system uses a gas sensor and a fire sensor to detect hazardous conditions. If gas or fire is detected, it activates a buzzer, displays the status on an LCD, opens a safety door with a servo motor, and sends real-time alerts through a Telegram bot using an ESP8266 module.

### **Introduction**
---
This safety system is designed for home or industrial use. It helps prevent accidents by continuously monitoring for gas leaks and fire. When a hazard is detected, the system responds locally (buzzer, LCD, servo) and remotely (Telegram alert).

### **Hardware Used**
---
- MQ Gas Sensor  
- IR Fire Sensor  
- 16x2 LCD Display  
- Servo Motor  
- ESP8266 (NodeMCU)  
- Arduino UNO  
- Power Supply and Connecting Wires  

### **Software Used**
---
- Arduino IDE (for programming the Arduino and ESP8266)  
- Telegram App (to receive real-time alerts)

### **Libraries Used**
---
- `LiquidCrystal` – for LCD display  
- `Servo` – to control the servo motor  
- `WiFi / WiFiClientSecure` – to connect ESP8266 to the internet  
- `UniversalTelegramBot` – to send alerts to Telegram  
- `ArduinoJson` – to format Telegram messages

### **Algorithm Used**
---
1. Read analog gas value and digital fire value continuously  
2. If gas > 300 → sound buzzer, open servo motor  
3. If fire is detected → sound buzzer, activate sprinkler (relay)  
4. Send the alert message to ESP8266 through Serial  
5. ESP8266 forwards the message to the Telegram chat  
6. Telegram bot responds to commands like `/start`, `/led_on`, `/led_off`, `/state`

### **How It Works**
---
- The Arduino UNO reads sensor values and controls outputs (buzzer, LCD, servo)  
- If danger is detected, Arduino sends a message to ESP8266 via Serial  
- The ESP8266 connects to WiFi and sends the message to Telegram  
- The user receives real-time alerts and can also control the LED remotely via Telegram commands  
