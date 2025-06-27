# 🔥 LPG/CNG Gas and Fire Detection System with Telegram Alerts

## **Project Summary**
---
This project is an IoT-based safety system that detects LPG/CNG gas and fire using appropriate sensors. It provides real-time alerts through a buzzer, LCD display, and a sprinkler system. Alerts are also sent remotely via Telegram using an ESP8266 module.

## **Abstract**
---
The system uses a gas sensor to monitor LPG/CNG levels and a fire sensor to detect flames. If either crosses the safety threshold, the system activates a buzzer and sprinkler, displays the values on an LCD, and sends an emergency message through a Telegram bot using Wi-Fi.

## **Introduction**
---
This embedded system enhances fire and gas safety in indoor environments. It combines sensor-based monitoring with IoT-based remote alerting to provide timely warnings and automatic response actions. Arduino handles the local logic, while ESP8266 takes care of Telegram communication.

## **Hardware Used**
---
- MQ Gas Sensor  
- IR Fire Sensor  
- 16x2 LCD Display  
- Buzzer  
- Relay-connected Sprinkler  
- ESP8266 Wi-Fi Module  
- Arduino UNO  
- Power Supply  

## **Software Used**
---
- Arduino IDE  
- Telegram App  

## **Libraries Used**
---
- LiquidCrystal  
- WiFi / WiFiClientSecure  
- UniversalTelegramBot  
- ArduinoJson  

## **Algorithm Used**
---
1. Arduino reads gas and fire sensor values.
2. LCD displays the sensor data in real time.
3. If gas value > 300:
   - Buzzer is activated.
   - Message is sent to ESP via Serial.
4. If fire is detected:
   - Buzzer is activated.
   - Sprinkler is turned ON through relay.
   - Message is sent to ESP via Serial.
5. ESP8266 sends the received message to Telegram using a bot.

## **How It Works**
---
- On startup, Arduino initializes sensors and LCD.
- System reads gas and fire inputs continuously.
- On danger detection, it activates buzzer and sprinkler.
- Simultaneously, ESP8266 sends a message to a preconfigured Telegram chat to alert the user.
