# Networking for Ethical Hackers

## What is Networking?

**Networking** is the process of connecting computers and devices so they can communicate and share data. Every website visit, API request, email, and penetration test relies on networking.

---

# Why Networking Matters for Ethical Hackers

Networking knowledge helps you:

- Discover devices on a network
- Identify open services
- Understand attack paths
- Analyze network traffic
- Detect vulnerabilities
- Perform penetration testing

Without networking, ethical hacking becomes guesswork.

---

# 1. OSI Model

## Definition

The **OSI (Open Systems Interconnection)** model is a conceptual framework that explains how data travels from one device to another through seven layers.

| Layer | Name | Examples |
|--------|--------|--------|
| 7 | Application | HTTP, HTTPS, FTP |
| 6 | Presentation | SSL/TLS |
| 5 | Session | NetBIOS |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP |
| 2 | Data Link | Ethernet, MAC |
| 1 | Physical | Cable, Fiber |

### Pentester Focus

- Layer 2 → ARP Spoofing
- Layer 3 → Routing & IP Analysis
- Layer 4 → TCP/UDP Enumeration
- Layer 7 → Web Application Security

---

# 2. TCP/IP Model

## Definition

The TCP/IP model is the practical networking model used by the Internet.

| Layer | Protocols |
|--------|--------|
| Application | HTTP, DNS, FTP |
| Transport | TCP, UDP |
| Internet | IP |
| Network Access | Ethernet |

This model explains how systems communicate across networks.

---

# 3. IP Addressing

## Definition

An IP Address is a unique identifier assigned to a device on a network.

Example:

192.168.1.10

IP addresses allow devices to find and communicate with each other.

---

# 4. IPv4

## Definition

IPv4 is the fourth version of the Internet Protocol and uses 32-bit addresses.

Example:

192.168.1.100

IPv4 supports approximately 4.3 billion addresses.

---

# 5. Public vs Private IP

## Definition

IP addresses can be public or private depending on where they are used.

### Public IP

Accessible from the Internet.

Example:

8.8.8.8

### Private IP

Used inside local networks.

Example:

192.168.1.10

### Private IP Ranges

| Class | Range |
|--------|--------|
| A | 10.0.0.0 - 10.255.255.255 |
| B | 172.16.0.0 - 172.31.255.255 |
| C | 192.168.0.0 - 192.168.255.255 |

Private addresses cannot be directly accessed from the Internet.

---

# 6. Subnetting

## Definition

Subnetting divides a large network into smaller networks to improve organization and security.

### Common CIDR Values

| CIDR | Subnet Mask |
|--------|--------|
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |

Example:

192.168.1.0/24

Host Range:

192.168.1.1 - 192.168.1.254

Subnetting is a fundamental networking skill for security professionals.

---

# 7. TCP

## Definition

Transmission Control Protocol (TCP) is a reliable communication protocol that guarantees data delivery.

### Features

- Reliable
- Ordered Delivery
- Error Checking
- Connection Oriented

TCP is used when data integrity is important.

---

# 8. TCP Three-Way Handshake

## Definition

The TCP handshake establishes a connection between two devices.

### Steps

1. SYN
2. SYN-ACK
3. ACK

After these steps, communication begins.

---

# 9. TCP Flags

## Definition

TCP flags control different stages of a TCP connection.

| Flag | Purpose |
|--------|--------|
| SYN | Start Connection |
| ACK | Acknowledge Data |
| FIN | Close Connection |
| RST | Reset Connection |
| PSH | Push Data |
| URG | Urgent Data |

Packet analysis often involves inspecting these flags.

---

# 10. UDP

## Definition

User Datagram Protocol (UDP) is a fast communication protocol that does not guarantee delivery.

| TCP | UDP |
|--------|--------|
| Reliable | Unreliable |
| Slower | Faster |
| Connection Oriented | Connectionless |

### Examples

- DNS
- VoIP
- Video Streaming

UDP is preferred where speed is more important than reliability.

---

# 11. Ports

## Definition

A port identifies a specific service running on a device.

### Common Ports

| Port | Service |
|--------|--------|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 161 | SNMP |
| 389 | LDAP |
| 443 | HTTPS |
| 445 | SMB |
| 3306 | MySQL |
| 3389 | RDP |
| 5432 | PostgreSQL |
| 6379 | Redis |
| 8080 | HTTP Alternate |

Open ports often reveal attack surfaces.

---

# 12. DNS

## Definition

Domain Name System (DNS) converts domain names into IP addresses.

