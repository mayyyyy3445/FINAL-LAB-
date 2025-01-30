# FINAL-LAB-


This circuit shows an Arduino Uno connected to a push button with a pull-down resistor.

Components and Connections:
	1.	Arduino Uno – The microcontroller.
	2.	Push Button – Connected to the Arduino to detect user input.
	3.	Resistor (likely 10kΩ) – Used as a pull-down resistor to ensure the button reads LOW when not pressed.
	4.	Connections:
	•	One side of the button connected to 5V (red wire).
	•	Other side of the button connected to:
	•	A digital pin (blue wire, likely pin 2 or 3).
	•	GND through a pull-down resistor (black wire).

How It Works:
	•	Button Released (Not Pressed):
	•	The input pin reads LOW (0V), since the pull-down resistor keeps it grounded.
	•	Button Pressed:
	•	The input pin reads HIGH (5V), since the circuit connects to power.

Arduino Code Example:

const int buttonPin = 2;  // Push button connected to pin 2
const int ledPin = 13;    // Built-in LED on pin 13

void setup() {
  pinMode(buttonPin, INPUT);  // Set button pin as input
  pinMode(ledPin, OUTPUT);    // Set LED pin as output
}

void loop() {
  int buttonState = digitalRead(buttonPin);  // Read button state

  if (buttonState == HIGH) {  // If button is pressed
    digitalWrite(ledPin, HIGH);  // Turn LED on
  } else {
    digitalWrite(ledPin, LOW);  // Turn LED off
  }
}


