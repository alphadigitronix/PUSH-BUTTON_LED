# 🔘 Push Button Controlled LED

A simple Arduino-based project that controls an LED using a push button.

When the push button is pressed, the LED turns ON. When the button is released, the LED turns OFF.

---

## 📌 Abstract

The Push Button Controlled LED project demonstrates basic digital input and output control using an Arduino Uno.

A push button is connected to a digital input pin, while an LED is connected to a digital output pin. The Arduino continuously reads the state of the push button and controls the LED accordingly.

The project also uses the Arduino's built-in `INPUT_PULLUP` feature, which eliminates the need for an external pull-up resistor.

This project provides a basic understanding of digital input, digital output, conditional statements, and simple hardware interfacing.

---

## 🎯 Objectives

- Understand digital input using a push button.
- Control an LED using Arduino.
- Learn how to use `INPUT_PULLUP`.
- Understand basic `if-else` logic.
- Learn simple Arduino hardware interfacing.

---

## 🧰 Components Required

| Component | Quantity |
|---|---:|
| Arduino Uno | 1 |
| Push Button | 1 |
| LED | 1 |
| 220Ω Resistor | 1 |
| Breadboard | 1 |
| Jumper Wires | As required |

---

## 🔌 Circuit Connections

### 🔘 Push Button → Arduino Uno

| Push Button | Arduino Uno |
|---|---|
| Terminal 1 | D2 |
| Terminal 2 | GND |

The Arduino internal pull-up resistor is used.

### 💡 LED → Arduino Uno

| LED | Arduino Uno |
|---|---|
| Anode (+) | D8 through 220Ω resistor |
| Cathode (-) | GND |

---

## 🔗 Connection Diagram

```text
                 ARDUINO UNO
              ┌───────────────┐
              │               │
        D2 ───┤               │
              │               │
        D8 ───┤               │
              │               │
       GND ───┤               │
              └───────┬───────┘
                      │
              ┌───────┴───────┐
              │               │
              ▼               ▼

          🔘 PUSH BUTTON     💡 LED
               │              │
               │             220Ω
               │              │
              GND            D8
                             
         LED Cathode → GND



⚙️ Working Principle

The push button acts as the input device, while the LED acts as the output device.

The Arduino continuously reads the state of the push button through digital pin D2.

Since INPUT_PULLUP is used:

When the button is not pressed, the Arduino reads HIGH.
When the button is pressed, the Arduino reads LOW.
When LOW is detected, Arduino turns the LED ON.
When HIGH is detected, Arduino turns the LED OFF.
🔄 System Logic
              ┌───────────┐
              │   START   │
              └─────┬─────┘
                    │
                    ▼
          ┌──────────────────┐
          │ Read Push Button │
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ Button Pressed?  │
          └───────┬─────┬────┘
                  │     │
                YES      NO
                  │       │
                  ▼       ▼
             ┌───────┐ ┌────────┐
             │LED ON │ │LED OFF │
             └───┬───┘ └───┬────┘
                 │           │
                 └─────┬─────┘
                       │
                       ▼
                 Read Again
📊 Expected Output
Button State	Arduino Input	LED Output
🔘 Button Pressed	LOW	💡 ON
⬆️ Button Released	HIGH	⚫ OFF
Example
Button Pressed
↓
Arduino detects LOW
↓
LED ON 💡
Button Released
↓
Arduino detects HIGH
↓
LED OFF
🧪 Tinkercad Simulation

The project can be simulated using Tinkercad Circuits.

🔗 Open Tinkercad Simulation

Replace YOUR_TINKERCAD_LINK_HERE with your actual Tinkercad simulation link.

🚀 How to Run
1️⃣ Open the Project

Open the Tinkercad simulation or build the circuit using the physical components.

2️⃣ Make the Connections

Connect:

Push Button → D2 + GND
LED → D8 through 220Ω resistor
LED Cathode → GND
3️⃣ Open Arduino IDE

Open the Arduino source file:

PUSH_BUTTON_LED.ino
4️⃣ Select Board

In Arduino IDE, select:

Board → Arduino Uno
5️⃣ Upload the Program

Connect the Arduino Uno to your computer and upload the program.

6️⃣ Test the System

Press the push button.

Expected result:

🔘 Button Pressed
        ↓
    💡 LED ON

Release the button:

⬆️ Button Released
        ↓
    ⚫ LED OFF
🌟 Features
🔘 Push button input
💡 LED output control
🔄 Digital input/output
⚡ Internal pull-up resistor
💻 Simple Arduino programming
🧪 Tinkercad simulation
🔧 Easy hardware implementation
🔮 Future Improvements
Add multiple push buttons.
Control multiple LEDs.
Implement push-button ON/OFF toggle.
Add a buzzer.
Add an LCD display.
Create a password-based control system.
Control a relay using the push button.
