---
title: "version-split"
github: "https://github.com/NeerajR18/version-split"
description: "Split Keyboard with per key RGB lighting, choc v1 switches and a reversible PCB. On board STM32F072CBT6 and USB-C interconnect."
created_at: "2026-11-06"
total_time: "1h 54m"
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

# November 7, 2026: Almost finished the schematic
<!-- fabricate:entry 2271 -->

I decided to go with the good old MX switches for my design. Mostly because of the very heavily expensive choc switches and no reliable footprint for gateron low profile switches. I plan to use mill max sockets instead of the traditional sockets to reduce the gap between the base and PCB.
I finished the entire schematic except for the USB-C interconnect. USB-C interconnect is still a very foreign concept in the world of split keyboards, with the TRRS cable being the most commonly used cable.

I started by laying out the keyboard matrix switch symbols first-

![](https://fabricate.hackclub-assets.com/145dbaa49c46ca3bd1776ed6c2d09583134946f13deff171ac8fe1035b1f181c/image-png/image.png)

After wiring up the matrix, here is how it looks -
![](https://fabricate.hackclub-assets.com/f2e1e01c7f00820f07a2bc2a5e2c778738bd16c4186277ad60312f4bdd40f36a/image-png/image.png)

a 6x5 matrix.

I then placed the symbols for the LEDs, now this is a tricky part where I have previously made a mistake, which cost me a lot of time.

![](https://fabricate.hackclub-assets.com/ee54050f41a08c0e80e383fce4a059e71d3730607066ed36ba4774e3ae3a1fdc/image-png/image.png)

Since the LEDs need 5v but the STM32F072 runs at a 3v3 voltage, I used a level shifter for converting 3v3 from the IC to 5v for the LEDs.

I also added the debug pins for the STM32. This, while not needed, is a good feature to have for debugging later.

Schematic- 
![](https://fabricate.hackclub-assets.com/e0a309e7a83956e2b44dfb4303351a0aa4586eee117d046ac1fa21905b31fc7d/image-png/image.png)

I finished up by adding the USB-C power circuit. I referenced my old design for this.

![](https://fabricate.hackclub-assets.com/8c08e1893790bed356cd305c3780052edb551068dfd583c60e57918dbad1859a/image-png/image.png)

Now, I need to add the interconnect, then move to routing.

**Total time spent: 1h 18m**
