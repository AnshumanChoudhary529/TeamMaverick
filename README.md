# Team Maverick – Formula Student Electronics & EV Systems

Electronics, data acquisition and electric-vehicle safety systems I designed and built as **Data Acquisition (DAQ) Lead** and **EV Lead** of Team Maverick, the Formula Student team of Pune Vidyarthi Griha's College of Engineering, Technology and Management (SPPU), Pune, India.

**Team results:** All India Rank 1 at SAE SUPRA 2025 and All India Rank 2 at SAE SUPRA 2024, among 60+ competing teams.

---

## About the team and my roles

| | |
|---|---|
| **Team** | Team Maverick, 54 members |
| **DAQ Lead** | Jul 2024 – Aug 2025, led a 10-member team on the combustion car (KTM Duke 390 EFI engine) |
| **EV Lead** | Aug 2025 – Oct 2026, leading an 18-member team through the move from a combustion car to an electric car for the 2027 season |
| **Certification** | Electrical Safety Officer (ESO) Level 3, Formula Bharat (authorized to work on live high-voltage systems while the tractive system is active) |

---

## 1. Data Acquisition (DAQ) System (combustion car)

A real-time system that measures vehicle data and shows it to the driver and the team.

**Measured parameters**
- Engine RPM
- Temperatures
- Brake disc temperature
- Vehicle orientation: yaw, pitch and roll
- Steering angle
- Gear position
- Fuel level

**How the data is used**
- **Driver display:** a TFT screen on the car shows the driver live gear position, fuel level and engine data.
- **Team telemetry:** an ESP32 hosts a web page that streams sensor data to team members' mobile phones in readable form, where it is stored for later analysis.

**Hardware:** ESP32, sensors connected through custom wiring, TFT display

---

## 2. ECU Communication over CAN Bus and OBD-II

- Traced the car's CAN wiring to the OBD port of the KTM Duke 390 EFI engine.
- Read engine operating parameters from the ECU using an OBD-II adapter.
- Used this data to monitor engine performance and diagnose electrical faults.

---

## 3. Shutdown System and Wiring Harness

- Built the car's **shutdown system** to meet the competition rulebook.
- Designed and built the **vehicle wiring harness** linking sensors, electronic controllers, driver interfaces and low-voltage subsystems.

---

## 4. Safety Circuits: BSPD and TSAL

**BSPD (Brake System Plausibility Device)**
- Shuts the vehicle down if hard braking and high power happen at the same time, which signals a fault.
- Built and working on the combustion car; it is being carried forward into the electric car.

**TSAL (Tractive System Active Light)**
- Warns everyone around the car when the high-voltage tractive system is live.
- Designed for the team's first electric car.

**Development process for both circuits:** schematic → PCB layout → breadboard prototype → Zero PCB prototype → hardware testing and validation.

---

## 5. Electric Vehicle Accumulator (in development)

| Parameter | Value |
|---|---|
| Cell | Molicel INR-21700-P50B (Lithium-ion) |
| Configuration | 21S10P (21 in series, 10 in parallel) |
| Maximum pack voltage | 88.2 V (21 × 4.2 V) |
| Nominal pack voltage | 75.6 V (21 × 3.6 V) |
| Pack capacity | 50 Ah (10 × 5 Ah) |
| Nominal pack energy | ≈ 3.78 kWh |
| Motor control unit | Sponsored by Tesla |

---

## 6. Drag Reduction System (DRS)

- Moves the car's aero flaps with servos to reduce drag on straights.
- Controlled by an Arduino Uno.

---

## 7. Electronic Pedal Shifters

- Turned the manual gear shift into **single-button electronic/pneumatic shifting**.
- Designed and tested for smooth gear changes.

---

## 8. Supercapacitor Cold-Start Study (design study)

- **Problem:** cold-starting the engine needed a parallel battery setup to supply the starter motor's high current.
- **Concept:** a custom supercapacitor pack supplies the starter motor's cold-start current instead, reducing the load on the battery.
- **Status:** calculations complete. Not built, because the budget went to higher-priority systems.

---

## Tools and technologies

| Area | Tools |
|---|---|
| Microcontrollers | ESP32, ESP32-S3, ESP8266, Arduino, STM32, 8051 |
| Languages | C, Embedded C, Arduino C++ |
| Communication | CAN Bus, OBD-II |
| PCB and circuit design | KiCad, EasyEDA, Proteus |
| Development and simulation | Arduino IDE, STM32CubeIDE, Keil, MATLAB, Simulink |

---

## Related work

- [Battery Management System, 3S3P Lithium-ion pack](https://github.com/AnshumanChoudhary529/Battery-Management-System): active cell balancing, plus over-voltage, over-current and over-temperature protection

---

## Contact

**Anshuman Choudhary**
- Email: anshumanchoudhary529@gmail.com
- LinkedIn: [linkedin.com/in/anshuman--choudhary](https://linkedin.com/in/anshuman--choudhary)
- GitHub: [github.com/AnshumanChoudhary529](https://github.com/AnshumanChoudhary529)
