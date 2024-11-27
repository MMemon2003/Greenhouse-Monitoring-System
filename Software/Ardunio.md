# What is Ardunio?
The Arduino platform was used to program and interface all the sensors, including the DS18B20 temperature sensor, LDR, LCD screen, potentiometer, and relay. While the Arduino served as the programming environment, the actual hardware implementation was carried out on the ATmega328P microcontroller, which connected and managed all the sensors and components in the system. This setup allowed efficient sensor integration and control within the Greenhouse Monitoring System.
# Use for in this code
LCD libraries: "LiquidCrystal.h" & "rgb_lcd.h," used for LiquidCrystal Library and Grove LCD RGB Backlight were utilised.  

DS18B20 Temperature Sensor libraries: "Onewire.h" & "DallasTemperature.h" used for the purpose of this DS18 is to measure the temperature of soil in a real-world environment.

DHT22 Humidity Sensor libraries: "Adafruit DHT Library" used to allow the functions that include DHT.getTemperature or DHT.getHumidity, which allowed users to obtain the temperature or humidity data, respectively. 
