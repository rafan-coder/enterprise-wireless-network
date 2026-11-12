\# Enterprise Wireless Network with Guest Wi-Fi



\## Project Overview

This project demonstrates an enterprise wireless network designed using Cisco Packet Tracer. It provides separate wireless networks for employees and guests using VLAN segmentation, router-on-a-stick inter-VLAN routing, and Access Control Lists (ACLs) for network isolation.



\## Network Topology

The network consists of:

\- 1 Cisco router (WIFI-R1)

\- 1 Cisco 2960 switch (WIFI-SW1)

\- 2 wireless access points (EMPLOYEE-AP and GUEST-AP)

\- 2 employee laptops

\- 2 guest laptops



\## Technologies and Concepts

\- Cisco Packet Tracer

\- VLAN configuration

\- VLAN trunking (802.1Q)

\- Router-on-a-stick

\- Wireless SSID configuration

\- WPA2-PSK security

\- IPv4 addressing

\- Extended Access Control Lists (ACLs)

\- Network segmentation and isolation



\## IP Addressing Plan



| Network | VLAN | Subnet | Default Gateway |

|---|---:|---|---|

| Employee | 10 | 192.168.10.0/24 | 192.168.10.1 |

| Guest | 20 | 192.168.20.0/24 | 192.168.20.1 |



\### Wireless Networks

\- Employee SSID: `EMPLOYEE\_WIFI`

\- Guest SSID: `GUEST\_WIFI`

\- Security: WPA2-PSK



\## VLAN Configuration

\- VLAN 10 – EMPLOYEE

\- VLAN 20 – GUEST

\- Switch access ports assigned to the appropriate VLANs.

\- Trunk link configured between the switch and router using 802.1Q.

\- VLANs 10 and 20 allowed on the trunk.



\## Inter-VLAN Routing

Router-on-a-stick was configured using subinterfaces:

\- GigabitEthernet0/0.10 – 192.168.10.1/24

\- GigabitEthernet0/0.20 – 192.168.20.1/24



\## Network Security

Extended ACLs were configured to prevent communication between employee and guest networks.



\- Guest devices cannot access the employee network.

\- Employee devices cannot access the guest network.

\- Devices within the same VLAN can communicate.

\- Both networks can reach their respective default gateways.



\## Testing and Verification

The following tests were completed successfully:

\- Employee-to-employee connectivity

\- Guest-to-guest connectivity

\- Employee-to-guest communication blocked

\- Guest-to-employee communication blocked

\- Employee gateway connectivity

\- Guest gateway connectivity



\## Project Screenshots



\### 1. Network Topology

!\[Network Topology](screenshots/topology.png)



\### 2. VLAN and Trunk Configuration

!\[VLAN and Trunk](screenshots/vlan-trunk.png)



\### 3. ACL Security Configuration

!\[ACL Security](screenshots/acl-security.png)



\## Project Outcome

Successfully implemented a segmented enterprise wireless network with separate employee and guest VLANs, inter-VLAN routing, WPA2 wireless security, and ACL-based network isolation using Cisco Packet Tracer.

