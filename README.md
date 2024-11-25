# Greenhouse-Monitoring-System
This project involves designing and construction of a greenhouse environtmental controller, that allows gardener(user) to see the temperature,humidity,and the light level, it also has a fan that turns on to allow cooling to the area.
This device is sutiable for the agriculture and inductrail environment, so that garden crops for the user are kept in a sutiablle condition. 

# Sensors 
- Temperature (DS1820 Sensor) - used for the temperature
- Humidity (DHT22 Sensor) - used for the Humidity
- Light Intensity (LDR Sensor) - used for the light level
- HD44780 LCD screen -  used for real-time data 
- Parameters - potentiometer to allow manual adjustment

# Software
- Algorithm Design - 
Software checks assigned pins for connected sensors.
Reads and refreshes sensor data continuously.
Outputs data to:
LCD Display: Cycles through sensor readings (temperature, luminance, humidity).
Fan: Automatically turns on/off based on preset temperature thresholds.
- LCD Programming - 
Libraries Used:
LiquidCrystal.h for standard LCDs.
rgb_lcd.h for Grove RGB Backlight LCDs.
Features:
Displays "Intermission" briefly before showing sensor data.
Sensor data displayed in a menu format using a switch statement.
- Sensor Measurements - 
Soil Temperature:
DS18 Temperature Sensor:
Utilizes OneWire and DallasTemperature libraries.
Measures soil temperature in real-time.
Humidity & Ambient Temperature:
DHT20 Sensor:
Utilizes DHT20 library.
Functions: DHT.read(), DHT.getTemperature(), DHT.getHumidity().
Light Level:
LDR Illuminator:
Measures ambient luminance levels.
Fan Control
Modes:
Manual Mode: Adjust fan speed via potentiometer.
Automatic Mode: Fan controlled by DS18 Temperature Sensor.
Activates when temperature exceeds 25°C.

# Hardware Design 
- Temperature Measurement (DS18 Temperature Sensor): - 
Pins:
VCC: Pin 20
SDA: Pin 27
SCL: Pin 28
GND: Pin 17
Function: Measures soil temperature for real-time monitoring.

- Humidity Measurement (DHT20 Sensor): - 
Pins:
VCC: Pin 20
SDA: Pin 27
SCL: Pin 28
GND: Pin 17
Function: Measures humidity and ambient temperature.

- Light Measurement (LDR Light Sensor): - 
Function: Monitors ambient luminance levels for light detection.
Fan Control
Manual Control:
Adjust fan speed using a potentiometer.
Automatic Control:
Trigger: DS18 Temperature Sensor activates fan when the temperature exceeds a set threshold (e.g., 25°C).
Purpose:
Provides cooling to a specific area as needed.

