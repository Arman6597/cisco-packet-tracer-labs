# Cisco Packet Tracer Labs & Network Projects

A hands-on networking portfolio built with **Cisco Packet Tracer**.

This repository contains **9 structured Packet Tracer labs** and **3 larger network projects** covering Cisco device configuration, VLANs, trunking, Inter-VLAN routing, OSPF, network services, remote administration, segmentation, ACLs, firewalls, DMZ design, and Site-to-Site IPSec VPN.

The repository is divided into:

- **Labs** — focused exercises for individual Cisco networking concepts.
- **Projects** — larger topologies that combine multiple technologies into complete network environments.

---

## Table of Contents

- [Repository Structure](#repository-structure)
- [Skills Demonstrated](#skills-demonstrated)
- [Labs](#labs)
  - [01 - Network Fundamentals](#01---network-fundamentals)
  - [03 - VLANs and Trunking](#03---vlans-and-trunking)
  - [04 - Inter-VLAN Routing](#04---inter-vlan-routing)
- [Projects](#projects)
  - [Enterprise HQ-Branch Network](#enterprise-hq-branch-network)
  - [Secure Enterprise Network with DMZ](#secure-enterprise-network-with-dmz)
  - [Multi-Router Network](#multi-router-network)
- [Verification and Troubleshooting](#verification-and-troubleshooting)
- [File Types](#file-types)
- [How to Open the Files](#how-to-open-the-files)
- [Security Notes](#security-notes)
- [Future Improvements](#future-improvements)

---

## Repository Structure

```text
cisco-packet-tracer-labs/
│
├── cisco-packet-labs/01-network-fundamentals/
│   ├── configure-initial-router-settings.pka
│   ├── configure-initial-switch-settings.pka
│   └── implement-basic-connectivity.pka
│
├── cisco-packet-labs/03-vlans-and-trunking/
│   ├── 3.3.12-vlan-configuration.pka
│   ├── 3.4.5-configure-trunks.pka
│   ├── 3.4.6-configure-vlans-and-trunking-physical-mode.pka
│   ├── 3.5.5-configure-dtp.pka
│   └── 3.6.1-implement-vlans-and-trunking.pka
│
├── cisco-packet-labs/04-inter-vlan-routing/
│   └── 4.5.1-inter-vlan-routing-challenge.pka
│
├── projects/
│   ├── enterprise-hq-branch-network.pkt
│   ├── multi-router-network.pkt
│   └── secure-enterprise-network-with-dmz.pkt
│
└── README.md
```

---

## Skills Demonstrated

### Routing and Switching

- Cisco IOS CLI
- Basic router and switch configuration
- IPv4 addressing and default gateways
- VLAN creation and access-port assignment
- IEEE 802.1Q trunking
- Dynamic Trunking Protocol (DTP)
- Inter-VLAN routing
- Multi-router connectivity
- OSPF dynamic routing

### Network Services

- DHCP
- DNS
- HTTP / Web services
- Email services
- Client-to-server communication

### Network Security

- SSH remote administration
- Access Control Lists (ACLs)
- Firewall-based segmentation
- DMZ architecture
- Separation of trusted and untrusted networks
- Site-to-Site IPSec VPN

### Verification and Troubleshooting Skills

- Interface-state verification
- VLAN and trunk verification
- Routing-table analysis
- ACL verification
- IPSec security-association verification
- ICMP connectivity testing
- DHCP addressing checks
- DNS resolution testing
- Application-layer service testing

---

## Labs

The `.pka` files are focused Packet Tracer activities. They are organized by topic to show progression from basic Cisco device configuration to switching and Inter-VLAN routing.

### 01 - Network Fundamentals

Directory:

```text
cisco-packet-labs/01-network-fundamentals/
```

#### Configure Initial Router Settings

File:

```text
configure-initial-router-settings.pka
```

Focus:

- Cisco IOS CLI navigation
- initial router configuration
- interface configuration
- configuration verification
- saving device configuration

Typical commands used during basic router configuration include:

```bash
enable
configure terminal
show running-config
show ip interface brief
copy running-config startup-config
```

#### Configure Initial Switch Settings

File:

```text
configure-initial-switch-settings.pka
```

Focus:

- initial switch configuration
- interface-state verification
- switch management basics
- configuration persistence

Useful verification commands include:

```bash
show running-config
show interfaces status
show ip interface brief
```

#### Implement Basic Connectivity

File:

```text
implement-basic-connectivity.pka
```

Focus:

- host addressing
- default gateways
- Layer 2 connectivity
- Layer 3 connectivity
- end-to-end testing
- basic troubleshooting

A basic reachability test is:

```bash
ping <destination-ip>
```

---

### 03 - VLANs and Trunking

Directory:

```text
cisco-packet-labs/03-vlans-and-trunking/
```

This section focuses on Layer 2 segmentation and communication between switches.

#### 3.3.12 - VLAN Configuration

File:

```text
3.3.12-vlan-configuration.pka
```

Focus:

- creating VLANs
- naming VLANs
- configuring access ports
- assigning interfaces to VLANs
- verifying VLAN membership

Example:

```bash
configure terminal

vlan 10
 name USERS

interface fa0/1
 switchport mode access
 switchport access vlan 10
```

Verification:

```bash
show vlan brief
```

#### 3.4.5 - Configure Trunks

File:

```text
3.4.5-configure-trunks.pka
```

Focus:

- IEEE 802.1Q trunking
- trunk-port configuration
- carrying multiple VLANs between switches
- native VLAN concepts
- trunk verification

Example:

```bash
interface g0/1
 switchport mode trunk
```

Verification:

```bash
show interfaces trunk
```

#### 3.4.6 - Configure VLANs and Trunking - Physical Mode

File:

```text
3.4.6-configure-vlans-and-trunking-physical-mode.pka
```

Focus:

- Packet Tracer Physical Mode
- VLAN configuration
- access-port assignment
- trunk configuration
- physical topology awareness
- connectivity verification

#### 3.5.5 - Configure DTP

File:

```text
3.5.5-configure-dtp.pka
```

Focus:

- Dynamic Trunking Protocol
- trunk negotiation
- `dynamic auto`
- `dynamic desirable`
- static trunk configuration
- verification of switchport behavior

Example DTP-related commands:

```bash
switchport mode dynamic auto
switchport mode dynamic desirable
switchport mode trunk
```

Verification:

```bash
show interfaces trunk
show interfaces switchport
```

#### 3.6.1 - Implement VLANs and Trunking

File:

```text
3.6.1-implement-vlans-and-trunking.pka
```

Focus:

- creating multiple VLANs
- assigning access ports
- configuring trunk links
- validating VLAN membership
- validating trunk operation
- troubleshooting Layer 2 segmentation

---

### 04 - Inter-VLAN Routing

Directory:

```text
cisco-packet-labs/04-inter-vlan-routing/
```

#### 4.5.1 - Inter-VLAN Routing Challenge

File:

```text
4.5.1-inter-vlan-routing-challenge.pka
```

Focus:

- communication between separate VLANs
- Layer 3 gateway configuration
- Inter-VLAN routing
- routing verification
- troubleshooting cross-VLAN connectivity

Useful verification commands include:

```bash
show vlan brief
show interfaces trunk
show ip interface brief
show ip route
ping <destination-ip>
```

---

## Projects

The `.pkt` files are larger Packet Tracer projects that combine multiple technologies into complete network environments.

### Enterprise HQ-Branch Network

File:

```text
projects/enterprise-hq-branch-network.pkt
```

#### HQ-Branch Project Overview

This project simulates a corporate network with two locations:

- **Headquarters (HQ)**
- **Branch Office**

The design combines network segmentation, dynamic routing, network services, secure remote management, access control, and encrypted site-to-site communication.

#### VLAN and Addressing Design

##### Headquarters

| VLAN | Name | Network | Purpose |
|---|---|---|---|
| 2 | USERS | `192.168.10.0/24` | User workstations |
| 3 | SERVERS | `192.168.11.0/24` | Internal servers |

HQ USERS default gateway:

```text
192.168.10.1
```

##### Branch

| VLAN | Name | Network | Purpose |
|---|---|---|---|
| 20 | USERS | `192.168.20.0/24` | Branch workstations |
| 21 | SERVERS | `192.168.21.0/24` | Branch servers |

Branch USERS default gateway:

```text
192.168.20.1
```

VLAN membership can be verified with:

```bash
show vlan brief
```

#### DHCP

Client devices receive IP configuration automatically through DHCP.

Typical client check:

```bash
ipconfig
```

Expected user networks:

```text
HQ USERS     -> 192.168.10.0/24
Branch USERS -> 192.168.20.0/24
```

#### OSPF Dynamic Routing

OSPF is used for dynamic route exchange.

On Cisco IOS routers, routing information can be checked with:

```bash
show ip route
```

On Cisco ASA devices, the routing table can be checked with:

```bash
show route
```

OSPF-learned routes are identified by the `O` route code.

#### Site-to-Site IPSec VPN

A Site-to-Site IPSec VPN protects traffic between HQ and Branch.

IKE / ISAKMP status:

```bash
show crypto isakmp sa
```

IPSec statistics:

```bash
show crypto ipsec sa
```

Useful counters include:

```text
pkts encaps
pkts decaps
```

When these counters increase during inter-site traffic, packets are being processed by the IPSec tunnel.

#### HQ-to-Branch Connectivity

Example tests:

From HQ to Branch:

```bash
ping 192.168.20.100
```

From Branch to HQ:

```bash
ping 192.168.10.100
```

These tests validate end-to-end reachability between the two user networks.

#### DNS and Web Services

Example HQ web server:

```text
192.168.11.10
```

Example DNS records used in the project:

```text
hq-web.com -> 192.168.11.10
mail.com   -> 192.168.11.12
```

Example DNS tests:

```bash
ping hq-web.com
ping mail.com
```

The HQ web service can be tested directly by IP address or by its configured DNS name.

#### Email Service

The project includes an email server at:

```text
192.168.11.12
```

The configured mail domain is:

```text
mail.com
```

Email communication between HQ and Branch can be used as an application-layer test of:

- DNS resolution
- routing
- server reachability
- inter-site connectivity

#### SSH Remote Management

Internal network devices can be administered through SSH.

Example HQ switch connection:

```bash
ssh -l admin 192.168.10.2
```

Example Branch switch connection:

```bash
ssh -l admin 192.168.20.2
```

Passwords and other credentials are intentionally not documented in this public README.

#### ACL-Based External Access Control

The project applies access-control rules so that selected HQ resources can be reached from the external side while Branch networks remain restricted.

ACLs can be inspected with:

```bash
show access-lists
```

Match counters help confirm that ACL entries are actually processing traffic.

#### Technologies Used

- VLANs
- OSPF
- DHCP
- DNS
- HTTP
- Email
- SSH
- ACLs
- Cisco ASA
- Site-to-Site IPSec VPN
- Network segmentation

---

### Secure Enterprise Network with DMZ

File:

```text
projects/secure-enterprise-network-with-dmz.pkt
```

#### DMZ Project Overview

This project demonstrates a security-focused enterprise topology divided into three logical security zones:

- **Private Network**
- **DMZ Network**
- **External Network**

A Cisco ASA firewall separates these zones.

#### Private Network

The private side contains internal and administrative endpoints, including:

- administrator workstation
- employee workstations
- HR devices
- management devices
- security workstation
- wireless clients
- wireless access points

This zone represents the internal enterprise LAN.

#### DMZ Network

The DMZ contains systems that are separated from the private user network, including:

- Web Server
- Email Server
- DNS Server
- DevOps workstation

The purpose of the DMZ is to isolate service systems from the internal user network and support controlled communication between zones.

#### External Network

The external zone represents systems outside the trusted enterprise LAN.

It can be used to test:

- external reachability
- permitted services
- blocked traffic
- firewall behavior
- separation between trust zones

#### Security Architecture

Conceptually, the design is:

```text
                    +----------------+
                    |  Private LAN   |
                    +--------+-------+
                             |
                         +---+---+
                         |  ASA  |
                         +---+---+
                            / \
                           /   \
                  +-------+     +--------+
                  |                      |
             +----+-----+          +-----+------+
             |   DMZ    |          |  External  |
             +----------+          +------------+
```

The topology is designed so that different traffic flows can be governed by different security policies rather than placing all systems in a single trust zone.

#### Concepts Demonstrated

- Cisco ASA firewall
- network segmentation
- trust zones
- DMZ architecture
- private LAN isolation
- external-network separation
- DNS services
- email services
- web services
- wired and wireless clients

---

### Multi-Router Network

File:

```text
projects/multi-router-network.pkt
```

#### Multi-Router Project Overview

This project contains two LAN environments connected through a multi-router topology.

The topology includes:

- multiple Cisco routers
- switches at the LAN edges
- end-user PCs
- servers
- several routed links between routers

The routed core provides more than one possible physical path through parts of the topology, making the project useful for routing and path-verification practice.

#### Main Learning Objectives

- designing a multi-router topology
- addressing routed links
- understanding routing tables
- validating LAN-to-LAN communication
- verifying server reachability
- troubleshooting hop-by-hop connectivity

#### Verification

Interface state:

```bash
show ip interface brief
```

Routing table:

```bash
show ip route
```

End-to-end reachability:

```bash
ping <remote-host>
```

The exact routing configuration is contained in the `.pkt` project file.

---

## Verification and Troubleshooting

The following commands are useful across the labs and projects.

| Purpose | Command |
|---|---|
| Check router interfaces | `show ip interface brief` |
| Check VLANs and access ports | `show vlan brief` |
| Check trunk links | `show interfaces trunk` |
| Check switchport mode | `show interfaces switchport` |
| Check IOS routing table | `show ip route` |
| Check ASA routing table | `show route` |
| Check ACLs and counters | `show access-lists` |
| Check IKE / ISAKMP SA | `show crypto isakmp sa` |
| Check IPSec counters | `show crypto ipsec sa` |
| Check PC addressing | `ipconfig` |
| Test IP reachability | `ping <destination>` |
| Test DNS resolution | `ping <hostname>` |

Troubleshooting should be performed layer by layer:

1. Verify physical/interface state.
2. Verify IP addressing and default gateways.
3. Verify VLAN membership and trunking where applicable.
4. Verify routing tables.
5. Verify ACL or firewall policy.
6. Verify DNS and application-layer services.
7. For VPN traffic, verify IKE/IPSec state and packet counters.

---

## File Types

### `.pka`

A Cisco Packet Tracer Activity file.

A `.pka` may contain:

- a predefined topology
- instructions
- activity/assessment logic
- expected configuration criteria

The `.pka` files in this repository are organized as learning labs.

### `.pkt`

A Cisco Packet Tracer network file.

The `.pkt` files in the `projects/` directory contain the larger network topologies used as portfolio projects.

---

## How to Open the Files

1. Install **Cisco Packet Tracer**.
2. Clone or download this repository.
3. Open Cisco Packet Tracer.
4. Select **File -> Open**.
5. Choose the required `.pka` or `.pkt` file.

Clone the repository:

```bash
git clone https://github.com/Arman6597/cisco-packet-tracer-labs.git
```

Enter the repository:

```bash
cd cisco-packet-tracer-labs
```

---

## Security Notes

This repository is intended for educational and portfolio purposes.

Public repositories should not contain real secrets. Before publishing network configurations, verify that they do not contain:

- production passwords
- private keys
- API credentials
- real VPN pre-shared keys
- other sensitive authentication material

The credentials used inside Packet Tracer lab environments should be treated as lab-only credentials and should not be reused in real systems.

---

## Future Improvements

Possible improvements that would make the repository easier to review:

- add topology screenshots for all three projects
- create a dedicated README for each large project
- add IP-addressing tables for each project
- document router and firewall interfaces
- add selected connectivity-test results
- document important troubleshooting cases
- add additional routing and switching labs as they are completed

---

## Portfolio Purpose

This repository documents my practical networking work with Cisco Packet Tracer.

The goal is to demonstrate both focused configuration skills and the ability to combine multiple networking technologies into larger designs.

Key areas represented in the current repository include:

- routing and switching
- VLAN segmentation
- enterprise network services
- dynamic routing
- secure remote management
- firewall and ACL policy
- DMZ design
- encrypted site-to-site communication
- network verification and troubleshooting

---

## Author

**Arman Stepanyan**

GitHub: `Arman6597`

---

### Disclaimer

Cisco and Cisco Packet Tracer are trademarks of Cisco Systems, Inc.

This repository is an educational portfolio and is not affiliated with or endorsed by Cisco.
