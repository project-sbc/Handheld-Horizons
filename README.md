<h1 align="center">Handheld Horizons</h1>

<p align="center">
  A controller-first control centre for Windows handheld gaming PCs.<br>
  Power, fans, controls, games and system settings in one place, without reaching for a mouse.
</p>

<p align="center">
  <a href="https://github.com/project-sbc/Handheld_Horizons/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/project-sbc/Handheld_Horizons?label=latest%20release"></a>
  <a href="https://github.com/project-sbc/Handheld_Horizons/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/project-sbc/Handheld_Horizons/total?label=downloads"></a>
  <a href="https://www.youtube.com/@HandheldHardware"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-Handheld%20Hardware-red?logo=youtube"></a>
  <a href="https://www.patreon.com/cw/u23425837"><img alt="Patreon" src="https://img.shields.io/badge/Patreon-early%20access-orange?logo=patreon"></a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=dE6AA1XwAIE">
    <img alt="Watch the Handheld Horizons overview video" src="https://img.youtube.com/vi/dE6AA1XwAIE/maxresdefault.jpg" width="720">
  </a>
  <br>
  <em>Watch the overview video</em>
</p>

## What it is

Handheld Horizons replaces the pile of utilities a Windows handheld usually needs with one
app built to be driven from the controller. It has two faces:

- **The full-screen app**: a console-style home for launching games and changing every setting.
- **Quick Access**: a side overlay you open on top of a running game with a hotkey, for the
  things you change mid-session.

A background service does the hardware work, so your settings keep applying whether or not
the app's window is open.

