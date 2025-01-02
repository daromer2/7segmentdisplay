# 7segmentdisplay



# Pin Assignments 
Device	Wemos Pin	Notes
* GPS TX	D7 (GPIO13)	Receive pin in SoftwareSerial
* GPS RX	D8 (GPIO15)	Transmit pin in SoftwareSerial
* GPS Power	3.3 V/GND or 5 V/GND	Depends on GPS module requirements; ensure logic-level compatibility
* RTC SCL	D1 (GPIO5)	I²C SCL
* RTC SDA	D2 (GPIO4)	I²C SDA
* DS22 (SCL)	D1 (GPIO5)	Same I²C bus
* DS22 (SDA)	D2 (GPIO4)	Same I²C bus
* WS2812 (Data In)	D4 (GPIO2)	Through ~300–500 Ω resistor
* WS2812 Power	5 V & GND	Large electrolytic capacitor across +5 V and GND near the LED strip
* LED #1	D5 (GPIO14)	Through ~220–330 Ω resistor, then to GND
* LED #2	D6 (GPIO12)	Through ~220–330 Ω resistor, then to GND
- Hardware RX/TX	RX (GPIO3) / TX (GPIO1)	Unused here, available for USB/serial debug
-  Note: For SoftwareSerial, pick pins that support RX. D8 (GPIO15) can be finicky because it’s usually pulled down at boot; if you encounter issues, consider using a different pair like D7 (RX) and D6 (TX), or D7 (RX) and D5 (TX). Always check your chosen pins for SoftwareSerial support in ESP8266.
