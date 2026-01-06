# Macropad – Custom ZMK-Based Input Device

## Project Description

This project is a **custom-designed macropad** featuring mechanical keys and rotary encoders, built around the **XIAO nRF52840** microcontroller and powered by **ZMK firmware**.
It is designed as a **low-power, compact, and fully programmable HID device**, supporting advanced key behaviors, rotary encoders, and layered layouts.

The macropad targets users who need **reliable hardware macros**, media control, or workflow automation, while retaining full control over both **hardware and firmware**.

---

## Hardware Architecture

### Input

* **11 mechanical keys** arranged in a 3×4 grid (Top left position unused)
* **2 incremental rotary encoders**, each with integrated push button
* Matrix-based key scanning to minimize GPIO usage

* **Pin-out is provided in /Resources/Pins.pdf**

### Controller

* **XIAO nRF52840 Plus**

  * ARM Cortex-M4F
  * Native USB + BLE
  * Ultra-low power sleep modes
  * Fully supported by ZMK

### Connectivity

* USB-C for power and firmware flashing
* Optional BLE support via ZMK (configurable)

---

## Firmware

### Firmware Stack

* **ZMK Firmware**

  * Layered keymaps
  * Encoder support
  * Mod-tap, tap-dance, combos
  * USB HID and optional Bluetooth HID

### Flashing

* UF2 bootloader
* Drag-and-drop firmware flashing
* Compatible with command-line and CI-based builds

---

## Hardware Bill of Materials (BOM)

### Core Components

| Qty | Component               | Notes                         |
| --: | ----------------------- | ----------------------------- |
|   1 | XIAO nRF52840           | Main MCU, BLE + USB           |
|   1 | Custom PCB              | Multi-layer PCB               |
|   9 | Mechanical key switches | MX-compatible                 |
|   9 | Keycaps                 | 1U standard                   |
|   2 | Rotary encoders         | Incremental, with push button |
|   2 | Encoder knobs           | Optional, user preference     |

### Electrical Components

| Qty | Component                     | Specification                        |
| --: | ----------------------------- | ------------------------------------ |
|  11 | Diodes                        | 1N4148 or equivalent (SMD or THT)    |

### Mechanical & Assembly

| Qty | Component     | Notes             |
| --: | ------------- | ----------------- |
|   1 | Case (top)    | 3D printed or CNC |
|   1 | Case (bottom) | 3D printed or CNC |
| 4–6 | Screws        | M2 or M2.5        |
|   1 | Spacer set    | Optional          |

---

## Power Characteristics

* Powered via Battery or USB
* Optimized for low idle current
* BLE sleep modes supported
* Suitable for future battery-powered revisions

---

## Keymap

### Buttons

|       | Collum 1    | Collum 2    | Collum 3    |
|-------|-------------|-------------|-------------|
| Row 1 | Dead        | C_Mute      | TOGL LAYER 1|
| Row 2 | Rewind      | Play/Pause  | Skip        |
| Row 3 | Copy        | Paste       | Cut         |
| Row 4 | CTRL+SHFT+M | CTRL+SHFT+D | CTRL+Z      |

### Encoders

* **Encoder Left**
  * Consumer Volume Up/Down
* **Encoder Right**
  * Page Up/Down

---

## License

This project is intended to be open hardware / open source.
License details will be added once the hardware and firmware stabilize.

---
