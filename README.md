# flashable-dmg-cartridge
PCB - Cartridge for original gameboy games with no mapper

## Front
![Alt text](/preview/front.svg "Cartridge Front")

This pcb is for flashing DMG games with no mapper such as the original Tetris game, or custom roms. The board is designed to take a PLCC-32 Socket + EEPROM Chip which can be removed from the socket and re-flashed to change gameboy ROMs. In order to make this cartridge you will need some soldering experience or determination plus the items listed in the BOM.

PCB is ready to be fabricated from anyone who takes gerber files - my fabricator of choice is PCBWay as they are professional and relatively quick. Feel free to open the files in KiCad and explore, modify and make your own variations of the board :) If you want to just fabricate what's already there you can upload the gerber.zip to PCBWay or any fabricator that takes gerber files. Make sure the following is specified (Note: if you are using another fabricator besides PCBWay this might vary):

* min via size is 0.3mm
* board thickness set to 0.8mm
* edge connector set to yes and 45 degree bevel with ENIG surface finish
* ENIG surface finish for the rest of the board (Note: You can use HASL which is a bit cheaper but wears out much quicker and is recommended against)

To flash a ROM onto the AT28C256 EEPROM Chip you will need a PLCC-32 to DIP-32 Adapter plus a flasher to program the chip. I use the same flasher paired with the Xgpro software that is used in this video: https://youtu.be/I4J-uNeLFRU?t=375 - make sure you are at least somewhat comfortable with what's going on in the video from ~6:15 - 7:15. The above video is great for getting familiar with flashing ROM chips. In the video, the chip being flashed is not electronically erasable and so a UV light is needed whereas we can blank our AT28C256 directly from Xgpro. Once the rom is flashed, verified and the PLCC-32 socket is soldered onto the board you can pop the rom chip in and plug the cartridge into any ol' gameboy - enjoy!


## BOM
| Refrence Designator | Part | Description | Link |
| :---: | :---: | :---: | --- |
| U1 | AT28C256-15JU | 32K 5V EEPROM Chip | https://www.mouser.com/ProductDetail/Microchip-Technology-Atmel/AT28C256-15JU?qs=MAR%2F2X5XOp4ElE%2FW%2FWXg2A%3D%3D
| U1 | 69802-432LF | PLCC-32 Socket | https://www.mouser.com/ProductDetail/Amphenol-FCI/69802-432LF?qs=kJUkXSjFC7xj%252BQ7fu6pp%2Fg%3D%3D
| C1 | C1206C106K4PACTU | 10 μF Capacitor | https://www.mouser.com/ProductDetail/80-C1206C106K4P
| R1 | ERA-8AEB123V | 12 kΩ 0.1% Resistor | https://www.mouser.com/ProductDetail/667-ERA-8AEB123V


# Cartridge Preview

## Front
![Alt text](/preview/front.svg "Cartridge Front")

## Back
![Alt text](/preview/back.svg "Cartridge Back")

# Schematic
![Alt text](/preview/cartridge_schematic.png "Cartridge Schematic")
