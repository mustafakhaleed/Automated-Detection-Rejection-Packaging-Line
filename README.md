# Dairy Production Factory: PLC Control System

This project involves the design and implementation of a Programmable Logic Controller (PLC) program to automate a milk production line. The system manages conveyor belts, level sensing, carton counting, and pneumatic ejection (push-rod) mechanisms.

## ⚙️ System Functionality
The PLC program follows a specific sequence to ensure efficient dairy packaging:
1. **Start/Stop Logic:** Latching circuits for system activation with Green/Red status indicators.
2. **Conveyor Control:** Motor management based on sensor feedback.
3. **Detection & Filling:** - **Capacitive Proximity Sensor:** Detects liquid levels inside cardboard cartons (non-invasive).
   - **Photoelectric Sensor (Diffuse):** High-speed counting of cartons.
4. **Ejection Mechanism:** A timed push-rod system for handling batches (3 packs per cycle).

## 🧩 Hardware & Sensors
* **PLC:** Programmed using Ladder Diagram (LD).
* **Capacitive Sensor:** Chosen for its ability to sense dielectric changes (liquid presence) through non-metallic packaging.
* **Photoelectric Sensor:** Used for reliable carton counting on moving conveyors.
* **Indicators:** Green (Running), Red (Stopped), Yellow (Standby/Batch processing).

## 📑 Program Logic (Rung Highlights)
* **Rung 0:** Main system start/stop with safety interlocks.
* **Rung 4:** Increments counter `C1` upon sensor detection.
* **Rung 7:** Motor control integrated with level sensors for filling timing.
* **Rung 33:** Activation of the pneumatic Push-Rod after a batch is complete.

## 🛠️ Tools Used
* **PLC Software:** [Insert Software Name, e.g., ISPSoft / TIA Portal / RSLogix]
* **Documentation:** Detailed I/O mapping and timing diagrams.
