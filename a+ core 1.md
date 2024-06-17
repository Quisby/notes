# A+ Core 1

## Udemy Total Seminars Course

**Cool Tools**
- CPU-Z

**Super Sites**
- PC Part Picker

**PC repair toolkits:**
- Hemostat
- IC inserter - plugs in integrated circuits

**Mobile repair kits:**
- iFixit has specialized nut drivers for mobile devices
- Spudgers
- Voltage testers
- Volt/ohm meter (multimeter)

Troubleshooting steps:
1. Identify problem
2. Establish a theory
3. Test the theory
4. Establish plan of action and implement solution
5. Verify functionality
6. Document

**Confusing acronyms:**
- SMTP: Simple Mail Transfer Protocol
- SNMP: Simple Network Management Protocol
- SNTP: Simple Network Time Protocol

Mini-DIN = PS/2 port

**I/O shield** - metal plate that encompasses ports on rear of system unit

S-Video



### CPUs
Registers: temporary byte storage for a CPU to do manipulations on (modern CPUs may have hundreds of registers that are 128 bits long)

Clock tells CPU to zero out and prepare for next command

CPU pipeline: Prefetch decides which specialized logic unit to send a command to 

2 measures of modern CPU:
1. Clock speed
2. Cores

APU: Accelerated Processing Unit (combines CPU and GPU)

CPU-Z is a great information tool on a computer's CPU

x86 (32bit) (called "x86" because it is based on the Intel 8086 processor)
x64 (64bit)

n.b. x86-64 refers to x64 that is backwards compatible with 32-bit applications
IA-32: Intel architecture 32-bit

**CPU name suffix meanings:**
- K in intel CPU names indicates that it is unlocked (so overclocking is possible)
- F in Intel CPU names indicates that there is no integrated graphics
- X in AMD CPU name indicates that it is overclocked out of the box
- G in AMD CPU name indicates integrated graphics (since AMD CPUs have none by default)

In the name "Intel Core i9 12900K": Intel is the brand, Core i9 is the tier, 12 is the generation, 900 is the model, and K is the suffix.

### RAM

SDRAM is only RAM stick with two pins (1 bit per 1 clock)
DDR (1 bits per 1 clock) 160 pin
DDR2 uses 240 pin
DDR3 uses 240 pin
DDR4 uses 288 pin

PC Rating = DDR Rating in bits
PC2 Rating = DDR2 Rating in bits
PC3 Rating = DDR3 Rating in bits

DDR Speed Rating is measured in bytes, PC Speed Rating is measured in bits (so just divide or multiply by 8 to convert)

Occasionally motherboards won't support double-sided RAM

RAM Channels: Most modern motherboards are dual-channel, meaning that you must use more than one RAM stick at a time, and those RAM sticks must match

Only installing a single RAM stick will give you a "single channel mode" error

Parity vs. error correction code (ECC): adding extra "parity" or ECC chip

Serial Presence Detect (SPD) chip: gives system a place to query RAM stick for specifications

Virtual memory prevents out of memory errors

`dir /ah` shows all hidden files (it can show you the size of the swap file)



### Motherboards and chipsets

Many motherboards today use a backup BIOS in case of failure

3 components of BIOS:
1. Communicates with mass storage devices
2. POST
3. MOS (System Setup)

POST runs as soon as CPU starts, all device controllers self-diagnose. All okay indicated by "POST beep"

Beep codes indicate errors in POST process

POST card indicates error with two digital hexadecimal codes, and can enable testing of "dead" computers

POST codes are only valid before OS boots


UEFI System Setup allows
1. Setting up both Administrator and User boot passwords
2. Changing USB permissions (preventing people from inserting USB sticks)

PROM (Programmable ROM) were the original chips used for BIOS

Single flash ROM chips are used now

RTC: Real-time clock

**Motherboard form factors:**
- ATX: biggest common form factor (12"x9.6")
- MixroATX: 9.6"x9.6"
- Mini-ITX: smallest common form factor
- ITX: larger version of Mini-ITX

Chipsets: dedicated chips that manage all the different peripherals and devices managed by singular chips on earliest PC motherboards
- Northbridge: traditionally fastest connections, including CPU
- Southbridge: slower components, like USB

Today, CPUs control Northbridge function
Southbridge are the actual chipsets on motherboards (they define compatibility with devices and RAM amounts)

ESD strap keeps you from damaging motherboard

Standoffs provide clearance to keep motherboard from contacting case and shorting out

Capacitor swelling: means motherboard is unusable and you should disconnect power

Burning smell: may indicate capacitor swelling

### Power Supply

Slider on back of older power supplies can switch voltage from European to American standards and back (newer power supplies are auto-sensing)

**Power supplies**: step-down transformers that convert AC to DC

"80 Plus" rating system is extremely important for determining efficiency of producing wattage rating

Original ATX power supplies had 20-pin connector 

Modern ATX power supplies generally have 24-pin connectors (ATX12V)

Types of power supplied by power supplies:
- 12 volt (yellow)
- 5 volt (red)
- 3.3 volt (orange)

ATX12V - extension of original ATX power standard that allows for more power

**Types of power connectors:**
- ATX12V looks like extra 4-pin connectors
- Molex - oldest power connector on computers
- Mini connector - originally used for floppy drives
- SATA power connector - generally for SATA drives
- PCIe connector - used for higher end video cards

Modular power supplies - have female ports for power connectors to reduce unnecessary cables (vs. soldered power supplies)

Volts x amps = watts

Power supply testers can be inserted between CPU and power supply


### Mass storage devices

LBA - logical block addressing

**Form factors:**
5.25" - used for optical media
3.5" - primary mass storage form factor for decades
2.5" - another mass storage form originally used in laptops
1.8" - less popular because it was taken over by SSDs
M.2 - dominant form factor for solid state devices

SSDs memory cells are "pages"
HDDs memory cells are "sectors" (~4096 bytes)

Issues with counting in binary values:
1. Decimal values
2. Binary IEC  Values
	- 2^10 = 1024 (called a "kibi")
	- 2^20 = 1,048,576 Mebi
	- 2^30 = 1,073,741,824 Gibi
	- 2^40 = Tebi
	- 2^50 = Pebi
	- 2^60 = Exbi

ATA - language spoken by historical and contemporary HDDS
PATA (or IDE) - original version of PATA
SATA - more modern version of ATA
eSATA - version of SATA created for external drives

HDD speeds include
5400 RPM
7200 RPM
10000 RPM
15000 RPM

SSDs may come in SATA connections

m.2 SSD drives use NVMe connections (much faster than SATA)

SCSI uses a parallel interface, but different from PATA. Competing language with ATA.

2 modern SCSI standards:
- Serial Attached SCSI (SAS) - uses SATA connector with SCSI command language
- iSCSI - SCSI connected via ethernet

RAID levels:
- RAID 0: striping
	- Minimum of 2 drives
	- Provides faster speed but no redundancy
- RAID 1: mirroring
	- Provides redundancy but slows
- RAID 5: striping with parity
	- Minimum of three drives
	- Can lose only one drive max
- RAID 6:
	- Minimum of four drives
	- Can lose maximum of two drives
- RAID 10: striping mirrors
	- Requires four drives
	- Runs two mirrored pairs
- RAID 0+1: mirror stripes
	- Can lose one 
- Proprietary RAID

Two types of RAID control:
1. Software RAID is controlled by the OS and CPU
2. Hardware RAID is controlled by expansion cards or motherboards

Hot spare/swappable options allows you to replace a disk in a RAID array

Windows Storage Spaces is a software RAID controller that allows you to create "pools." You can create different RAID types as well as create a "theoretical" max volume size, which is ready to expand with new drives.


