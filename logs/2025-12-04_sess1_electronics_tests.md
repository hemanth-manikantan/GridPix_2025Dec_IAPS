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
- Idle measured V/I : Comm 3.3V/0.218A, VDDA 1.523V/0.445A, VDDD 1.521V/0.099A (Recommended currents VDDA/D 50-90/300-500 mA, 300-500 mA)

#Scans
- Equalization W15-G6_equal-Bonn.h5 (from Markus?)
- Mask W15-G6_mask-Bonn.h5 (from Markus?)
- DAC settings in ../images/Gridpix_006_2025-12-04 15-00-25.png
- A noise scan between THL 1390 and 1600 shows noise cut close to THL 1550 ../plots/NoiseScan_2025-12-04_14-41-45.pdf
- 15:06 hrs Threshold Calibration to find THL to electron conversion. 16 ith, 100 tp, 4 data points
- 18:28 hrs During the THL scan : 3.3V/0.219A, 1.523/0.077A, 1.521/0.210A [VDDA,VDDD currents flip!]
- 19:32 THL Calibration finish. Results: THL = (1289.839 ± 3.034) + (0.078 ± 0.001)*Ne; Ne is the number of electrons. This means threshold at noise cut of 1550 is (1550-1290)/0.078 = 3333 e. ../plots/ThresholdCalib_2025-12-04_15-06-15.pdf. Too high!
- 20:34 Noise scan (Noise cut at THL 1550) and THL Calibration (Really good data point at THL 1500) contradicts. One of it should be wrong!
-20:38 Equalization Testpulse-1300-2900-64 started. Will run over night.
