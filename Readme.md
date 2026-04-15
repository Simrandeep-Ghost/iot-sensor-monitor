# IoT Smart Sensor Monitor (ESP32 + MQTT)

A beginner-friendly IoT project that reads sensor data (example: temperature/humidity) and publishes it to an MQTT broker so it can be monitored from a dashboard.

## Features
- Reads sensor values on an interval
- Publishes data to MQTT topics (ex: `home/lab/sensor1/temperature`)
- Simple dashboard view (example: Node-RED) + optional alerts

## Tech / Tools
- ESP32 (Arduino framework)
- Sensor (example: DHT11/DHT22/BME280 — any works)
- MQTT broker (Mosquitto recommended)
- Node-RED (optional) for dashboard
- Wi‑Fi network
- Linux machine (Raspberry Pi / Ubuntu) *or* any PC that can run an MQTT broker

## How it works (basic flow)
1. ESP32 reads the sensor
2. ESP32 connects to Wi‑Fi
3. ESP32 publishes readings to MQTT
4. Subscriber (Node-RED / Python / MQTT client) displays readings

## Setup (high level)
1. Flash ESP32 code (Arduino IDE or PlatformIO)
2. Start an MQTT broker (Mosquitto)
3. Subscribe to the topic to verify messages
4. (Optional) Create a Node-RED dashboard

## MQTT topic example
- `lab/sensor/temperature`
- `lab/sensor/humidity`

## Notes
This repo is intended as a learning project. Hardware and exact wiring depend on the sensor you use.

## Future improvements
- Add Wi‑Fi reconnect handling
- Send JSON payloads with timestamp + device ID
- Store data in a database (InfluxDB/Postgres) and graph it
- Add OTA firmware updates
