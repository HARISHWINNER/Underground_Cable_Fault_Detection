<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
<body>
    <div class="container">
        <h1>Underground Cable Fault Detection System using Arduino</h1>
        <h2>Introduction</h2>
        <p>This project demonstrates an underground cable fault detection system using Arduino. The system detects faults in underground cables and indicates the fault location to the user via an LCD display.</p>
        <h2>Components Required</h2>
        <ul>
            <li>Arduino Uno</li>
            <li>LCD Display (16x2)</li>
            <li>Relays</li>
            <li>Resistors</li>
            <li>LEDs</li>
            <li>Diodes (1N4007)</li>
            <li>Buzzer</li>
            <li>Switches</li>
            <li>ULN2003A</li>
        </ul>
        <h2>Circuit Diagram</h2>
        <div class="image-container">
            <img src="How to make a Underground Cable Fault Detection using Arduino.png" alt="Underground Cable Fault Detection Circuit Diagram">
        </div>
        <h2>Working Principle</h2>
        <p>The system works by sending a signal through the cable and measuring the return signal. If a fault is detected, the location of the fault is displayed on the LCD screen. The fault is indicated by turning on the corresponding LED and sounding a buzzer.</p>
        <h2>Code</h2>
        <p>Below is the sample Arduino code used in this project:</p>
        <pre>
<code>
#include &lt;LiquidCrystal.h&gt;

const int rs = 7, en = 8, d4 = 9, d5 = 10, d6 = 11, d7 = 12;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() {
  lcd.begin(16, 2);
  lcd.print("Cable Fault");
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
}

void loop() {
  // Your fault detection logic here
  lcd.setCursor(0, 1);
  lcd.print("Detection System");
}
</code>
        </pre>

  <h2>How to Run</h2>
        <ol>
            <li>Connect the components as shown in the circuit diagram.</li>
            <li>Upload the Arduino code to your Arduino Uno.</li>
            <li>Power on the system.</li>
            <li>Observe the LCD display for fault locations.</li>
        </ol>
      <h2>Conclusion</h2>
        <p>This underground cable fault detection system is a simple and effective way to monitor and locate faults in underground cables. It can be further enhanced with more advanced fault detection algorithms and components.</p>
        <h2>License</h2>
        <p>This project is licensed under the MIT License.</p>
    </div>
</body>
</html>
