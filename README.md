# Leaf65

> **Disclaimer!**
> These are not the original files created by foxlab!
> They were created (and currently used) by me, as I couldn't find the original ones.

## Usage

There are two directories:

- **`mast3rsoda`** has all the files required to compile the `.hex` file which you can then flash onto the board.
It's pretty straight forward if you've use qmk. If not, in there is a link to the newbs guide which explains things pretty well.

- **`via_config`** is pretty self-explanatory I think.

- **`solder`** has firmware for the solder (non-hotswap) Leaf65 PCB, including a prebuilt VIA `.hex`.
The `mast3rsoda` firmware is for the hotswap PCB and scrambles keys on the solder PCB. See `solder/readme.md`.
