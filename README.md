# Avionics sensor board

I'm interested in rocket avionics and wanted to design a board of my own to learn more about the hardware side. This is a four-layer sensor board built around an STM32 microcontroller, with motion and environmental sensors, USB-C and a 3.3 V power supply.

I worked on the component selection, schematic and PCB layout in KiCad. The aim is to get experience with the whole process, from reading datasheets and routing a board to assembling it and getting sensor readings back.

![Top view of the board](images/board.png)

*KiCad 3D render. Some components may not have a 3D model.*

## Hardware

| Part | Purpose |
| --- | --- |
| STM32G474 | Microcontroller |
| BMI088 | Accelerometer and gyroscope |
| BME680 | Environmental sensor |
| TPS62162 | 3.3 V buck regulator |
| USB-C | Power and USB connection |
| Debug header | Programming and debugging |

## Where it is now

The schematic and PCB layout have been designed and sent for PCB manufacture. Assembly, firmware bring-up and testing are still ahead. This is a learning prototype, and I haven't validated it for use in flight.

My next steps are to assemble the board, check the power supply, connect a debugger and bring up the sensors one at a time. I'll document what works and what needs changing.

## Files

- [Schematic preview](images/v1.svg)
- [KiCad project](hardware/v1.kicad_pro)
- [Schematic source](hardware/v1.kicad_sch)
- [PCB layout](hardware/v1.kicad_pcb)
- [Project footprint library](hardware/v1_custom.pretty/)

To open it locally, download or clone the repository and open `hardware/v1.kicad_pro` in KiCad 10. Keep `fp-lib-table` and `v1_custom.pretty` beside the project files. The original project filename is still `v1`.
