# HackPad

A 12-key macropad I built as my second hardware project for Stasis, designed to pair with my 60% keyboard for editing, shortcuts, media control, etc...

Hi there, this is my fully custom keypad from scratch, and I tried to keep it clean, practical, and actually buildable.

## Quick Project Summary

- Project: 3x4 macropad + rotary encoder
- MCU: RP2040 Zero
- Switches: 12x MX-style
- Extra input: 1x EC11 rotary encoder with push switch
- Matrix: 3 rows x 4 columns
- PCB size target: about 100mm x 65mm
- Case workflow: KiCad PCB export -> Onshape assembly -> custom bottom case + plate

## Why I Made This

I wanted a dedicated macropad next to my keyboard for common shortcuts (copy/paste, app switching, media, timeline scrubbing, etc.) and I wanted to learn the full flow:

1. keyboard layout planning
2. schematic capture
3. PCB routing
4. case CAD around real board geometry

## Features

- 12 programmable keys (MX style)
- Rotary encoder with click for volume/scroll/tool size/etc.
- RP2040-based and easy to firmware-program
- Through-hole diodes for matrix
- UART header exposed
- Custom silkscreen logos for personality

## Bill of Materials (BOM)

From [production/bom.csv](production/bom.csv):

| Item | Qty | Notes |
|---|---:|---|
| RP2040 Zero module | 1 | Main controller |
| MX-style switches | 12 | 1u keys |
| 1N4148 diodes | 12 | Matrix diodes |
| EC11 rotary encoder (with switch) | 1 | Knob + click |
| 1x4 right-angle pin header | 1 | UART / expansion |

## Design Files Included

- Schematic: [PCB/HackPad.kicad_sch](PCB/HackPad.kicad_sch)
- PCB: [PCB/HackPad.kicad_pcb](PCB/HackPad.kicad_pcb)
- KiCad project: [PCB/HackPad.kicad_pro](PCB/HackPad.kicad_pro)
- Layout JSON: [PCB/keyboard-layout.json](PCB/keyboard-layout.json)
- Plate DXF: [PCB/plate.dxf](PCB/plate.dxf)
- CAD model: [CAD/HackPad.step](CAD/HackPad.step)
- Production files:
	- [production/bom.csv](production/bom.csv)
	- [production/positions.csv](production/positions.csv)
	- [production/designators.csv](production/designators.csv)
	- [production/netlist.ipc](production/netlist.ipc)

## Progress Pictures

### Research

![Research start / Stasis planning](https://stasis.hackclub-assets.com/images/1775168515512-bcedee.png)

### Schematic Stage

![Keyboard layout planning](https://stasis.hackclub-assets.com/images/1775169181678-kfhkz6.png)

![Schematic routing](https://stasis.hackclub-assets.com/images/1775170155354-trwtav.png)

### PCB Stage

![PCB routing](https://stasis.hackclub-assets.com/images/1775170758454-iaydro.png)

![PCB front silkscreen](https://stasis.hackclub-assets.com/images/1775170877334-m3it0k.png)

![PCB back silkscreen](https://stasis.hackclub-assets.com/images/1775170919019-cimvy5.png)

### CAD / Case Stage

![CAD view 1](https://stasis.hackclub-assets.com/images/1775325159730-egpcag.png)

![CAD view 2](https://stasis.hackclub-assets.com/images/1775325211567-d3jrj5.png)

![CAD view 3](https://stasis.hackclub-assets.com/images/1775325284665-im1yju.png)

![CAD view 4](https://stasis.hackclub-assets.com/images/1775325322588-8375t2.png)

![CAD view 5](https://stasis.hackclub-assets.com/images/1775325347015-y8mn5v.png)

![CAD view 6](https://stasis.hackclub-assets.com/images/1775325385497-r7jfrc.png)

## Time Spent (from Journal)

- Research: ~0.33h
- Schematic: ~2.25h
- PCB: ~3.25h
- CAD: ~3.45h

Total logged so far: ~9.3h

## What I Learned

- Importing the actual PCB into CAD early saves a lot of pain later.
- Matrix labeling in schematic makes routing way less confusing.
- Tiny mechanical details (insert depth, nut traps, plate thickness) matter a lot more than expected.
- Silkscreen art is optional, but morale is not.

