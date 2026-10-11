# H2S-alert-system
The  H₂S Gas Safety System detects gas levels and displays readings and safety alerts on the OLED. When gas exceeds the set threshold, the buzzer activates. ESP32 sends live sensor data through Wi-Fi to Firebase, which updates the web dashboard for remote monitoring.
<img width="1200" height="1600" alt="WhatsApp Image 2026-10-11 at 12 35 16 PM" src="https://github.com/user-attachments/assets/7cc6d1e3-9ffc-4d1f-85e3-b9ccbbf79967" />
## Working Principle of  H₂S Gas Safety System

1\. Gas Detection: The H₂S gas sensor continuously monitors the surrounding environment for hydrogen sulfide gas and produces an electrical signal based on the detected gas level.

2\. Data Processing: The ESP32 receives the sensor signal, processes the readings, and calculates the gas level according to the sensor configuration and calibration.

3\. OLED Display: The OLED displays the current gas reading, safety status, and person detection status, allowing users to monitor the system locally.

4\. Gas Leak Alert: When the detected gas level exceeds the configured threshold of 40 ppm, the ESP32 activates the buzzer and displays a danger warning on the OLED.

5\. Person Detection: The PIR sensor detects movement in the monitored area. The ESP32 processes its output and displays whether motion has been detected.

6\. Wi-Fi Communication: The ESP32 connects to Wi-Fi and sends the sensor readings, gas level, person status, date, time, and safety status to Firebase Realtime Database.

7\. Firebase Cloud Storage: Firebase receives and stores the transmitted data, making the latest readings and recorded history available to the web dashboard.

8\. Web Dashboard Monitoring: The web dashboard retrieves data from Firebase and displays gas levels, safety alerts, person status, date, time, and historical readings on laptops and mobile devices.

9\. Real-Time Updates: Whenever new readings are uploaded to Firebase, the dashboard updates automatically, allowing users to monitor the system remotely without refreshing the page.

10\. Safety Monitoring: The system provides local warnings through the OLED and buzzer while enabling remote monitoring through the web dashboard. It helps users identify potentially dangerous gas levels and respond quickly.

