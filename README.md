# Home-Automation-System
This code provides a basic home automation system with web-based control and real-time temperature monitoring.

Block Diagram:
![image](https://github.com/user-attachments/assets/bba79366-4041-4506-82e7-9f2077a5dd4f)


This code sets up an ESP8266 microcontroller with an LCD display, servo motor, and temperature sensor, and allows for control via a web interface. Here’s a breakdown of its functionalities:

1. **Setup and Initialization:**
   - Connects to a Wi-Fi network.
   - Initializes an LCD display, a servo motor, and a temperature sensor.
   - Starts a web server on port 80.

2. **Web Interface:**
   - Provides a web page accessible through the IP address of the ESP8266.
   - The page includes options to:
     - Unlock a door (by rotating the servo motor).
     - Turn a light on or off.

3. **Temperature Monitoring:**
   - Reads temperature data from an LM35 sensor.
   - Displays the temperature on the LCD.
   - Activates a buzzer if the temperature exceeds 50°C.

4. **Web Requests Handling:**
   - **Unlock Door**: When the `/unlock` URL is requested, it rotates the servo motor to unlock the door, updates the LCD to show a welcome message, and changes the status of LEDs.
   - **Turn Light On**: When the `/lights_ON` URL is requested, it turns on a light (by activating an LED) and updates the LCD.
   - **Turn Light Off**: When the `/lights_OFF` URL is requested, it turns off the light and updates the LCD.

5. **LED and Buzzer Control:**
   - Controls an LED (green and red) and a buzzer based on the state of the system.
