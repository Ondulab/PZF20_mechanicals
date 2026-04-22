# PZF20 – Mechanical Enclosure

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

> **© 2026 Ondulab** — This project is licensed under [CC BY-NC-SA 4.0](LICENSE).
> Free to share and adapt for **non-commercial use only**, with attribution and under the same licence.

---

This repository contains the mechanical design files for the **PZF20 piezoelectric balanced preamplifier** enclosure, designed with [FreeCAD](https://www.freecad.org/).

The enclosure is intended to house the PZF20 electronics board — a small board using a **LSK389B dual N-channel JFET** and a **LSK170B N-channel JFET** for preamplification and impedance matching of two piezoelectric crystals wired in balance. These JFETs are ultra-low noise components.

➡️ Electronics project: [PZF20_electronics](https://github.com/Ondulab/PZF20_electronics)

---

## Contents

- `Enclosure.FCStd` — FreeCAD source file for the mechanical enclosure

---

## About the PZF20

The problem with piezo guitar pickups and piezoelectric crystals is that they are not well matched to typical audio inputs. By their nature, they can generate a lot of signal, but they cannot drive a 50 kΩ typical line input. The pickup needs to work into a much higher impedance, typically 1 MΩ or so.

When a piezoelectric disk's output is plugged directly into a line input (typical impedance 50 kΩ) or a plug-in-power mic input (typical impedance ~7 kΩ), the result sounds tinny. This is because the piezo sensor presents its signal through a small series capacitance (typically 15 nF or less), which — combined with a normal line input — forms a high-pass filter that eliminates bass frequencies.

The PZF20 circuit solves that, amplifying the signal by approximately 15–30 dB depending on the impedance of the recording equipment. With a 10 kΩ impedance recorder input (simulated), approximately **24 dB** of gain is achieved.

It features:
- **Balanced input and output** — minimises electric noise picked up from the environment ([Balanced audio](https://en.m.wikipedia.org/wiki/Balanced_audio))
- **+48 V phantom power** operation ([Phantom power](https://en.m.wikipedia.org/wiki/Phantom_power))
- XLR 3-pin connector (standard wiring: Pin 1 = shield, Pin 2 = hot, Pin 3 = cold)

---

## Enclosure Requirements

- The PCB **must not come into contact with the metal box** — use standoffs to mount it, or provide appropriate insulation.
- The piezoelectric disks must be **electrically insulated** from the metal box.
- Non-electrically-conductive super glue can be used to mount piezoelectric disks to a flat surface inside.
- Use a **shielded cable with 3 conductors** for best results (suggested: Digi-Key Part Number `30-00910-5-ND`).

---

## Applications

The complete system (electronics + enclosure) can be used for:

- Piezo guitar/instrument pickups
- Reverb plate microphones
- Listening to the insides of an engine
- Recording vibrating surfaces
- Bearing fault detection (with a dedicated +48 V phantom power supply and headphone jack)
- **Hydrophone** — using PZT-5H piezoelectric tubes encapsulated in resin (e.g. Ecopoxy Flowcast) or oil (olive/sunflower oil as an eco-friendly alternative to kerosene)

---

## References

- Electronics project: [PZF20_electronics](https://github.com/Ondulab/PZF20_electronics)
- [Wikipedia – Balanced audio](https://en.m.wikipedia.org/wiki/Balanced_audio)
- [Wikipedia – Phantom power](https://en.m.wikipedia.org/wiki/Phantom_power)
- [Phantom power supply with headphone jack (9V battery)](https://github.com/Supermagnum/48power)
- [Locus Onus – Hydrophone mounting methods](https://locusonus.org/wiki/index.php?page=Hydrophone.en)
- [FreeCAD](https://www.freecad.org/)

---

## Made With

- [FreeCAD](https://www.freecad.org/) — free and open-source parametric 3D CAD modeller
