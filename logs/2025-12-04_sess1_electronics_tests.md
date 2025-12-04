#Test session log 2025-12-04 12:35

#1.
**Purpose:** Swap VDDD (1.52V/1A) (new channel 3) and Comm (3.3V/2A) (new channel 1) Voltage channel and change voltages/currents in Keysight power supply. Keyence power suplly port 1 has current limit of 5 A, while other two have current limits of 1 A. Comm recommended current limit is 2 A.

#Channel changes
- Original port : 1-VDDA 2-VDDD 3-Comm
- New port : 1-Comm 2-VDDA 3-VDDD
- Saved as State2 Auto recall in Keysight power supply

#Setup
- FEC to GridPix connection made
- FEC switched on (Verified LEDs first Red, Red+Green after LV on)
- Idle measured V/I : Comm 3.3V/0.218A, VDDA 1.523V/0.445A, VDDD 1.521V/0.099A

#Scans
- Equalization W15-G6_equal-Bonn.h5 (from Markus?)
- Mask W15-G6_mask-Bonn.h5 (from Markus?)