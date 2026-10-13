# StarBoy

StarBoy is an **ESP32-C3-WROOM-02** hardware project for [Hack Club's Half Life](halflife.hackclub.com).

This repo is set up to document build progress, wiring, and milestones as the board comes together (push buttons, 01x07 OLED/sensor socket, and other modules). This project is based off [Lil Guy in collaboration with Creature Co.](https://hesjustalittleguy.com/). 



## Project Progress
[Current PCB](/Assets/09-10-2026/PCB.png)
[Open the interactive PCB viewer](docs/pcb-viewer.html)

<iframe
  src="docs/pcb-viewer.html"
  title="Interactive PCB viewer"
  width="100%"
  height="800"
  style="border: 0;">
</iframe>

- Created initial CAD models for the bottom body, top body, PCB area, and keychain.
- Designed the first KiCad schematic and PCB layout.
- Completed an Electrical Rules Check (ERC) with no errors.
- Completed a Design Rules Check (DRC) with 18 errors and 26 warnings. The issues came from tight routing and component placement in this first PCB version.
- Started a new PCB layout after learning from the first routing attempt and a routing tutorial.
- Added a full ground layer and custom routing constraints for power, ground, and signal traces.
- Created a separate enclosure for the OLED screen to increase the available PCB working area.

### Next Steps

- Finish routing the new PCB and review all power, ground, and signal connections.
- Re-run ERC and DRC, resolve all errors, and then address the warnings.
- Check the ground layer, vias, routing constraints, and separate OLED enclosure.

## Bill of Materials

### First 30 Schematic Components

| References | Quantity | Component | Footprint or part |
| --- | ---: | --- | --- |
| C1, C2, C5, C6 | 4 | 10 uF capacitors | Capacitor_SMD:C_0805_2012Metric |
| C3, C4 | 2 | 100 nF capacitors | Capacitor_SMD:C_0805_2012Metric |
| D1-D4 | 4 | LEDs | LED_SMD:LED_0805_2012Metric |
| Down1, Left1, Right1, SW5 | 4 | Push buttons | Button_Switch_THT:SW_PUSH_6mm |
| J1 | 1 | OLED socket | Connector_PinHeader_2.54mm:PinHeader_1x07_P2.54mm_Vertical |
| J2 | 1 | MPU6050 module | Package_SO:SOIC-16W_7.5x10.3mm_P1.27mm |
| J4 | 1 | USB-C receptacle | USB_C_Receptacle_USB2.0_16P |
| R1-R4 | 4 | 150 ohm resistors | Resistor_SMD:R_0805_2012Metric |
| R5, R6, R9 | 3 | 10 kohm resistors | Resistor_SMD:R_0805_2012Metric |
| R7, R8 | 2 | 5.1 kohm resistors | Resistor_SMD:R_0805_2012Metric |
| R_LED1-R_LED4 | 4 | 330 ohm resistors | Resistor_SMD:R_0805_2012Metric |

### Additional Components

| Quantity | Component | Footprint or part |
| ---: | --- | --- |
| 1 | ESP32-C3-WROOM-02 | RF_Module:ESP32-C3-WROOM-02 |
| 1 | DHT11 | Sensor:Aosong_DHT11_5.5x12.0_P2.54mm |
| 1 | AP2112K-3.3 | Package_TO_SOT_SMD:SOT-23-5 |
| 1 | PCF8574AP | Package_DIP:DIP-16_W7.62mm |
| 1 | Push button | Button_Switch_THT:SW_PUSH_6mm |

## How I Used This Repo for Progress Logging

1. Reported progress each day here [`docs/PROGRESS.md`](docs/PROGRESS.md)
2. New entries were added if I have:
   - Soldered or wired something
   - Changed pin mapping
   - Added/tested a component
   - Fixed a hardware or firmware issue
3. Photos, notes, and next steps are included in each entry

