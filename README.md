# My Klipper config for the Kingroon KP5L
(without BLTouch *for now*)

this should work on stock KP5Ls.

## Compiling the firmware
> There is also a precompiled binary provided that you can use.

Kingroon KP5L Klipper compile settings:

```
[*] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32)  --->
    Processor model (STM32F103)  --->
[*] Disable SWD at startup (for GigaDevice stm32f103 clones)
    Bootloader offset (28KiB bootloader)  --->
    Clock Reference (8 MHz crystal)  --->
    Communication interface (Serial (on USART3 PB11/PB10))  --->
(250000) Baud rate for serial port
(!PC6,!PD13) GPIO pins to set at micro-controller startup
```

Then put the file named `Robin_nano.bin` on an empty SD card and power on the printer to flash it.

If you get MCU errors, try lowering the Baud rate to 114200 (change in build and in this file)

## Tuning steps
1. Bed Leveling (https://www.klipper3d.org/Bed_Level.html):
   1. tuning the z endstop switch and physically leveling the bed: https://www.klipper3d.org/Manual_Level.html
   2. leveling the bed in software: https://www.klipper3d.org/Bed_Mesh.html (use the paper test, you don’t need a probe)
2. Temperature PID Tuning: https://all3dp.com/2/klipper-pid-tune-tuning-3d-printer/
3. Input shaping: the tech that makes your printer *fast*: https://damlobster.github.io/klipper/Resonance_Compensation.html / https://all3dp.com/2/klipper-input-shaping-simply-explained/
4. Pressure Advance: https://damlobster.github.io/klipper/Pressure_Advance.html / https://obico.io/blog/klipper-pressure-advance/
