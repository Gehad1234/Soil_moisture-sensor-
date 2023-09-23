# Soil Moisture Monitoring with ThingSpeak Integration
one of semicolon startup IOT projects (My startup) 

### Description

This Arduino project is a soil moisture monitoring system that uses a soil moisture sensor to measure soil moisture levels and sends the data to the ThingSpeak IoT platform. The system is designed for applications such as plant watering automation or agricultural monitoring.

### Components

- **Soil Moisture Sensor**: The project uses a soil moisture sensor connected to analog pin A0 on the NodeMCU to measure soil moisture levels.

- **Wi-Fi Module (ESP8266)**: The ESP8266 Wi-Fi module is used to connect to Wi-Fi and send data to the ThingSpeak platform.

- **OLED Display**: An OLED display is used to visualize the soil moisture data.

### Setup

1. Connect the soil moisture sensor to the NodeMCU:
   - Connect the sensor's analog output pin to analog pin A0 on the NodeMCU.
   
2. Connect the OLED display to the NodeMCU using I2C:
   - Connect the display's SDA pin to the SDA (data) pin on the NodeMCU.
   - Connect the display's SCL pin to the SCL (clock) pin on the NodeMCU.

3. Ensure you have the required libraries installed in your Arduino IDE:
   - Adafruit GFX Library
   - Adafruit SSD1306 Library

4. Replace the placeholders in the code with your specific configuration:
   - `apiKey`: Replace it with your ThingSpeak Write API key.
   - `ssid`: Replace it with your Wi-Fi SSID.
   - `pass`: Replace it with your Wi-Fi password.

5. Upload the code to your NodeMCU board.

### Usage

Once the project is set up and the NodeMCU is powered on, it will continuously read soil moisture measurements from the sensor. The soil moisture data is then displayed on the OLED display and sent to the ThingSpeak platform, allowing you to monitor and analyze soil moisture data over time.

### ThingSpeak Configuration

Make sure you have set up a ThingSpeak channel with the appropriate fields to receive and display the soil moisture data. The channel should match the fields used in the code for data upload.

### Additional Note

- The code calculates the soil moisture percentage based on the sensor readings.
- It uses a delay of 2000 milliseconds (2 seconds) between data updates to ThingSpeak, but ThingSpeak typically requires a minimum of 15 seconds between updates.

### Contributing

Feel free to modify and extend this project to suit your specific needs. You can enhance it by adding additional sensors, data logging features, or integrating it with other IoT platforms. Contributions and improvements are welcome!

### License

This project is open-source and available under an open-source license (mention the specific license used). Please refer to the LICENSE.md file for more details.

### Author

Gehad Abdellah 

### Acknowledgments

Special thanks to the authors and contributors of the libraries used in this project for their work in making this project possible.
