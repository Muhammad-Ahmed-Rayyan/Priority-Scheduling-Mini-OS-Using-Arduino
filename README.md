<div align="center">


# 🧠 Priority-Based Scheduling Mini OS (Arduino)

*Simulating Core Operating System Scheduling Concepts on Embedded Hardware*

![C++](https://img.shields.io/badge/Language-C%2B%2B-orange)
![Last Commit](https://img.shields.io/github/last-commit/Muhammad-Ahmed-Rayyan/Priority-Scheduling-Mini-OS-Using-Arduino)

<br>

Built with the tools and technologies:

![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)


</div>

---

## 📌 Project Overview

This project implements a **Priority-Based CPU Scheduling Mini Operating System** using an **Arduino Uno**, inspired by core **Operating System concepts**.

The system dynamically schedules tasks based on **priority levels determined by a potentiometer**, while a **manual interrupt button** preempts all tasks — simulating **real-time OS behavior**.

System activity is visualized using:
- LEDs
- Active buzzer
- 16×2 I2C LCD display

---

## 🎯 Objectives

- Demonstrate **Priority-Based Scheduling**
- Simulate **preemptive multitasking**
- Implement **interrupt-driven execution**
- Visualize OS task execution using hardware
- Bridge **theoretical OS concepts** with embedded systems

---

## 🧠 Operating System Concepts Mapping

| OS Concept              | Arduino Implementation           |
|------------------------|----------------------------------|
| Kernel                 | Arduino Sketch                   |
| Scheduler              | `loop()` function                |
| Processes              | LED & buzzer tasks               |
| Priority Scheduling    | Potentiometer input              |
| Preemption             | External interrupt (button)      |
| Interrupt Handling     | ISR (`manualResetISR`)            |
| System Monitor         | 16×2 I2C LCD                     |

---

## 🔧 Hardware Requirements

- Arduino Uno
- 16×2 I2C LCD
- 10kΩ Potentiometer
- Green LED
- Yellow LED
- Red LED
- Active Buzzer
- Push Button
- 220Ω Resistors (×3)
- Breadboard & Jumper Wires

---

## 🔌 Hardware Connections

| Device        | Device Pin  | Arduino Pin | Notes                    |
|--------------|------------|-------------|--------------------------|
| Green LED    | Anode (+)  | D7          | 220Ω resistor            |
| Yellow LED   | Anode (+)  | D8          | 220Ω resistor            |
| Red LED      | Anode (+)  | D10         | 220Ω resistor            |
| Active Buzzer| +          | D9          | Digital output           |
| Potentiometer| Middle Pin | A0          | Priority control         |
| I2C LCD      | SDA        | A4          | I2C Data                 |
|              | SCL        | A5          | I2C Clock                |
| Push Button  | One leg    | D2          | Interrupt (INPUT_PULLUP)|
|              | Other leg  | GND         | —                        |

---

## ⚙️ Priority Logic

| Input Range / Event | Priority Level | Output Action            |
|-------------------|---------------|--------------------------|
| 0 – 341           | Low           | Green LED                |
| 342 – 682         | Medium        | Yellow LED               |
| 683 – 1023        | High          | Red LED + Buzzer         |
| Button Press      | Highest       | Manual Reset (Interrupt) |

---

## 🧪 System Workflow

1. System boots and initializes OS
2. Scheduler continuously monitors input
3. Potentiometer value determines priority
4. Highest-priority task executes
5. Button interrupt preempts all tasks
6. LCD displays current task & input value

---

## 📂 Repository Structure

Priority-Scheduling-Mini-OS-Using-Arduino/
│
├── Arduino.txt
└── README.md


---

## ▶️ How to Run

1. Open **Arduino IDE**
2. Paste the arduino.txt code in sketch
3. Connect Arduino Uno board
4. Upload the code
5. Adjust potentiometer to change task priority
6. Press button to trigger **manual reset interrupt**

---

<div align="center">

⭐ If you like this project, give it a star on GitHub!

</div>
