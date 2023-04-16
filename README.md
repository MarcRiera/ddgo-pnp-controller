# Controller mod for Densha de GO! Plug & Play

This mod allows you to use your Densha de GO! Plug & Play as a USB controller for other games.

## Requirements

- USB flash drive
- Powered micro USB OTG adapter
- Micro USB data cable

## Installation

1. Prepare the USB flash drive by formatting it with a single FAT32 partition.
2. Download the latest release from the [Releases](https://github.com/MarcRiera/ddgo-pnp-controller/releases) section.
3. Extract the content to the root of the USB drive.
4. Plug the USB drive to the OTG adapter, plug the adapter to the Plug & Play and plug the data cable to the adapter and a power source.
5. Turn on the Plug & Play. The door lamp will turn on to show the installation has begun. Once it has finished, the lamp will turn off. Turn off the unit and remove everything.

## Usage

Connect the Plug & Play to a PC or console using the data cable. Press one of the following button combinations to select the controller you want to emulate:

| Controller                              | Button combination    | Notes                                        |
|-----------------------------------------|-----------------------|----------------------------------------------|
| Two handle controller (PC)              | RIGHT                 | D-Pad is mapped to SELECT+ABCD               |
| Two handle controller "Type 2" (PS2)    | D                     |                                              |
| Shinkansen controller (PS2)             | B                     | Power notches are mapped to P2-P4-P7-P10-P13 |
| Multi Train Controller (PS2) - P4/B7    | C + Power handle at 0 |                                              |
| Multi Train Controller (PS2) - P4/B2-B6 | C + Power handle at 1 |                                              |
| Multi Train Controller (PS2) - P5/B5    | C + Power handle at 2 |                                              |
| Multi Train Controller (PS2) - P5/B7    | C + Power handle at 3 |                                              |

Hold the buttons until the controller vibrates to confirm selection. If no button is pressed, you can play with the Plug & Play as usual.

If you need more information regarding each controller and supported software, please check the [Densha de GO! controller documentation](https://marcriera.github.io/ddgo-controller-docs).

## RNDIS access (advanced users)

When no controller is selected, RNDIS access is enabled in the device. You can access SSH on the Plug & Play at 169.254.215.100. SFTP is not supported out of the box, but SCP is available. Keep in mind the root filesystem is mounted read-only by default.

## Notes

- During the first installation, the device's kernel is backed up to a folder named *BACKUP* in the root of the USB drive. Copy its contents to a safe location.
- If detected, the [original mod by GMMan](https://github.com/GMMan/dengo-plug-and-play-controller) will be uninstalled to avoid conflicts.
