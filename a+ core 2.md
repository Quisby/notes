# A+ Core 2
#tech #type/subject 

> [!Links]
> 
> **Related Notes**
> - [[CompTIA Certs]]
> 	- [[ITF+]]
> 	- [[A+ Core 1]]
> 
> **Online Links**
> - 
> 
> **Jump to sections:**
> - 


## Plan of Study
- [x] Total Seminars Udemy videos
- [ ] Go through Objectives
- [ ] [Watch DeanCuber 1102 PBQs](https://www.youtube.com/watch?v=jqc-yEnfQow&list=PL5rnkhBIKwIzEM7cnxA2ySLknThyaZD35)
- [ ] Sybex Study Guide
- [ ] Jason Dion Udemy videos
- [ ] Messer videos
- [ ] All-in-One
- [ ] Certification Passport (Meyers)
- [ ] Jason Dion study sheet
- [ ] Certmike

**Jason Dion Practice Tests:**
1. 86 (2024-02-13)
2. 


## Total Seminars

"C"-rated Class of fire extinguishers is best for electronic fires

OS key functions:
- Kernel handles primary memory management
- Processes
	- PID = process ID in Resource Manager
- Hardware/Device drivers (e.g. Device Managers)
- Storage
- Networking

Microsoft "domain" concept: domain controller manages an "Active Directory" of computers that can log into remotely managed accounts, allowing for SSO

Samba allows Linux computers to  participate in an Active Directory domain

Surge protector online protects devices from power spikes

UPS protects devices from power spikes and sags

Windows uses a swap file, but Linux uses a separate swap partition

Master Boot Record (MBR) - oldest partitioning style
- Tells computer where OS resides
- `LBA 0` - contained "boot loader" as well as partition tables
- Could only use four partitions, and only one would be active
- Max size of 2 TB per partition

"Extended partitions" - can create multiple "logical drives" inside of an "extended" fourth partition in MBR

GPT (GUID Partition Table) - replaced MBR
- GUID - global unique identifier - 128-bit identifier that identifies an individual partition scheme
- 128 partitions per drive
- 18.8 million terabytes limit per partition
- `LBA 1` contains "primary GPT header"

Windows 10 requires GPT

"Disk management" can convert between MBR and GPT partitions

File Allocation Table - index of all the LBAs on a drive
- FAT16
- FAT32

**File systems**
- FAT32 - oldest, predates Windows; first file system that enabled long filenames; 8 TiB max size 
- NTFS - up to 16 EiB, individual files can be up to 256 TiB size
	- Supports encryption, compression
	- NTFS is so powerful it can be too large and overkill for smaller thumb drives
- exFAT - compromise between FAT32 lightness and NTFS features
- CDFS - designed for optical discs to organize file system
- ext3 - supports 32 TiB volumes, 2 GiB files
- ext4 - supports 2 EiB volumes, 16 TiB files

Dynamic disks - unique to Windows
- Can expand or shrink size of partition
- Can create spanned volumes across multiple drives
	- Spanned drives create multiple points of failure and are for emergencyes only

Good rules of thumb:
1. Keep boot drive basic rather than dynamic
2. Set boot drive to GTP
3. Easy to create dynamic drives, but reverting dynamic to basic erases data

Storage Spaces - Windows tool to manage RAID arrays

EFS - (Encrypting File System) - file-level encryption built into NTFS

Mass storage maintenance:
1. Error checking (e.g. chkdsk)
2. Defragmentation

USB Type-A = downstream
USB Type-B = upstream

**Windows 10 Editions and Features**
- Home
- Pro
- Pro for workstations
- Enterprise

Requires 1GB RAM for 32-bit, or 2GB RAM for 64-bit editions



**Windows 11 Editions and Features**
- Requires UEFI, Secure Boot, and TPM 2.0
- First "Zero Trust" OS
- Requires active internet connection
Home
Pro
Pro for Workstations
Enterprises

Requires 4GB RAM and 2 core processor

Only enterprise supports Long-Term Servicing Channel/"Branch"

2 options for booting over a network:
1. PXE (Pre-boot Execution Environment)
2. Apple NetBoot

WinRE (Recovery Environment) - creates a recovery disk/drive with a USB drive

Image deployment - clones hard drive and remotely installs multiple computers on a network

`winver` command will give you full system version information in Windows



Services - perform critical background tasks for OS
Processes - upper-level user-run apps

`.cpl` files are the applets within Control Panel
`appwiz.cpl` is the uninstall applet. You can run it by simply typing in the name after the Windows key

"USB selective suspend" - cuts of power to USB devices in order to conserve battery

MMC (Microsoft Management Console)

Administrative Tools (Windows 10) -> Windows Tools (Windows 11)

`msinfo` condenses all system information into one screen
`resmon` provides hardware information
`msconfig` allows you to configure safe boot and other things
`mmc` starts Microsoft Management Console

"Snap-ins" - plugins for MMC

`regedit` works with Windows registry

Windows Registry has five root keys

HKLM = shorthand for HKEY_LOCAL_MACHINE 

registry files are stored in the `C:\Windows\System32\config`

Managed Users & Groups in Windows
Basic: in settings
Moderate: control panel

You can access Users & Groups  by going `Control Panel > Windows Settings > Computer Management`

NTFS Permission Attributes for a Folder:
1. Full control
2. Modify - read, write, delete
3. Read and execute - can run executables and open documents
4. List folder contents
5. Read - view contents and open files
6. Write - 

NTFS Permissions Attributes for a File:
1. Full control
2. Modify - read, write, delete
3. Read and execute - can open and run a file
4. Read
5. Write - can read and write

Inheritance - subfolders will inherit permissions from containing folder

"Deny" - can revoke permissions from subfolders

NTFS permissions are distinct from "network share" permissions

UNC (Universal Naming Convention) - using this format for network shares: `\\DanielsPC\DanielC`

"Mapping" shared drives gives it a permanent drive letter on a local machine

Security settings for users can be set in the `Local Security Policy` utility
1. Password requirements under "Password Policy" tab
2. "Account Lockout Policy" tab

Domain policies will always override local security policies

`sudo apt-get update` will update repository and package lists
`sudo apt-get upgrade` will apply updates found with the `sudo apt-get update` command

3-2-1 backup principle: 3 copies across 2 media with at least one in the cloud

`dir /p` shows directory contents step-by-step

Two ways to access cmd help:

1. `/?` switch
2. `help <command>`

`su` allows you to set a `sudo` command for the rest of the session

`man` is Bash equivalent of `help`

`cd\` takes you to root directory in Windows

`..` double dot allows `cd` to move up a folder

To jump from drive to drive, just type in the drive letter and colon (e.g. `D:`)

Use `cd` once on a particular drive letter

`cd ~` brings you back to user home directory in Linux

`cd /` brings you to root directory in Linux

`pwd` shows working directory in Linux

`md` makes a folder in cmd

Windows is not capitalization-sensitive, but Linux is

`rd` removes a folder in cmd

`rd /s` deletes a directory in cmd

`rmdir` deletes a folder in Linux

`rm -r` removes a directory and its contents in Linux

`del <filename.jpg` deletes a file in cmd

`del *.txt` deletes all .txt files in a directory in cmd

`del *.*` deletes everything in a directory in cmd

`copy <orginal.txt> <destinatiion>` copies a file to a new directory

`rm <filename>` deletes a file in Linux

`cp` copies files in Linux (`copy` in Windows)

`mv` moves files in Linux (`move` in Windows)

`chkdsk` checks a drive for errors
`chkdsk /f` checks for errors and fixes errors

SFC (System File Checker) checks system files

`sfc /scannow`

`DISM` - compares system to stored online copy of Windows

`dism /online /cleanup-image /restorehealth`

Always run in order SFC > DISM

`diskpart` interactive tool that manages drive and storage

3 types of super copy commands:
1. `xcopy` - designed to copy large folders of files
2. `robocopy` - similar to `xcopy`, but improved with speed and more verification
3. `dd` - bit-by-bit copier for Linux that copies entire partitions
	1. Can wipe drive by specifying zero as source `dd if=/dev/zero of=/dev/sdb`

`icacls` can manage NTFS permissions in cmd

`chmod` is the Linux equivalent of `icacls`, changes permissions

`chown` allows you to take ownership of any file or folder

`sudo passwd` changes the password for the current user in Linux

`shutdown` allows you to shutdown a Windows computer

`shutdown /s` fully shuts down, but there are many other switches


**Advanced Windows commands:**
`tasklist` - lists processes
`taskkill` - can stop a process using IM or PID

`gpupdate` - queries domain controller for current group policies and forces update
`gpresult` - lists result of a `gpupdate` command


**Advanced Linux commands:**
1. `shutdown` - 
2. `apt-get` (older) or `apt` both install programs
	1. `update`
	2. `upgrade`
	3. `install`
	4. `remove`
	5. `ps` - controls processes
	6. `grep`
	7. `kill` - kills processes

`set` command in cmd.exe provides list of environmental variables

Powershell scripts use extension `.ps1`

`pathping` 

`Time drift` - when system clock 

**WinPE** - Windows Preinstallation Environment
**WinRE** - Windows Recovery Environment
- WinRE is accessed by clicking "Repair your windows""
	- System Restore
	- Uninstall/roll back updates
	- System Image Recovery
	- Startup Repair
	- Command Prompt

3 categories of Windows troubleshooting problems:
1. Boot problems
2. Windows can't load desktop
3. Bizarre things happen on desktop (e.g. BSOD)

When you have a device driver issue, get into safe mode

Mark Russonovich Sysinternals
- Autoruns

Services not starting - restart the service or set it to start automatically. Also check event viewer.

**Public IP address classes:**
A: 1.0.0.0 - 126.0.0.0
B: 128.x.0.0 - 191.x.0.0
C: 192.x.x.0 - 223.x.x.0
D: 224.x.x.x
E: 240.x.x.x

Nowadays, the initial number rules aren't usually followed

**3 sets of Private IP Addresses:**
A: 10.x.x.x
B: 172.16.x.x - 172.31.x.x
C: 192.168.x.x

**Loopback address:** 127.0.0.1

`ping`
`ping -t` - continues ping past default 4 attempts
`ipconfig`
`ipconfig /all`

Gateway router - connects LAN with ISP

If DHCP doesn't work, computer will fall back to APIPA 

169.254.x.x is the default APIPA address (Class B)

`ipconfig /renew` will connect to a DHCP server
`ipconfig /release` will disconnect from a DHCP server

"Troubleshoot Network" will reset the NIC

The "Alternate Configuration" tab under IPv4 Properties in Network and Sharing Center allow you to adjust APIPA address settings

`netstat`
`netstat -n` removes titles and shows only IP addresses and port numbers

`netstat -a` shows every connection, including listening ports

"TCPView" from sysinternals provides a graphical version of netstat

DNS replaced original "hosts" file

`nslookup` - indicates if a DNS server is good

Grab the IP address of the DNS server using  `ipconfig`
Type in `server <IP address of DNS server>` in netstat interactive mode, then test it by typing in generic domain names. If the requests time out, the DNS server is down.

NetBIOS / NetBT - naming convention for Windows computers

All Windows systems will either belong to a "Workgroup" or "Active Directory Domain"

You can determine which in the system properties Windows

NetBIOS / NetBEUI - original naming system used for small LANs, used MAC addresses

Superseded by NetBIOS / NetBT 

OU (Organizational Units) - Container/folder that you can use to hold users or groups in AD administration

Original LAN manager developed into SMB

`net` commands
	`net view`
	`net share`
	`net use`
	`net user`

Stateful firewalls monitor traffic for abuses and block those connections

Stateless firewalls block all non-allowed connections

WPA uses TKIP
WPA2 uses AES

ESSID is a single SSID spread across multiple WAPs (commonly used in enterprise environments)

Telnet (port 23) - one of oldest internet protocols
- PuTTY - one of most common Telnet clients

RDP (port 3389) - 

MSRA - dual control (can remote in but still control locally)
RDP - only controlled remotely

VNC Virtual network computing - most popular thirty party protocol

TightVNC - runs VNC on Windows

FTP Passive Mode - port 21
FTP Active Mode (traditional default) - initiates client-server transfer on port 21, but also initiates server-client transfers on port 20. Active mode is 5x faster, but all routers will block it (unless port triggering is enabled)

Port triggering opens port 20 when a connection is initiated on 21. Many games also require port triggering

TFTP - uses UDP instead of TCP, resulting in a lot of data loss. Only used for LANs. Uses port 69.

Reasons for proxy servers:
1. Firewall filtering
2. Filtering for content
3. Caching

Windows Internet Options > LAN settings contains settings for establishing proxy servers

802.11
Zigbee - wireless 2.4 GHz connection used for IoT
Z-Wave - 900 MHz used for IoT

`tracert` (Windows) `traceroute` (Linux/Mac) - run when everything functions to see how network is supposed to look

ACPI - advanced power controls (like sleep/hibernate, etc.) Can be managed in OS or BIOS

ACPI Level 0 - powered on
ACPI Level 3 - sleep mode (RAM keeps running)
ACPI Level 4 - RAM is copied to HD, then everything is shut off

`*#06#*` will always get you to your IMI number

Host based :: Network based :: Physical security

Common security threats:
1. MitM
2. Spoofing
3. Denial of Service
4. Distributed denial of service
5. Zero day

Symptoms: Renamed files, missing files, loss of control

Mitigation for individual hosts:
1. Patch host
2. Anti-malware and anti-virus
3. Host-based firewall

UTM consolidates security products (e.g. firewalls, IPS, anti-malware)

These include cloud-based UTMs

Physical security levels:
1. Perimeter (security guard, mantrap, doorlocks)
2. Room (badge reader, smart card, biometric locks)
3. Device (cable locks, server lock, USB locks, privacy screens, key fobs, hardware token)

Password cracking:
1. Brute force
2. Dictionary hack
3. Rainbow tables - combination of dictionaries and patterns

Password best practices:
1. Complex passwords
2. Password expiration
3. Screen locks
4. Mobile lock screens
5. BIOS/UEFI passwords
6. MFA

MFA types:
1. Something you know (e.g. password)
2. Something you have (physical device, authenticator)
3. Something you are (biometrics)
4. Somewhere you are (more common in industrial environments)

Malware types:
1. Virus - replicate and activate
2. Worm - first generation of malware to use network to replicate themselves (essentially all of today's malware does this now)
3. Trojan - replication caused by person copying some other software
4. Rootkit - malware hidden in boot sector
5. Ransomware
	1. Rogue antivirus
6. Botnets
7. Keylogger
8. Spyware

Anti-malware best practices:
1. Backup/restore/reimage
2. End-user education


7-step anti-malware procedure
1. Identify and research malware symptoms
2. Quarantine infected systems
3. Disable system restore
4. Remediate infected systems
5. Schedule scans
6. Return to old restore
7. Educate end user

Environmental Controls
1. Government regulations (e.g. industry standards, OSHA)
2. Use MSDS for chemicals
3. Temperature and humidity
4. Proper ventilation
5. Battery backup/UPS
6. Surge suppressor


"Documents you should know:"
Network topology diagrams can be either
1. Logical
2. Physical

Best resources:
- Microsoft Knowledge Base
- AWS Documentation
- Cisco Documentation

Regulation and compliance
1. Legal
2. Industry standards
3. Best practices
4. Tradition
5. SOPs
6. AUP
7. Password policy

Inventory management
1. Asset tags (e.g. barcodes)

4 types of data with legal protection:
1. PII
2. PHI (Personal health information)
3. GDPR
4. PCI-DSS

Change management - system for upgrading enterprise equipment
1. "Change board" considers requests
	1. Document business practice
	2. Document purpose
	3. Document scope
	4. Risk analysis
2. Upon approval, plan change
3. Obtain end-user acceptance
4. Develop rollback plan
5. Document changes ("lessons learned")

File-level backup
- Works for critical files
Image-level backup
- More popular level backup nowadays

Proper battery disposal:
1. Lithium-ion battery most be recycled
2. Toner cartridges
3. CRT monitors

Can't really low-level format modern hard drives
Must be overwritten with 

Hard drive demolition:
1. Degaussing machines - use a magnetic field
2. Shredding machine
3. Punchdown machine

osTicket  - open source ticketing system


## Objective List

**List of Windows commands:**
- cd
- dir
- md
- rmdir
- ipconfig
- ping
- hostname
- netstat
- nslookup
- chkdsk
- net user
- net use
- tracert
- format
- xcopy
- copy
- robocopy
- gpudate
- gpresult
- shutdon
- sfc
- /?
- diskpart
- pathping
- winver

**Microsoft Management Console (MMC) snap ins:*
- mmc.exe
- eventvwr.msc = Event Viewer
- diskmgmt.msc = Disk Management
- taskschd.msc = Task Scheduler
- devmgmt.msc = Device Manager
- certmgr.msc = Certificate Manager
- lusrmgr.msc = Local Users and Groups
- perfmon.msc = Performance Monitor
- gpedit.msc = Group Policy Editor (gathers longterm data, can set alerts)
- gpmc.msc = Group Policy Management Console (Enterprise level)
- msinfo32.exe = System Information
- resmon.exe = Resource Monitor
- msconfig.exe = System Configuration
- cleanmgr.exe = Disk Cleanup
- dfrgui.exe = Disk Defragment
- regedit.exe = Registry Editor

**Linux commands:**
- ls
- pwd
- mv
- cp
- rm
- chmod
- chown
- su/sudo
- apt-get (apt)
- yum
- ip
- df
- grep
- ps
- man
- top
- find
- dig
- cat
- nano

Synthetic backup - creates a full backup by using a previous full backup and related incremental backups


Linux octal permissions:

Triplets occur in this order:
Owner - Group - Others

Numerical values for permissions:
- r (read): 4
- w (write): 2
- x (execute): 1

[Good Red Hat article on Linux permissions](https://www.redhat.com/sysadmin/linux-file-permissions-explained)

## Professor Messer

Windows 10 Pro features:
- RDP host ability
- Bitlocker
- Windows Domain
- Group policy management

Windows 10 Pro for Workstations:
- Up to 4 physical CPUs
- Up to 6 TB RAM
- Support for ReFS (Resilient File System)

Windows 10 Enterprise
- Volume licensing
- AppLocker (what applications can run)
- BranchCache (remote site file caching)
- Granular User Experience (UX) 

Windows 10 Max RAM:
- Home: 128 GB
- Pro: 2 TB
- Pro for Workstations: 6 TB
- Enterprise: 6 TB

Useful `copy` switches:
- `/v` verifies that copy worked
- `/y` skips yes/no prompts during copy

`xcopy /s` copies working directory along with subdirectories

Robocopy is more advanced (included in Windows 10 and 11)

`shutdown` switches:
- `/s` - perform a full shutdown
- `/t <nn>` - time in seconds to delay
- `/r` - restart
- `/a` - abort shutdown!

- `gpupdate /target:{computer|user} /force`
- `gpupdate /target:user /force`

`gpupdate` can change group policies without requiring reboot

`gpresult /r` provides information on latest group policy changes

`nestat -a` - show all active connections
`netstat -b` - shows binaries being used

`pathping` - combines `tracert` and `ping`, making a map with a reply time

`Ctrl-Shift-Esc` - launches Task manager


Windows network shares ending with a dollar sign ($) are hidden
