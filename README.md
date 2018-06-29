# Embedded-Bicycle

LPC1114 chip used to power an 18-speed bicycle.

This program controls an electric bicycle. The pedals are hooked up to hall effect sensors, the front gears are connected to a servo motorc
and the back gears are connected to a stepper motor.

When the pedals are moved, they move magnets near the hall effect sensor. Using an ADC converter to monitor high/low voltage drops, the program
counts how many pedals are moved per second.
If there are less than two pedals detected per second, the bike raises its gear. If there are more than six pedals per second, the bike lowers its gears.

The servo and stepper motors are controlled using varying amounts of pulse widths. An I2C display writes the current overall gear, the front gear,
and the back gear.

The code is written in C, and compiled and executed using GCC-ARM. The commands are executed on a Linux command line.

