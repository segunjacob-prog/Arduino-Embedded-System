# Project 01: Arduino LED Control System

![Project Banner](circuit/project-banner.png)

**Project Type:** Embedded Systems  
**Platform:** Arduino Uno R3  
**Programming Language:** C++ (Arduino)  
**Difficulty:** Beginner  
**Status:** Simulation Verified

---

## 1. Project Overview

The Arduino LED Control System is a beginner-level embedded systems project that demonstrates how a microcontroller controls an external electronic component through a digital output pin.

The project uses an Arduino Uno R3 to switch an external LED ON and OFF at one-second intervals.

A 330Ω resistor is connected in series with the LED to limit current and protect the component from excessive current.

## 2. Project Objectives

- Understand basic Arduino digital output operations.
- Learn how to connect an LED to a microcontroller.
- Understand LED polarity.
- Apply Ohm's law to calculate electrical current.
- Understand `pinMode()`, `digitalWrite()` and `delay()`.
- Practise circuit simulation and hardware implementation.

## 3. Components Required

| Component | Quantity |
|---|---:|
| Arduino Uno R3 | 1 |
| Red LED | 1 |
| 330Ω resistor | 1 |
| Breadboard | 1 |
| Jumper wires | As required |

## 4. Circuit Design and Connections

The circuit uses the following connections:

1. Arduino digital pin 13 connects to one end of the 330Ω resistor.
2. The other end of the resistor connects to the LED anode (long leg).
3. The LED cathode (short leg) connects to Arduino GND.

The resistor and LED are connected in series.

## 5. Electronics Theory

### 5.1 Ohm's Law

Ohm's law describes the relationship between voltage, current and resistance.

**V = IR**

Where:

- V = Voltage (volts)
- I = Current (amperes)
- R = Resistance (ohms)

### 5.2 Current-Limiting Resistor Calculation

Assumed values:

- Arduino output voltage = 5V
- Red LED forward voltage = 2V
- Resistance = 330Ω

Voltage across the resistor:

VR = 5V − 2V = 3V

Using Ohm's law:

I = VR / R

I = 3 / 330

I = 0.00909A

**Theoretical LED current ≈ 9.09mA**

The resistor limits current flowing through the LED and helps prevent damage.

*Note: Actual current depends on the LED forward voltage and the Arduino output voltage under load.*

## 6. Arduino Source Code

```cpp
// Project 01: Arduino LED Control System

int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(1000);

  digitalWrite(ledPin, LOW);
  delay(1000);
}
```

## 7. Code Explanation

| Instruction | Function |
|---|---|
| `int ledPin = 13;` | Stores the LED pin number |
| `setup()` | Runs once when the Arduino starts |
| `pinMode()` | Configures pin 13 as an output |
| `loop()` | Repeats continuously |
| `digitalWrite(HIGH)` | Sets the output HIGH |
| `digitalWrite(LOW)` | Sets the output LOW |
| `delay(1000)` | Pauses execution for 1,000 milliseconds |

## 8. Testing and Results

### Expected Behaviour

| Test | Expected Result |
|---|---|
| Arduino powered | Program starts |
| Pin 13 HIGH | LED turns ON |
| 1-second delay | LED remains ON |
| Pin 13 LOW | LED turns OFF |
| Second 1-second delay | LED remains OFF |
| Loop repeats | LED continuously blinks |

**Simulation result:** Successfully simulated. The LED switches ON and OFF repeatedly at one-second intervals.

**Physical hardware result:** To be recorded separately after physical testing.

## 9. Engineering Knowledge Gained

This project introduced:

- Basic electrical circuit construction.
- LED polarity identification.
- Current-limiting resistor selection.
- Ohm's law application.
- Arduino digital output programming.
- Basic embedded C++ programming.
- Circuit simulation and testing.

## 10. Project Evidence

The following evidence will be maintained:

- [ ] Wokwi simulation screenshot.
- [ ] Circuit diagram or schematic.
- [ ] Physical circuit photograph.
- [ ] Short demonstration video.
- [ ] Source code.

## 11. Future Improvements

Possible extensions include:

- Controlling multiple LEDs.
- Implementing different blinking patterns.
- Introducing push-button control.
- Using `millis()` for non-blocking timing.
- Building an automatic traffic-light system.

## 12. Conclusion

This project introduced the fundamental relationship between electronic circuits and microcontroller programming.

It established a foundation for more advanced embedded systems projects involving sensors, actuators, automation and robotics.

---

**Project Series:** Arduino and Embedded Systems Learning Journey  
**Portfolio:** TechwithJacobs  
**Discipline:** Mechatronics Engineering | Embedded Systems | IoT