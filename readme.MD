## Installation

Clone this repository to your ~/printer_data/config folder, e.g.

Clone the reposity
`git clone git@github.com:Karter87/klipper-conf.git ~/printer_data/config`

Install the softlinks, or use your own config files. 
`ln -sf /home/pi/mainsail-config/mainsail.cfg mainsail.cfg`
`ln -sf /home/pi/moonraker-timelapse/klipper_macro/timelapse.cfg timelapse.cfg`

## Configuration


### Printer
The printer.cfg is the main configuration file used by Mainsail. 
It contains inclusions of the files:
- mainsail.cfg, containing a read only version managed by the Github repository of mainsail-config
- klipper.cfg, containing the printer specific settings
- timelapse.cfg, optional config file for the timelapse which is read only
- _CLIENT_VARIABLE macro, to set the variables for the mainsail.cfg
- paramters for the PID parameters, probe offset and bed meshes. Do not change!

### Moonraker
Contains the update managers and power managers.


### Klipper




The concept is to have components of 3D printer and it configuration modular. Just like programming Marlin-2.x.
This phylosphy makes modification on a printer easier to implement.

- boards/<Board_name>/ping.cfg 
    - contains the pin configuration of a board

- boards/<Board_name>/default.cfg 
    - contains the board specific configuration
	- contains the mcu settings

steppers/default.cfg

extruder/Mk3_PT1000.cfg

## Slicers
- SuperSlicer, (based on PrusaSlicer (based on Slicer))
    - Klipper Native commands
    - Calibration tools built in
- PrusaSlicer, since version 2.6 a Klipper support is included. 
- Cura 
- Repetier

## Other Remarks
Klipper uses a python based approach where the MCU is programmed with a base configuration, all settings are managed in Klipper. Where with Marlin Fw, the configuration is compiled for the MCU with all settings.

After years of using Marlin, Klipper is much faster in configuring own build 3d printers. 
