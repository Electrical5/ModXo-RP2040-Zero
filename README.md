# ModXo-RP2040-Zero
Unofficial board for the original Xbox modchip "[ModXo](https://github.com/shalxmva/modxo)" by Shalx
Using the smaller (USB-C) version RP2040-Zero by WaveShare.
Cut-out in the middle of the PCB to allow the RP2040 to lay flush / improve cooling.
Fully checked DRC (Design Rule Checks)

![3d](3d.png)

# Parts
Required:
- 4x 100Ω resistor
- 1x RP2040-Zero (WaveShare)

Optional:
- Power LED (+ 1kΩ resistor)
- Diode to protect when both PC and XBox are connected. (Can be bypassed with solder jumper)
- Solder jumpers for SMBus

Note:
On 1.6 you will need to rebuild LPC before being able to install a modchip.
On 1.0-1.5 you will need to use D0 (solder pad on board).

![2d](pcb.png)

# Fully open source

The KiCad (free application) source files (full schematics!) are included, so you can add/remove components based on your preferences.

![schematics](schematics.png)

# Cutout for RP2040-Zero

The RP2040-Zero has components on the back of the board, to allow for easier installation, there's a cutout in the board.
Though do note you can also install the RP2040-Zero using headers:

![flush](flush.png)

# SMBus

Currently ModXo doesn't implement reading SMBus via I2C, in the future this could add functionality such as monitoring temperature/fanspeed, LED control or restarting/shutdown the xbox remotely.
However, there's two solder jumpers to connect the SMBus of the Xbox to the RP2040-Zero.

# License

GNU GENERAL PUBLIC LICENSE
Version 3, 29 June 2007

You can sell this board as-is, but disclose the source.
If you sell modifications of this board (additional headers for LED strips / LCD / fan), share the modifications / source files under the same license.

# More info

https://github.com/shalxmva/modxo
https://consolemods.org/wiki/Xbox:ModXo
