# Arduino Dev Kit 2-Layer PCB

##  Introduction

**Arduino Dev Kit 2-Layer PCB** is a versatile, entry-level development board designed specifically for educational purposes and soldering workshops. Based on the popular **ATmega328P** microcontroller, it serves as a robust platform for students to learn both hardware assembly and embedded programming.

The board mirrors the classic **Arduino Nano** pinout and functionality but features modern enhancements like a **USB-C connector** for power and communication. It also integrates user-controllable peripherals, making it an all-in-one "lab on a board" for university courses.

---

##  Table of Contents

- Introduction  
- Project Overview  
- Key Features  
- System Architecture  
- Hardware Components  
- Interfaces and Connections  
- Power Supply  
- Installation & Assembly  
- Usage  
- Troubleshooting  

---

##  Project Overview

The goal of this project is to provide a comprehensive **educational soldering kit** that results in a fully functional Arduino-compatible development board. Key objectives include:

- Teaching **SMD and THT soldering** techniques to students.
- Providing a standard **ATmega328P** environment for firmware development.
- Ensuring modern connectivity via **USB-C**.
- Including built-in peripherals (**Buzzer, LEDs**) for immediate "Hello World" feedback.
- Maintaining compatibility with standard breadboards and Arduino IDE.

---

##  Key Features

- **Microcontroller:** ATmega328P (8-bit AVR).
- **USB-to-Serial:** CH340 interface for seamless programming.
- **Form Factor:** Compact 2-layer PCB with Arduino Nano-compatible pinout.
- **User Peripherals:**
  - Integrated **Buzzer** for acoustic feedback.
  - Multiple **User LEDs** for status indication and debugging.
- **Connectivity:** USB-C connector for modern cables.
- **Standard GPIO:** Full access to Digital, Analog, PWM, and I2C/SPI pins.
- **Reset Button:** Tactile switch for easy firmware restarts.

---

##  System Architecture

The board architecture focuses on simplicity and accessibility:

- **Processing Core:** ATmega328P running at 16MHz.
- **Communication Bridge:** CH340 chip converts USB-C signals to UART for the MCU.
- **I/O Logic:** All GPIOs are broken out to standard 2.54mm pitch headers.
- **Feedback Loop:** Dedicated traces connect specific GPIOs to the onboard buzzer and LEDs.

<img width="1747" height="1156" alt="Screenshot 2026-02-11 154807" src="https://github.com/user-attachments/assets/b7d022e7-f97a-47a6-982e-c4d25b382d53" />

---

##  Hardware Components

| Component | Description |
|-----------|-------------|
| **MCU** | ATmega328P (AU package) |
| **USB Interface** | CH340 Serial-to-USB Converter |
| **USB Connector** | USB-C (Power + Data) |
| **Buzzer** | Magnetic or Piezo transducer |
| **User LEDs** | General purpose LEDs (various colors) |
| **Oscillator** | 16MHz Crystal / Resonator |
| **Voltage Regulator** | 5V and 3.3V LDOs for stable operation |

<img width="1208" height="903" alt="Screenshot 2026-02-11 154814" src="https://github.com/user-attachments/assets/33567e8d-456e-429b-946f-79df36f67c59" />

---

##  Interfaces and Connections

### GPIO Headers
- **Digital Pins:** D0 - D13 (including PWM support).
- **Analog Pins:** A0 - A7.
- **Power Rails:** 5V, 3.3V, and multiple GND pins.

### USB Interface
- **USB-C Port:** Used for uploading sketches via Arduino IDE and powering the board.

### User Interaction
- **Buzzer:** Connected to a PWM-capable pin for frequency control.
- **LEDs:** Connected to user-defined GPIOs with current-limiting resistors.

---

##  Power Supply

- **Input:** 5V via USB-C.
- **On-board Regulation:** - **5V Rail:** Direct from USB or via LDO.
  - **3.3V Rail:** Provided for low-power sensors and peripherals.
- **Protection:** Includes decoupling capacitors to minimize noise during switching.

---

##  Installation & Assembly

1. **PCB Fabrication:** Order the 2-layer board using the provided Gerber files.
2. **USB-C & CH340:** Solder the USB-C connector and the CH340 chip first (finer pitch).
3. **Microcontroller:** Solder the ATmega328P and the 16MHz crystal.
4. **Passives:** Install SMD resistors, capacitors, and LEDs.
5. **THT Components:** Solder the tactile reset button, buzzer, and pin headers.
6. **Testing:** Check for shorts between VCC and GND before plugging into a computer.

---

##  Usage

1. Connect the board to a PC using a **USB-C cable**.
2. Install the **CH340 drivers** if not already present on your system.
3. Open the **Arduino IDE**.
4. Select **"Arduino Nano"** as the board and **"ATmega328P"** as the processor.
5. Write your code (e.g., a simple "Blink" or "Buzzer Melody").
6. Click **Upload** and interact with your custom-built hardware!

---

##  Troubleshooting

| Issue | Possible Cause |
|-------|----------------|
| **Board not recognized** | Faulty USB-C cable or missing CH340 drivers. |
| **Upload Error** | Incorrect board/processor selected in IDE or soldering bridge on UART lines. |
| **LED/Buzzer not working** | Incorrect component polarity (reversed LED) or cold solder joint. |
| **No Power** | Short circuit in the 5V rail or damaged USB-C port pins. |
