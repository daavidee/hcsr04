<h1>About</h1>
This is a library which will interface a Raspberry Pi with the HC-SR04 ultrasonic sensor through the use of an Atmel AVR for precise ultrasonic sensing. Uses the i2C bus between the Pi and AVR.

<h1>Installation</h1>
Flash the Arduino sketch to a suitable AVR (I used avrdude and linuxspi with my raspberry pi as an ISP) and test with the ping_test.py or the hcsr04 class.

<h1>Notes</h1>
<ol>
	<li>Power the AVR with 3.3v so 5v doesn't go back to the pi through the i2c pins</li>
	<li>Power the sensor with 5V from the pi for stable readings and !!USE A LEVEL SHIFTER ON THE ECHO PIN!! to the AVR</li>
	<li>The included hex file is for an ATmega328P with the 8MHz internal oscillator and NO BOOTLOADER</li>	
	<li>NewPing and RunningMedian libraries used on the sketch</li>
</ol>