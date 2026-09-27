
# STAR-FLIGHT
<img width="2160" height="2407" alt="3D_PCB1_2026-09-27" src="https://github.com/user-attachments/assets/6ae6d5b7-d5b1-40fe-8c42-37f5612b501c" />
 
A specially designed flight computer intended for use with model/high power rockets, 
based on the RP2350 microcontroller, a dedicated 6-axis IMU, a barometer to track altitude, and the internal CAN bus to connect with other modules of rocket's avionics suite (payload bay module, recovery electronics, telemetry module, and others).
The concept of this board is to create a completely new rocket avionics platform which would feature sufficient processing capabilities, sensors accuracy, and storage space for such purposes as flight state recognition, logging, and inter-board communication

## Features
 
- RP2350A dual-core flight-computer MCU
- ICM-42688-P 6-axis IMU
  - 3-axis gyroscope
  - 3-axis accelerometer
- Onboard barometric pressure sensor for altitude/apogee sensing
- 128 Mbit QSPI flash for onboard data logging
- Built-in CAN bus interface (controller + transceiver) for multi-board avionics networks
- USB Type-C for programming and data download
- Battery input with dedicated power-path protection and a physical power switch
- RGB status LED + auxiliary LED
- SWD programming and debugging interface
- Designed primarily for rocket avionics, adaptable to other autonomous vehicle projects

  ## Main Processor
 
At the core of the electronics is the **RP2350A**, providing sufficient real-time capability for the flight computer to perform tasks such as sensor fusion, flight state detection, logging and CAN communication at the same time. The main controller starts up from the onboard QSPI flash and runs at 12 MHz crystal clock speed.
 
## Motion Detection
 
A **ICM-42688-P** 6-axis IMU, which consists of a 3-axis gyroscope and a 3-axis accelerometer, is interfaced with the MCU using the SPI bus and interrupts from the IMU to the MCU for low-latency motion events, such as detecting liftoff and high-gs during the boost phase.

## Altitude Sensing
A dedicated **barometric pressure sensor** sits on its own I²C bus. This gives the flight computer the ability to track altitude changes in real time, which is central to detecting apogee and triggering recovery events (e.g. parachute deployment logic in firmware).


## Design Concept

Aiming to have a rocket avionics board which is more than just a simple IMU breakout board but rather a complete flight computer with its own logging storage, a proper altitude sensor, proper power path for battery-powered operation, and CAN capability, such that it could serve as a “brains” of an avionics bay consisting of multiple boards.

## Credits

Designed and developed by Omer Ruknuddin

PCB Design: EasyEDA Pro
