# How to Run This Project

## Required Libraries

To run this project successfully, install the following libraries in the Arduino IDE.

### DHT Sensor Library
1. Open Arduino IDE  
2. Go to Sketch → Include Library → Manage Libraries  
3. Search for: **DHT sensor library by Adafruit**  
4. Click Install  
5. Also install **Adafruit Unified Sensor** if prompted  

### LiquidCrystal_I2C Library
1. Open Library Manager  
2. Search for: **LiquidCrystal I2C**  
3. Install **LiquidCrystal I2C by Frank de Brabander** or **by Marco Schwartz**

---

## Arduino IDE Setup

### Configuration

| Setting | Value |
|--------|-------|
| Board | Arduino Uno |
| Port | Select your COM port |
| Programmer | AVRISP mkII |

To set this:
1. Go to Tools → Board → Arduino Uno  
2. Go to Tools → Port → Select COM Port  
3. Go to Tools → Programmer → AVRISP mkII  

---

## Uploading the Code

1. Connect Arduino Uno to your computer using USB cable  
2. Open the `.ino` file in Arduino IDE  
3. Click **Verify** to compile the code  
4. Click **Upload** to upload the code to Arduino  
5. After uploading, open **Serial Monitor**  
6. Set baud rate to **9600**  

---

## How the System Should Work

After powering the system:

| Feature | Expected Behavior |
|--------|-------------------|
| LCD Display | Shows temperature, humidity, and plant status |
| Buzzer | Turns ON when soil is very dry |
| Water Pump | Turns ON when soil is dry (moisture > 800) |
| Pump Stops | Turns OFF when soil is wet (moisture < 600) |
| Relay | Controlled through pin D8 |
| Sensors | Update every 1 second |

---

## Testing Procedure

Follow this to test your system:

1. Power ON the system  
2. Check LCD shows temperature and humidity  
3. Put moisture sensor in dry soil → Pump should turn ON  
4. Put moisture sensor in wet soil → Pump should turn OFF  
5. Disconnect DHT11 → Error should appear  
6. Very dry soil → Buzzer should turn ON  

---

## Important Notes

- Ensure all components share a common ground  
- Ensure relay module is connected correctly  
- Use external battery for water pump, do not power pump from Arduino  
- Check relay active HIGH / LOW logic if pump behaves opposite  
- Adjust wetThreshold and dryThreshold based on your soil  

---

This completes the setup and running procedure for the Smart Irrigation System.
