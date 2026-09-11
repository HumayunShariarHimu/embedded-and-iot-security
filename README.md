# embedded-and-iot-security

> A curated and organized collection of resources related to **embedded-and-iot-security**.

**Maintained by [Humayun Shariar Himu](https://github.com/HumayunShariarHimu)**

# Embedded & IoT Security

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

> A curated collection of tools, frameworks, hardware, books, research papers, case studies, training resources, and communities for embedded systems and IoT security research.

Botnets like [Mirai](<https://en.wikipedia.org/wiki/Mirai_(malware)>) demonstrated how weak security in embedded and IoT devices can be leveraged at massive scale. This list exists to help both newcomers and experienced researchers navigate the field.

- **New to embedded/IoT security?** Start with [Books](#books), [Standards & Guidelines](#standards--guidelines), and [Case Studies](#case-studies).
- **Ready to analyze a device or firmware image?** Jump straight to [Analysis Frameworks](#analysis-frameworks) — most require no prior expertise to get meaningful first results.
- **Want hands-on practice?** See [Free Training & CTFs](#free-training--ctfs).

---

## Contents

- [Software Tools](#software-tools)
  - [Analysis Frameworks](#analysis-frameworks)
  - [Analysis Tools](#analysis-tools)
  - [Extraction Tools](#extraction-tools)
  - [Support Tools](#support-tools)
  - [Misc Tools](#misc-tools)
- [Hardware Tools](#hardware-tools)
  - [Bluetooth / BLE Tools](#bluetooth--ble-tools)
  - [ZigBee Tools](#zigbee-tools)
  - [SDR Tools](#sdr-tools)
  - [RFID / NFC Tools](#rfid--nfc-tools)
- [Standards & Guidelines](#standards--guidelines)
- [Books](#books)
- [Research Papers](#research-papers)
- [Case Studies](#case-studies)
- [Free Training & CTFs](#free-training--ctfs)
- [Websites](#websites)
  - [Blogs](#blogs)
  - [Tutorials and Technical Background](#tutorials-and-technical-background)
  - [YouTube Channels](#youtube-channels)
- [Conferences & Communities](#conferences--communities)
- [Contributing](#contributing)
- [License](#license)

---

## Software Tools

Software tools for analyzing embedded/IoT devices and firmware.

### Analysis Frameworks

- [EXPLIoT](https://gitlab.com/expliot_framework/expliot) — Pentest framework in the spirit of Metasploit, purpose-built for IoT.
- [FACT — The Firmware Analysis and Comparison Tool](https://fkie-cad.github.io/FACT_core/) — Full-featured static analysis framework: firmware extraction, plug-in based analysis, and cross-version comparison.
  - [Improving your firmware security analysis process with FACT](https://passthesalt.ubicast.tv/videos/improving-your-firmware-security-analysis-process-with-fact/) — Conference talk about FACT. 🎥
- [FwAnalyzer](https://github.com/cruise-automation/fwanalyzer) — Rule-based firmware security analysis, designed to slot into a DevSecOps/CI pipeline.
- [HAL — The Hardware Analyzer](https://github.com/emsec/hal) — Reverse engineering and manipulation framework for gate-level netlists.
- [HomePWN](https://github.com/ElevenPaths/HomePWN) — Swiss Army knife for IoT device pentesting.
- [IoTSecFuzz](https://gitlab.com/invuls/iot-projects/iotsecfuzz) — Automates IoT security analysis across hardware, software, and communication layers.
- [Killerbee](https://github.com/riverloopsec/killerbee) — Framework for testing and auditing ZigBee and IEEE 802.15.4 networks.
- [PRET](https://github.com/RUB-NDS/PRET) — Printer Exploitation Toolkit.
- [Routersploit](https://github.com/threat9/routersploit) — Exploitation framework dedicated to embedded/networking devices.
- [Attify-Zigbee-Framework (AZSploit)](https://github.com/Cisco-Talos/attify-zigbee-framework) — Framework for identifying vulnerabilities in ZigBee-based IoT devices.
- [GATTacker](https://github.com/securing/gattacker) — Node.js framework for BLE man-in-the-middle attacks and device impersonation.
- [IoTSeeker](https://github.com/rapid7/IoTSeeker) — Scans networks for IoT devices still using vendor default credentials.

### Analysis Tools

- [Binwalk](https://github.com/ReFirmLabs/binwalk) — Searches binaries for embedded files/signatures and extracts them.
- [unblob](https://github.com/onekey-sec/unblob) — Modern, actively maintained firmware extraction suite; a strong complement (or alternative) to Binwalk for deeply nested container formats.
- [cwe_checker](https://github.com/fkie-cad/cwe_checker) — Detects vulnerable patterns in ELF binaries (x86, ARM, MIPS; experimental bare-metal support).
- [emba](https://github.com/e-m-b-a/emba) — Analyzes Linux-based firmware of embedded devices end-to-end.
- [Firmadyne](https://github.com/firmadyne/firmadyne) — Emulates and pentests firmware images.
- [Firmwalker](https://github.com/craigz28/firmwalker) — Searches extracted firmware for files and strings of interest.
- [Firmware Slap](https://github.com/ChrisTheCoolHut/Firmware_Slap) — Finds vulnerabilities via concolic analysis and function clustering.
- [Ghidra](https://ghidra-sre.org/) — NSA-developed software reverse engineering suite; handles arbitrary binaries given CPU architecture and endianness.
- [angr](https://angr.io/) — Binary analysis platform supporting symbolic execution, useful for firmware and embedded binary triage.
- [Radare2](https://github.com/radare/radare2) — Reverse engineering framework with an extensive CLI toolset and broad format support.
- [Trommel](https://github.com/CERTCC/trommel) — Searches extracted firmware images for files and information of interest.

### Extraction Tools

- [FACT Extractor](https://github.com/fkie-cad/fact_extractor) — Auto-detects container formats and runs the matching extraction tool.
- [Firmware Mod Kit](https://github.com/rampageX/firmware-mod-kit/wiki) — Extraction utilities for a range of firmware container formats.
- [The SRecord Package](http://srecord.sourceforge.net/) — Tools for manipulating EPROM files and converting between binary formats.

### Support Tools

- [JTAGenum](https://github.com/cyphunk/JTAGenum) — Adds JTAG enumeration capability to an Arduino.
- [OpenOCD](http://openocd.org/) — Free, open on-chip debugging, in-system programming, and boundary-scan testing.
- [QEMU](https://www.qemu.org/) — General-purpose CPU emulator commonly used to emulate firmware/user-mode binaries for dynamic analysis (paired with Firmadyne, FirmAE, etc.).

### Misc Tools

- [Cotopaxi](https://github.com/Samsung/cotopaxi) — Security testing tools targeting IoT-specific network protocols.
- [dumpflash](https://github.com/ohjeongwook/dumpflash) — Low-level NAND flash dump and parsing utility.
- [flashrom](https://github.com/flashrom/flashrom) — Detects, reads, writes, verifies, and erases flash chips.
- [Samsung Firmware Magic](https://github.com/chrivers/samsung-firmware-magic) — Decrypts Samsung SSD firmware updates.

## Hardware Tools

- [Bus Blaster](http://dangerousprototypes.com/docs/Bus_Blaster) — Interacts with hardware debug ports such as [UART](https://en.wikipedia.org/wiki/Universal_asynchronous_receiver-transmitter) and [JTAG](https://en.wikipedia.org/wiki/JTAG).
- [Bus Pirate](http://dangerousprototypes.com/docs/Bus_Pirate) — Interacts with UART, JTAG, and other hardware debug interfaces.
- [Shikra](https://int3.cc/products/the-shikra) — Interacts with UART, JTAG, and several other embedded protocols.
- [JTAGULATOR](http://www.grandideastudio.com/jtagulator/) — Rapidly identifies JTAG (and UART) pinouts.
- [Saleae](https://www.saleae.com/) — Popular, easy-to-use logic analyzer with broad protocol support. 💶
- [Ikalogic](https://www.ikalogic.com/pages/logic-analyzer-sp-series-sp209) — Logic analyzer alternative to Saleae. 💶
- [HydraBus](https://hydrabus.com/hydrabus-1-0-specifications/) — Open-source multi-protocol tool similar to the Bus Pirate, with added NFC capability.
- [ChipWhisperer](https://newae.com/chipwhisperer/) — Platform for glitch and side-channel attack research.
- [Glasgow](https://github.com/GlasgowEmbedded/Glasgow) — Versatile tool for exploring and debugging digital interfaces.
- [J-Link](https://www.segger.com/products/debug-probes/j-link/models/model-overview/) — USB-powered JTAG/SWD debug probes for a wide range of CPU cores. 💶

### Bluetooth / BLE Tools

- [Ubertooth One](https://greatscottgadgets.com/ubertoothone/) — Open-source 2.4 GHz wireless development platform, well suited to Bluetooth experimentation.
- [Bluefruit LE Sniffer](https://www.adafruit.com/product/2269) — Accessible Bluetooth Low Energy sniffer.
- [nRF Sniffer for Bluetooth LE](https://www.nordicsemi.com/Products/Development-tools/nRF-Sniffer-for-Bluetooth-LE) — Free BLE packet sniffer from Nordic Semiconductor, built on inexpensive nRF52 hardware.

### ZigBee Tools

- [ApiMote](http://apimote.com) — ZigBee security research hardware for IEEE 802.15.4/ZigBee evaluation; Killerbee-compatible.
- Atmel RZUSBstick — Discontinued, but Killerbee-compatible hardware for IEEE 802.15.4, 6LoWPAN, and ZigBee development/debugging, if you can find one.
- [Freakduino](https://freaklabsstore.com/index.php?main_page=product_info&cPath=22&products_id=219&zenid=fpmu2kuuk4abjf6aurt3bjnfk4) — Low-cost, battery-powered Arduino board that doubles as an IEEE 802.15.4 sniffer.

### SDR Tools

- [RTL-SDR](https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/) — The cheapest entry point into SDR; receives 500 kHz–1.75 GHz.
- [HackRF One](https://greatscottgadgets.com/hackrf/) — Half-duplex SDR peripheral covering 1 MHz–6 GHz transmit/receive.
- [YardStick One](https://greatscottgadgets.com/yardstickone/) — Half-duplex sub-1 GHz transceiver.
- [LimeSDR](https://www.crowdsupply.com/lime-micro/limesdr) — Full-duplex SDR peripheral covering 100 kHz–3.8 GHz.
- [BladeRF 2.0](https://www.nuand.com/bladerf-2-0-micro/) — Full-duplex SDR peripheral covering 47 MHz–6 GHz.
- [USRP B Series](https://www.ettus.com/product-categories/usrp-bus-series/) — Full-duplex SDR peripheral covering 70 MHz–6 GHz.

### RFID / NFC Tools

- [Proxmark 3 RDV4](https://www.proxmark.com/) — General-purpose RFID research tool spanning LF (125 kHz) to HF (13.56 MHz).
- [ChameleonMini](http://chameleontiny.com/) — Programmable, portable platform for NFC security analysis.
- [HydraNFC](https://hydrabus.com/hydranfc-1-0-specifications/) — 13.56 MHz RFID/NFC platform supporting read/write/crack/sniff/emulate workflows.
- [Flipper Zero](https://flipperzero.one/) — Multi-tool for RFID, NFC, sub-GHz, infrared, and hardware debugging in a portable form factor.

## Standards & Guidelines

Reference material for understanding IoT security requirements and assessment methodology.

- [OWASP Internet of Things Top 10](https://owasp.org/www-project-internet-of-things/) — The most widely referenced classification of common IoT security risks.
- [OWASP IoT Security Testing Guide (ISTG)](https://github.com/OWASP/owasp-istg) — Methodology for structuring penetration tests across an IoT device's full attack surface.
- [ETSI EN 303 645](https://www.etsi.org/deliver/etsi_en/303600_303699/303645/02.01.01_60/en_303645v020101p.pdf) — European baseline standard for consumer IoT cybersecurity.
- [NIST IR 8259](https://csrc.nist.gov/pubs/ir/8259/final) — Foundational cybersecurity activities for IoT device manufacturers.
- [OWASP Embedded Application Security Project](https://owasp.org/www-project-embedded-application-security/) — Development best practices and a curated tool list.

## Books

- 2020, Fotios Chantzis, Evangel Deirme, Ioannis Stais, Paulino Calderon, Beau Woods — [Practical IoT Hacking](https://www.amazon.com/Fotios-Chantzis-ebook/dp/B085BVVSN6/)
- 2020, Jasper van Woudenberg, Colin O'Flynn — [The Hardware Hacking Handbook: Breaking Embedded Security with Hardware Attacks](https://nostarch.com/hardwarehacking)
- 2019, Yago Hansen — [The Hacker's Hardware Toolkit](https://github.com/yadox666/The-Hackers-Hardware-Toolkit/blob/master/TheHackersHardwareToolkit.pdf)
- 2019, Aditya Gupta — [The IoT Hacker's Handbook: A Practical Guide to Hacking the Internet of Things](https://www.apress.com/us/book/9781484242995)
- 2018, Mark (Swarup) Tehranipoor — [Hardware Security: A Hands-on Learning Approach](https://www.elsevier.com/books/hardware-security/bhunia/978-0-12-812477-2)
- 2018, Mark Carney — [Pentesting Hardware — A Practical Handbook (Draft)](https://github.com/unprovable/PentestHardware)
- 2018, Qing Yang, Lin Huang — [Inside Radio: An Attack and Defense Guide](https://link.springer.com/book/10.1007/978-981-10-8447-8)
- 2017, Aditya Gupta, Aaron Guzman — [IoT Penetration Testing Cookbook](https://www.packtpub.com/networking-and-servers/iot-penetration-testing-cookbook)
- 2017, Andrew Huang — [The Hardware Hacker: Adventures in Making and Breaking Hardware](https://nostarch.com/hardwarehackerpaperback)
- 2016, Craig Smith — [The Car Hacker's Handbook: A Guide for the Penetration Tester](https://nostarch.com/carhacking)
- 2015, Keng Tiong Ng — [The Art of PCB Reverse Engineering](https://visio-for-engineers.blogspot.com/p/order.html)
- 2015, Nitesh Dhanjani — [Abusing the Internet of Things: Blackouts, Freakouts, and Stakeouts](https://shop.oreilly.com/product/0636920033547.do)
- 2015, Joshua Wright, Johnny Cache — [Hacking Exposed Wireless](https://www.mhprofessional.com/9780071827638-usa-hacking-exposed-wireless-third-edition-group)
- 2014, Debdeep Mukhopadhyay — [Hardware Security: Design, Threats, and Safeguards](https://www.taylorfrancis.com/books/9780429066900)
- 2014, Jack Ganssle — [The Firmware Handbook (Embedded Technology)](https://www.elsevier.com/books/the-firmware-handbook/ganssle/978-0-7506-7606-9)
- 2013, Andrew Huang — [Hacking the Xbox](https://nostarch.com/xboxfree)

## Research Papers

- 2020, Oser et al. — [SAFER: Development and Evaluation of an IoT Device Risk Assessment Framework in a Multinational Organization](https://dl.acm.org/doi/abs/10.1145/3414173)
- 2019, Agarwal et al. — [Detecting IoT Devices and How They Put Large Heterogeneous Networks at Security Risk](https://www.mdpi.com/1424-8220/19/19/4107)
- 2019, Almakhdhub et al. — [BenchIoT: A Security Benchmark for the Internet of Things](https://nebelwelt.net/publications/files/19DSN.pdf)
- 2019, Alrawi et al. — [SoK: Security Evaluation of Home-Based IoT Deployments](https://alrawi.github.io/static/papers/alrawi_sok_sp19.pdf)
- 2019, Abbasi et al. — [Challenges in Designing Exploit Mitigations for Deeply Embedded Systems](https://ieeexplore.ieee.org/abstract/document/8806725)
- 2019, Song et al. — [PeriScope: An Effective Probing and Fuzzing Framework for the Hardware-OS Boundary](https://www.ndss-symposium.org/wp-content/uploads/2019/02/ndss2019_04A-1_Song_paper.pdf)
- 2018, Muench et al. — [What You Corrupt Is Not What You Crash: Challenges in Fuzzing Embedded Devices](http://www.eurecom.fr/en/publication/5417/download/sec-publi-5417.pdf)
- 2017, O'Meara et al. — [Embedded Device Vulnerability Analysis Case Study Using Trommel](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=509271)
- 2017, Jacob et al. — [How to Break Secure Boot on FPGA SoCs through Malicious Hardware](https://eprint.iacr.org/2017/625.pdf)
- 2017, Costin et al. — [Towards Automated Classification of Firmware Images and Identification of Embedded Devices](http://s3.eurecom.fr/docs/ifip17_costin.pdf)
- 2016, Kammerstetter et al. — [Embedded Security Testing with Peripheral Device Caching and Runtime Program State Approximation](https://www.thinkmind.org/download.php?articleid=securware_2016_2_10_30082)
- 2016, Chen et al. — [Towards Automated Dynamic Analysis for Linux-based Embedded Firmware](https://www.dcddcc.com/docs/2016_paper_firmadyne.pdf)
- 2016, Costin et al. — [Automated Dynamic Firmware Analysis at Scale: A Case Study on Embedded Web Interfaces](http://s3.eurecom.fr/docs/asiaccs16_costin.pdf)
- 2015, Shoshitaishvili et al. — [Firmalice: Automatic Detection of Authentication Bypass Vulnerabilities in Binary Firmware](https://www.ndss-symposium.org/wp-content/uploads/2017/09/11_1_2.pdf)
- 2015, Papp et al. — [Embedded Systems Security: Threats, Vulnerabilities, and Attack Taxonomy](http://www.cse.psu.edu/~pdm12/cse597g-f15/readings/cse597g-embedded_systems.pdf)
- 2014, Zaddach et al. — [Avatar: A Framework to Support Dynamic Security Analysis of Embedded Systems' Firmwares](http://www.eurecom.fr/en/publication/4158/download/rs-publi-4158.pdf)
- 2014, Alimi et al. — [Analysis of Embedded Applications by Evolutionary Fuzzing](http://ieeexplore.ieee.org/document/6903734/)
- 2014, Costin et al. — [A Large-Scale Analysis of the Security of Embedded Firmwares](http://www.s3.eurecom.fr/docs/usenixsec14_costin.pdf)
- 2013, Davidson et al. — [FIE on Firmware: Finding Vulnerabilities in Embedded Systems Using Symbolic Execution](https://www.usenix.org/system/files/conference/usenixsecurity13/sec13-paper_davidson.pdf)

## Case Studies

- [Binary Hardening in IoT Products](https://cyber-itl.org/2019/08/26/iot-data-writeup.html)
- [Cracking Linksys "Encryption"](http://www.devttys0.com/2014/02/cracking-linksys-crypto/)
- [Deadly Sins Of Development](https://youtu.be/nXyglaY9N9w) — Conference talk on real-world implementation failures. 🎥
- [Dumping Firmware from a Device's SPI Flash with a Bus Pirate](https://www.iotpentest.com/2019/06/dumping-firmware-from-device-using.html)
- [Hacking the DSP-W215, Again](http://www.devttys0.com/2014/05/hacking-the-dspw215-again/)
- [Hacking the PS4](https://cturt.github.io/ps4.html) — Introduction to the PS4's security architecture.
- [IoT Security @ CERN](https://doi.org/10.5281/zenodo.1035034)
- [Multiple Vulnerabilities Found in the D-Link DWR-932B](https://pierrekim.github.io/blog/2016-09-28-dlink-dwr-932b-lte-routers-vulnerabilities.html)
- [Pwning the D-Link 850L Routers and Abusing the MyDlink Cloud Protocol](https://pierrekim.github.io/blog/2017-09-08-dlink-850l-mydlink-cloud-0days-vulnerabilities.html)
- [PWN Xerox Printers (...Again)](https://www.fkie.fraunhofer.de/content/dam/fkie/de/documents/xerox_phaser_6700_white_paper.pdf)
- [Reversing Firmware With Radare](https://www.bored-nerds.com/reversing/radare/automotive/2019/07/07/reversing-firmware-with-radare.html)
- [Reversing the Huawei HG533](http://jcjc-dev.com/2016/04/08/reversing-huawei-router-1-find-uart/)

## Free Training & CTFs

- [CSAW Embedded Security Challenge 2019](https://github.com/TrustworthyComputing/csaw_esc_2019) — CSAW 2019 Embedded Security Challenge (ESC).
- [Embedded Security CTF (Microcorruption)](https://microcorruption.com) — Browser-based embedded exploitation CTF.
- [Hardware Hacking 101](https://github.com/rdomanski/hardware_hacking/tree/master/my_talks/Hardware_Hacking_101) — Workshop materials from BSides Munich 2019.
- [IoTGoat](https://github.com/scriptingxss/IoTGoat) — Deliberately insecure OpenWrt-based firmware for practicing OWASP IoT Top 10 vulnerabilities.
- [Damn Vulnerable IoT Device (DVID)](https://github.com/Vulcainreo/DVID) — Purpose-built vulnerable IoT device firmware for hands-on practice.
- [Damn Vulnerable ARM Router (DVAR)](https://blog.attify.com/2017/07/07/damn-vulnerable-arm-router-dvar/) — Vulnerable ARM-based router firmware for practicing binary and firmware exploitation.
- [ARM-X Firmware Emulation Framework](https://github.com/therealsaumil/armx) — Emulation framework and challenge set for ARM-based embedded firmware.
- [Rhme-2015](https://github.com/Riscure/RHme-2015) — First Riscure Hack Me hardware CTF challenge.
- [Rhme-2016](https://github.com/Riscure/Rhme-2016) — Riscure Hack Me 2, a low-level hardware CTF challenge.
- [Rhme-2017/2018](https://github.com/Riscure/Rhme-2017) — Riscure Hack Me 3 embedded hardware CTF.

## Websites

- [Hacking Printers Wiki](http://hacking-printers.net/wiki/index.php/Main_Page) — Comprehensive resource on printer security.
- [OWASP Embedded Application Security Project](https://owasp.org/www-project-embedded-application-security/) — Development best practices and a tool list.
- [OWASP Internet of Things Project](https://owasp.org/www-project-internet-of-things/) — IoT common vulnerabilities and attack surfaces.
- [Router Passwords](https://192-168-1-1ip.mobi/default-router-passwords-list/) — Default credential database sorted by manufacturer.
- [Siliconpr0n](https://siliconpr0n.org/) — Wiki/archive dedicated to IC reverse engineering.

### Blogs

- [RTL-SDR](https://www.rtl-sdr.com/)
- [/dev/ttyS0's Embedded Device Hacking](http://www.devttys0.com/blog/)
- [Exploiteers](https://www.exploitee.rs/)
- [Hackaday](https://hackaday.com)
- [jcjc's Hack The World](https://jcjc-dev.com/)
- [Quarkslab](https://blog.quarkslab.com/)
- [wrong baud](https://wrongbaud.github.io/)
- [Firmware Security](https://firmwaresecurity.com/)
- [PenTestPartners — IoT](https://www.pentestpartners.com/internet-of-things/)
- [Attify](https://blog.attify.com/)
- [Payatu](https://payatu.com/blog)
- [GracefulSecurity — Hardware](https://gracefulsecurity.com/category/hardware/)
- [Black Hills InfoSec — Hardware Hacking](https://www.blackhillsinfosec.com/tag/hardware-hacking/)

### Tutorials and Technical Background

- [Azeria Labs](https://azeria-labs.com/) — In-depth ARM reverse engineering and exploitation tutorials.
- [JTAG Explained](https://blog.senr.io/blog/jtag-explained#) — Walkthrough covering UART/JTAG discovery and protected shell bypass.
- [Reverse Engineering Serial Ports](http://www.devttys0.com/2012/11/reverse-engineering-serial-ports/) — Detailed guide to spotting debug pads on a PCB.
- [UART Explained](https://www.mikroe.com/blog/uart-serial-communication) — In-depth explanation of the UART protocol.

### YouTube Channels

## Conferences & Communities

Conferences and community spaces with a strong embedded/IoT security focus.

- [Hardwear.io](https://hardwear.io/) — EU (The Hague, September) and USA (Santa Clara, June) editions dedicated to hardware and embedded security.
- **DEF CON** — Several long-running villages focus on this space: [IoT Village](https://www.iotvillage.org/), [Hardware Hacking Village (DC HHV)](https://dchhv.org/), [ICS Village](https://www.icsvillage.com/), and [Car Hacking Village](https://www.carhackingvillage.com/).
- [Chaos Communication Congress (CCC)](https://www.ccc.de/) — Annual conference with a consistent track record of embedded/hardware security talks.
- [REcon](https://recon.cx/) — Reverse engineering conference with frequent embedded and firmware content.
- Regional [BSides](http://www.securitybsides.com/) events — Many chapters run dedicated hardware hacking villages or talk tracks.

## Contributing

Suggestions are welcome. Please open an issue or pull request with a short description of the resource and why it belongs in this list; broken links and outdated tools are removed on discovery.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, Fraunhofer FKIE has waived all copyright and related or neighboring rights to this work.


---

**embedded-and-iot-security** — Represented By [Humayun Shariar Himu](https://github.com/HumayunShariarHimu)

*A Passionated Psychologist & Tech Lover*

### Connect

- [GitHub](https://github.com/HumayunShariarHimu)
- [YouTube](https://youtube.com/@HumayunShariarHimu)
- [Facebook](https://www.facebook.com/humayunshariarhimu)
- [CodePen](https://codepen.io/HumayunShariarHimu)
- [Google Bug Hunters](https://bughunters.google.com/profile/b97693e9-aa31-4451-9c65-f7548e85bfc9)
