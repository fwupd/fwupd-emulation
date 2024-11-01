# fwupd enumeration emulation data

This repo collects emulation data used solely for testing device enumeration.
It can be gathered and populated by anyone.

Emulation data that contains an upgrade should continue to be stored at LVFS.

## Repository organization

The top level contains directories with the same names as the fwupd plugins/ directory.
In each child directory there are subdirectories that match the GUID for a given device.
In that child directory the json files captured from emulation can be stored.

For example this layout:
```
amd-gpu
|->fec45400-2aa5-51b9-9bba-091bfb972433
|-->setup.json
```

Can reflect this device:
```
├─Lexa XT [Radeon PRO WX 3200]:
│     Device ID:          202d09740f7addab7b2ee4f2b0b62713c80c2754
│     Summary:            D01555 Polaris23 GLXT DT A0 GDDR5 256Mx32 4GB 35W
│     Current version:    015.050.003.000.012636
│     Vendor:             Advanced Micro Devices, Inc. [AMD/ATI] (PCI:0x1002)
│     GUID:               fec45400-2aa5-51b9-9bba-091bfb972433 ← AMD\113-D01555
│     Device Flags:       • Internal device
│                         • Cryptographic hash verification is available
│                         • Emulated
│                         • Can tag for emulation
```