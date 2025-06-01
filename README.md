# Smart Irrigation
Smart Irrigation using IoT
A smart irrigation system using IoT leverages sensors, microcontrollers, and cloud connectivity to automate water delivery based on real-time soil moisture conditions. The core of such a system involves reading soil moisture data, making decisions based on pre-defined thresholds, and controlling a water pump or valve. 
Here's a more detailed breakdown of the components and code involved:


 **Hardware Components:****

Microcontroller: An ESP8266 or ESP32, or Arduino Uno, acts as the brain of the system, reading sensor data and controlling the pump. 
Soil Moisture Sensor: Measures the moisture content of the soil. 
DHT Sensor (DHT11 or DHT22): Measures temperature and humidity. 
Relay Module: Controls the water pump's on/off state. 
Water Pump: Delivers water to the irrigation system. 
Optional: LCD display for local feedback. 
Optional: WiFi module for cloud connectivity. 

**Explanation of the Code:**
The code initializes the DHT sensor and sets up the required pins.
getSoilMoisture() function reads the analog value from the soil moisture sensor and maps it to a percentage (0-100).
The loop() function continuously reads the soil moisture and checks if it's below the defined threshold.
If the moisture level is below the threshold, it turns the pump on for a specified duration (e.g., 5 seconds) and then off.
The code also includes WiFi connectivity for remote monitoring and control (e.g., using platforms like Blynk or Thingspeak). 
