# My Klipper config for the Kingroon KP5L
(without BLTouch *for now*)

this should work on stock KP5Ls.

### Tuning steps:
1. Bed Leveling (https://www.klipper3d.org/Bed_Level.html):
   1. tuning the z endstop switch and physically leveling the bed: https://www.klipper3d.org/Manual_Level.html
   2. leveling the bed in software: https://www.klipper3d.org/Bed_Mesh.html (use the paper test, you don’t need a probe)
2. Temperature PID Tuning: https://all3dp.com/2/klipper-pid-tune-tuning-3d-printer/
3. Input shaping: the tech that makes your printer *fast*: https://damlobster.github.io/klipper/Resonance_Compensation.html / https://all3dp.com/2/klipper-input-shaping-simply-explained/
4. Pressure Advance: https://damlobster.github.io/klipper/Pressure_Advance.html / https://obico.io/blog/klipper-pressure-advance/
