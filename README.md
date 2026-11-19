# kaos-2

KAOS-2 HAB technology demonstration: a high-altitude balloon payload built around a Raspberry Pi Pico flight computer, two Raspberry Pi Zero 2 W camera recorders, and a LightAPRS tracker.

Plan and design notes: [`KAOS_PLAN.md`](KAOS_PLAN.md) and [`KAOS-2_Documentation.md`](KAOS-2_Documentation.md).

## Layout

| Folder | Contents |
|---|---|
| [`Software/`](Software/) | Flight computer code (Pico, Arduino core) |
| [`Electrical/KAOS-2_MainPCB/`](Electrical/KAOS-2_MainPCB/) | Main PCB KiCad project (`KAOS-2_Main.kicad_pro`), with its symbol and footprint library |
| [`Electrical/Symbols/`](Electrical/Symbols/), [`Electrical/Footprints/`](Electrical/Footprints/) | Shared KiCad symbol library and extra footprints (SCD30) |
| [`Test_Modules/`](Test_Modules/) | Bench tests for each module: LightAPRS 2.0 / HAB firmware, BMP388 (C SDK and Arduino), SCD30 (incl. calibration utility), SD card, clock, buzzer, MOSFET, Pico 2 W, and the Pi Zero camera recorder (`Camera/Video_Recorder/`) |
| Root images | Pinouts for the Pico, Pi Zero 2 W and LightAPRS |

## Open items

- **Two flight software versions.** [`Software/KAOS-2.ino`](Software/KAOS-2.ino) (559 lines, last changed 2026-09-21) and [`Software/KAOS-2/KAOS-2.ino`](Software/KAOS-2/KAOS-2.ino) (809 lines, last changed 2026-07-17) differ. Pick the flight version and delete or archive the other.
- **Not yet on GitHub:** the APRS PCB layout and the radio filter test board.
- The main PCB's symbol library (`Electrical/KAOS-2_MainPCB/KAOS-2.kicad_sym`) and the shared one (`Electrical/Symbols/KAOS-2.kicad_sym`) have drifted apart; merge them into one.

## History

Imported from [ColdBloodV/KSC](https://github.com/ColdBloodV/KSC) (`KAOS-2/`) with its commit history. Content from unmerged branches there was added too: the SCD30 calibration utility (`Star-Eater-patch-4`), the BMP_C README (`Star-Eater-patch-2`) and a `2Wscript.py` comment fix (`ColdBloodV-patch-1`).
