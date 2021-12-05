Description:
  bin2iso converts a cdrdao bin file to an iso image file

Usage:
  bin2iso [options]

Options:
  -c, --config bin2iso.conf
    Load bin2iso.conf after trying /etc/bin2iso.conf and ~/.bin2iso.conf
  -h, --help
    Display this help message and exit.
  -i, --input file.bin
    Input bin file.
  -o, --output file.iso
    Output file.iso.
  -t, --type auto
    auto
      Automatically detect the image type
    mode1raw
      2352 Byte CD-ROM Mode 1 Raw Sector Format:
      12 Bytes (Sync Pattern)
      3 Bytes (Address)
      1 Bytes (Mode, 0x01)
      2048 Bytes (Data)
      4 Bytes (Error Detection)
      8 Bytes (Reserved, 0x0000000000000000)
      276 Bytes (Error Correction)
    mode1rawsub
      CD-ROM Mode 1 Raw with Subchannels Sector Format:
      12 Bytes (Sync Pattern)
      3 Bytes (Address)
      1 Bytes (Mode, 0x01)
      2048 Bytes (Data)
      4 Bytes (Error Detection)
      8 Bytes (Reserved, 0x0000000000000000)
      276 Bytes (Error Correction)
      96 Bytes (Subcannels)
    mode2form1raw
      2448 Byte 2352 Byte CD-ROM XA Mode 2 Form 1 Sector Format:
      12 Bytes (Sync Pattern)
      3 Bytes (Address)
      1 Bytes (Mode, 0x01)
      8 Bytes (Subeader)
      2048 Bytes (Data)
      4 Bytes (Error Detection)
      276 Bytes (Error Correction)
    mode2form2raw
      2352 Byte CD-ROM XA Mode 2 Form 2 Sector Format:
      12 Bytes (Sync Pattern)
      3 Bytes (Address)
      1 Bytes (Mode, 0x01)
      8 Bytes (Subeader)
      2324 Bytes (Data)
      4 Bytes (Error Detection)

Examples:
  bin2iso -i windows.bin -t mode1rawsub -o windows.iso
  bin2iso -i playstation.bin -t auto -o playstation.iso

Version:
  bin2iso 2.0.0.0
  Copyright (C) 2014 Nathan Shearer
  Licensed under GNU General Public License 2.0
