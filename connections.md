# Smart Solar-Powered Irrigation System

An automated, eco-friendly irrigation system powered by solar energy. It intelligently monitors soil moisture and environmental conditions to water plants only when necessary, saving water and reducing manual effort.

---

## Components Used

- Solar Panel – Generates renewable energy to power the system  
- DHT11 Sensor – Measures temperature and humidity  
- Buzzer – Sounds an alert when soil is dry  
- Arduino UNO R3 – Central controller for sensors and actuators  
- Breadboard – Used to prototype circuit connections  
- Jumper Wires – Connect components and modules  
- LCD Display (I2C) – Shows sensor data in real-time  
- Relay Module – Controls power to the water pump  
- Rechargeable Batteries – Stores energy from the solar panel  
- Soil Moisture Sensor – Detects soil moisture level  
- Soil – The growth medium for plants  
- Water Pipes – Direct water to the soil  
- Water Pump – Pumps water when soil is dry  

---

## Circuit Connections

### DHT11 Sensor
| DHT11 Pin | Arduino Connection |
|-----------|-------------------|
| VCC | 5V |
| GND | GND |
| DATA | D4 |

---

### Buzzer
| Buzzer Pin | Arduino Connection |
|------------|-------------------|
| + | D7 |
| - | GND |

---

### Soil Moisture Sensor
| Sensor Wire | Arduino Connection |
|--------------|-------------------|
| Brown (GND) | GND |
| Red (VCC) | 5V |
| Yellow (Signal) | A0 |

---

### Relay Module
| Relay Pin | Connection |
|-----------|------------|
| VCC | 5V |
| GND | GND |
| IN | D8 |
| COM | Battery Positive |
| NO | Water Pump Positive |

---

### Water Pump
| Pump Wire | Connection |
|-----------|------------|
| Positive | Relay NO |
| Negative | Battery Negative |

---

### Solar Panel
| Solar Panel | Connection |
|--------------|------------|
| Positive | Battery Positive |
| Negative | Battery Negative |

---

### LCD Display (I2C)
| LCD Pin | Arduino Connection |
|---------|-------------------|
| VCC | 5V |
| GND | GND |
| SDA | A4 |
| SCL | A5 |

---

## Important Notes

- Use a common ground (GND) across all components  
- Add a diode across the pump terminals to prevent back EMF damage  
- Use a voltage regulator if the solar panel output is more than 5V  
- Ensure the relay module has a proper power supply  
- Keep wiring secure to avoid loose connections  

---

## System Working Summary

1. Soil moisture sensor reads soil condition  
2. DHT11 reads temperature and humidity  
3. Arduino processes sensor data  
4. If soil is dry, relay turns ON and pump starts  
5. If soil is wet, relay turns OFF and pump stops  
6. LCD displays plant status and environment data  
7. Buzzer alerts when soil is very dry  

---

This system reduces water usage, automates irrigation, and enables solar-powered smart farming.
