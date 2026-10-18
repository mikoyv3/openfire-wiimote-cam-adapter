# OpenFIRE DIY Wiimote IR Camera PCB

<p align="center">
  <table align="center">
    <tr>
      <td align="center"><b>PCB Layout Views</b></td>
      <td align="center"><b>Camera Pin Labels</b></td>
      <td align="center"><b>OpenFIRE Wiring Diagram</b></td>
    </tr>
    <tr>
      <td align="center" valign="middle">
        <img src="pics/front_pcb.png" width="280" alt="OpenFIRE Wiimote Camera PCB Front View">
        <br><br>
        <img src="pics/back_pcb.png" width="280" alt="OpenFIRE Wiimote Camera PCB Back View">
      </td>
      <td align="center" valign="middle">
        <img src="pics/Wiimote_IR_Camera_Back_-_tab_on_top_with_labels.png" width="280" alt="Wiimote IR Camera Back View Tab On Top With Pin Labels">
      </td>
      <td align="center" valign="middle">
        <img src="pics/openfire_pico_wii_ir_wiring.png" width="310" alt="OpenFIRE Raspberry Pi Pico Wiimote IR Wiring Diagram">
      </td>
    </tr>
  </table>
</p>




⚠️ **PRELIMINARY DESIGN NOTICE**
This PCB design has just been created and recently ordered with **JLCPCB**. It has **not yet been physically tested** or hand-assembled. However, the circuit topology is exceptionally simple and directly follows verified OpenFIRE community documentation, so it is highly anticipated to work without issues. Build at your own discretion while physical validation is underway!

---

## 🎗️ Credits & Attribution
This hardware design is an evolutionary community effort built upon the foundations laid by local open-source creators:
* **Circuit Architecture:** Derived from and heavily based on the open-source layout by **[@eatnooM](https://github.com/eatnooM)** ([eatnooM/pixart-sensor-adapter](https://github.com/eatnooM/pixart-sensor-adapter)).
* **3D Enclosure Development:** Enclosure integrations, printing assets, and specialized repository files are hosted, maintained, and credited to **[@slikvik55](https://github.com/slikvik55)** ([slikvik55/Lightgun3DParts](https://github.com/slikvik55/Lightgun3DParts)).
* **Assembly Tools:** Special thanks to **Gzus348** for creating the original camera jig design that makes sensor alignment straightforward.

---

## 🚀 Key Features of This Variant

* **Beginner-Friendly Through-Hole Resistors:** Uses through-hole **1/8 Watt axial resistors** for easy hand-soldering and a slim profile.
* **Optional 5-Pin JST Connector:** Features an elongated breakout footprint where the physical JST socket is optional for tight shell fits.
* **Zero Onboard Crystal Needed:** Relies on OpenFIRE's native pin-generated clock (`CLK`), omitting external oscillators.
* **Direct 3.3V Power Line:** Streamlined 3.3V power path supplied directly by a Raspberry Pi PICO.

---

## 📐 3D Shell Compatibility & Enclosure Notes

Tailored for **RetroMidget's Wiimote Camera Enclosure** using assets from [@slikvik55's Lightgun3DParts Repository](https://github.com/slikvik55/Lightgun3DParts/tree/main/WiiCamEnclosure):
* 📥 **Main Shell:** [WiiCamEnclosure Barrel STL](https://github.com/slikvik55/Lightgun3DParts/blob/main/WiiCamEnclosure/Barrel.stl)
* 📥 **Internal Mount:** [Camera Holder STL](https://github.com/slikvik55/Lightgun3DParts/blob/main/WiiCamEnclosure/CamHolder.stl)
* 📥 **Assembly Tool:** [Soldering Alignment Jig STL from **Gzus348**](https://github.com/eatnooM/pixart-sensor-adapter/blob/main/inline/printables/Wii-IR-camera-solder-guideGun4IR-v7.stl)

### Assembly & Soldering Tips:
* **Flux Recommendation:** Use high-quality flux like **Chip Quik SMD291** when soldering the Wii IR camera onto the PCB.
* **Soldering Assist:** Print and use the [Soldering Alignment Jig](https://github.com/eatnooM/pixart-sensor-adapter/blob/main/inline/printables/Wii-IR-camera-solder-guideGun4IR-v7.stl) to maintain flush alignment.

---

## 🛠 Ordering & Assembly Instructions

### PCB Ordering Specifications
⚠️ **CRITICAL FABRICATION NOTE:** When ordering from fabricators like **JLCPCB (Preferred)**, PCBWay, or OSH Park, you **MUST specify a PCB Thickness of 0.8mm**, standard 1.6mm thickness boards are too thick; the camera's rear header pins will not pass completely through the board to reach the solder pads!

* **Layers:** 2-layer
* **Thickness:** 0.8 mm (Do not use standard 1.6mm!)
* **Surface Finish:** HASL Lead-Free or ENIG (Recommended)

### Bill of Materials (BOM)
* **U1:** Salvaged Nintendo Wiimote IR Camera Sensor
* **R1:** 4.7kΩ Through-Hole Resistor (**1/4 Watt / Axial**)
* **R2:** 4.7kΩ Through-Hole Resistor (**1/4 Watt / Axial**)
* **JST (Optional):** 5-pin JST PH 2.0 Connector (GND, CLK, SDA, SCL, VCC)

## 📌 Wiring Diagram Alignment
Ensure your microcontroller pinouts map directly to the corresponding board output lines:
* **VCC:** Connect to `3V3 OUT`
* **CLK:** Connect to your configured Clock generation pin (e.g., `GP22`)
* **GND:** Connect to `GND`
* **SCL:** Connect I2C SCL (e.g., `GP21`)
* **SDA:** Connect I2C SDA (e.g., `GP20`)

---

## 📜 License
Following the upstream license of the original work, this project is licensed under the **Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)**. You are free to share and adapt this work as long as you provide appropriate attribution and distribute your contributions under the same license.
