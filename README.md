# GCHDMI by @citrus3000psi

This fork of the original project covers both DOL-001 and DOL-101 GameCube Consoles. All credits goes to @citrus3000psi for the hardware execution and @ikorb for the GCVideo software implementation.

GCVideo v3.1 should be the final version of the firmware as it hasn't been updated for many years. I have included it in this depository as well for you to flash it onto the M25P40 Nor Flash Memory Chip easily using any of the modern day XGecu Programmers such as the T48/T56/T76 and a SOP8>DIP8 150mil Adapter. Just be mindful to flash the firmware into the FLASH portion of the chip!

## DOL-001
This will be a 1:1 adaption of the original project.

The project consists of 3 separate boards:-
1. GCHDMI Main Board v4.1
2. HDMI Breakout Board (New)
3. Digital Port Breakout Board v4.0

### 1. GCHDMI Main Board v4.1
<ins>**PCB Thickness: 0.8mm**</ins>

- C1,C2,C3,C4,C5,C6,C10,C11,C12,C13,C14  :  0.1uF 0603 MLCC x 11
- C8     :  10uF 0603 MLCC x 01
- C9     :  4.7uF 0603 MLCC x 01
- R3,R4  :  4k7Ω 0603 Resistor x 02
- R2     :  330Ω 0603 Resistor x 01
- R5     :  180Ω 0603 Resistor x 01
- R7,R6  :  10kΩ 0603 Resistor x 02
- U1     :  XC3S200A-4VQG100C / XC3S200A-4VQG100I / XC3S200A-5VQG100C QFP FPGA x 01 (AliExpress)
- U2     :  MIC3975-5.0YMM MSOP8 LDO x 01 (AliExpress/Mouser)
- U3     :  TPS74012DGKR MSOP8 LDO x 01 (AliExpress/Mouser)
- U4     :  M25P40-VMN6PB / M25P40-VMN6TPB / MX25V4006EM1I-13 SOP8 NOR FLASH MEMORY x 01 (AliExpress/DigiKey/Mouser)
- FFC Connector  :  20-Pin, 0.5mm Pitch, Bottom Contact, Right-Angle Mount x 01
- FFC Flex Cable :  20-Pin, 0.5mm Pitch, Same-Sided, 150mm / 200mm

All SMD capacitors (MLCC)/resistors are 0603. Make sure to use caps rated 6.3v or higher.

### 2. HDMI Breakout Board (New)
<ins>**PCB Thickness: 1.6mm**</ins>

- HDMI-C Connector  :  XUNPU HDMI-201 x 01 (LCSC)
- FCC Connector     :  20-Pin, 0.5mm Pitch, Side Contact, Vertical Mount x 01
- TVS Diode         :  TPD4S010DQAR / TPD4E02B04DQAR USON10 4-Channel ESR Protection Diode x 03
- M2.5 x 6 mmm Pan/Flat Head Screw w/ Nut for fastening to the backplate mount

### 3. Digital Port Breakout Board v4.0
<ins>**PCB Thickness: 2.0mm**</ins>

## DOL-101
This section will be a combination of both the Digital AV Port and GCHDMI projects to create a solution for the Analog AV Port only DOL-101.

The project consists of 3 separate boards:-
1. GCHDMI Main Board v4.1
2. HDMI Breakout Board (New)
3. Digital AV Port Flex QSB

### 1. GCHDMI Main Board v4.1
Same as above for DOL-001.

### 2. HDMI Breakout Board (New)
Same as above for DOL-001.

### 3. Digital AV Port Flex QSB
<ins>**Flex QSB Thickness: 0.12mm**</ins>

Please make use of the Digital AV Flex Mapping excel sheet in the PCB folder as reference to route the corresponding connections between the Flex QSB and the GCHDMI Main Board. Till the day someone who's savvy enough to create a modified Flex QSB that interfaces with the GCHDMI Main Board perfectly, this solution will serve its purpose well enough. The Mappings excel sheet is kinda rough currently but all the signal points have been carefully matched and mapped out.  
  
  *** Remember to pull CableDetect High to 3v3 on the Flex Cable to enable 480p options. i.e. bridge CDET to 3v3