2 ways to encrypt data on Windows:
1. File level with EFS (built into NTFS)
2. Disk level with BitLocker (Mac OS equivalent is FileVault)

Trusted Platform Module (TPM) - key attached to laptop motherboard which is necessary for HDD decryption. Necessary for BitLocker.

BitLocker To Go works on removable media and doesn't require TPM


Mass storage issues:
RAID not found/RAID stopped working
- Is RAID controller active?

Read/write failure
- S.M.A.R.T. technology provides self-diagnostic information on HD

Slow performance
- Usually a RAM issue

Great click of death
- Mechanical failure. Must replace the hard drive

Failure to boot

Drive not recognized
- Usually a formatting issue, might require reformatting

OS not found
- Almost always a boot order issue

Attempts to boot incorrect device
- Boot order issue

Continuous rebooting
- Corrupt OS

### USB

Memorize this table:

| Standard | Max speed|
| - | - |
|USB 1.0 | 1.5 Mbps
|USB 1.1 | 12 Mbps
|USB 2.0 | 480 Mbps
|USB 3.0 | 5 Gbps
|USB 3.1 Gen 1 | 5 Gbps
|USB 3.1 Gen 2 | 10 Gbps

USB-A connectors:
- USB 1.1 = white
- USB 2.0 = black
- USB 3.0 = blue
- USB 3.1 gen 1 = blue
- red, orange, yellow = charging port

Other types of USB connectors:
- USB-B
- USB mini-B
- USB micro-B
- USB 3.0 micro-B
- USB Type-C

A connectors: downstream
B connectors: upstream

USB-C automatically configures up and downstream

Thunderbolt 1 = 10 Gbps
Thunderbolt 2 = 20 Gbps
Thunderbolt 3 uses USB-C up to 40 Gbps

Lightning - proprietary for Apple world

Smart card reader
Magnetic scanner
Flash memory reader

### Display technologies

LCD backlight types:
1. Earlier: Cold cathode flourescent lamp (CCFL)
2. More recent: LEDs

Imaging is LCD
Backlighting is CCFL or LED

CCFL LCDs require an inverter to invert DC to AC

Different types of LCD technologies:
- TN (inexpensive)
- IPS (wide range of views)

Alternative display technologies:
1. OLED: produce own light
2. DLP: grid of tiny mirrors, used in projectors

Video connectors:
1. VGA - 15 pins on 3 rows (almost always blue) - analog signal only
2. DVI - first popular digital connector
	1. DVI-I - digital or analog (have a cross on connector)
	2. DVI-D - digital only (only has a dash on connector)
	3. Single link DVI
	4. Dual link DVI - to handle large resolution monitors
3. HDMI - includes audio output
4. Mini-HDMI
5. DisplayPort - dedicated video connector
	1. Mini DisplayPort

Monitor aspect ratios:
4:3
VGA: 640x480
SVGA: 800x600
SXGA: 1280x1024
UXGA: 1600x1200

16:10 (golden ratio)
WSXGA: 1440x900
WUXGA: 1920x1200

720p ("progressive scan")
1280x720
1366x768
2560x1440 QHD or WQHD

1080p
1920x1080
4K: 3840x2160 (classic 4K)

Two dominant projector technologies:
1. DLP
2. LED

2 main criteria for projectors:
1. Brightness
2. Throw: distance to optimal image projection

Geometric shapes present when adjusting projector
1. Pincushion
2. Keystone
3. Skew

Projector troubleshooting:
1. Intermittent projector shutdown: usually caused by overheating
2. Burned out bulb

Monitor troubleshooting:
1. Incorrect data source
2. Cabling issues
3. Dead pixel
4. Incorrect color or brightness mis-setting
5. Flashing screen: usually cabling issue

### Networking

LAN

Frame: 1500-byte chunks used in ethernet networking

Consists of sender/receiver addresses + FCS (frame check sequence)

MAC address: 48-bit (12 hexadecimal characters) identifies devices on LAN
- First six characters: OEM ID
- To determine, use `ipconfig` on Windows or `ifconfig` on Mac/Linux

Hub: repeats all communications, all nodes share same bandwidth
Switch: collects Mac addresses by observing packets and routes data to receiver

There are 16 possible combinations of any 4 binary characters, hence the convenience of hexadecimal

Every hexadecimal value equals four bits

WAN: LANs interconnected via routers that use IP addressing to overcome limitations of LAN MAC addressing

Routers: differentiate LANs as well as devices
- Use logical addresses
- Use DHCP

Ethernet defines 1) frame and 2) cabling

