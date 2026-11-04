# AltSDR

A receive-only SDR application for Windows, in one glued window: spectrum and waterfall, noise reduction, band buttons, memory banks and a scanner. It runs the **SDRplay RSPdx / RSPdx-R2**, an **RTL-SDR (Blog V4)** and an **Airspy HF+ / HF+ Discovery**.

This repository holds the installers only.

## Download

**[Latest installer](https://github.com/Jull1ano/altsdr-releases/releases/latest)**: under *Assets*, download `AltSDR-<version>-setup.exe`.

## Install

1. Run the setup file. It needs Windows 10 or 11 (64-bit) and asks for administrator rights.
2. The installer is not code-signed, so Windows may warn you:
   - **"Windows protected your PC"** (SmartScreen): click **More info**, then **Run anyway**.
   - **Smart App Control** (Windows 11, when it is on) blocks unsigned programs and offers no per-file exception.
3. Install what your radio needs:
   - **RSPdx / RSPdx-R2:** the [SDRplay API 3.x](https://www.sdrplay.com/api/). The setup offers the page when the API is missing.
   - **RTL-SDR or Airspy HF+:** the WinUSB driver (Zadig). The steps are in `docs\RTLSDR_SETUP.md` and `docs\AIRSPY_HF_SETUP.md` in the install folder. Choose the radio under **OPT -> Select Input**.
4. Start AltSDR and press **PLAY!** if the radio has not started by itself.

## Good to know

- AltSDR starts with a tuned, ready-made setup: colours, layout, noise reduction and band memories. It is yours to change, and **OPT -> Reset to Default Settings** brings it back.
- Your settings live in `%APPDATA%\AltSDR`. Installing a newer version keeps them, and the uninstaller asks before removing them.
- There are no memory banks in the installer. Make your own in the **MEM PAN** panel, or open SDRuno `.s1b` banks.
- **Bias-T is off** and stays off until you switch it on: it puts DC on the antenna port.

## Licence

AltSDR is free software under the [GNU General Public License v3](LICENSE) and includes third-party GPL code (WDSP, FFTW). For the source code of a release, open an issue in this repository.

SDRuno, SDRplay and RSPdx are trademarks of SDRplay Ltd. AltSDR is an independent project and is not affiliated with or endorsed by SDRplay. The SDRplay API is not included: it comes from SDRplay's own installer.
