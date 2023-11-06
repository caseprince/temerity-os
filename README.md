# temerity-os

Arduino code &amp; docs for bike-mounted rainbow LEDs

![Bicycle with Rainbow LEDs](https://github.com/caseprince/temerity-os/blob/main/images/20230708_224618.jpg?raw=true)

## CAD Models for 3D Printing Designed in OnShape

- [Control Unit Enclosure & Brackets](https://cad.onshape.com/documents/c0d84c6ffa9bdc5b4e96d84a/w/ab7fa442840c19dcdb86b606/e/6a70e81d8de3d289a5feaf4a?renderMode=0&uiState=6282715ed8c5dc67710ff45d)
- [LED brackets](https://cad.onshape.com/documents/a2c029861f4f6949a2b490da/w/bb1c7454e5ed916324910a7b/e/fb98fe964bbb7c3be6a0288d?renderMode=0&uiState=6282724977f99b45e28dc207) for [silicone diffused NeoPixel strips](NeoPixel RGB Neon-like LED Flex Strip with Silicone Tube)

## Toolpaths for lazer-cut acrylic back & face plates

 - https://github.com/caseprince/temerity-os/tree/main/lazer-toolpaths
 - https://www.ponoko.com/ is a great option

## Full Hardware List & Notes

1. 12v Battery. [This one from TalentCell](https://talentcell.com/lithium-ion-battery/12v/pb120b1.html) works well and lasts all night. A LiFePO4 like [this one from Bioenno](https://powerwerx.com/bioenno-blf-1212a-12v-12ah-lithium-iron-pvc) might also be a sweet spot (needs testing.)
2. [Female 12v DC Power Jack Connector](https://www.amazon.com/Ksmile%C2%AE-Female-2-1x5-5mm-Adapter-Connector/dp/B015OCV5Y8/) & cable.
3. Main board is a [Feather](https://learn.adafruit.com/adafruit-feather/overview) from Adafruit: [HalloWing M4](https://www.adafruit.com/product/4300) ([DigiKey links](https://www.digikey.com/en/products/category/evaluation-boards/2041?s=N4IgjCBcoLQBxVAYygMwIYBsDOBTANCAPZQDa4ArAEwIC6AvvYVWSACwDMADFyA0A) may be avilable for stuff that's out of stock on adafruit.com. There are many [Feathers](https://learn.adafruit.com/adafruit-feather/overview) to choose from, but the HalloWing is chaped like a 💀!)
4. 3.3V Converter for powering Feather: [MPM3610 3.3V Buck Converter Breakout - 21V In 3.3V Out at 1.2A](https://www.adafruit.com/product/4683)
5. [NEOPXL8 FeatherWing](https://www.adafruit.com/product/3249) - This allows for 7-8 neopixel channels ([8 if I could figure out compatible pin assignment?](https://forums.adafruit.com/viewtopic.php?p=964067#p964067)), and the screw-down-connection headers allow for easy wiring directly to JST connectors (below).
6. [NeoPixel RGB Neon-like LED Flex Strip with Silicone Tube - 1 meter](https://www.adafruit.com/product/3869) - These are powered directly from the 12V battery.
7. [NeoTrellis](https://learn.adafruit.com/adafruit-neotrellis) with [Silicone Elastomer 4x4 Button Keypad](https://www.adafruit.com/product/1611)- I2C neopixel buttons!
8. Bits and Bobs: [JST Connectors x10](https://www.adafruit.com/product/1663), [White Nylon Machine Screw and Stand-off Set – M2.5 Thread](https://www.adafruit.com/product/3658), [Heat Shrink Pack](https://www.adafruit.com/product/344), 500–1000+ µF Capacitor as per [Adafruit NeoPixel Überguide](https://learn.adafruit.com/adafruit-neopixel-uberguide/best-practices)
9. USB routing for external programming port: [Micro USB elbow thing](https://www.aliexpress.us/item/3256803950842339.html), [Panel Mount Extension](https://www.adafruit.com/product/3258)

### Optional Upgrade
1.  [DotStar Digital LED Strips](https://www.adafruit.com/product/2328) - These require beefy 5v converters, eg: [UBEC DC/DC Step-Down (Buck) Converter - 5V @ 3A output](https://www.adafruit.com/product/1385)

### Future Features
- There are 2 holes sized for [Panel Mount 1/8" / 3.5mm TRS Audio Jack Connectors](https://www.adafruit.com/product/3692). These could be for external GPIO, audio in and/or out for sound reactivity, BPM detection or bicycle bell sound-effects?


## Spinning Beachball of Death:
![Bicycle with Animated Rainbow LEDs](https://github.com/caseprince/temerity-os/blob/main/images/temerity-loop.gif?raw=true)

*All the pixels know where they are relative to each other in 3D space with XYZ coords, which makes it a joy to program spatial animations like this rotating rainbow.*