Article on [types of ethernet cable](https://www.geeksforgeeks.org/types-of-ethernet-cable/#) at GeeksforGeeks
- 10BaseT
- 10GBaseT

RG ratings (e.g. RG-59, RG-58, RG-6) apply to coaxial cabling
F-type connectors used with coaxial cabling
RG-58 used BNC connector

Twisted pair (e.g. UTP) is most common networking cable now - has a rough maximum distance of 100m

UTP ethernet cables have four pairs of wires

RJ-11 connector used with telephone wire
RJ-45 - eight contacts
STP - shielded twisted pair uses RJ-45, provides more protection from interference

Two types of fiber optic cable 
- Multimode uses LEDs
- Singlemode uses lasers

Fiber optic connectors usually come in send/receive pairs

TP Cat ratings
- Cat 5 - 100 Mbps
- Cat 5e - 1 Gbps
- Cat 6 - 1 Gbps 100 m, or 10 Gbps 55 m
- Cat 6a - 10 gbps at 100 m

Plenum rating (ability to resist fire)
- PVC
- Riser-rated cable
- Plenum-rated cable

Direct-burial cabling - have greater protection for environment

Two standards for connecting twisted pair wires to crimps:
1. TIA 568A
2. TIA 568B

Crossover cables are wired differently on each end. 

Structured cabling: cabling run systematically through the walls

MDF: Main distribution frame - equipment closet

Patch panel: used for cable management

Loopback cable/plug can test functionality of port

Speed and duplex: 

Full-duplex: talking and listening at the same time
Half-duplex: throttles

Wake-on-LAN: "magic packet" - wakes computers on network

Link lights tell you three things:
1. Connected
2. Speed
3. Activity

"Fox and hound" or tone probe and generator, identify specific cables within a bundle

Solid-core cable is used in walls and horizontal runs because it is good for long runs and is not exposed to frequent bending.

Classic IPv4 address classes (max of 4 billion addresses):
- Class C: block of addresses where first three numbers locked (210.11.12.x) - 254 hosts
- Class B: block of addresses where first two numbers locked (172.16.x.x) - 65,534 hosts
- Class A: block of addresses where first number is locked (6.x.x.x) - millions of hosts

Subnet mask: e.g. 255.255.255.0 (distinguishes local connections from connections via default gateway)

Subnet masks only used with IPv4 addresses

Default gateway: x.x.x.1

DHCP provides dynamic IP addressing

APIPA - fallback in case you can't find DHCP

`ipconfig /release` - disconnects device from DHCP server
`ipconfig /renew` - forces new device connection to DHCP server

IPv4: 4 billion addresses
IPv6: 128-bit, 8 groups with 7 colons

IPv6 shorthand
1. Eliminate leading 0s
2. Merge groups of 0s and write as double colon ::

Always have two addresses in IPv6:
1. Link-local address: `fe80:0000`
2. Global unicast (internet) address: determined by

IPv6 use prefixes instead of subnet masks

Port numbers range from 0 - 65535
Port numbers help direct traffic on the application level

3 types of ports:
1. "Well-known ports": 0-1023
2. "Registered ports": 1024 - 49151
3. "Dynamic/ephemeral ports" 49152 - 65535

Common port numbers you need to know (all these are in Anki 2023-10-10):

| Port | Protocol |
| - | - |
| 20/21 | FTP
| 22 | SSH
| 23 | Telnet
| 25 | SMTP
| 53 | DNS
| 67/68 | DHCP
| 80 | HTTP
| 110 | POP3
| 137/139 | NetBIOS
| 143 | IMAP
| 161/162 | SNMP
| 389 | LDAP
| 443 | HTTPS
| 445 | SMB/CIFS
| 3389 | RDP

Protocol: set of rules that allow for compatibility

TCP/IP
TCP: connection-based protocol (i.e. handshakes)
UDP: User Datagram Protocol: connectionless protocol
ICMP: Internet Control Message Protocol: single-packet only (e.g. `ping` packet)

PDU: Protocol data unit

IP Packet: subsection of ethernet frame

TCP segment (a.k.a. UDP datagram)

**DNS**

DNS determines IP address affiliated with FQDN (Fully Qualified Domain Name)

FQDNS have a 256-character limit

DNS replaced historical hosts file

Root servers > first level domains (.com, .edu, etc) > Second level domains (e.g. totalsem.com)

DMARC: Domain-based Message Authentication, Reporting, and Conformance: verifies and prevents spoofing of sender domain

SPF: email authentication protocol that can be used to prevent spammers and attackers from sending messages that appear to come from a trusted domain

DMARC uses DKIM (DomainKeys Identified Mail), which allows sender to sign message

DNS is provided by DHCP

`ipconfig /all` 

To verify if DNS is working or not:
1. Manually configure DNS server
	1. 8.8.8.8 or 8.8.4.4: Google's DNS servers
	2. Indicates that a local DNS might not be working
2. Use `nslookup` to see if it is functioning
	1. Stores AAAA records and MX records


**Routers**

Console port is a serial connection to configure routers
DB-9 connector

SOHO router configurations:
- DHCP
	1. range/scope - configure range of addresses in LAN
	2. Lease time - length of time device given address
	3. Default username and password
	4. DHCP reservations - reserve addresses for statically addressed device

VLAN: takes one physical switch and divides it into separate virtual LANs (i.e. to segregate VoIP)

If devices can't communicate over a switch, they may be separated by VLANs

"Port security" locks a port down to a specific MAC address

Managed vs unmanaged switches: Managed switches are VLAN capable

SDN (Software Defined Networking): separates control from data-sharing components of network and minimizes human error

Wired network troubleshooting:
1. No connectivity
	1. Patch panel
	2. IP addressing (i.e. IP conflicts with static IP addresses)
2. Limited connectivity:
	1. DHCP or APIPA server issues
	2. Rogue DHCP server
3. Intermittent connectivity:
	1. Interference
	2. Unavailable resources:
4. Slow transfer speeds
	1. Rare in wired networks, but check task manager for bandwidth-heavy processes
	2. QoS can resolve many of these issues

### Wireless networking

IEEE 802.11 standard - primary wireless connection

Wireless Access Point (WAP) - bridge between wireless 802.11 and ethernet network

2 wireless network modes:
1. Infrastructure (the much more common default mode, uses WAP)
2. Ad hoc - wireless network that connects individual devices to each other, treats specific computer as if it were a WAP

2 requirements for "infrastructure" mode:
1. NIC on individual devices
2. WAP


3 basic types of antennas:
1. Omnidirectional
2. Dipole - large flat circular signal (ideal for a single-floor office)
3. Patch - propagates half of a sphere
4. Directional (e.g. Yagi or parabolic) - stretched football propagation pattern

Laptop antennas typically run around monitor

2.4 GHz band: 2.412 - 2.4884 GHz
1. 14 premade channels in Japan
2. 11 only in U.S.

5.0 GHz band
1. Has many more channels than 2.4 GHz

**Table: 802.11 Extension Standards**

| Extension | Speed | Frequency | Note |
|- | - | - | - |
| 802.11a | 54Mbps |5GHz 
| 802.11b | 11Mbps | 2.4GHz
| 802.11g | 54Mbps | 2.4 GHz | Only backwards compatible with b
| 802.11n | 150Mbps | 2.4 or 5GHz | a.k.a. WiFI-4, MIMO, backwards compatible with a,b, and g
| 802.11ac |  | 5GHz | a.k.a. Wi-Fi 5, MU-MIMO (usually has additional 2.4GHz antenna for backwards compatibility)
| 802.11ax |  | 6GHz | |


WMN: Wireless Mesh Network
- Base station connected to actual modem network
- External base stations can be placed around home to get good wireless signal anywhere
- These are analogous to low powered enterprise mesh networks

Enterprise wireless
- PoE: power over ethernet
	- "PoE" is first generation
	- "PoE+" provides  more electricity
	- Requires PoE compatible switch
	- PoE injector can be used to provide PoE capability to switch
- AAA: Authorization, Authentication, and Accounting
	- RADIUS or TACACS+ 
- ESSID: two or more WAPs sharing the same SSID
- Captive Portal
- Special enterprise wireless WLAN switches: propagates one ESSID and captive portal to all WAPs

Different wireless technologies:
1. RFID
	1. Used for NFC is consumer electronics
	2. Requires reader to activate radio with frequency power
	3. NFC is RFID
		1. Tap-to-pay
		2. Tap-to-print
2. Bluetooth
	- Designed to only connect two devices at the same time (PAN network)

**Table: 3 classes of Bluetooth**

| Class | Power | Range |
| - | - | - |
| 1 | 100 mW | 100 m |
| 2 | 2.5 mW | 10 m |
| 3 | 1 mW | 1 m |

**Troubleshooting Wireless Connections:**
1. Use Wi-Fi analyzer!
2. No connectivity
	1. Changed authentication
	2. Low signal
		1. Get closer
		2. Adjust antennas
	3. Disabled SSID broadcast
		1. Have to manually connect with precise information
3. Limited connection
	1. External interference
		1. Change location
4. Intermittent connectivity


LANs connected by routers constitute WAN
MAN: Metropolitan Area Network
PAN: Personal Area Network, Bluetooth only

Internet Tiers:
Tier 1 internet providers create peering agreements
- NOCs (Network Operation Centers) - third party-operated connections between Tier 1 internet providers

Tier 2 providers pay tier 1 providers for access

Tier 3 are main ISPs for individuals and corporations

Broadband
- DSL (Digital Subscriber Line) - piggybacked on phone line, first broadband option
	- ADSL - Asymmetric DSL (slower up than down)
	- SDSL - Symmetric (same up and down)
	- PPPoE can be helpful for DSL
- Cable
	- Uses DOCSIS protocol (which enables internet and TV at the same time)
- Satellite
- 802.11 - High-powerful antenna version of 802.11 for longer distances

WISPS: Wireless Internet Service Providers

Public-facing servers use "stateful firewalls" that watch for pings, etc. but don't actually block incoming port 80/443 connections

SOHO routers don't need to worry about open incoming port 80/443 connections because they're not servers


Email protocols
- SMTP (port 25) - sends emails up to server
- POP3 (port 110) - brings email down permanently
- IMAP4 (port 143) - stores everything on server

An outgoing mail server with always be SMTP
An incoming mail server can be either POP3 or IMAP

Proxy servers
1. Can act as firewalls/filters
2. Proxy settings are application specific
3. Can act as a cache

Different VPN protocols
- PPTP
- L2TP
- IPsec

Troubleshooting internet issues:
1. `tracert` (windows) or `traceroute` on Linux/Mac - run when system is up to see what connection should look like
2. `ping`
3. `ipconfig`



Virtualization
- Type 1 hypervisor - directly on hardware
- Type 2 hypervisor - runs on OS


Benefits of cloud computing
- Rapid elasticity - quality of Cloud computing, which allows for quick increases in capacity
- On-demand - scaling out virtual machines to meet seasonal fluctuations
- More efficient because of resource pooling
- IaaS (Infrastructure as a Service)
- PaaS (Platform as a Service) - e.g. Heroku, sets up IaaS as well as platforms needed to run applications as they are developed
- SaaS - e.g. Google Docs, applications as website



### Mobile Devices
CDMA - don't come with SIM cards
- Require lots of firmware updates
	- Baseband
	- Broadband
- PRL (Preferred Roaming List)
- PRI (Product Release Information) 
GSM - come with SIM cards

IMSI - International Mobile Subscriber Identity

S/MIME - 

3 ways A+ talks about synchronization
1. Desktop synchronization
2. Automobile synchronization
3. Cloud synchronization

Mobile device troubleshooting
1. Power drain or significant signal drop indicates malware
2. Unintended connections also suggest hacking
3. Non-responsive touchscreen may just indicate overloaded system


### Printers

Laser printer
- Toner cartridge
- Photosensitive imaging drum
- Processing
	- Print jobs stored in memory
	- Primary corona charging
- Exposing
- Developing
	- Voltage difference sucks toner onto photosensitive drum
- Imaging
- Pick up roller
- Separation pads
- Transfer corona
- Fuser assembly melts toner and seals it to paper

7 steps needed for exam:
1. Processing
2. Charging
3. Exposing
4. Developing
5. Transferring
6. Fusing
7. Cleaning (rubber scraper removes excess toner)

Color laser printers use a belt to apply multiple colors (CMYK)

Color laser printers require calibration of belts


Inkjet printer
- Print head stores all color jets
- Roller moves print head across page
- Tend to be safer because they don't involve high voltages
- Maintenance they may require
	- Cleaning nozzles
	- Calibration (for color printers)
	- Replacing cartridges
	- Clear jams

Impact printers (Dot matrix) printers
- Predate PCs
- Main components
	- Print head
	- Ink ribbon
	- Platen
- Use tractor feed paper
- Popular in industrial environments or for multipart forms

Thermal printers
- Two components
	- Feed assembly
	- Heating element

Local printer setup
- Printer
- Spooler - software that queues print jobs from connected computers (called "print queues" in Windows Device Manager)

Collation prints off multiple copies in page order

Changes to printer spooler requires administrator privileges

Zero conf (Windows) / Bonjour (Mac OS) AirPrint - handle printer installation and configuration

Troubleshooting printers:
- Unable to install printer
	- Rights issue (permissions)
- No connectivity
	- Often sign of generic network issue
	- DHCP issue? Physical connection issue?
	- Rollback device drivers
- Access denied
	- Permissions issue with shared printers or spooler
- No image on printer display
	- Possible sleep mode
	- Possible lockout from administrator
- Paper trouble
	- Issues with either:
		- Pick up rollers
		- Separation pads
	- Humidity and storage may cause issues
	- Maintenance kits can help
- Low memory errors (laser printers)
	- Try to reduce resolution
	- Install extra RAM
	- Error codes 
- Garbled characters on paper
	- Bad or corrupted drivers
	- Reset printer or rollback drivers
- Vertical lines on page (laser printers!)
	- Foreign matter on optically sensitive roller
		- Toss toner cartridge
- Color prints in wrong print color
	- Driver issue or dead cartridge
- Blank pages
- Streaks on printed pages (inkjet issue)
	- Dirty inkjets with ink around jet streaking paper
- Faded prints
	- Lower cartridges, ribbon running out, clogged jets
- Ghost images (laser)
	- Rubber cleaning scraper
- Toner not fusing to paper
	- Replace fuser, issue with fuser assembly
- Creased paper
	- Pick up rollers are at variance, causing tugging on paper at angles
	- Can be fixed with maintenance kits

## Complete Study Guide (Docter)

> [!Assessment Test for 220-1101]-
> 1. C
> 2. A
> 3. A, B
> 4. A
> 5. C
> 6. C, D
> 7. A
> 8. D
> 9. C, D
> 10. D
> 11. B (C)
> 12. A
> 13. B (C)
> 14. B (C)
> 15. A
> 16. C, D (A, B)
> 17. A
> 18. C (D)
> 19. SSH, HTTPS
> 20. B
> 21. B
> 22. C, A
> 23. C
> 24. A
> 25. D
> 26. A
> 27. B
> 28. D
> 29. D (C)
> 30. D
> 31. C (D)
> 32. C (B)
> 33. C
> 34. D (C)
> 35. D (B)
> 36. A, C 


### Chapter 1: Motherboards, Processors, and Memory

Motherboard form factors:

ATX (Standard- of Micro-)
ITX Family: Mini-ITX, Nano-ITX, Pico-ITX

Internal CPU bus speed is derived from FSB clock

Northbridge FSB: signal pathways between CPU and main memory
Northbridge BSB: signal pathways between CPU and external cache memory

PCI (original, not PCIe) expansion buses operate at either 33 MHz or 66 MHz.
PCI (original not PCIe) expansion buses also come in either 3.3V or 5V versions

PCIe uses serial connections over 

"Up-plugging": using a small PCIe expansion card in a longer slot

Each separate processor core generally has its own L1 and L2 caches, while L3 caches are shared between cores.

**Header** - a series of pins that connect the buttons and lights for a desktop case

BIOS/UEFI used in conjunction with TPM (a dedicated security coprocessor) confirms that hardware being booted is tied to the same system ("sealing").

When a device doesn't have an inbuilt TPM, a user can use an external HSM (e.g. a USB or PCIe peripheral) to store encryption keys

CMOS - memory chip that stores core settings for a PC

#### Processors
2 major categories of CPU instruction set architecture (ISA):
1. Complex Instruction Set Computing (CISC)
2. Reduced Instruction Set Computer (RISC)

**Superscalar processors** "can have multiple instructions operating on separate data in parallel" (45)

**Multithreading** - running multiple virtual cores (threads) on each hardware CPU core. So a 2-core processor will run four threads (i.e. virtual cores).

**Hyper-Threading Technology (HTT)** - Intel's marketing version of simultaneous multithreading. OS treats as separate processors


#### Memory

Important terms:
1. Parity checking
2. Error-correction code (ECC)
3. Single- and double-sided memory
4. Single-, dual-, triple- and quad-channel memory

**Parity checking**: rudimentary error-detection with no correction. Comes in *odd, even, mark,* or *space* forms.
- Adds a ninth "check" or parity bit to a byte

**Error Checking and Correction**: can detect single- and double-bit errors in a byte, and correct single-bit errors.

**Single- and doubled-sided memory**: memory sticks with modules on just one or both sides.

**Multi-channel memory**: try to alleviate bottleneck between CPU and memory

DDR5 pins: 288
DDR4 pins: 288
DDR3 pins: 240
DDR2 pins: 240
DDR pins: 184


### Chapter 2: Expansion, Storage, and Power
#### Storage

3 components of hard disk drive system:
1. Controller
2. Hard Disk
3. Host Bus Adapter (HBA) - converts controller signals into computer 

Hard drive components include:
- Platters
- Read/write heads
- Tracks
- Sectors
- Cylinders
- Clusters (allocation units)

**Tracks** - concentric, magnetic rings drawn around drives which help divide up sectors
**Sectors** - magnetic domains the represent smallest units of storage on disk (typically 512 bytes)

Actual physical sector geometry is much denser than the geometry the controller reports to the BIOS, owing to limitations of the latter

7200 rpm SATA drive can sustain ~100 MBps
10,000 rpm SATA drive can sustain ~200 MBps
15,000 rpm drives are primarily enterprise SAS drives 


SSHD (Solid-state hybrid drive) - conventional HDD with flash-memory onboard acting as enormous cache

**3 SSD communication interfaces:**

1. SATA
2. PCIe (faster)
3. NVMe (fastest)

SATA is the cheapest but poorest performing SSD connector

Some motherboards may not support booting from NVMe unless they have a built-in NVMe slot

**2 SSD form factors:**
1. mSATA (30mm 52-pin connector)
2. M.2 (22mm 66-pin connector)

M.2 form factor can support any of the three communication interfaces (SATA, PCIe, NVMe) but is limited to their inherent transfer speeds


RAID 0 = "disk striping"
RAID 1 = "disk mirroring"
- Has a max of two drives
- Considered "duplexing" if a separate host adapter is used for second drive
RAID 5 = "stripe set with parity"
- Requires a minimum of three drives
RAID 10 = adds fault tolerance to RAID 0
- 2 types of RAID 10 (see this [article](https://www.thegeekstuff.com/2011/10/raid10-vs-raid01/) explaining the difference)
	- RAID 1+0 (requires 4 disks) - mirrors pairs
	- RAID 0+1 (requires 3 disks) - divides hard drives into 2 groups and mirrors each group

SCA (Single Connector Attachment) - connection that relays both power and data


There were two competing standards for DVD encoding "-" and "+" formatting

The Blu-Ray equivalent to DVD-RW (Rewritable) is BD-RE ("re-recordable")


#### Power Supply

Converts 110V or 220V AC into computer's required DC voltage:

**These are some of the voltages used by computers:**
1. +3.3VDC
2. +5VDC
3. -5VDC
4. +12VDC
5. -12VDC

**Power connector types**
- 20-pin ATX power connector
- ATX12V P4 power connector (supplies +12V power to CPUs from Pentium 4 onward)
- ATX12V 2.x connector created for PCIe
- 6-pin 75W ATX12V 2.1 PCIe connector
- 8-pin 150W ATX12V 2.2 PCIe connector replaced original 6-pin connector


> [! Chapter 2 Review Questions]-
> 1. D
> 2. A
> 3. B
> 4. D
> 5. B
> 6. B
> 7. B (A)
> 8. C
> 9. A, C, D, E, F
> 10. D
> 11. C
> 12. A
> 13. A
> 14. E
> 15. B
> 16. C
> 17. C
> 18. D
> 19. C, D
> 20. A

## Chapter 3: Peripherals, Cables, and Connectors

3 types of LCD monitors
1. TN - fastest but worst color and contrast
2. VA - slowest but most vivid color
3. IPS - somewhere in between

1080p = FHD
1440p = QHD ("Quad High Definition")
2160p = UHD = 4K

4 components of a SAS (Serial Attached SCSI) system:
1. Initiator (like a controller)
2. Target (attached hard drive device or RAID array)
3. Service Delivery Subsystem
4. Expander

> [! Chapter 3 review questions]-
> 1. B, E
> 2. A
> 3. C
> 4. D
> 5. C
> 6. A
> 7. B, D
> 8. A
> 9. B, C
> 10. C
> 11. D
> 12. D
> 13. A, C, E
> 14. D
> 15. B
> 16. C
> 17. B
> 18. B
> 19. C
> 20. B

## Chapter 4: Printers and MFDs

Four classic printer classifications:
1. Impact
2. Inkjet
3. Laser
4. Thermal

2 major types of impact printers:
1. Daisy-wheel
2. Dot matrix

**Daisy wheel printers** use a circular "print head" of raised characters struck by a "solenoid" against an inked ribbon, stamping the character on a sheet of paper

Dot-matrix printers use smaller pinheads with a series of dots

Adjusting distance of print head on impact printer effects contrast of printing

**Inkjet Printers**

Parts of an inkjet printer:
1. Print head/ink cartridge
2. Head carriage, belt, stepper motor
3. Paper feed mechanism
4. Control, interface, and power circuitry

Head carriage moves back and forth during printing

Printer control circuit - controls stepper motors
Interface circuit - manages connection from source (USB, serial, network, infrared)
Power circuit - transformer that converts 110 or 220V AC to DC (often 12V DC)

Printer buffer - small amount of memory used to store print jobs received from the computer

"Page printer" = a printer that prints a page at a time (e.g. inkjet, laser)



**Laser printing**
EP photosensitive drums holds charged when not exposed to light

Types of rollers in laser printers:
1. Feed roller (a.k.a. paper pickup roller) - works with separation pad to feed one page at a time
2. Registration roller - synchronize paper with EP cartridge

Both feed and registration rollers are operated by electronic stepper motors

**One of two mechanisms transfers toner onto paper from charged drum:**
1. Transfer corona wire
2. Transfer corona roller

The transfer corona roller is faster and more widely used today

Fuser heats and pressurizes toner on paper to keep it from brushing right off

HVPS (High-voltage Power Supply) - supplies voltages for charging and transferring corona assemblies

**7 steps for Electrophotographic Image process:**
1. Processing - Scan or raster lines created by Raster Image Processor (RIP) using PostScript or Printer Control Language from image sent by computer
2. Charging - charging corona applies a high negative voltage to EP drum (around -600VDC)
3. Exposing - laser scans drum from side to side, wherever it touches charge is reduced to around -100VDC
4. Developing - toner is transferred to EP drum in form of image
5. Transferring - corona wire/roller applies positive charge to paper, which pulls negatively charged toner onto sheets of paper from EP drum
6. Fusing - pressure and heat permanently adhere the toner to the paper
7. Cleaning - rubber wiper removes leftover toner on the drum

Infrastructure mode - when wireless is used more-or-less permanently to connect a printer to a network

2 major components of printer interface software:
1. Page-description language (PDL)
	1. 3 most common PDLs:
		1. PostScript (PS) - sometimes better for graphics-intensive printing than PCL
		2. Printer Control Language (PCL) - de facto industry standard (better for text-heavy applications)
		3. Graphics Device Interface (GDI) - a Windows program that uses computer processor instead of printer (making for cheaper printers)
2. Driver software

Occasionally the incorrect PDL driver for an older printer can result in garbage output

Two types of print servers:
1. Integrated print server (incorporated into printer itself)
2. Hardware print server

Server Message Block (SMB) - the protocol used by a printer to transport a scan file onto a network folder

Three types of scanning:
1. Scan to email
2. Scan to folder (SMB)
3. Scan to cloud service (Google Drive, OneDrive)

3 qualities of paper
1. Composition (ratios of wood pulp or cotton)
2. Basis weight - weight in pounds of a ream (500 sheets)
3. Caliper - thickness


> [! Chapter 4 Review Questions]-
> 1. A
> 2. C, D
> 3. D
> 4. D
> 5. A
> 6. C
> 7. A, B, C
> 8. B
> 9. D
> 10. C, E
> 11. A, B, D
> 12. A
> 13. A, C, D
> 14. C
> 15. B
> 16. A
> 17. C
> 18. D
> 19. B
> 20. A


## Chapter 5: Networking Fundamentals

File locking - constraint on early LANs that only one user could alter a file at a time
Piconet - dynamically created ad hoc network (as in a bluetooth connection)
Scatternet - two or more linked piconets, where devices serve as bridges

Block storage - Breaks files into equal chunks. allows modification of one part of a file (like a very large one) without modifying the rest of the file

2 different types of "resource access models"
1. Peer-to-peer
2. Client-server

Domains - server-based networks

Five primary network topologies:
1. Bus
2. Star (a.k.a. hub-and-spoke)
3. Ring
4. Mesh
5. Hybrid

OSI network model layers:
7: Application - file services, print services, other applications
6: Presentation - protocol conversion, translation, encryption
5: Session 
4: Transport - data flow, transmitting or receiving datagrams
3: Network - logical addressing, packets
2: Data link - frames. Consists of Media Access Control (MAC) and Logical Link Control (LLC).
1: Physical layer

Helpful mnemonic: **"All People Seem To Need Data Processing"**


802.3 = CSMA/CD = ethernet
802.11 = Wi-Fi

CS = Carrier Sense - computers on network are always listening
MA = Multiple Access - multiple computers have access to the line simultaneously
CD = Collision Detection - detects when a collision occurs, and communications reset for a short, random period

CSMA/CD is a type of "contention-based" access method.

CSMA/CD vs CSMA/CA

Half-duplex communication - between sender and receiver, only one can transmit at any one time
Full-duplex communication - a computer can send and receive at the same time

F-type connectors are used for cable coaxial cables

Plenum-rated cable doesn't produce toxic gas when burned (as would PVC-coated cable)

Cat 5 - 100 Mbps
Cat 5e - 1 Gbps
Cat 6 - 10 Gbps up to 55 m
Cat 6a - 10 Gbps up to 100 m

Direct burial cable - STP with extra waterproof sheathing

Multimode fiber (MMF) - more bandwidth for shorter distances (10 Gbps for 550 m)
Singlemode fiber (SMF) - Lower bandwidth for longer distances (10 Gbps for 40 km)

**T568A order:**
1. white/green
2. green
3. white/orange
4. blue
5. white/blue
6. orange
7. white/brown
8. brown

**T568B order:**
1. white/orange
2. orange
3. white/green
4. blue
5. white/blue
6. green
7. white/brown
8. brown



**Fiber-Optic Connectors**
1. Straight-tip (ST) - probably the most common, twist-and-lock attachment
2. Subscriber connector (SC) - latched connectors
3. Lucent connector (LC) - popular for Fibre Channel, fast storage area networks, and Gigabit ethernet

Managed switches are enterprise devices that add administrative functionality and protocols such as SNMP

Additional functions of managed switches:
1. QoS
2. Redundancy - using Spanning Tree Protocol (STP) to implement redundancy
3. Port mirroring - creates a mirror of port traffic that can be analyzed without affecting original port
4. VLANs

Layer 2 switches only deal with MAC addresses.

Layer 3 (network) switches handle IP addresses as well as handling VLANs

All routers operate on Layer 3 (network) layer

Screened subnet = DMZ

3 advantages of SDNs:
1. Agility
2. Flexibility
3. Centralized monitoring

MFF - miniform factor connector for fiber-optic

MMF - multimode fiber


> [! Chapter 5 Review Questions]-
> 1. D
> 2. C
> 3. A (C)
> 4. C (B)
> 5. A
> 6. D
> 7. C
> 8. A
> 9. D
> 10. A
> 11. C
> 12. A
> 13. A (D)
> 14. B (A)
> 15. A, D (B,C)
> 16. C
> 17. B
> 18. A
> 19. D
> 20. D

## Chapter 6: Introduction to TCP/IP

DoD Model layers:
1. Process/Application
2. Host-to-Host
3. Internet
4. Network Access

Primary internet layer protocol is IP
Three support protocols of internet layer:
1. ICMP - delivers error messages
2. ARP - resolves IP addresses to physical MAC addresses
3. RARP - (Reverse ARP) resolves MAC addresses to IP addresses

Only 2 Host-to-Host protocols:
1. TCP
2. UDP

"Sockets" = host IP address + port number (e.g. 192.168.2.116:80)

Four protocols that use UDP instead of TCP:
1. DNS (port 53) - can use either
2. DHCP (67, 68)
3. TFTP (69)
4. SNMP (161, 162)

NetBIOS provides three services:
1. Name registration and resolution
2. Datagram distribution service, for connectionless communication
3. Session management, for connection-oriented communication

SNMP gathers and manages network performance information

LDAP provides access to directory information; can be managed with ACLs

SMB/CIFS - SMB provides access to shared network resources (e.g. printers)
CIFS is an enhancement of SMB
CIFS is the default file and print sharing protocol in Windows


Subnet masks differentiate when a network ID ends and a host address begins

Three requirements for communicating via IPv4:
1. IP address
2. Correct subnet mask
3. Default gateway - the IP address of the device that connects outside of local network

Classless interdomain routing (CIDR) - divides up bits further than default subnetting method, allowing for finger tuning of network sizes (basically ignores classes)

CIDR uses variable length subnet masking (VLSM)

Private IP address ranges:

1. Class A: 10.0.0.0 through 10.255.255.255 (subnet mask: 255.0.0.0)
2. Class B: 172.16.0.0 through 172.31.255.255 (subnet mask 255.240.0.0)
3. Class C: 192.168.0.0 through 192.168.255.255 (subnet mask 255.255.0.0)

CNAME ("canonical name") allows multiples names assigned to the same host or address

Three standards used in DNS TXT records to combat email spam:
1. SPF - authenticates email server based on IP address
2. DKIM - uses encryption and public-private key pairs to authenticate the message sender
3. DMARC - combines SPF and DKIM into one framework

IPv6 uses three types of addresses:
1. Unicast - identifies single network node
2. Anycast - an address for multiple nodes (packet is delivered to closest)
3. Multicast - an address for multiple hosts, used to communicate to groups of computers

::1 = IPv6 loopback address
2000::/3 range = global unicast



VLANs are partly managed by switches with Spanning Tree Protocol (STP)

VLAN benefits:
1. Reduced need for broadcast traffic, enhancing speed
2. Security
3. Multiple locations can belong to same VLAN
4. Easier reconfiguration

VLANs are implemented on switches.
Subnets are implemented on routers.

Both VLANs and subnets separate broadcast domains.


> [! Chapter 6 Review Questions]
> 1. B
> 2. B
> 3. A
> 4. C (D)
> 5. A, B, C
> 6. B (A)
> 7. B (D)
> 8. C
> 9. C (D)
> 10. D
> 11. A, D
> 12. B
> 13. A
> 14. A, B
> 15. D
> 16. D
> 17. A
> 18. A (E)
> 19. D (A)
> 20. C

## Chapter 7: Wireless and SOHO Networks

802.11 networks use CSMA/CA (Collision Avoidance)
Ethernet networks use SMA/CD (Collision Detection)

3 types of wireless modulation:
1. Frequency-Hopping Spread Spectrum (FHSS) - synchronized changes between frequencies gives appearance of single transmission channel
2. Direct-Sequence Spread Spectrum (DSSS) - redundancies offset higher speed transmission for accuracy
3. Orthogonal Frequency Division Multiplexing (OFDM) - breaks data into subsignals sent simultaneously on different frequency subbands

802.11a uses DSSS
802.11a uses OFDM
802.11g uses OFDM or DSSS
802.11n uses OFDM or DSSS
802.11ac uses OFDM
802.11ax uses OFDMA

In 5 GHz spectrum there are 25 nonoverlapping 20 MHz channels (as opposed to 3 nonverlapping channels in 2.5 GHz)

Bonding spectrum channels can increase throughput

802.11n bonds 2 channels for a 40 MHz spread
802.11ac can bond into 80 MHz or even two 160 MHz channels 

Dynamic Frequency Selection (DFS) - technology in wireless routers that changes frequency usage if it detects radar interference

Basic Service Set (BSS) coloring is a Wi-Fi 6 feature that reduces channel interference

OFDMA is a modulation technique that improves speed by allowing transmission to multiple clients at once

**Bluetooth version features:**
1.x Basic Rate (BR) - minimum of 1.0 Mbps data transfer rate
2.x Enhanced Data Rate (EDR) - 3.0 Mbps
3.x High Speed (HS) - 24 Mbps
4.x Low Energy (LE)
5.x Slow Availability Masking (SAM) - uses frequency hopping to limit interference from Wi-Fi

**Bluetooth classes:**
1 - 100m - 100mW power usage
2 - 10 m - 2.5 mW
3 - 1 m - 1 mW
4 - 0.5 m - 0.5 mW


Windows computers fall back on APIPA (with addresses in the 169.254.x.x format) if DHCP is unavailable


WPA Personal uses the individual's device to handle authentication
WPA Enterprise consolidates authentication in a separate central server (like a RADIUS)

PAT (Port Address Translation) is a specific kind of NAT called "port forwarding"


> [!Chapter 7 Review Questions]-
> 1. B, D
> 2. C
> 3. B, C (A, C)
> 4. C
> 5. C
> 6. A, B
> 7. D
> 8. D
> 9. C
> 10. C, D, A
> 11. D (B)
> 12. C (B)
> 13. A (B)
> 14. B
> 15. D
> 16. D
> 17. B
> 18. C
> 19. A, C
> 20. D


## Chapter 8: Network Services, Virtualization, Cloud Computing



Syslog:

Syslog message components:
1. Facility code - number between 0 and 23 identifying type of device message came from
2. Severity level
3. Text description

Syslog servers use UDP port 514 by default behind a firewall


Domain controller - jargon in Windows Server setups for a centralized authentication server

Alternative centralized authentication servers:
1. Remote Access Service (RAS)
2. Remote Authentication Dial-In User Service (RADIUS)
3. Terminal Access Controller Access-Control System Plus (TACACS+)
4. Kerberos


Load-balancing configurations:
1. Identical duplicates
2. Cross-region
3. Content-based

Proxy server benefits
1. Caching speeds up subsequent requests
2. Filtering
3. Privacy by blocking senders identity

Characteristics of cloud computing:
1. Shared resources
2. Metered utilization
3. Rapid elasticity
4. High availability
5. File synchronization

> [!Chapter 8 Review Questions]-
> 1. B
> 2. C
> 3. C
> 4. A
> 5. A, B (A, C)
> 6. A
> 7. A
> 8. D
> 9. B
> 10. A (C)
> 11. A
> 12. B, C, D
> 13. D
> 14. B
> 15. D
> 16. B
> 17. A, B, C, D
> 18. D
> 19. B
> 20. A



## Chapter 9: Laptop and Mobile Hardware

Mini PCIe is a real laptop expansion slot

Battery specifications:
1. Energy density - how much energy a battery can hold
2. Power density - how quickly stored energy can be accessed
3. Rate of self-discharge - how quickly an unused battery reduces stored charge


> [!Chapter 9 Review Questions]-
> 1. D
> 2. B
> 3. B, D
> 4. A
> 5. A (B)
> 6. C
> 7. C
> 8. C, D
> 9. C
> 10. C
> 11. D
> 12. C
> 13. D
> 14. A
> 15. D
> 16. B
> 17. C
> 18. D
> 19. B
> 20. A


## Chapter 10: Mobile Connectivity and Application Support



3G: either GSM or CDMA

4G: based on IP instead of telephone circuits

5G: three classifications:
1. eMBB (Enhanced Mobile Broadband) - for mobile communication
2. URLLC (Ultra-Reliable Low-Latency Communications) - for autonomous vehicles and industrial applications
3. mMTC (Massive Machine Type Communications) for sensors


Mobile phones use three operating systems:
1. Primary iOS or Android
2. There are two different RTOSs (Real-Time Operating Systems):
	1. Baseband OS - manages all wireless communication
	2. Subscriber identity module (SIM) OS

Updating RTOSs is generally out of the control of users

2 other characteristic mobile phone updates:
1. Product release instruction (PRI) - manages device's network configurations
2. Preferred roaming list (PRL) - manages proper cell tower connections when roaming

IMEI - International Mobile Equipment Identity, unique 15-digit serial number for every mobile device. Dialing `*#06*` will display IMEI

MEID - Mobile Equipment Identifier - alternate serial number taken from first 14 digits of IMEI

IMSI - International Mobile Subscriber Identity - 15-digit identifier with 3 components:
1. MCC - Mobile County Code (e.g. 310 for the U.S.)
2. MNC - Mobile Network Code (e.g. 006 for Verizon)
3. MSIN - serial number
4. ICCID - Integrated Circuit Card Identifier - 20-digi identifier for SIM chips
5. SEID - Secure Element Identifier - hexadecimal code used for security, NFC, payments, etc.

Bluetooth pairing steps:
1. Enable Bluetooth
2. Enable pairing
3. Find a device for pairing
4. Enter the appropriate PIN code
5. Test connectivity


Three components of GPS:
1. Satellite constellation
2. Ground control network
3. Receiver

Location services can include a combination of GPS, cellular location services, and Wi-Fi based location services

Companies using MDM manage the whole device as a corporate device
Companies using MAM can remotely manage particular software on a personal device


SMTP, POP, and IMAP are all insecure

SSL or TLS can be used to secure SMTP, POP, and IMAP

They change the port numbers for each protocol:

| Protocol | Port |
| - | - |
| SMTP SSL | 465 |
| SMTP TLS | 587 |
| IMAP SSL/TLS | 993 |
| POP SSL/TLS | 995 |

STARTTLS secures SMTP, POP, and IMAP, but it doesn't change their port numbers


ActiveSync - an alternate Microsoft Exchange Server protocol that allows syncing emails, calendars, etc. with mobile devices


> [! Chapter 10 Review Questions]-
> 1. D
> 2. C
> 3. A
> 4. B
> 5. D (B)
> 6. B (C)
> 7. C
> 8. A
> 9. A
> 10. C
> 11. A, B, D
> 12. B
> 13. A (B)
> 14. A, B, C
> 15. C, D
> 16. C
> 17. A
> 18. B
> 19. C, D
> 20. B

## Chapter 11: Troubleshooting

Good bedside manner:
- Can you show me the problem?
- How often does this happen?
- Has any new hardware or software been installed recently?
- Has the computer recently been moved?
- Has someone who normally doesn't use the computer recently used it?
- Have any other changes been made to the computer recently?

Grinding, whirring, or scraping noises indicate an issue with a moving component:
- Hard drive platters
- Power supply fan
- Optical drives

Consistent whining sound is probably a bad or dirty fan
Squealing sound is a head crashing into a platter of a mechanical hard drive
Rhythmic ticking is likely to be caused by a mechanical hard drive

Losing date/time and hard drive settings indicates a CMOS battery issue

A single beep indicates a successful POST routine


## Chapter 12

### RAID arrays and storage

3 primary causes:
1. Bad adapter
2. Failing disc
3. Incorrect connection between adapter and disc

Bootable device not found:
1. Connection issue
2. If OS can't be found, may be an MBR problem (this can be fixed with Windows Recovery Environment)

S.M.A.R.T. Diagnostics theoretically help detect failing drives, although it's primarily used in the design stage for manufacturers


### Video systems


**Input issues** 
- Projector: burned-out bulb
- Fuzzy image
- Display burn-in
- Dead pixels
- Flashing screen could either be a bad backlight or a loose connection
- Incorrect color display could be caused by failing controller board
- Dim image caused by failing backlight



**Image problems**

**Other display issues**

### Mobile devices

5 steps to remove malware:
1. Identify
2. Quarantine
3. Remediate
4. Schedule
5. Educate


### Printers

**Impact printers**

**Laser Printers**
Feed jams can occur because of
1) worn out rollers
2) broken drive gear/clutch for pickup roller 
3) worn out exit rollers
4) defective static-charge eliminator strip

