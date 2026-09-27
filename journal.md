# STAR-FLIGHT — Design Journal
 
## Project Summary
 
| Project Name | Time Taken | Design Tool |
|---|---|---|
| STAR-FLIGHT | ~8 hours | EasyEDA Pro |
 
## Build Log

### Hour 1 — Component Placement
Imported all necessary components and placed them on the PCB/Schematic sheet—MCU, 
IMU, Barometer, Flash, CAN Controller/Transceiver, Power Regulator, USB-C Port, Battery Management Components,
LEDs, Crystals, and Mounting Holes. My objective during this period was placing everything on the board before moving to the wiring process.
 
### Hours 2-3 — Component Wiring
Connected all components to each other—connected MCU to IMU, barometer, flash, and CAN blocks, 
provided power path (VBUS/VBAT -> Regulator -> VCC), USB Data Lines, LED Drive Circuit, and CAN Transceiver/Termination. 
During hour 3, all connections were made.

<img width="4698" height="3326" alt="SCH_Schematic1_1-P1_2026-09-27" src="https://github.com/user-attachments/assets/86bdbef3-b5dd-4c0a-803e-265aad06c780" />
### Hour 4 - PCB Layout Placement
Switched to PCB layout placement mode and placed the footprints on the board, arranging component blocks (power supply, microcontroller, sensor blocks, CAN bus, USB-C, battery block).

### Hour 5 - PCB Layout Placement (continued)
Further fine tuning of the part placement was done by repositioning components for better routing clearance,
moving the analog blocks and IMU from noise of the power lines and USB traces, and defining the location of mounting holes.

### Hour 6 - Routing
Routing of the PCB traces – power lines, buses for I²C/SPI communication with the IMU and barometer,
QSPI bus for the flash memory, CAN bus lines, USB differential bus and LED/GPIOs.
<img width="2160" height="2405" alt="PCB_PCB1" src="https://github.com/user-attachments/assets/ed471cb9-8f59-4e43-bcd1-9e0c4ad1a472" />

### Hour 7 - DRC Checks and Fixes
DRC (Design Rule Check) was performed and all reported errors were fixed – clearance violations, unrouted nets and footprint/net mismatch.

### Hour 8 — Final Review
Did a final pass over the whole board — double-checked silkscreen labels, 
connector orientations, and net names against the schematic before calling the layout done.
<img width="2160" height="2407" alt="3D_PCB1_2026-09-27" src="https://github.com/user-attachments/assets/a3cfc78b-60c1-4f47-aaf6-1cbaa096da9c" />

 
