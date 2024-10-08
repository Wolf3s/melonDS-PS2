# melonDS-PS2

PS2 port of MelonDS emulator, PoC, horrible performance.

I just wanted to see if i could port this in a day xD.
 
It remains to adapt the touch system and complete the sound integration with the AUDSRV

It just works with < 8MB ROMs

![gs_20220317164216](https://user-images.githubusercontent.com/47725160/158883327-42822ef0-762e-4ee8-8fe2-42ef6fd8261d.png)
![gs_20220317164222](https://user-images.githubusercontent.com/47725160/158883342-b0823598-c087-4423-9940-6a174f56d38e.png)
![gs_20220317164505](https://user-images.githubusercontent.com/47725160/158883352-91ccb9ac-cbfe-4e06-b2d8-a78cb2546198.png)


The source code is provided under the GPLv3 license.

## How to Use

melonDS requires BIOS/firmware copies from a DS. Files required:
 * bios7.bin, 16KB: ARM7 BIOS
 * bios9.bin, 4KB: ARM9 BIOS
 * firmware.bin, 128/256/512KB: firmware
 
Firmware boot requires a firmware dump from an original DS or DS Lite.
DS firmwares dumped from a DSi or 3DS aren't bootable and only contain configuration data, thus they are only suitable when booting games directly.

### Possible Firmware Sizes

 * 128KB: DSi/3DS DS-mode firmware (reduced size due to lacking bootcode)
 * 256KB: regular DS firmware
 * 512KB: iQue DS firmware

DS BIOS dumps from a DSi or 3DS can be used with no compatibility issues. DSi BIOS dumps (in DSi mode) are not compatible. Or maybe they are. I don't know.

## How to Build

### Linux:

Requires PS2DEV to compile. Directions for installing PS2DEV are found at [PS2DEV](https://github.com/ps2dev)

```
make all
```

## How to Install

1- melonDS requires BIOS/firmware copies from a DS... Paste the bios7.bin, bios9.bin and firmware.bin next to the emulator (APPS/melonDS/)
2- Paste the games in a folder called "roms" next to the emulator (APPS/melonDS/roms/)
3- Paste the APPS and PLG folders in XEB+ folder to run it from XEB+ or just copy the melonDS folder somewhere

## How to make it work

Well... I'm very sorry to said that I failed to make it run on real hardware (tested on DECKARD, SCPH-79001), but it works fine in PCSX2, so go test it there.

## PS2-port credits:
Ported by: Daniel Santos
Color fix and quality of life improvements: Howling Wolf & Chelsea
Thanks to ffgriever, fjtrujy and uyjulian for their help
Forked from: https://github.com/Rinnegatamante/melonDS-Vita
