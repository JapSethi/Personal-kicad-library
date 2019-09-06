# Personal-kicad-library
My Personal KiCad Library of symbols created during MSc Research
Custom KiCad parts library containing parts not available in KiCad's default kicad-library repository or Digi-Key's digikey-kicad-library. This repository attempts to follow Digi-Key's organizational structure for ease of component purchasing.

## Creating a Custom Component

If a component schematic symbol or footprint required for a board is not already available in KiCad's default kicad-library repository, Digi-Key's digikey-kicad-library repository, or this repository, then a new component symbol or footprint must be created. The following guidelines should be followed for schematic symbol and footprint creation:

### Schematic Symbols: 

Schematic symbols, specifically ICs, should follow these appearance guidelines.

(A) Pin Name text size: 1.270 mm
(B) Pin Number text size: 1.270 mm
(C) Pin Length: 2.540 mm
(D) Separation between pins: 2.540 mm
(E) Fill component background
Avoid multi-part components unless doing do greatly improves organization. Pins do not necessarily need to be placed in order; if moving a pin allows wires to be uncrossed or placed in a more organized way then moving the pin is preferred.

Add documentation to the component by going to `Edit component properties -> Description`. Under `Description`, paste the part's description from Digi-Key or a short description of the part. Under `Keywords`, place the part's Digi-Key part number, or manufacturer part number. Under `Documentation File Name`, place a link to the part's datasheet.

To save a new schematic symbol, first determine the [family](https://www.digikey.com/eewiki/display/Resources/Become+a+Digi-Key+Master#BecomeaDigi-KeyMaster-Digi-KeyTerminology) that the component belongs to in Digi-Key. If the part is not on Digi-Key, make your best guess based on the part's function. If the part's family already has a library (.lib) file in this repository, save the component to that library. If the family library file does not exist, save it to a new library file in the `JapSethi-symbols` folder using the following naming scheme:

`JapSethi_Family-Name.lib`

### Footprints

Part names should try to follow the convention:

`Part_Function_Part-Number`

Follow the part's datasheet's recommended footprint layout. The footprint should include the part REF**, a pin 1 indicator, and any part outlines or graphics on front silkscreen (F.silkS). All custom part footprints are saved to the `JapSethi-footprints.pretty` folder
