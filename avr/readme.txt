This is a library which will interface a Raspberry Pi with the HC-SR04 ultrasonic sensor through the use of an ATmega328P (internal 8MHz oscillator) for precise ultrasonic sensing. (uses i2C bus between the Pi and AVR)

To use flash the sketch to a suitable AVR (I used avrdude and linuxspi with my raspberry pi as an ISP) and test with the ping_test.py

notes:
-power the avr with 3.3v so 5v doesn't go back to the pi through the i2c pins
-power the sensor with 5V from the pi for stable readings and !!USE A LEVEL SHIFTER ON THE ECHO PIN!! to the avr
-the included hex file is for an ATmega328P with the 8MHz internal oscillator and NO BOOTLOADER


libraries used:
NewPing and RunningMedian (median function in newping had some quirks)