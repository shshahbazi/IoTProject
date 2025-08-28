# IoTProject

This repository contains the final project for the **Internet of Things Programming** course.  
The project demonstrates how to integrate **Arduino (ESP8266 Wi-Fi module)**, a **Django web server**, and a **Telegram bot** to remotely control and monitor IoT devices.  

---

##  Features
- Control an LED connected to the Arduino board via **local Wi-Fi** or the **Internet**.  
- Run a **Django web server** to store and display data.  
- Control the device remotely using a **Telegram bot**.    

---

##  Requirements
- **Hardware:**
  - ESP8266 Wi-Fi module
  - LED + Resistor
- **Software:**
  - [Arduino IDE](https://www.arduino.cc/en/software)
  - Python 3.12
  - Django 5.0
  - Telegram Bot API (Python library)

---

## Setup & Usage

### 1\. Arduino

1.  Open the .ino files in Arduino IDE (local.ino, telegram.ino, web_server.ino).
  
2.  Configure Wi-Fi credentials inside the code:
    ```
    const char* ssid = "YOUR_WIFI_SSID";
    const char* password = "YOUR_WIFI_PASSWORD";
    ```
    
4.  Upload the code to the ESP8266 board.
    

### 2\. Django Server

Run the web server:
  ```
 cd IoTProject/IoTProjectServer
 python manage.py migrate
 python manage.py runserver
 ```

Access the server at: http://127.0.0.1:8000/

### 3\. Telegram Bot

1.  Create a Telegram bot using BotFather.
    
2.  Copy your bot token into `telegram_bot.py`.
    
3.  ```python telegram_bot.py```
    

Now you can send commands via Telegram to control the device.

---
