# OpenFIRE (I2C) DIY Wiimote IR Camera PCB

<p align="center">
  <table align="center">
    <tr>
      <td align="center"><b>Variant Layout</b></td>
      <td align="center"><b>PCB Front View</b></td>
      <td align="center"><b>PCB Back View</b></td>
      <td align="center"><b>OpenFIRE Official Wiring Diagram & Camera Pin Labels</b></td>
    </tr>
    <tr>
      <td align="center" valign="middle"><b>JST PH 2.0</b><br>(1/4W Resistors)<br>PCB Size<br>13*30.1 mm</td>
      <td align="center" valign="middle">
        <img src="pics/front_jlcpcb.png" width="160" alt="JST PH 2.0 Front View">
      </td>
      <td align="center" valign="middle">
        <img src="pics/back_jlcpcb.png" width="160" alt="JST PH 2.0 Back View">
      </td>
      <td align="center" valign="middle" rowspan="4">
        <img src="pics/openfire_pico_wii_ir_wiring_official.png" width="410" alt="OpenFIRE Raspberry Pi Pico Wiimote IR Wiring Diagram">
      </td>
    </tr>
    <tr>
      <td align="center" valign="middle" colspan="3">
        <b>🟣 <a href="https://oshpark.com/shared_projects/DqOJEs91" target="_blank">Order JST PH 2.0 Board from OSH Park (0.8mm thickness)</a></b>
      </td>
    </tr>
  </table>
</p>

<p align="center">
  <table align="center">
    <tr>
      <td align="center"><b>Variant Layout</b></td>
      <td align="center"><b>PCB Front View</b></td>
      <td align="center"><b>PCB Back View</b></td>
      <td align="center"><b>OpenFIRE Unofficial Wiring Diagram</b></td>
    </tr>
    <tr>
      <td align="center" valign="middle"><b>JST PH 2.0</b><br>(1/4W Resistors<br><b> and 0.1µF Capacitor)</b><br>PCB Size<br>13*30.1 mm</td>
      <td align="center" valign="middle">
        <img src="pics/OpenFIRE-Resistors-PCB-JST_PH2_UO_Front.png" width="160" alt="JST PH 2.0 Front View">
      </td>
      <td align="center" valign="middle">
        <img src="pics/OpenFIRE-Resistors-PCB-JST_PH2_UO_Back.png" width="160" alt="JST PH 2.0 Back View">
      </td>
      <td align="center" valign="middle">
        <img src="pics/openfire_pico_wii_ir_wiring_unofficial.png" width="380" alt="OpenFIRE Raspberry Pi Pico Wiimote IR Wiring Diagram">
      </td>
    </tr>
    <tr>
      <td align="center" valign="middle"><b>Design Purpose & Deviation Notes</b></td>
      <td align="center" valign="middle" colspan="3" align="left">
     Discussions from OpenFIRE Discord suggested that adding a decoupling ceramic capacitor on the camera module's power rail is best practice to stabilize voltage delivery and minimize potential noise. There is an active documentation change request to update the official OpenFIRE schematic guidelines accordingly (<a href="https://github.com/TeamOpenFIRE/OpenFIRE-App/issues/120" target="_blank">Issue #120</a>). In the meantime, this layout provides that feature as an option.
      </td>
    </tr>
    <tr>
      <td align="center" valign="middle" colspan="4">
        <b>🟣 <a href="https://oshpark.com/shared_projects/3LxfKNea" target="_blank">Order JST PH 2.0 Unofficial Board from OSH Park (0.8mm thickness)</a></b>
      </td>
    </tr>
  </table>
</p>



<kbd>
<p align="center">
🛑⚠️ Gun4IR/OpenFIRE/Blamcon DIY: The Easy, Pre-Assembled JLCPCB Method ⚠️🛑 <br>  (ALTERNATIVE / PLAN B / OPTION 2)
</p>
<p align="center">
  <img src="pics/pixart-sensor-adapter-inline-connector-panel-2-vert.png" width="360" alt="v1.3">
