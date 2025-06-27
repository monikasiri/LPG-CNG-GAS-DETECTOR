# 🚨 LPG/CNG Gas and Fire Detector with Telegram Alerts

### **Project Summary**
---
This project is a safety system designed to detect LPG/CNG gas leakage and fire. It uses a gas sensor, fire sensor, buzzer, LCD for local alerting, and a servo to open a door. It sends real-time alerts via Telegram using an ESP-based board connected over WiFi.

### **Abstract**
---
The system monitors gas concentration and fire presence using analog/digital sensors. In case of gas leakage or fire, it triggers a buzzer and activates safety actions like opening a door or enabling a sprinkler. It also sends real-time notifications to a predefined Telegram chat using the UniversalTelegramBot library.

### **Introduction**
---
This embedded IoT-based project focuses on gas and fire safety in homes or industries. It reads values from a gas and fire sensor, displays them on an LCD, activates response systems (buzzer, servo motor, and sprinkler), and sends status updates to a user via Telegram bot. The ESP8266/ESP32 manages the cloud communication.

### **Hardware Used**
---
- MQ Gas Sensor  
- IR Fire Sensor  
- 16x2 LCD Display  
- Servo Motor  
- Sprinkler (Relay Based)  
- Buzzer  
- ESP8266 / ESP32  
- WiFi Router  
- Power Supply  

### **Software Used**
---
- Arduino IDE (for coding and uploading)  
- Telegram App (for receiving alerts)  

### **Libraries Used**
---
- LiquidCrystal  
- Servo  
- WiFi / WiFiClientSecure  
- UniversalTelegramBot  
- ArduinoJson  

### **Algorithm Used**
---
- Continuously read gas sensor (analog) and fire sensor (digital)  
- If gas level > threshold → trigger buzzer, open servo door  
- If fire detected → activate buzzer and sprinkler  
- Format the alert string and send via Telegram bot using WiFi  
- Command options via Telegram: `/start`, `/led_on`, `/led_off`, `/state`  

### **How It Works**
---
1. System boots and connects to WiFi  
2. LCD displays real-time gas and fire readings  
3. If gas value > 300 → buzzer ON, servo door opens  
4. If fire sensor reads high → buzzer ON, sprinkler activated  
5. ESP receives alerts via serial and forwards them to Telegram  
6. Telegram bot responds to user commands and notifies emergencies  
