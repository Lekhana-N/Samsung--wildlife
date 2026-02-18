📌 Project Overview

The IoT-Based Wildlife Alert & Monitoring System is a real-time embedded system designed to detect wildlife intrusion and instantly notify authorities or property owners.

The system uses a Raspberry Pi, multiple sensors, cloud monitoring via Blynk, and alert mechanisms including:

📧 Email Notifications

📱 WhatsApp Alerts (via Twilio)

🔔 Buzzer Alarm

💡 LED Visual Indicator

🌡️ Live Temperature & Humidity Monitoring

This project is ideal for:

Farms & agricultural land protection

Forest boundary monitoring

Smart wildlife conservation systems

Rural property intrusion detection

🛠️ Technologies & Components Used
💻 Hardware

Raspberry Pi

DHT11 Temperature & Humidity Sensor

PIR Motion Sensor

Touch Sensor

Ultrasonic Sensor (TRIG & ECHO)

Buzzer

LED

Jumper wires & Breadboard

🧠 Software & Libraries

Python 3

RPi.GPIO

adafruit_dht

blynklib

Twilio API

SMTP (Gmail)

⚙️ System Architecture

Sensors continuously monitor environment.

When Touch Sensor is triggered:

LED turns ON

Buzzer activates

Email is sent

WhatsApp alert is sent

DHT11 sensor continuously updates:

Temperature → Blynk Virtual Pin V0

Humidity → Blynk Virtual Pin V1

Alerts are prevented from repeating continuously using a flag mechanism.

🔌 GPIO Pin Configuration
Component	GPIO Pin
Ultrasonic TRIG	20
Ultrasonic ECHO	21
PIR Sensor	26
Touch Sensor	17
Buzzer	12
LED	16
DHT11	GPIO 4
📱 Cloud Integration
🔹 Blynk IoT Platform

Used for real-time temperature & humidity monitoring.

Virtual Pin V0 → Temperature

Virtual Pin V1 → Humidity

🔹 Twilio WhatsApp API

Sends instant WhatsApp alerts when intrusion is detected.

🔹 SMTP (Gmail)

Sends email alerts for wildlife detection.

🚀 How It Works
System Start
     ↓
Sensors Monitor Environment
     ↓
Touch Detected?
     ↓ Yes
Turn ON LED & Buzzer
     ↓
Send Email Alert
Send WhatsApp Alert
     ↓
Reset When Touch Released
