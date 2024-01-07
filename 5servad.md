# Server Administration Essential Training

### Server Architecture
**Form factor**. This refers to the size, shape, and overall packaging of the computer device.
1. **Tower Server.** This server is similar to desktop computers.
2. **Rack Mount Server.** It is designed to save space; servers that slide in and out of a rack.
3. **Blade Technology.** This is designed for largest number of servers in a smallest area. Unlike a rack server that is independent to other servers, blade technology works as one; server in a single card.

#### Server Components
1. Motherboard. It is the main circuit board that provides communication to all other components.
2. CPU (Processor). Differs in socket type, like AM4 or Intel Socket type.
3. RAM (Memory). ECC or non-ECC: error correction code; DDR versions like DDR4, DDR3, DDR5. 
4. Expansion Slots. These are PCI, PCI Express, AGP, etc.
5. Hard Drives and Solid State Drives.

**Hot Swappable**: This is a component that can be changed without shutting down the server.

#### Power and Cooling components
Wattage = Voltage * Amperage

Cooling concepts:
1. Airflow
2. Thermal dissipation
3. Baffles and shrouds
4. Fans
5. Liquid Cooling

### Server Administration
#### Server Installation (Windows Server 2019)

No notes. Just demonstration of installation and configuration on HyperV.

### Server Maintenance
Tools Available in Windows Server 2019
1. Server Manager. Tool used for configuring the server, adding servers, server group, etc.
2. Task Manager. The usual task manager in Windows OSes.

#### Event Logging
Event Viewer. An event logging tool for Windows Server 2019.
Event Viewer logs everything that is happening on the machine. It could be a level of:
* Information
* Error
* Warning

**Logging skill** is an important skill for a server administrator; _Knowing problems way before users start noticing and complaining about it is a great skill to have for a server administrator._ 

#### Asset Management
No notes.

#### Documentation
- Includes server manuals, diagrams like network, architecture, and dataflow.
- Documenting your recovery process. The last thing you want to do is stressing over what to do when the data gets lost.
- Documenting your changes -- be very familiar with the change management.
- Service-level agreements.

### Networking
No important notes.

**SMTP protocol**: uses port 25, port 587 for security. It is a protocol for sending email between email servers.
**FTP/S protocol**: uses ports 20 and 21; ports 989 and 990 for security. It is a protocol for transferring files.
**DNS**: uses port 53, for host name resolution (AWS Route 53 for better memory)
**DHCP**: uses port 67 and 68.

#### Network Cabling
Ethernet (Twisted Pair)
* CAT5 (100Mbps)
* CAT5e (1Gbps)
* CAT6 (10Gbps)
* Patch Cables (straight; TIA/EIA standards)

Fiber Cables
* Single
    - Single beam, longer distance, faster
* Multimode
    - Multiple beam, shorter distance, slower

#### Wireless Networking
No notes. Just: wireless is less hassle over physical cabling.

### Storage

#### Storage Technologies
Two types of Hard Drive:
1. Magnetic: Inexpensive.
    - RPM (revolutions per minute)
    - Dimensions (is it for Laptop or PC?)
    - Capacity
    - IOPS (input/output per second)
    - Seek time and latency
    - Hot swappable
2. SSD (Solid State Drive): Quiet, durable, yet expensive.
3. Direct-attached storage (NAS)
4. Network-attached storage (NAS)
5. Storage-area network (SAN)
6. Just a bunch of disks (JBOD)

#### Understanding RAID
RAID: Redudant array of independent disk; Idea of multiple disks putting them together in an array to function together as one storage server. It provides **FAULT TOLERANCE**.

RAID 0
- disk striping;
- zero fault tolerance;
- minimum of two disks;
- increased read performance;
- 100% drive space utilization

RAID 1 (with fault tolerance)
- disk mirroring;
- **exactly** two disks;
- increased read performance;
- 50% drive space utilization: you can only store 1 TB of data in a 1TBx2 disks, due to mirroring.

RAID 5
- disk striping with parity;
- minimum of three disks;
- increased read performance;
- efficient disk space utilization;
- provides fault tolerance in case of single-drive failure.

#### Capacity Planning
What to consider?
1. OS Growth
    * patches
    * service packs
    * log files
    * temp files
2. Data Growth
    * customer data
    * archived data
    * recovery data

**Mitigation Strategies**
1. Disk quotas
    - soft quota (alerts)
    - hard quota

2. Compression
3. Regular cleanup
4. Routine archival

### Security

#### Server Hardening
OS and Application Hardening
- Stop and/or uninstall unneeded services.
- Close unneeded ports.
- Minimize software installations.
- Keep security patches up to date.

Hardware Hardening
- Disable unneeded hardware and physical ports or devices
- BIOS Password
- Disable WOL (Wake-on-LAN)
- Set appropriate boot order
- Chassis locks

### Environmental Protection
use uninterruptible power supply (UPS)
specifications to consider when buying UPS:
1. Runtime
2. Capacity
3. Automated graceful shutdown
4. Remote management

UPS features
1. power conditioning
2. surge protection
3. periodic testing

#### Secure Storage Disposal
1. Soft wipe
2. Hard wipe - actually deletes everything.
3. Remote wipe - portable devices.
4. Physical destruction
5. Environmentally safe disposal