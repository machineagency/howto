# Clanklin Delano Roosevelt (Clank XY)

Last updated on 3 May 2023

This is the Standard Operating Procedure for the Machine Agency Clank XY machine. While this machine can use several end effectors, this document assumes it will be used for **milling**. For questions about this machine, contact the machine
manager.

Clank XY was designed by Jake Read. [His documentation for the machine can be found here](https://clank.tools/).

- Author: Jasper Tran O'Leary
- PI: Nadya Peek
- Shop Safety Coordinator: Nadya Peek

|                                               |                                                                                   |
| --------------------------------------------- | --------------------------------------------------------------------------------- |
| #1 Process (if applicable)                    | See instructions detailed below.                                                  |
| #2 Equipment                                  | Clank machine, a workpiece to be milled (e.g. wood, PCB blank, Delrin), and fixturing materials (clamps and/or tape), collet wrenches. |
| #3 Personal Protective Equipment PPE)         | Ear and eye protection are both required. An N-95 mask is needed if milling wood, foam, or PCB blanks. Tie back long hair, jewelry, and clothing.   |
| #4 Environmental/Ventilation controls         | Run the machine in Sieg 112 with the dust filter on.                              |
| #5 Required training or approval              | Must be trained by machine manager.                                               |
| #6 Inspection requirements before use         | The workpiece must be fastened securely.                                                         |
| #7 Safe operating procedures or precautions   | Machine must be watched at all times while milling. Use the emergency stop if needed.                                       |
| #8 Chemicals/ spill procedures/waste disposal | N/A                                         |

## General Information

**Machine Manager:** Jasper Tran O'Leary, jaspero@cs.washington.edu

**Description:** The Clank XY is a fabricatable machine with a toolchanging head. Its primary purpose is for milling small objects.

**Who can use the machine:** People who have been trained by the machine manager
and are documented in the machine training spreadsheet.

**How to get access:** Contact Jasper via email or discord

**How to get your access revoked:** Repeatedly breaking the rules.

---

## Rules

**Do not mill deep into the bed.** Clank does not have a spoilboard and the the bed provides stiffness for the rest of the machine. If you need to mill deep for some reason, drill in a separate board to the bed and mill on top of that instead.

## Materials

The materials that Clanklin can mill are limited by the relatively low power of its DC motor spindle.

You should be able to mill the following materials:

- FR1
- Delrin
- Machining Wax
- Wood (composite, plywood, soft and hard wood)

Consult with Jasper for other materials.

## Step-by-step Instructions

### Before use

1. Plug in the power supply to an outlet. Note that there is no on/off switch, just whether the power supply is plugged in or not.
2. Plug in the ethernet cable to your computer. If this is the first time your computer is connecting to the machine, [follow these instructions](https://jubilee3d.com/index.php?title=Connecting_to_Jubilee).
3. Navigate to `192.168.1.2/` in a web browser. When prompted for a password, it is `clanklin`.
4. Home the **Y axis FIRST**, using either the GUI or `G28 Y`. Ensure that cables are out of the way of the end stops which are optical. Note that the controller won't let you move on an axis until it is homed.
5. Home the X and Z axes similarly, order does not matter here.
6. Fixture your workpiece.
7. Install the end mill in the collet by using the collet wrenches. Keep the collet very loose around the end mill for now.
8. To zero the X axis, loosen the collet until the bit sits on top of the workpiece. If you need to, move the Z axis up or down so enough of the end mill shaft is engaged with the collet.
9. Once satisfied, tighten the collet and set the Z axis position to zero using the G-code `G92 Z0`.
10. Raise the Z-axis by 5mm or so i.e. `G0 Z5`.
11. In the Duet interface, upload a G-code file user `File Management > System`, then run it by right clicking the file and pressing Run. **NOTE:** please see the note about setting spindle speeds below—you will most likely need to manually edit any generated G-Code files to address this. 

Before running the file, make sure your workpiece is in the correct location relative to where the machine will move. Feel free to re-zero the X and Y axes  by moving the end mill to the desired zero location and running `G92 X Y`.

### During use

The spindle is quite loud; note that ear protection is required as mentioned earlier.

Keep a window open or the air filter (WEN brand dust filter, not the UW-provided air filter) running during milling and for a resonable time afterwards.

### After use

Vacuum up any chips and dispose of or put back fixures.

## Best Practices

 WARNING: the current design of the spindle and motor is not ideal. Because we're using a brushless DC motor wired directly to the controller, the spindle cannot increase its RPM by more than 5000RPM or so per second. There is currently no automatic ramping functionality for this. 
 
 **This, it is your responsibility to never increase the RPM by more than 5000RPM at once.** This means you need to manually set RPM and then dwell incrementally, including in any G-code files you send to it. As an example, to set the spindle to 12000RPM:
 
```
M03 S5000
G04 S1
M03 S10000
G04 S1
M03 S12000
G04 S1
```

If you don't do this, the current from the power supply will drop too quickly and reset the controller board.

## Tips and Tricks

Another way to zero the Z axis is to lower it to e.g. 5mm above the bed and insert the New York Subway Metrocard (should be labeled and next to the machine) underneath the bit that has already been installed in the collet. Wiggle the card back and forth as you lower the bit closer to the bed. Once the bit catches on the card, set the Z position to be 0.29mm or similar (`G92 Z0.20`).

## Additional Information and Resources

- [Jake's Clank Documentation](https://clank.tools/)
- See Duet3d resources (scattered about the internet) for info on diagnosing the controller.
