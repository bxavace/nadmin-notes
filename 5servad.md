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
