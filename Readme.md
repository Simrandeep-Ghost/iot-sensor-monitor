---

## 🏗️ Architecture

ESP32 Sensor → MQTT Broker → Processing Service → Dashboard  
                          ↓  
                     Data Storage

---

## 🧠 System Design

- ESP32 sends sensor data using MQTT
- MQTT broker receives and distributes messages
- Processing service reads data and checks conditions
- Dashboard shows real-time values

---

## ⚡ Performance

- Data updates in near real-time (~100–300ms delay)
- Works with multiple sensor messages
- Lightweight communication using MQTT

---

## ⚖️ Trade-offs

- MQTT used instead of HTTP for faster updates
- Simple design used instead of complex microservices
- Not optimized for large-scale production yet
