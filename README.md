# Matterhorn 64 CORE
<img src="Images/logo_text.jpg" width="800" />
<img src="Images/front.JPG" width="400" /> <img src="Images/back.JPG" width="400" /> 

Matterhorn 64 CORE is the world's smallest open-source Nintendo 64 motherboard redesign. 
It relies on the original components taken from an original Nintendo 64 console. 
Since it does **not** rely on emulation, it works perfectly with all the games ever released on the system. 

This board redesign offers smaller, better, cleaner and more reliable builds. 
Matterhorn 64 CORE can easily be integrated in different kinds of builds such as Nintendo 64 portables devices or mini consoles. 

It is fully open-source and released under the CERN-OHL-S-2.0 license. 

More technical information will be found here: [BB Thread] 

## Features
The Matterhorn 64 CORE redesign:
- The world's smallest open source Nintendo 64 motherboard
- Fits in a tiny 78x77.2 mm form factor 
- Runs on real hardware, **no emulation**
- 100% original with **all** the games released on the system, including flashcarts
- Runs on 3.3V @2A 
- Designed on KiCad 9
- Optimized for clean and optimized Nintendo 64 portable builds
- 100% open-source and release under the CERN-OHL-S-2.0 license

## Compatibility
### General compatbility
Due to the complexity of the Nintendo 64 hardware, some of its feature are not availble on this design. 
Please note that:
- The console is compatible with both NTSC and PAL console. However, it is **NOT** region free. It will only accepts games release on the same region as the donor board.
- The console does accept memory expansion, but it is not natively compatible with the orignal Expansion Pak cartridge. You'll need to solder two RDRAM36 4MB onto the console instead of the two RDRAM18 2MB chips present by default on the console in order to enable the Expansion Pak.
- The console does **NOT** have any video output system. You'll either need to hock up an original composite encoder compatible with your region or an HDMI kit
- The console does **NOT** have on-board voltage regulators. An additional N64 PSU or 3.3V PSU will be needed in order to use it. The console requires only requires 3.3V at 2A, but please consider that some HDMI mod or composite encoders may require 5V as well.
- The console is compatible with original controllers
- It is also compatible with original cartridges using the breakout board.

### Nintendo 64 donor board revision compatibility
This mod is **ONLY** compatible with the following motherboard revisions:
#### NTSC Revisions (North America and Japan)
- NUS-CPU-01 (Japan only - 1996)
- NUS-CPU-02 (1996)
- NUS-CPU-03 (1996)
- NUS-CPU-04 (1996-1997)
- NUS-CPU-05 (1997)
- NUS-CPU-05-1 (1997)
- NUS-CPU-06 (1998)
- NUS-CPU-07 (1998)

#### PAL REVISION (Europe and Australia)
- NUS-CPU(P)-01 (1996)
- NUS-CPU(R)-01 (France only - 1997)

**ANY NEWER REVISION WILL NOT BE COMPATIBLE**

## Disclamer
This project requires advanced soldering techniques. It relies on small pitch QFP and 0402 passives.
Removing the components from the original board can be fatal for them if done incorrectly.

Due to the nature of this project, I am not responsible for any physical damages that may occur. 

## PCB Files
The Matterhorn 64 CORE motherboard has been entirely designed using KiCad 9. 
All the files are available in the KiCad files folder of this repository. 
The libraries created are also available in that same folder. 

Gerbers can be found in the Gerber folder. 

The console needs those two PCBs in order to make it work:
- Matterhorn 64 CORE redesign
- Matterhorn Cartridge Breakout

The CORE itself represents the main logic of the console. The breakout board is used easily connect a full size game cartridge to the console. 

## Board ordering
For this project, I recommand ordering the board through JLCPCB or PCBWay. 
I personally ordered mine through JLCPCB. 

You'll find here the list of settings that must be applied when ordering. 

### Matterhorn 64 CORE
- Material: FR4
- Layers: 4
- Thickness: 1.6mm
- Specify Stackup: YES - JLC0416H-3313
- Impedance Control: ±10%
- Stencil: Recommanded but not obligatory.

### Matterhorn Cartridge Breakout
- Material: FR4
- Layers: 2

### Board Impedance Control
As you might notice, the CORE requires controlled impedance. 
The Nintendo 64 uses an extremely fast Rambus Dynamic Random Access Memory Bus (RDRAM BUS). 
In order to work, the CORE requires controlled impedance to match the 50Ω required by the RDRAM BUS. 

The Gerbers files for this board inclues an Excel document which specifies which traces require those controller impedance. 

Please note that the board **might** work by using the 3313 stackup with no controlled impedance. 
To make sure my prototype was working, I did order it using those specifications. 
Ordering without it has not been tried and is at your own risks. 

## Assembly 