Three major causes of blank pages in laser printers
1. Toner issues:
	1. Empty toner cartridge
	2. Recycled toner cartridge
	3. Sealing tape not removed from cartridge during installation
2. Transfer Corona may be missing or damaged
3. HVPS issues - if self-test shows an image on the drum but not on the paper, and the transfer corona assembly is present, then it's an HVPS issue

Cause of all-black pages: defective charging unit, causing toner to stick to entirety of EP drum. Fix by replacing toner cartridge.

Repetitive marks or smudges are caused by dirty rollers. The spacing is characteristic of the specific roller.

Vertical white lines are caused by foreign matter on the transfer corona wire (which prevents toner transfer)

Vertical blacks are caused by a scratch in the EP drum or a dirty charging corona wire, both of which keep a sufficient charge from being placed on EP drum

Image smudging after print: fuser problem

Two causes of ghosting or echo images:
1. Broken cleaning blade
2. Bad erasure lamps

Two causes of printing gibberish:
1. Printer driver
2. Formatter board (usually looks like wavy lines of print or random dots)

**Static charge eliminator strip** - drains corona charge away from paper after toner has been applied
**Erasure lamps** - wipe away previous electrostatic discharges on EP drum

### Networks

**Troubleshooting hardware tools:**
- Multimeter
- Crimpers
- Cable strippers
- Wi-Fi Analyzer
- Toner probe (fox and hound)
- Punch-down tool
- Cable tester
- Loopback plug
- Network tap ("test access port")