> [!WARNING]
> Handheld Horizons is in **early access**. It changes low-level hardware settings and is
> provided as is, with no warranty. Read the [disclaimer](#disclaimer) before installing.

## Features

**Performance and power**
- TDP profiles with separate sustained and burst limits, and optional battery-only values
- Power profiles for CPU behaviour
- Fan profiles with a draggable fan curve and presets
- AMD Radeon driver settings, on devices with a supported AMD GPU
- A performance overlay with FPS, frame times and power readings

**Controls**
- Controller profiles: button remapping, stick response curves and deadzones
- RGB lighting profiles
- Hotkeys on the handheld's own buttons, with a record-to-bind editor
- Optional controller hiding while a menu is open, through [HidHide](https://github.com/nefarius/HidHide)

**Games**
- A game library that finds your installed games and fetches cover art
- Per-game profiles: a game gets its own TDP, power, fan and controller profiles, applied
  when it launches and put back when it closes
- A second set of per-game profiles for when an eGPU is connected
- An app switcher for jumping between, suspending and closing running games

**Automation**
- Scenes: one profile from each category, applied together in one press
- Triggers that run actions on events such as charger plugged in, controller connected,
  a temperature or a time of day
- Radial menus and Quick Actions tiles for anything an action can do

**System**
- Display management: resolution, refresh rate and arrangement
- Audio, brightness, Wi-Fi and Bluetooth controls
- Task manager, startup apps, installed programs, services and disk cleanup
- A phone remote: control the handheld from a phone's browser on the same Wi-Fi, paired by QR code

**Make it yours**
- Edit Mode: rearrange, resize, add and remove what is on the Home and Quick Access pages
- Themes, colours and wallpaper
- A setup wizard with Simple and Advanced starting layouts
- A built-in updater

## Supported devices

| Device | Support |
| :--- | :--- |
| Lenovo Legion Go | Full: TDP, fans, controller remapping, RGB, device buttons |
| Lenovo Legion Go 2 | Supported, less tested than the Legion Go |
| Other AMD handhelds and PCs | Generic: TDP, power profiles and everything that is not device-specific |
| Other Intel handhelds and PCs | Generic: power profiles and everything that is not device-specific |

Features a device cannot do are hidden on that device.

## Contact

Reach out to me at handheld.hardware@outlook.com for device support or general communication.

Come join me in the Handheld Horizons channel at the Handhelds United [Discord](https://discord.gg/2ePs7bWgkM)

## Requirements

- 64-bit Windows 10 (version 2004 or later) or Windows 11
- Administrator rights to install, because Setup registers a Windows service
- **[PawnIO](https://pawnio.eu/)** for TDP control. PawnIO is a separate, signed driver and is
  not bundled. Setup offers to open its download page if it is missing. Without it, TDP
  control is unavailable and everything else works.
- **[HidHide](https://github.com/nefarius/HidHide)** (optional) to hide the controller from
  games while a Handheld Horizons menu is open. Setup can download and install it for you.

## Installation

1. Download `HandheldHorizons-SystemSetup-<version>.exe` from the
   [latest release](https://github.com/project-sbc/Handheld_Horizons/releases/latest).
2. Run it and follow the wizard. Install PawnIO when Setup asks, if you want TDP control.
3. Handheld Horizons starts when Setup finishes and walks you through first-time setup.

**Legion Go owners:** Legion Space and Handheld Horizons both try to control the controller,
and running them together causes problems. Handheld Horizons detects Legion Space and offers
to stop and disable it.

**Updating:** the app checks this repository for new releases and installs them from
About ▸ Updates. You can also run a newer installer over the top of an existing install.

**Uninstalling:** use Windows Settings ▸ Apps. The uninstaller asks whether to keep your
profiles and settings.

## Early access and support

Handheld Horizons is built by one person and funded by the people who use it.
[Patreon](https://www.patreon.com/cw/u23425837) supporters on the early-access tier get new
builds before they are released here.

- [Patreon](https://www.patreon.com/cw/u23425837): early-access builds and ongoing support
- [Ko-fi](https://ko-fi.com/project_sbc) or [PayPal](https://www.paypal.com/donate?business=NQFQSSJBTTYY4&currency_code=USD): a one-off tip
- [YouTube](https://www.youtube.com/@HandheldHardware): guides and release videos

## Bugs and feature requests

Open an [issue](https://github.com/project-sbc/Handheld_Horizons/issues) and include:

- your device and Windows version
- the Handheld Horizons version, from the About page
- what you did, what you expected and what happened
- the logs from `C:\ProgramData\HandheldHorizons\logs`

This repository holds releases only. The source code is not published here.

## Disclaimer

Handheld Horizons changes low-level hardware settings: processor power limits, fan speeds,
controller firmware settings and driver settings. Values outside what the manufacturer
intended can cause instability, overheating, data loss, shortened battery or component life,
or permanent hardware damage, and may void your device's warranty.

**THE SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE", WITHOUT WARRANTY OF ANY KIND, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
PARTICULAR PURPOSE AND NON-INFRINGEMENT. YOU USE IT ENTIRELY AT YOUR OWN RISK. TO THE MAXIMUM
EXTENT PERMITTED BY LAW, IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, INCLUDING DAMAGE TO HARDWARE, LOSS OF DATA OR LOSS OF USE, ARISING
FROM OR IN CONNECTION WITH THE SOFTWARE OR ITS USE.**

By downloading, installing or using Handheld Horizons you accept these terms. If you do not
accept them, do not install it.

Handheld Horizons is an independent project. It is not affiliated with, endorsed by or
supported by Lenovo, AMD, Intel, Microsoft, Valve or any other hardware or software vendor.
All product names and trademarks belong to their owners. Do not contact your device's
manufacturer for support with problems caused by this software.

## Credits

Handheld Horizons is built on open-source work, including [Avalonia](https://avaloniaui.net/),
[PawnIO](https://pawnio.eu/), [HidHide](https://github.com/nefarius/HidHide) and Intel's
[PresentMon](https://github.com/GameTechDev/PresentMon). Every bundled component and the full
text of its licence is listed in the app under About ▸ Credits ▸ Open-source licenses.
