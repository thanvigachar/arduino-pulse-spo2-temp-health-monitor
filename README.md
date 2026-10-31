# Arduino-Pulse-spo2-temp-Health-Monitor

A real-time health monitoring system that tracks heart rate, body
temperature and blood oxygen (SpO2) using sensors connected to an
Arduino Uno. Readings are shown on a 16x2 LCD, an LED indicates abnormal
values, and an ESP8266 Wi-Fi module can send data to ThingSpeak for
remote monitoring.

Developed as a Microprocessor and Computer Architecture Laboratory
project (UE23CS251B), PES University, Jan–May 2025.

## Components

| Component | Purpose |
|-----------|---------|
| Arduino Uno | Microcontroller |
| Pulse sensor | Heart rate (photodiode + LED, analog signal) |
| LM35 | Body temperature |
| MAX30100 / MAX30102 | SpO2 (red and infrared light) and heart rate |
| 16x2 LCD | Displays BPM, temperature and SpO2 |
| ESP8266 Wi-Fi module | Remote data upload (optional) |
| LED | Alert for abnormal readings |

## Circuit connections (MAX30100/30102)

| Sensor pin | Arduino pin |
|------------|-------------|
| VCC | 3.3V |
| GND | GND |
| SCL | A5 (I2C clock) |
| SDA | A4 (I2C data) |

## How it works

1. Sensors measure heart rate, temperature and SpO2.
2. The Arduino reads the values and shows them on the LCD.
3. An LED lights up when a reading is outside the normal range.
4. The ESP8266 sends the data to a ThingSpeak channel over Wi-Fi.

## Setup

1. Install the Arduino IDE and the ESP8266WiFi and ThingSpeak libraries.

## Documentation

- [Project report](docs/MPCA_Lab_Project_Report.docx)
- [Components list](docs/Components_Used.docx)

## Team

Sukrutha D ,Thanvi G Achar ,T G Sanjana

## Future improvements

- Replace placeholder values with live sensor readings in the upload code
- Add configurable thresholds and a buzzer alert
- Add a mobile or web dashboard