**Troubleshooting command-line tools:**
- `ipconfig`  - displays info on Windows about NIC setup, and DHCP status. If the IP address is in the `169.254.x.x` range, that means APIPA is being used
	- `ipconfig /all` - Provides full configuration info
	- `ipconfig /release` - Releases IP address DHCP
	- `ipconfig /release6` - Releases IPv6 addresses
	- `ipconfig /renew` - Obtains a new IP address from a DHCP server
	- `ipconfig /renew6` - Obtains a new IPv6 address
	- `ipconfig /flushdns` - Flushes the DNS server's name resolver cache

`ip` - Linux/MacOS equivalent to `ipconfig`

- `ping` - a.k.a. ICMP echo requests/replies, send packets and receive response, providing time info
	- Can use either `ping hostname` or `ping IP address` syntax
	- `ping -t` - persistent ping
	- `ping - n (count)` - specifies number of echo requests to send
	- `ping l (size)` - specifics packet size
	- `ping -4` or `ping -6` - specifies use of IpV4 or IPv6 network

- `hostname` - returns name of host computer

- `netstat` - lists all TCP/IP connections on machine
	- `netstat -a` - displays all connections
	- `netstat -b` - displays executable involved with connections
	- `netstat -e` - displays ethernet statistics
	- `netstat -f` - displays FQDNs
	- `netstat -n` - displays info in numerical form
	- `netstat -o` - displays owning process associated with each connection
	- `netstat -p` - uses proto (?)
	- `netstat -r` - displays routing table
	- `netstat -s` - displays per-protocol statistics

