## Computer Science Principles: The Internet

### Internet Basics
It first started as a project for the US Government called ARPANET. It was a way to connect computers together.

Packets - blocks of information sent to a computer.

TCP/IP - Transmission Control Protocol/Internet Protocol; developed in the 1970s by Vint Cerf and Robert Kahn.

In 1982, it was decided to be the protocol for ARPANET.

World Wide Web - named Nexus, created by Bernes-Lee using NeXT Computer at CERN.

Hypertext Transfer Protocol - also created by Bernes-Lee along with HTML.

High-Performance Computing Act of 1991 - funding of new technologies like Mosaic; commercialization of internet.

W3C - WWW Consortium; slow organization.
WHATWG - Web Hypertext Application Technology Working Group; continued to develop HTML as standard.

ICANN - non-profit created in 1988; organizes terms used to created addresses like .com, .net, etc.

ICANN manages the identifiers that are part of a website URL or domain name.

### Addressing and Routing Information

Header - an important information inside a packet -- like an acknowledgement whether the information is sent or not and how long it is.

IP Addresses - used by the internet protocol.

IPv4 - 4 sets of three digit numbers separated by a period; the IP address.

IANA - organization that determines what numbers and subsets are assigned to different groups. Some IPs are private, and some IPs are public.

IPv4 - can only support 4 billion devices. It needed to be scaled, so in 1995, IPv6 was created to take into account the other devices and future devices.

IPv4 - uses 32 bits.
IPv6 - uses 128 bits; organized into 8x16 bits.
Example: 21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A

Dual Stack - supported by some operating systems.

#### Domain Name Servers (DNS)
DNS has a technique for mapping IP-addreses to human-readable names.

DNS name resolution - translating domain name to an IP address. E.g. http://google.com maps to 8.8.8.8.

Parts of a URL domain `www.dougwinnie.com`
1. Top level domain - the `.com` in the URL.
2. Domain name/Host name - the `dougwinnie` in the URL; collection of servers under `dougwinnie` name.
3. Subdomain - the `www.` in the URL; it means that it is the server type -- a web server.

Router - directing requests to the internet, the middleman of the internet-client connection. It also can be the connection gateway between the other devices connected under it (e.g. connecting with your laptop PC from your smartphone, under the same router, is possible)

Packets - messages that are broken down into small pieces of data before sending throughout the internet.

**Part of the header of a Packet**:
1. Length of the packet
2. Source of the packet
3. Total number of packets
4. Destination of the packet

**Fault tolerance with the packet traversals** - solved with headers. A network is able to re-route information if a server in the network is down.

#### Reliability and TCP
**TCP** - Transmission Control Protocol; acts as a auditor and reviewer of the packet.

**TCP** - uses a process that analyzes and reviews the packets. Kind of like the verification step before recreating the original file from the collection of packets.

#### Reliability vs Speed
* **TCP** - values reliablity in communication
* **UDP** - values speed and latency in communication

TCP - foundation of how data is transmitted over the networks.

### Web Servers
Recall that a URL has 3 parts to it. A DNS server is able to resolve that URL to its IP address aprt.

**Subdomains** can link to a specific web server (e.g., `www`, `dev`, `ftp`, and others)

In DNS, there are two _records_:
1. **A** records - address record; this is the IP address that we want to map to the URL.
2. **CNAME** records - canonical name record; acts like an alias that redirects the user to another location. For instance, you might want to redirect users requesting `blog.example.com` to `example.com`.

**HTTP** - the *request* part of this protocol takes place on top of the TCP/IP protocol.

**Daemon** - program that runs on a server and works on the background (see Linux Fundamentals for this). An example of this is `httpd`. 

#### Remembering Requests with Cookies
**Session** - time you're on a web site; when the browser is closed or shut down, the session is lost or destroyed.
**Cookie** - remembered by browsers so you don't have to re-log-in again; can also be used to **track browsing habits**!

Cookies are made to make web browsing a personal experience.

#### Securing Requests with SSL and TLS
**SSL** - Secure Sockets Layer; an early version of security created by NetScape.
**TLS** - Transport Layer Security; the `s` in the `https` or the lock icon before it.

TLS is the modern encryption protocol used to secure HTTPS connections. It is also the successor to SSL (Secure Sockets Layer), which is now considered outdated and insecure.

**handshaking** - creates and verifies connection from the client to the server and vice-versa.

Authentication - done using a security certificate; confirms that a website is legitimate. Websites using HTTPS have a TLS/SSL certificate issued by a trusted Certificate Authority (CA).

### Encryption

Symmetric and Asymmetric Keys
**Symmetric keys **- like Caesar Cipher where it uses one (similar/same) key to encrypt and decrypt information.
**Asymmetric keys** - two keys; one used by sender and another used by receiver. Data encrypted with the public key can only be decrypted with the corresponding private key.

**Public keys** are used to encrypt information and be shared; **Private keys** are used to decrypt information.