Example:

google.com → IP Address

### DNS Records

| Record | Purpose |
|--------|--------|
| A | IPv4 Address |
| AAAA | IPv6 Address |
| MX | Mail Server |
| TXT | Text Information |
| CNAME | Alias |
| NS | Name Server |

### Commands

```bash
nslookup google.com
dig google.com

DNS enumeration is a common reconnaissance activity.

---

13. ARP

Definition

Address Resolution Protocol (ARP) maps IP addresses to MAC addresses.

Command

arp -a

Common Attacks

- ARP Spoofing
- Man-in-the-Middle (MITM)

ARP is important in local network attacks.

---

14. DHCP

Definition

Dynamic Host Configuration Protocol (DHCP) automatically assigns network settings.

DHCP Provides:

- IP Address
- Gateway
- DNS Server

DORA Process

Step| Meaning
D| Discover
O| Offer
R| Request
A| Acknowledge

Most devices obtain their configuration through DHCP.

---

15. Routing

Definition

Routing determines the path packets take between networks.

Commands

ip route
route print

Routers use routing tables to make forwarding decisions.

---

16. NAT

Definition

Network Address Translation (NAT) converts private IP addresses into public IP addresses.

Benefits

- Conserves IPv4 addresses
- Hides internal devices
- Adds a security layer

Most home routers use NAT.

---

17. VPN

Definition

A Virtual Private Network (VPN) creates an encrypted tunnel between devices.

VPN Protocols

Protocol| Description
OpenVPN| Secure & Popular
WireGuard| Fast & Modern
IPSec| Enterprise Standard

VPNs protect data over untrusted networks.

---

18. Firewalls

Definition

A Firewall filters incoming and outgoing network traffic based on rules.

Examples

- Windows Firewall
- pfSense
- Cisco ASA

Firewalls help prevent unauthorized access.

---

19. Packet Analysis

Definition

Packet analysis is the process of inspecting network traffic.

Tool

Wireshark

Skills

- Follow TCP Streams
- Analyze Protocols
- Detect Malware Traffic
- Investigate Security Incidents

Packet analysis is a critical skill for pentesters and SOC analysts.

---

20. Nmap

Definition

Nmap is the most widely used network scanning tool.

Host Discovery

nmap 192.168.1.0/24

Service Detection

nmap -sV target.com

OS Detection

nmap -O target.com

Aggressive Scan

nmap -A target.com

Nmap is typically the first tool used during reconnaissance.

---

21. SMB

Definition

Server Message Block (SMB) is used for file and printer sharing.

Port

445

Tools

smbclient
enum4linux

SMB enumeration often reveals users, shares, and permissions.

---

22. Active Directory Basics

Definition

Active Directory (AD) is Microsoft's centralized identity and access management system.

Important Services

Service| Purpose
LDAP| Directory Queries
Kerberos| Authentication
DNS| Name Resolution
SMB| File Sharing

Important Terms

- Domain
- Forest
- Organizational Unit (OU)
- Group Policy

Most enterprise environments rely on Active Directory.

---

23. Wireless Networking

Definition

Wireless networking allows devices to communicate without physical cables.

Wireless Security Standards

Standard| Status
WEP| Broken
WPA| Legacy
WPA2| Common
WPA3| Modern

Tools

- Aircrack-ng
- Kismet
- Wireshark

Wireless security testing is a common penetration testing service.

---

Essential Commands

Linux

ip a
ip route
arp -a
ping google.com
traceroute google.com
netstat -tulpn
ss -tulpn

Windows

ipconfig
arp -a
netstat -ano
route print
tracert google.com

Practice these commands until you can use them without reference.

---

Networking Mastery Checklist

- [ ] OSI Model
- [ ] TCP/IP Model
- [ ] IPv4
- [ ] Public & Private IP
- [ ] Subnetting
- [ ] TCP
- [ ] UDP
- [ ] Ports
- [ ] DNS
- [ ] ARP
- [ ] DHCP
- [ ] Routing
- [ ] NAT
- [ ] VPN
- [ ] Firewalls
- [ ] Wireshark
- [ ] Nmap
- [ ] SMB
- [ ] Active Directory
- [ ] Packet Analysis
- [ ] Network Enumeration

---

Goal

By mastering this README, you should be able to:

- Understand network communication
- Analyze packets using Wireshark
- Scan networks using Nmap
- Enumerate services and hosts
- Prepare for TryHackMe and Hack The Box
- Build a strong foundation for VAPT and Penetration Testing