- `nslookup` - verifies entries on a DNS server

- `net` - many administrative tools for groups, sharing, accounts, etc. in Windows
	- `net share` - shares a folder across the network

- `tracert` - verifies route to remote host

- `pathping` - combines `ping` and `tracert` functions
	- `pathping -h (number)` - specifies maximum number of hops to search
	- `pathping -n` - does not resolve hostnames
	- `pathping -p (number)` - number of milliseconds to wait between pings
	- `pathping -q (number)` - number of queries per hop
	- `pathping -w (number)` - number of milliseconds to wait for each reply


If you can ping an IP address but not a hostname, it's a DNS error
If you can ping a hostname but can't access it with a browser, it's an HTTP or port 80 issue

"Link local addresses" - IPv6 version of APIPA. They always start with fe80::


Latency - delay on a network
Jitter - variable latency
Port flapping  - when a switch opens and closes rapidly


> [! Chapter 12 Review Questions]-
> 1. A, D (A, B)
> 2. C
> 3. A
> 4. C
> 5. B
> 6. B
> 7. A, D
> 8. B
> 9. A
> 10. B
> 11. D (A)
> 12. B
> 13. C, D
> 14. D
> 15. B
> 16. C
> 17. B (C)
> 18. A
> 19. D
> 20. C




---

