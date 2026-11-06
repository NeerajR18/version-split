---
title: "version-split"
github: "https://github.com/NeerajR18/version-split"
description: "Split Keyboard with per key RGB lighting, choc v1 switches and a reversible PCB. On board STM32F072CBT6 and USB-C interconnect."
created_at: "2026-11-06"
total_time: "36m"
---

# November 6, 2026: Starting Out
<!-- fabricate:entry 2254 -->

Starting a new design for a split keyboard! 
I have decided to use Low profile switches, mill max sockets and USB-C interconnect for this keyboard.

I chose the STM32F072CBT6 because of its reliability. Old, but still capable for keyboards.
Since its a reversible design, I need to think about placement and a lot of other stuff.

I started the schematic by placing the MCU and wiring the very important BOOT and RESET circuits. I also added the decoupling capacitors for the 3v3 pins.
 
![](https://fabricate.hackclub-assets.com/e04ec055d632fe79fe6b8975642c654bcfca5f7b2a9b5c006f21d70641e9cef4/image-png/image.png)

After this, I moved on to the actual layout of the keyboard.
I have decided for 6x4 layout along with a 4 key thumb cluster.
I am still deciding on the actual switch type, which will decide the next few steps.

![](https://fabricate.hackclub-assets.com/c9ceefa7f4d046e13ec30d5406c43d2ac9045ff6b06b2fb55f3e863a43eaf64a/image-png/image.png)

**Total time spent: 36m**
