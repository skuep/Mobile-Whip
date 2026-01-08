[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/F2F415AKJV)

# Mobile-Whip
The Mobile-Whip is an active (receive only) wideband antenna mainly designed for the HF frequency range (100kHz - 30MHz). The design is heavily based on the very famous **Mini-Whip** Antenna by PA0RDT (and DL4ZAO) with the main design change of making it operate on a single cell lithium battery (or USB supply voltage) to be able to use it on a mobile radio. 

This led to the following improvements:

- Operates on a single lithium cell, 5V USB Supply, 4.0V RTL-SDR V4 Bias-Tee or 12V-15V Mini-Whip Bias-Tee
- Includes lithium battery charger
- Uses a LTC6268 ultra-low input capacitance OPAMP instead of JFET input
- Requires only 20mA (instead of roughly 50mA)
- (Probably) Has better large signal interferer resiliency (causing intermodulation) so it might perform better indoors
- Designed for 0.1MHz to 30MHz, but works reasonably well also for listening on FM Radio (100MHz) and VHF bands (150MHz)
- Can be easily mounted on a HT (such as the UV-K5 with HF mod) or mobile scanner and is thus ideally suited for e.g. SHTF Emergency Operations
- Very compact, only 200mm length
- 3D-Printed Enclosure (TBD)

**Important**: This project is currently in it's first revision for preview purposes only. There may (and are) some issues with this design still that need to be addressed in the future.

**Attention**: There is currently no reverse-TX protection, should you mount the Mobile-Whip on a mobile and press the PTT button. The Mobile-Whip might break.

![Mobile Whip on a UV-K5 with HF-mod](images/mobile-whip.jpg?raw=true "Mobile Whip on a UV-K5 with HF-mod")            |  ![Mobile Whip on a RTL-SDR with Bias-Tee](images/mobile-whip-rtlsdr.jpg?raw=true "Mobile Whip on a RTL-SDR with Bias-Tee")
:-------------------------:|:-------------------------:
Mobile Whip on a UV-K5 with HF-mod | Mobile Whip on a RTL-SDR with Bias-Tee

![S9+ on UV-K5](images/mobile-whip-s9p.jpg?raw=true "S9+ on UV-K5")            |  ![Integrated USB-Charger](images/mobile-whip-charging.jpg?raw=true "Integrated USB-Charger")
:-------------------------:|:-------------------------:
S9+ on UV-K5 | Integrated USB-Charger

## How can I get one?
The PCB can be ordered fully-assembled (apart from SMA male connector and lithium cell holder) at JLCPCB by following these instructions:

- Go to JLCPCB.com and upload the ``GERBER-mobile-whip.zip`` package (under ``kicad/mobile-whip/jlcpcb/production_files``)
  - Select PCB Thickness 1.6mm
  - You may want to select LeadFree HASL
  - Select Silkscreen/Soldermask color to your liking
- Check "PCB Assembly"
  - PCBA Type "Economic"
  - Assembly Side "Top Side"
  - Tooling Holes "Added by Customer"
  - Press Next
  - Click "Add BOM File" and upload ``BOM-mobile-whip.csv``
  - Click "Add CPL File" and upload ``CPL-mobile-whip.csv``
  - Press Next
  - Look Through components, see if something is missing or problematic
  - **Make sure that all listed components are selected** and press Next 
  - Check everything looks roughly good (rotations are already baked-in and should be correct). Save to Cart

**Note**:
The following warning is okay and can be ignored:

*The below parts won't be assembled due to missing data: 
C3, D4, C4, D6, J1, H1, H2, BT1*

This will give you 5 (or more) SMD assembled mobile-whip antennas for roughly 25€ per piece.