## Objectives notes

**LCD types:**
1. TN (Twisted Nematic) - oldest, most common type. Molecules twist, turning off or on 
	1. Molecules are parallel to glass panel, rotate.
	2. Cheapest to produce
	3. Color reproduction and viewing angle are weaker
2. IPS (In Plane switching)
	1. Excellent color quality
	2. Poor refresh rate (bad for gamers)
	3. Suffers from "IPS glow" where backlight is visible from the side
3. VA (Vertical alignment) - molecules are arranged vertically, perpendicular to glass.
	1. Essentially a compromise between TN and IPS
	2. Slow response time but good image quality (slower than IPS)

**Smartphone digitizer:** The touchscreen that sits below protective glass and detects inputs

**(PRL) Preferred Roaming List**: Database that prioritizes connections and frequency bands a mobile device should use. This allows it to use different carriers outside of home network.

**(MDM) Mobile Device Management** - management software for large numbers of mobile devices, like corporate phones

**(MAM) Mobile Application Management** - ditto, but applications rather than devices

**LDAP (Lightweight Directory Access Protocol)** - open, vendor-neutral protocol for internet contact directories. Thorough Red Hat [article](https://www.redhat.com/en/topics/security/what-is-ldap-authentication) on LDAP


### TCP vs. UDP

TCP: connection-oriented, more reliable, sequence and data are verifiable
- Used for:
	- email
	- transferring files
	- general web browsing
- HTTPS and SSH

UDP: connectionless, broadcast and multicast are possible; no confirmation of successful transfers or sequence of data
- Used for:
	- gaming
	- video streaming
	- video chatting
- DHCP and TFTP

Good [article](https://www.geeksforgeeks.org/differences-between-tcp-and-udp/#) on the difference between TCP and UDP

---

**Managed vs unmanaged switches**
- Unmanaged switches are typical SOHO switches
- Managed switches are larger enterprise-oriented, and have many more features

**PoE Injectors** enable PoE even when an ethernet switch doesn't support PoE


**ONT (Optical Network Terminal)**: converts fiber network signals into ethernet wiring compatible with SOHO router

**Unified Threat Management (UTM)** - single device that manages multiple security features and services on a network

### DNS

**DNS Records:**
- [This is a very helpful article on DNS records](https://www.pbrumby.com/2018/05/09/dns-records-explained/)
- **A record** (a.k.a. IPv4 address record) points domain name to one or multiple IP addresses
	- Three fields in A records:
		1. name (a.k.a. hostname, alias, prefix or DNS entry)
		2. destination (IP address)
		3. TTL (time-to-live) - interval between checking with authoritative nameserver
- **AAAA record** (a.k.a. IPv6 address record) has the same functionality but for IPv6 
- **MX records** create mail server for a domain
	- Four fields in MX records:
		1. Name
		2. Priority - which server should be attempted first
		3. Destination
		4. TTL
- **TXT records** add arbitrary text (often for verification of domain ownership)


### **Spam management:**
Cloudflare [article on DMARC, DKIM, and SPF](https://www.cloudflare.com/learning/email-security/dmarc-dkim-spf/)

Three email authentication methods:
1. **DKIM** - uses public key cryptography to verify identity of a sending mail server
2. **SPF (Sender Policy Framework)** - lists IP addresses of all servers allowed to send emails from a domain
3. **DMARC** - tells mail servers what to do with given DKIM and SPF records

DKIM, SPF, and DMARC are stored as DNS TXT records



**DHCP**
- **Lease time**: interval that an IP addresses remains attached to a device
	- DHCP assumes all connections are temporary. This keeps IP addresses free for Wi-Fi networks with fast turnover.
	- Check with `ipconfig /all`
- **Reservation**: a reserved IP address on a DHCP server, like a static address
- **Scope:** range of IP addresses that the DHCP server can lease to devices on the network


## Jason Dion Udemy

