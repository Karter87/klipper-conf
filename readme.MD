## Motivation

During my studies in 2014, I build my first RepRap 3d Printer.
Using Prusa's initial i3 design. Only the RAMPS-1.4 and Steppermotors were bought.

The materials I scattered in the workshop of ForZe where I used a MAHO CNC capable mill.
I modified the serial bus of the machine, so I was able to hook it up to a Laptop with CAM software.

The printer was running repetier firmware and printed 3 other printers. 
The last one being a Prusa i3 MK3 Clone with Bear modification. (Re)building often the firmware with Marlin-2.x bugfix branch.

When I started with Klipper3D, I missed the default Config approach of Marlin.
https://github.com/Prutsium/3D-Druckerplausch-Klipper/ from The 602 Wasteland Discord Channel.

## Installation

Klipper requires to have a printer.cfg file in the pi home folder. Move the example-printer.cfg file to /home/pi/printer.cfg

## Configuration

The concept is to have components of 3D printer and it configuration modular. Just like programming Marlin-2.x.
This phylosphy makes modification on a printer easier to implement.

- Boards/<Board_name>/ping.cfg 
    - contains the pin configuration of a board

- Boards/<Board_name>/default.cfg 
    - contains the board specific configuration

Steppers/default.cfg

Extruder/Mk3_PT1000.cfg

Mcu/main.cfg


## Slicers
- SuperSlicer, (based on PrusaSlicer (based on Slicer))
    - Klipper Native commands
    - Calibration tools built in
- Cura 
- Repetier

## Klipper Hosts
- Fluidd
- MainSailOS
- OctoKlipper

## Firmware based
- Marlin
- Repetier
