#  Tank Filling Automation using TIA Portal V17 + S7-1200 + PLCSIM Advanced



This project simulates an automated tank filling operation using Siemens TIA Portal V17 and PLCSIM Advanced. The logic is implemented using SCL (Structured Control Language), and device emulation is performed via PLCSIM. 

![](<images/TIA.png>)


## Simulation

The dynamic changes in the outputs when the inputs are toggled in PLCSIM can be visulized [here](https://youtu.be/kniRlD8wU6w)


## 🛠️ Tools Used


- TIA Portal V17

- Siemens S7-1200 PLC

- PLCSIM Advanced

- SCL Programming Language





##  System Description



The system automates the filling of a tank using digital inputs and outputs. It includes:



- A ``valve`` that controls the flow of liquid into the tank.

- A ``switch`` to turn the system on/off.

- A ``Fill button`` to initiate the filling process.

- A ``Lamp test button`` to verify all indicator lamps.

- ``Four level sensors`` to detect the tank's fill level.

- ``Indicator level lamps`` to show the current level of the tank.







##  Working Principle



### Valve Control
- The ``valve`` opens **only** when:
  - The system ``switch`` is **ON**, and  
  - The ``Fill button`` button is pressed.  
- Both conditions must be met for the tank to start filling.

### Tank Level Indication
- Lamps indicate the current fill level of the tank.  
- Behavior of each lamp:  
  - ``Lamp_Level1`` → Turns on if `Sensor_Level1` is active.  
  - ``Lamp_Level2`` → Turns on if ``Sensor_Level1`` and ``Sensor_Level2`` are active.  
  - ``Lamp_Level3`` → Turns on if ``Sensor_Level1``, ``Sensor_Level2``, and ``Sensor_Level3`` are active.  
  - ``Lamp_Level4`` → Turns on if **all four sensors (Level1–Level4)** are active.  
- Lamps also turn on if the system ``switch`` is **ON** and the ``Lamp Test button`` is pressed.

### Lamp Test Function
- The ``Lamp Test button``  lights up all lamps for verification, regardless of sensor status.
- This function works only when the main system ``switch`` is **ON**.

### Simulation
- **PLCSIM Advanced** is used to emulate sensor inputs and monitor tag values in real-time.  
- This allows testing and debugging without physical hardware.











