# Networking-notes-
# Networking for Ethical Hackers

## Why Networking Matters

Without networking knowledge you cannot:

- Discover hosts
- Enumerate services
- Understand attack paths
- Analyze packets
- Exploit vulnerabilities
- Perform internal penetration testing

Networking is one of the most important skills for every ethical hacker.

---

# 1. OSI Model

| Layer | Name | Examples |
|---------|---------|---------|
| 7 | Application | HTTP, HTTPS, FTP |
| 6 | Presentation | SSL/TLS |
| 5 | Session | NetBIOS |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP |
| 2 | Data Link | MAC Address |
| 1 | Physical | Cable, Fiber |

### Pentester Focus

- Layer 2 Attacks
- Layer 3 Routing
- Layer 4 TCP/UDP
- Layer 7 Web Applications

---

# 2. TCP/IP Model

| Layer | Protocols |
|---------|---------|
| Application | HTTP, DNS, FTP |
| Transport | TCP, UDP |
| Internet | IP |
| Network Access | Ethernet |

---

# 3. IP Addressing

## IPv4

Example:

192.168.1.10

Structure:

Network Portion + Host Portion

---

## Private IP Ranges

### Class A

10.0.0.0 - 10.255.255.255

### Class B

172.16.0.0 - 172.31.255.255

### Class C

192.168.0.0 - 192.168.255.255

---

# 4. Public vs Private IP

## Public

Accessible from internet

Example:

8.8.8.8

## Private

Used inside local networks

Example:

192.168.1.100

---

# 5. Subnetting

## Common CIDRs

| CIDR | Mask |
|---------|---------|
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |

### Example

192.168.1.0/24

Hosts:

192.168.1.1 - 192.168.1.254

---

# 6. TCP Handshake

## Three-Way Handshake

1. SYN
2. SYN-ACK
3. ACK

Connection Established

---

# 7. TCP Flags

| Flag | Purpose |
|---------|---------|
| SYN | Start Connection |
| ACK | Acknowledge |
| FIN | Close Connection |
| RST | Reset |
| PSH | Push Data |
| URG | Urgent Data |

---

# 8. UDP

Characteristics:

- Connectionless
- Fast
- No delivery guarantee

Examples:

- DNS
- VoIP
- Streaming

---

# 9. Ports

## Common Ports

| Port | Service |
|---------|---------|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 67/68 | DHCP |
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

---

# 10. DNS

Purpose:

Converts domain names to IP addresses

Example:

google.com → 142.x.x.x

Records:

- A
- AAAA
- MX
- TXT
- CNAME
- NS

Tools:

```bash
nslookup google.com

dig google.com
```

---

# 11. ARP

Maps:

IP Address → MAC Address

Command:

```bash
arp -a
```

Attack:

- ARP Spoofing
- MITM

---

# 12. DHCP

Automatically assigns:

- IP Address
- Gateway
- DNS

Process:

DORA

1. Discover
2. Offer
3. Request
4. Acknowledge

---

# 13. Routing

Command:

```bash
route print

ip route
```

Purpose:

Determines packet path

---

# 14. NAT

Network Address Translation

Converts:

Private IP → Public IP

Used in routers.

---

# 15. VPN

Benefits:

- Encryption
- Privacy
- Secure Remote Access

Protocols:

- OpenVPN
- WireGuard
- IPSec

---

# 16. Firewalls

Purpose:

Filter network traffic

Examples:

- Windows Firewall
- pfSense
- Cisco ASA

---

# 17. Packet Analysis

Tool:

Wireshark

Skills:

- Follow TCP Stream
- Analyze DNS
- Detect Malware Traffic
- Extract Credentials

---

# 18. Nmap

Host Discovery

```bash
nmap 192.168.1.0/24
```

Service Detection

```bash
nmap -sV target.com
```

OS Detection

```bash
nmap -O target.com
```

Aggressive Scan

```bash
nmap -A target.com
```

---

# 19. SMB Enumeration

Port:

445

Tools:

```bash
smbclient

enum4linux
```

Common Findings:

- Shared Folders
- Users
- Password Policies

---

# 20. Active Directory Basics

Important Services:

- LDAP
- Kerberos
- SMB
- DNS

Important Terms:

- Domain
- Forest
- OU
- Group Policy

---

# 21. Wireless Networking

Encryption:

- WEP (Broken)
- WPA
- WPA2
- WPA3

Tools:

- Aircrack-ng
- Kismet
- Wireshark

---

# 22. Pentester Workflow

1. Network Discovery
2. Port Scanning
3. Service Enumeration
4. Vulnerability Identification
5. Exploitation
6. Privilege Escalation
7. Post Exploitation
8. Reporting

---

# Essential Commands

## Linux

```bash
ip a

ip route

netstat -tulpn

ss -tulpn

arp -a

ping google.com

traceroute google.com
```

## Windows

```powershell
ipconfig

arp -a

netstat -ano

route print

tracert google.com
``` 

---

# Labs To Practice

- Cisco Packet Tracer
- GNS3
- EVE-NG
- TryHackMe
- Hack The Box
- OverTheWire

---

# Networking Mastery Checklist

- [ ] OSI Model
- [ ] TCP/IP
- [ ] IPv4
- [ ] Subnetting
- [ ] TCP vs UDP
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
- [ ] Active Directory Basics
- [ ] Packet Analysis
- [ ] Network Enumeratio
