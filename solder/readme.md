# Leaf65 Solder PCB

Firmware for the **solder** (non-hotswap, multi-layout) Leaf65 PCB, including boards
with Mill-Max sockets soldered in. The `mast3rsoda` folder targets the hotswap PCB and
produces scrambled keys on the solder PCB.

Based on QMK's `foxlab/key65/universal` (same matrix pins), with the USB PID changed to
`0x0005` to match the Leaf65 VIA definition. Tested on a real Leaf65 solder PCB: all keys
register correctly.

* MCU: ATmega32U4, bootloader: Atmel DFU
* Matrix: 5 x 16
* VID/PID: `0x464C` / `0x0005`

## Files

* `leaf65_solder_via.hex` - prebuilt firmware with VIA enabled (qmk_firmware `d194c077`)
* `keyboard.json`, `keymaps/default` - QMK source used to build it
* `../via_config/leaf65_solder_via_v3.json` - VIA V3 definition (load in usevia Design tab,
  "Use V2 definitions" off)

## Build

Copy this folder to `qmk_firmware/keyboards/leaf65/solder`, then:

    make leaf65/solder:default

## Flash

Flash the `.hex` with QMK Toolbox (MCU `ATmega32U4`).

Enter the bootloader with any of:

* Fn + Esc (`QK_BOOT` on layer 1)
* Hold Esc while plugging in (Bootmagic)
* Press the `RE` button on the back of the PCB
