## Warning 

**Project under dev. Not yet ready for production.**

## Installation

1. Create a folder named `hardware` indise your Arduino sketches folder. Unzip and copy the `leonardoat90`folder inside.

2. Re-open the Arduino IDE.

## Contents

### Boards

The Board.txt defines the Arduino version for the **AT90USB1286** at **8 Mhz** wich is temporary called **leonardoAT90**.

### Pins

Pin definitions for the **AT90USB1286** are found on the variants folder. This are based on the [DynamicPerception](https://github.com/DynamicPerception/ArduinoAT90USB) version and the [Tensy 2.0++](http://www.pjrc.com/teensy/) core.

### Bootloader

Arduino Leonardo Bootloader is called **[Caterina](https://github.com/arduino/Arduino/tree/master/hardware/arduino/bootloaders/caterina)** and it is base on the [LUFA](http://www.fourwalledcubicle.com/LUFA.php) by Dean Camera. 

**LUFA** can be natively compiled to work with the **AT90USB1286**, here is a version of the **Caterina** bootloader for this chip.


#### Compile the bootloader

1. To compiler the bootloader you will need the `LUFA-111009` source you can download [here](http://fourwalledcubicle.com/blog/2011/10/lufa-111009-released/). The path for the LUFA folder is defined on the `makefile`. By default unzip it an copied inside the `bootloaders` folder.

2. The `makefile` is currently set to compile a bootloader for the AT90USB1286 at 8MHZ. 

3. Run `makefile clean` and `makefile all` to generate a new `caterina.hex` file for the AT90USB1286.

4. Rename the file as it is called in the *boards.txt* `Caterina-Leonardo-AT90-8.hex`

5. The other Caterina bootloaders on the folder (Leonardo, Esplora and Micro) are not affected by the build process.

