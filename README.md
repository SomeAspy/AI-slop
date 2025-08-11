# AI-slop

Stuff made by AI that I just want to be public
**Yes I hate "vibe-coding" so each has an explanation of why I used AI.**

## DO NOT SUBMIT FEATURE REQUESTS OR ASK FOR SUPPORT. EVERYTHING IS PROVIDED AS-IS

## Munbyn RW402B Linux Driver

### What

Linux Driver for the [Munbyn RW402B Thermal Printer](https://munbyn.com/products/munbyn-realwritter-402-bluetooth-thermal-label-printer)

### Why

Munbyn does not offer a Linux driver for their RW402B Thermal printer
I needed this to use Linux at work, so I used AI to make it as I am not interested in learning C at the moment and I needed it quickly and to just work.
I decompiled the macOS driver package using xar and gave gemini the files to support building a Linux driver.

### How to use it

`RW402B-Linux-Driver/rastertorw402b` is built using `gcc -o rastertorw402b rastertorw402b.c -lcups -lcupsimage`.

1. Save `RW402B-Linux-Driver/rastertorw402b` to `/usr/lib/cups/filter/rastertorw402b`
2. Make the saved file executable (`chmod +x`)
3. Add the printer via USB using your favorite CUPS printer manager, and use `RW402B-Linux-Driver/Munbyn-RW402B-linux.ppd` as the PPD.