</p>

If you need the easiest and fastest way to build your IR camera pcb. By leveraging JLCPCB’s PCBA (PCB Assembly) service, you receive a nearly complete, surface-mount-assembled board straight from the factory.

You do not need to hand-solder tiny surface-mount components. The factory handles 99% of the work. Your only job is to hand-solder the Wii IR camera (and standard through-hole connectors like the Pro Micro headers or pins) once the board arrives.

For step-by-step instructions on how to configure your fabrication settings, upload your files, and complete your order, follow my detailed [JLCPCB PCBA Ordering Guide](https://github.com/mikoyv3/openfire-wiimote-cam-adapter/blob/main/JLCPCB/PCBA_Ordering.md).

* **Base Board Design:** [eatnooM PixArt Sensor Adapter (Release v1.3)](https://github.com/eatnooM/pixart-sensor-adapter/releases/tag/v1.3)
* **Required (not included):** [JST MX 1.25mm Wire Cable Connector (4 Pin)](https://www.aliexpress.com/item/1005007277110532.html)
* **Preferred Fabricator:** [JLCPCB](https://jlcpcb.com/)

</kbd>

## 🛠️ Assets
[Download](https://github.com/mikoyv3/openfire-wiimote-cam-adapter/releases) the corresponding Gerber zip files depending on your preferred connector type and size layout constraint.



---

## 🎗️ Credits & Attribution
This hardware design is an evolutionary community effort built upon the foundations laid by local open-source creators:
* **Circuit Architecture:** Derived from and heavily based on the open-source layout by **[@eatnooM](https://github.com/eatnooM)** ([eatnooM/pixart-sensor-adapter](https://github.com/eatnooM/pixart-sensor-adapter)).
* **3D Enclosure Development:** Enclosure integrations, printing assets, and specialized repository files are hosted, maintained, and credited to **[@slikvik55](https://github.com/slikvik55)** ([slikvik55/Lightgun3DParts](https://github.com/slikvik55/Lightgun3DParts)).
* **Assembly Tools:** Special thanks to **Gzus348** for creating the original camera jig design that makes sensor alignment straightforward.

---

## 🚀 Key Features

* **Beginner-Friendly Through-Hole Resistors:** Uses through-hole resistors (4.7kΩ) for easy hand-soldering and a slim profile.
* **Official Hardware Guide Aligned:** The trace layout is designed directly from the "DIY Wiimote Conversion (Using Clock Pin)" schematic on **page 4** of the official **[OpenFIRE-Hardware-Guide_1.3.pdf](https://openfirelightgun.org/wp-content/uploads/2026/10/OpenFIRE-Hardware-Guide_1.3.pdf)** manual.
* **Optional 5-Pin JST Connector:** Physical JST socket will fit the barrel shell and should be inserted from the back and the IR camera cover last. 
* **Enclosure-Ready Geometry:** Formatted specifically to seat right into RetroMidget's Wiimote camera housing using standard dimensions from @slikvik55's Lightgun3DParts repository.
* **Zero Onboard Crystal Needed:** Relies on OpenFIRE's native pin-generated clock (`CLK`), omitting external oscillators.
* **Direct 3.3V Power Line:** Streamlined 3.3V power path supplied directly by a Raspberry Pi Pico.

---

## 📐 3D Shell Compatibility & Enclosure Notes

Tailored for **RetroMidget's Wiimote Camera Enclosure** using assets from [@slikvik55's Lightgun3DParts Repository](https://github.com/slikvik55/Lightgun3DParts/tree/main/WiiCamEnclosure):
* 📥 **Main Shell:** [WiiCamEnclosure Barrel STL](https://github.com/slikvik55/Lightgun3DParts/blob/main/WiiCamEnclosure/Barrel.stl)
* 📥 **Internal Mount:** [Camera Holder STL](https://github.com/slikvik55/Lightgun3DParts/blob/main/WiiCamEnclosure/CamHolder.stl)
* 📥 **Assembly Tool:** [Soldering Alignment Jig STL from **Gzus348**](https://github.com/eatnooM/pixart-sensor-adapter/blob/main/inline/printables/Wii-IR-camera-solder-guideGun4IR-v7.stl)

### Assembly & Soldering Tips:
* **Wii IR Plastic Placement:** Remember to salvage the original dark translucent **Wii IR plastic screen** from the front of the donor Wii remote shell. It needs to be **cut to fit** cleanly inside the [Camera Holder](https://github.com/slikvik55/Lightgun3DParts/blob/main/WiiCamEnclosure/CamHolder.stl) piece during assembly. This lens acts as an essential optical filter that blocks ambient room light, ensuring the camera tracks only pure infrared lightbar signals.
* **Flux Recommendation:** Use high-quality flux like **Chip Quik SMD291** when soldering the Wii IR camera onto the PCB.
* **Soldering Assist:** Print and use the [Soldering Alignment Jig](https://github.com/eatnooM/pixart-sensor-adapter/blob/main/inline/printables/Wii-IR-camera-solder-guideGun4IR-v7.stl) to maintain flush alignment.

<img src="pics/JST_PH_OK.jpg" width="150" alt="JST PH 2.0"> <img src="pics/JST_PH_OK2.jpg" width="150" alt="JST PH 2.0"> <img src="pics/JST_PH_OK3.jpg" width="150" alt="JST PH 2.0"> <img src="pics/JST_PH_OK5.jpg" width="150" alt="JST PH 2.0"> <img src="pics/JST_PH_OK4.jpg" width="150" alt="JST PH 2.0">

---

## 🛠 Ordering & Assembly Instructions

### PCB Ordering Specifications
⚠️ **CRITICAL FABRICATION NOTE:** When ordering from fabricators like **JLCPCB (Preferred)**, PCBWay, or OSH Park, you **MUST specify a PCB Thickness of 0.8mm**, standard 1.6mm thickness boards are too thick and will not go through the Jig and Barrel!

* **Layers:** 2-layer
* **Thickness:** 0.8 mm (Do not use standard 1.6mm!)
* **Surface Finish:** HASL
  
### Bill of Materials (BOM)
* **U1:** Salvaged Nintendo Wiimote IR Camera Sensor
* **R1:** 4.7kΩ Through-Hole Metal Film Resistor 
* **R2:** 4.7kΩ Through-Hole Metal Film Resistor
* **C1:** 100NF 0.1uF Through-Hole Monolithic Ceramic Capacitor (Unofficial)
* **JST (Optional):** 5-pin JST (PH 2.0) Connector (GND, VCC, SDA, SCL, CLK) https://www.aliexpress.com/item/1005010712096781.html

## 📌 Wiring Diagram Alignment

<img src="pics/Wiimote_IR_Camera_Back_-_tab_on_top_with_labels.png" width="280" alt="Wiimote IR Camera Back View Tab On Top With Pin Labels ">
        
Ensure the Raspberry Pi Pico pinouts map directly to the corresponding board output lines. While you can configure your own pinouts in firmware, here is the recommended standard layout:

* **GND:** Connect board **GND** ➔ Raspberry Pi Pico **GND** (Any ground pin)
* **VCC:** Connect board **VCC** ➔ Raspberry Pi Pico **3V3 OUT**
* **SDA:** Connect board **SDA** ➔ Raspberry Pi Pico **GP20**
* **SCL:** Connect board **SCL** ➔ Raspberry Pi Pico **GP21**
* **CLK:** Connect board **CLK** ➔ Raspberry Pi Pico **GP22**
  *(💡 Note: GP22 is the suggested pin-out. Clock pin will need to be set in the OpenFIRE application).*


---

## 📜 License
Following the upstream license of the original work, this project is licensed under the **Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)**. You are free to share and adapt this work as long as you provide appropriate attribution and distribute your contributions under the same license.
