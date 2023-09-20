  > **Warning**
  >
  > This branch of klippain is in beta state for using with the new BETA Happy_Hare v2 for MMU/ERCF module https://github.com/moggieuk/Happy-Hare.git **use it at your own risks and make sure to have a backup of your config before using it**.


# Klippain

> Klippain - The pain-free recipe for (french)bread and butter Klipper configuration!

Klippain is a generic, modular, and highly customizable Klipper configuration for 3D printers. Designed for use on various machines such as Cartesian, CoreXY and CoreXZ, it has been reported working correctly on Voron V2.4, Voron Trident, Voron V0, Voron SwitchWire, TriZero, VZbot, Ender5, Ender3, Prusas, etc...

![Klippain](./docs/klippain.png)

Klippain is regularly updated with new features and merged PRs from users. You can reach me on the Voron Discord as **Frix_x#0161**.

Fun fact: "pain" \pɛ̃\ is the French word for bread, so there's no pain in this pain—only joy! Thanks to the French channel "honhonhonbaguette-FR" on the Voron Discord for the joke and name suggestion!


## Features

Klippain is designed for versatility. By selecting and enabling the desired hardware and software options, it can be used on a wide range of machines.

Custom features available out of the box include **adaptive bed mesh**, **custom printer calibration macros**, **automated input shaper workflows**, and **vibration measurement** macros and scripts, ... Refer to the [features documentation](./docs/features.md) for a detailed list and usage instructions.


## Installation

To install Klippain, first ensure you have already Klipper, Moonraker, and a WebUI installed on your printer. If not, use [KIAUH](https://github.com/th33xitus/kiauh).

Then, run the installation script using the following command over SSH. This script will backup your old configuration, download this GitHub repository to your RaspberryPi home directory, and set up Klippain in `~/printer_data/config`. You will also be prompted to select and install MCU board_pins templates. This is recommended for faster `mcu.cfg` setup, but you can do it manually later if you prefer.

  > before install this branch of klippain I recommand to make a clear install... So remove **.VERSION** in config folder and then remove the klippain_config (cloned git source tree). Then you can reinstall klippain Happy_Hare branch so:
```bash
rm ~/printer_data/config/.VERSION
rm -rf ~/klippain_config
```
```bash
wget -O - https://raw.githubusercontent.com/Frix-x/klippain/Happy_Hare/install.sh | bash
```

After this you need to install Happy_Hare V2 from it's own repo: https://github.com/moggieuk/Happy-Hare.git see [mmu guide](./docs/mmu.md).

Finally, Klippain requires a few simple steps to configure and customize it for your printer: please follow the [configuration guide](./docs/configuration.md).

  > **Warning**
  >
  > General rule to keep the auto-update feature working: **never modify Klippain files directly**, but instead add overrides as per the documentation! To proceed, you can modify all the pre-installed templates in your config root folder (`printer.cfg`, `mcu.cfg`, `variables.cfg` and `overrides.cfg`) as they will be preserved on update.


## Support the Project

I strive to accommodate user requests that align with this configuration's design. Feel free to open an issue or a PR for specific hardware device support or new features.

Alternatively, consider buying me a coffee or contributing to new hardware purchases to support my work!
