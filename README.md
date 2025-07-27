Arduino Light & Temperature-Based Control System

Description
This Arduino sketch reads light and temperature values and controls two output devices (like a fan and light) based on:
-> A digital switch
-> Ambient brightness
-> Room temperature

Components Required
-> Arduino Uno/Nano
-> LDR sensor (connected to A5)
-> LM35 Temperature sensor (connected to A4)
-> Digital switch/button (connected to pin 8)
-> Two output devices (e.g., fan, bulb, LEDs) on pins 5 and 6

Pin Configuration
-> Pin 8: Digital Input (Switch)
-> Pin A5: Analog Input (LDR - Light Sensor)
-> Pin A4: Analog Input (LM35 - Temperature Sensor)
-> Pin 5: Digital Output (e.g., Fan)
-> Pin 6: Digital Output (e.g., Light)

Working Logic
1. Reads digital switch (`x`), light (`y`), and temperature (`z`)
2. Converts `z` to Celsius
3. Based on light and temperature, controls output devices
4. Displays all readings in the Serial Monitor

Sample Logic:
-> If switch ON and it's dark and hot → Turn ON both fan and light
-> If switch ON, it's dark but cool → Turn ON fan only
-> If it's bright and hot → Turn ON only fan
-> Else → Turn everything OFF

How to Use
1. Upload the code to your Arduino.
2. Connect sensors and actuators as per pin config.
3. Open Serial Monitor to view live readings.
4. Flip the switch (pin 8) to activate the system.

