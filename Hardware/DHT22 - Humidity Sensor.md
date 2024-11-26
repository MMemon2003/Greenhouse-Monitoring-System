# DHT22 - Humidity Sensor
The DHT22 Humidity and Temperature Sensor measures air temperature and moisture content to provide accurate atmospheric readings. 
This data enables precise adjustments to greenhouse controls.
The sensor converts humidity data—such as relative, absolute, and specific humidity—into electrical signals for processing.

# Pins for the Humidity Sensor 
![{93DFBC9C-EF49-4BC3-9153-5D19A9A93C16}](https://github.com/user-attachments/assets/31d9cbf5-cc5b-4755-a3c8-06e378b5d7a2)

# Schematic design of the DHT22 Sensor
![{51B7A000-66D4-4269-91D9-E1C93A97241E}](https://github.com/user-attachments/assets/9e544262-1330-4a7e-ad2d-0d93abfe28e9)

# DS18 Ardunio Code 
/********************************************************************/
// First we include the libraries
#include <OneWire.h> 
#include <DallasTemperature.h>
/********************************************************************/
// Data wire is plugged into pin 2 on the Arduino 
#define ONE_WIRE_BUS 2 
/********************************************************************/
// Setup a oneWire instance to communicate with any OneWire devices  
// (not just Maxim/Dallas temperature ICs) 
OneWire oneWire(ONE_WIRE_BUS); 
/********************************************************************/
// Pass our oneWire reference to Dallas Temperature. 
DallasTemperature sensors(&oneWire);
/********************************************************************/ 
void setup(void) 
{ 
 // start serial port 
 Serial.begin(9600); 
 Serial.println("Dallas Temperature IC Control Library Demo"); 
 // Start up the library 
 sensors.begin(); 
} 
void loop(void) 
{ 
 // call sensors.requestTemperatures() to issue a global temperature 
 // request to all devices on the bus 
/********************************************************************/
 Serial.print(" Requesting temperatures..."); 
 sensors.requestTemperatures(); // Send the command to get temperature readings 
 Serial.println("DONE"); 
/********************************************************************/
 Serial.print("Temperature is: "); 
 Serial.print(sensors.getTempCByIndex(0)); // Why "byIndex"?  
   // You can have more than one DS18B20 on the same bus.  
   // 0 refers to the first IC on the wire 
   delay(1000); 
} 

