# Uncanny_Eyes

'Uncanny eyes' for Adafruit 1.5" OLED (product #1431) or 1.44" TFT LCD (#2088).  Works on PJRC Teensy 3.x and on Adafruit M0 and M4 boards (Feather, Metro, etc.).  This code uses features specific to these boards and WILL NOT work on normal Arduino or other boards!

How-to guide with parts list and 3D models is here:
https://learn.adafruit.com/animated-electronic-eyes-using-teensy-3-1/overview

Teensy 3.x w/OLED screens: use 72 MHz board speed -- 96 MHz requires throttling back SPI bitrate and actually runs slower!

Directory 'uncannyEyes' contains Arduino sketch for PJRC Teensy 3.1 & Adafruit M0 & M4. 'graphics' subfolder has various eye designs, as #include-able header files.

Folder 'convert' contains Python sketch for generating graphics header files. Requires Python Imaging Library. Example images are also in this directory.

# Forked by github.com/Mark-MDO47
uncannyEyes/config.h shows compile/load status for different eye selections. Two do not fit on Adafruit Hallowing M0 Express https://www.adafruit.com/product/3900:
```C
//#include "graphics/dragonEye.h"     // Slit pupil fiery dragon/demon eye -OR-  // M0 ld.exe: region `FLASH' overflowed by 4664 bytes
//#include "graphics/noScleraEye.h"   // Large iris, no sclera -OR-              // M0 ld.exe: region `FLASH' overflowed by 4664 bytes
```

I suspect that the code has grown since the last time they checked this on an M0 Hallowing. These two have larger iris bitmaps which more than makes up for the smaller sclera bitmaps.

The UF2 files pointed at in the M0 Hallowing "Learning" file do still work. I saved all the official M0 UF2 files in the repo.

