# StarBoy Progress Log (Hack Club)

Use this file as your running build journal.

## Entry Number One 

### Initial Version - 09-10-2026 

**What I worked on**
In this progress update, I built the initial [CAD files](/CAD/) and [PCB and schematics](/Firmware/). I first started with created the CAD models so that I could easily understand how to map the location of components. I have actually come to regret this due to very tight routing and component placement. The CAD files took a relatively low time to complete and during designing i learned about mate placements and creating screws to enhance repairability. Furthermore, I also developed the schematics and PCB designs using Kicad software, which was especially challenging due to it being the first time I have ever attempted such a thing. Unfortunately I could not complete the PCB designs without routing errors as seen here 

**Hardware changes**
Developed initial:
- CAD files:
    - [Bottom Body](/CAD/Part%20Studio%201%20-%20Bottom%20Body.step)
    - [Top Body](/CAD/Part%20Studio%201%20-%20Top%20Body.step)
    - [PCB area](/CAD/Part%20Studio%201%20-%20PCB.step)
    - [Keychain](/CAD/Part%20Studio%201%20-%20Keychain.step)

- Firmware:
These files are `.kicad_pcb` and `.kicad_sch`
    - Here lies the PCB developed in Kicad: [PCB](/Firmware/Starboi%20hopefully.kicad_pcb)
![[/Assets/09-10-2026/PCB.png]]
    - Here lies the schematics developed in Kicad: [Schematics](/Firmware/Starboi%20hopefully.kicad_sch)
![Schematics](/Assets/09-10-2026/Schematic.png)

**Firmware/tests done**
Completed two KiCad design-rule checks. The Electrical Rules Check (ERC) found no errors, which means the schematic connections and electrical relationships passed KiCad's checks. The Design Rules Check (DRC) found 18 errors and 26 warnings, showing that the physical PCB layout still needs work even though the schematic itself is electrically consistent.

**Problems found**
- I ran both an ERC and a DRC.
- ERC: no errors were found in the schematic.
- DRC: 18 errors and 26 warnings were found in the PCB layout. These issues are consistent with the tight routing and component placement in this first PCB version and need to be reviewed before manufacturing.
![[/Assets/09-10-2026/ERC.png]]

**Fixes / decisions**
- Since this was my first time routing a PCB, I used the DRC results and a routing tutorial to understand what needed to change.
- I started a new PCB layout with a full layer dedicated to ground to improve grounding and make routing more reliable.
- I added custom routing constraints for power, ground, and signal traces so that each type of connection can be routed more intentionally.
- I created a separate enclosure for the OLED screen outside the PCB, which increased the available working area and gives the screen more room.


**Next steps**
- Finish routing the new PCB and review the power, ground, and signal connections.
- Re-run ERC and DRC on the new design, then resolve all DRC errors before addressing the warnings.
- Check that the ground layer is connected properly with the required vias and that the custom routing constraints are being followed.
- Update and test the separate OLED enclosure and its connection to the PCB.
- Document what I learned from this first routing attempt and compare the new DRC results with the original 18 errors and 26 warnings.

---

## Progress Entries

### 2026-10-09 — Project documentation setup

**What I worked on**
- Initialized repository documentation for Hack Club progress tracking.

**Hardware changes**
- No hardware changes in this entry (documentation setup only).

**Firmware/tests done**
- No firmware changes.

**Problems found**
- None.

**Fixes / decisions**
- Keep all ongoing progress entries in this single file for easy timeline review.

**Photos / links**
- Add your first build photos here.

**Next steps**
- Add wiring/pin notes for ESP32-C3-WROOM-02 and push buttons.
- Log first OLED/sensor socket test.
