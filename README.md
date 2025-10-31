
# Pi Probe  
*A handheld Raspberry Pi–based network diagnostic and analysis tool*

---

## Overview

**Pi Probe** is a compact, modular device built around the **Raspberry Pi Zero 2W**, designed to function as a multi-purpose network diagnostic interface. It consolidates essential utilities for **field diagnostics**, **system monitoring**, and **serial console access** into a single, portable device.

The project aims to create a self-contained platform capable of interfacing with network equipment, analyzing connectivity, and providing real-time system feedback — suitable for engineers, homelab environments, and educational settings.

---

## Objectives

- Develop a portable Linux-based device for on-site network analysis.  
- Integrate a simple **menu-driven interface** accessible through a small touchscreen or terminal UI.  
- Support key utilities:  
  - Network scanning and interface diagnostics (ping, traceroute, nmap).  
  - Serial console access for routers, switches, and embedded systems.  
  - Wi-Fi signal analysis and capture tools.  
  - SSH client capabilities for remote management.  
- Optimize for power efficiency and rapid deployment in the field.  
- Document all build stages, hardware integration, and code modules for reproducibility.

---

## Hardware

| Component                     | Description                          | Purpose                          |
|-------------------------------|--------------------------------------|----------------------------------|
| **Raspberry Pi Zero 2W**      | 1GHz quad-core ARM CPU, 512MB RAM    | Core compute platform            |
| **2.8" or 3.5" TFT Display**  | SPI touchscreen interface             | Local UI and diagnostics output  |
| **LiPo Battery (3.7V 2000–4000mAh)** | Rechargeable power source          | Portability                      |
| **USB Audio Interface (opt.)**| USB DAC for audio diagnostics         | Peripheral expansion              |
| **Micro-HDMI / USB OTG**      | External connectivity                 | Debugging, networking             |
| **3D-printed or acrylic shell**| Custom enclosure                     | Physical protection and usability |

---

## Software Stack

| Layer             | Tools / Frameworks                 | Function                          |
|-------------------|------------------------------------|-----------------------------------|
| **OS**            | Raspberry Pi OS Lite (Debian-based)| Base operating system             |
| **Interface**     | Python (Textual / curses), Bash     | User interface and menu logic     |
| **Networking**    | nmap, netcat, iperf3, tcpdump       | Network diagnostic suite          |
| **Serial Access** | minicom, pyserial                   | Console connectivity              |
| **Monitoring**    | psutil, vcgencmd, iwconfig          | Resource and network monitoring   |
| **Package Mgmt.** | apt, custom install scripts         | Dependency management             |

---

## System Architecture


+---------------------------------------------------+
|                  Pi Probe Stack                   |
+---------------------------------------------------+
|  Interface Layer: Python TUI / Touchscreen UI     |
|---------------------------------------------------|
|  Core Tools: nmap • tcpdump • ssh • minicom       |
|---------------------------------------------------|
|  OS Layer: Raspberry Pi OS Lite                   |
|---------------------------------------------------|
|  Hardware: Pi Zero 2W + TFT Display + LiPo        |
+---------------------------------------------------+

## Timeline


| Phase                                      | Timeframe    | Goals                                                                  |
| ------------------------------------------ | ------------ | ---------------------------------------------------------------------- |
| **Phase 1 – Research & Planning**          | Oct 2025     | Define problem, establish requirements, outline feature set            |
| **Phase 2 – Hardware Assembly**            | Nov 2025     | Source components, wire display and power circuits, verify connections |
| **Phase 3 – Software Setup**               | Dec 2025     | Flash OS, configure environment, set up diagnostic tools               |
| **Phase 4 – Interface Development**        | Jan–Feb 2026 | Build Python-based TUI, menu system, and scripts                       |
| **Phase 5 – Integration & Testing**        | Mar 2026     | Combine all subsystems, test in networked environments                 |
| **Phase 6 – Optimization & Documentation** | Apr–May 2026 | Power management, documentation, final Flex Friday presentation        |

Deliverables
Functional handheld diagnostic device
Custom Python interface and automation scripts
Documentation and hardware assembly guide
Presentation demo showcasing capabilities and workflow

## Long-Term Vision
Future revisions may include:
Modular expansion ports (GPIO headers for sensors)
Integration with Bluetooth LE for remote telemetry
Enhanced battery management and solar charging
Wi-Fi packet injection for advanced wireless analysis
Compact enclosure redesign using CNC or resin printing



## JOURNAL (whooo the boring part):

2025-10-31: did research to find tools for CAD, sourced some parts, and did research on comaptible components
2025-10-24: Wrote this README.md


License

This project is released under the MIT License.
All documentation, source code, and design files are open for educational and personal use.

Author

Wilder Forbes
Baxter Academy for Technology and Science
2025–2026 Engineering Design / Flex Friday Project
