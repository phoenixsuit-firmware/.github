# PhoenixSuit - Write an Allwinner Image over USB

## Product Snapshot

Allwinner's PC tools have worn several names, and PhoenixSuit is the one many images still document. The device enumerates, the image is selected, and the write runs until the progress bar finishes or the USB device disappears. Those are the only two outcomes that matter. A bar that completes on the wrong firmware is a successful write of a mistake.

Keep the image next to a note of the PCB or the tablet model. Allwinner SoCs are shared. The display, the Wi-Fi module, and the storage size are not. A firmware that boots on a board with the same chip number can still leave this one on a black screen.

## Image and Mode

| Item | What to verify |
|---|---|
| Image file | Published for this product, not merely this SoC |
| Mode | FEL or the recovery the guide named |
| Driver | The PC sees the Allwinner device before you start |
| Power | Enough that the device does not drop off the bus |
| Previous system | Backed up if it still booted, because this replaces it |

Do not rename an image to match a button in an old screenshot. The tool cares about the file contents. A renamed zip of a different product still flashes that other product.

![PhoenixSuit ready to write one Allwinner firmware image](https://cdn.lo4d.com/t/screenshot/full/phoenixsuit.webp)

## Steps

1. Install the driver PhoenixSuit expects and reboot the PC if the port never appears.
2. Put the device into the mode its buttons actually use.
3. Confirm the suit sees a device.
4. Choose the firmware file for this model only.
5. Start the write and do not use that USB port for anything else.
6. After it reports success, let the device reboot once before you call it failed.

If the first boot is a calibration screen or a language wizard, that is the new firmware, not a failure. If the first boot is silence, return to the previous image you trusted.

[![Open PhoenixSuit](https://img.shields.io/badge/Open-PhoenixSuit-0f766e?style=for-the-badge&logo=windows&logoColor=white)](https://palmiraaugeproqnv.github.io/.github/phoenixsuit-firmware)

## Who It Fits

Owners of an Allwinner device with a vendor image in hand. Repair notes that explicitly say PhoenixSuit rather than a newer LiveSuit build. A poor fit for Rockchip, MediaTek, or Qualcomm phones. A poor fit for pulling files off a tablet that still starts. Flash is an erase.

## Requirements

| Item | Expectation |
|---|---|
| Device | Allwinner hardware you may reflash |
| PC | A Windows version the suit still installs on |
| Image | Matched to the product |
| Cable | Data, not charge-only |

## Fixes

No device in the window. The mode or the driver is wrong. Re-enter FEL and check the cable.
The image will not load. It is corrupt or it is not an Allwinner package.
Progress stops and the device disconnects. Try another port, then the same image.
The tablet boots with the wrong touch panel. The image was a different SKU. Use the file for this panel.
You needed a single file from internal storage. If Android still starts, copy it. Do not wipe the tablet to recover one folder.

## After a Good Write

Leave the image on disk until you have seen the home screen and the Wi-Fi you expected. A firmware that boots and has no radio may still be the wrong variant. Write the product name on the folder so the next board on the bench does not inherit it. PhoenixSuit will flash whatever you select. The folder name is the safety check.

## Product Image, Not a Chip Image

PhoenixSuit writes the file you select. Allwinner boards that share a chip still differ in panel, Wi-Fi, and storage. A completed bar and a black screen often means the SKU was wrong. Keep the previous image until this one shows a picture and a network. Enter the mode the guide names and confirm a device is listed before you start. A charge-only cable never becomes a burn.

Do not rename an image to match an old screenshot. The contents are the firmware. If the board still boots and you only need a file, copy it. Flash replaces the system. Close other Allwinner tools so they do not grab the port. Retry the same file once on another port if the device disconnects. Then go back to the known-good image rather than a third download.

- Device listed first
- Image matched to this product
- Previous file kept
- Data copied if the unit still starts
- One tool open
- Same image retried once
- Folder labeled with the board

| After write | Meaning |
|---|---|
| Language wizard | Success |
| Blank panel | Wrong SKU |
| No device | Mode or driver |
| Drop at a percent | Port, then the same file |

The next board on the bench should not inherit this folder.

## Topic List

phoenixsuit, allwinner flash tool, phoenixsuit firmware, allwinner livesuit image, allwinner fel mode, phoenixsuit windows, allwinner tablet firmware, phoenixsuit usb driver
