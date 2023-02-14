### General Information

**Machine Manager:** Jeremy Cyphers, cyphers@uw.edu

**Machine Location:** Machine Agency Shop

**Equipment covered by SOP:** Roland MDX-540

**Who can use the machine:** People who have been trained by the machine manager
and are documented in the machine training spreadsheet.

**How to get access:** Follow the pre-training steps, then contact the machine
manager to set up in-person training.

**How to get your access revoked:** Not cleaning up chips/waste material,
running jobs with enclosure door open, leaving the mill unattended during a job,
leaving the compressor pressurized or running after use.

### Terms

See pages 26-28 of the user manual (linked at bottom of SOP) for a description
of common terms.

### Rules

- Do not operate the mill without another person present.
- Close the enclosure door when the mill is cutting material.
- No necklaces, jewelry, loose clothing, or untied long hair.
- Never use cutting oil or pneumatic blowers, the mill is not fully sealed
  against oil or cutting waste.

### Important Information and Safety

- The cutting tools and spindle motor can become very hot.
- There are pinch hazards located throughout the machine. Keep hands clear of
  moving parts.
- Shavings and other cutting waste are a fire hazard. Use a brush instead of a
  vacuum to clean messes that might be flammable.
- Make sure the cutting tool and workpiece are securely fastened. Then check
  again.

### Materials

If you have questions about acceptable materials, contact the machine manager.
They can add additional materials to this list if needed.

**Acceptable Materials**

- Plastic resin
- Light metals
- Machining Wax

**Unacceptable Materials**

- Magnesium
- Other flammables

### Step-by-step Instructions

**Before training**

- If you plan to use your own computer, you will need software from the Machine
  Agency drive:
  - Download the VPanel folder, run setup.exe
  - Download the VPanel updater folder, run updater.exe
  - Install the Modela Driver for Windows. If you don’t do this, you may see an
    error saying that the machine is not found when connecting over USB. Note
    that you might have to have admin privileges to install this driver
    correctly.
  - Bring an adapter if your computer doesn’t have USB-A ports
- If you plan to use the dedicated Roland computer, the above software is
  already installed.
- Read the user manual and automatic toolchanger manual (except any assembly
  steps).

**Before using the machine**

- Turn on compressor (under workbench, red lever on left side)
- Ensure machine is plugged into power and the computer you’re using
- Turn on power switch on the right side of the mill control panel
- Turn on worklight inside enclosure
- Close the enclosure door, making sure that the orange interlock trigger on the
  inside of the door is aligned with the cutout on the frame.
- Open VPanel. Follow prompts, choose NC code.
- **Pressing ENTER to select the mode will move the machine – make sure cables,
  material, worklight, body parts, etc. are clear!**
- Once the mill has stopped moving, open the enclosure door and install all the
  tools in the tool changer as designated in your CAM file.
- For each tool:
  - Remove the tool by gently sliding it out of the holder
  - Place the tool in the tool maintenance harness and tighten the bolt on the
    side to secure the tool
  - Use the wrench and then your fingers to unscrew the housing
  - Gently snap out the collet
  - Thoroughly clean the interior of the housing with a brush
  - Replace the collet and re-tighten the housing to almost tight
  - Insert the end mill inside the collet
  - Tighten completely with two fingers on the wrench and replace inside the
    tool changer, making sure you hear the “click” of the switch in the tool
    changer that registers the tool
  - Verify in VPanel that the tool has been detected in the magazine
  - In VPanel, run the automatic tool offset calculation routine for each tool
    you plan to use. As indicated on the screen, plug the sensing cable (seated
    in the brass cylinder) into the z sensor pole at the lower right. Not doing
    this will cause a tool crash.
  - Press “calculate” and wait for the machine to touch each tool to the pole,
    then repeat with each tool.
- In VPanel, manually home the x-y plane by jogging the machine to the point
  that you want your x-y plane origin to be (looking from different angles,
  etc.) and set the home point.
- Then home the z-plane using the following procedure by placing the brass
  cylinder on the workpiece directly under the end mill. The machine will then
  touch the cylinder to zero the z axis.
- Move the brass Z sensor off the machine, clear of any moving parts.
- Make sure that you have exported a CAM file to the Roland as a post using .nc
  and not their proprietary instruction language. Then go to “cut,” load the
  file, and press “apply” to send the code to the machine.
- Close the enclosure door.
- Making sure the air compressor is still on, you can then start the job by
  pressing “enter” on the pendant.

**While using the machine**

- Keep the enclosure door closed when the machine is moving.
- Monitor the entire job, standing within arm’s reach of the emergency stop
  button.
- When the job is finished, allow the spindle and machine to come to a complete
  stop before opening the enclosure door.

**When you have finished using the machine**

- Use VPanel “Attach/Detach” function to return tool to magazine
- Vacuum excess material. Jog the Y axis to vacuum under the machine bed.
- Turn off compressor, release air using knob on underside of tank
- Turn off machine power
- Turn off worklight

### Best Practices

- Be mindful of the appropriate feeds and speeds for the material and tooling
  you’ve selected. Cutting too fast or slow can damage tooling and ruin
  projects.

### Tips and Tricks

- Be gentle with the enclosure interlock trigger (orange plastic bit on inside
  left corner of hatch). It is fragile and the mill can’t be operated if it
  breaks!
- Many operations require the enclosure door to be closed – if the machine is
  not moving, it may be because the door is open.

### Additional Information

- [User Manual](https://rolanddga.sharepoint.com/:b:/s/dealers/ETzhmoeLdblAnEOG604Djz8B_U1jLIMaPl2WpHwKRBIMIA)
- [Automatic Toolchanger Manual](https://rolanddga.sharepoint.com/:b:/s/dealers/EYKgwqHPIxpMoEJkDG_lipIBcGm8Ixgm-WRjPv2okXqpPA)

_(Both archived in Machine Agency drive)_
