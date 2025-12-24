# Enterprise Network Design for Radeon Company Ltd.

A Cisco Packet Tracer–based enterprise campus network design for Radeon Company Ltd. featuring a segmented VLAN architecture with a centralized core, wired + wireless access, dynamic IP addressing, and secure remote management. [file:1][file:2]

## Project overview
The network is designed for a small-to-medium enterprise campus and supports multiple departments through VLAN segmentation to improve performance, security, and manageability. [file:2]  
The solution was simulated and tested in Cisco Packet Tracer using connectivity checks, DHCP validation, SSH access tests, and port-security tests. [file:1]

## Problem & goals
Radeon Company Ltd. needs a scalable, secure, and efficient network infrastructure to support multi-department operations (and future expansion), while ensuring smooth communication and controlled access. [file:1]  
Goals include scalability, secure segmentation, inter-VLAN routing, dynamic addressing (DHCP), wireless coverage, and secure remote access. [file:1][file:2]

## Scope (high level)
- Campus segmentation across **12 departments/zones** with about **74 connected devices** in the presented design. [file:2]
- Department-based VLANs with an IP addressing scheme per VLAN/subnet. [file:2]
- Centralized inter-VLAN routing controlled through the core. [file:2]
- Wireless deployment with departmental SSIDs and an isolated guest Wi‑Fi/VLAN. [file:2]
- Centralized server/services design including dedicated DHCP services. [file:2]

## VLANs & IP addressing (from the design)
The design assigns each department a unique VLAN ID and subnet, for example: VLAN 10 (Management) 192.168.10.0/26, VLAN 20 (Research) 192.168.10.64/26, VLAN 30 (HR) 192.168.10.128/26, VLAN 40 (Marketing) 192.168.10.192/26, VLAN 50 (Accounting) 192.168.11.0/26, VLAN 60 (Finance) 192.168.11.64/26, VLAN 70 (Logistics Store) 192.168.11.128/26, VLAN 80 (Customer Care) 192.168.11.192/26, VLAN 90 (Guest) 192.168.12.0/26, VLAN 100 (Admin) 192.168.12.64/26, VLAN 110 (IT) 192.168.12.128/26, VLAN 120 (Server Room) 192.168.12.192/26, and a services/server DHCP VLAN (e.g., VLAN 150) 192.168.100.0/24. [file:2]

## Routing protocols (used all three)
This project uses three routing protocols to match different routing needs in the network:
- **OSPF**: Configured for dynamic route advertisement across the network (as included in the project approach). [file:1]
- **EIGRP**: Used for internal routing inside the campus network for efficient convergence and routing between internal segments. [file:2]
- **BGP**: Used for external connectivity/border routing to reach outside networks (internet/edge/remote connections). [file:2]

## Core services & security
- DHCP is implemented to provide dynamic IP allocation across departments/VLANs, supported by dedicated DHCP servers and centralized service design. [file:1][file:2]
- SSH is configured on routers for secure remote management. [file:1]
- Switch port security is enabled using sticky MAC addressing with shutdown violation mode to block unauthorized devices. [file:1]
- Guest access is isolated in a dedicated Guest VLAN, and inter-VLAN traffic control is enforced via core routing and ACL concepts described in the design. [file:2]

## Testing (Packet Tracer)
Validation steps include:
- Ping/connectivity tests between required VLANs and across the core. [file:1]
- DHCP assignment tests to confirm correct addressing per VLAN. [file:1]
- SSH remote access tests to confirm secure management connectivity. [file:1]
- Port-security tests to confirm unauthorized devices are blocked. [file:1]

## Cost summary (USD)
Total project investment: **$276,450** including hardware, cabling infrastructure, security/surveillance, and annual maintenance. [file:3]  
Key hardware costs include access switches ($45,000), servers ($42,000), PCs ($32,400), and core switches ($20,000), with structured cabling and fiber backbone also included. [file:3]

## Included documents
- `Presentation.pdf` — Full campus design details (departments, VLAN plan, routing, services, wireless, security). [file:2]
- `AIU-Research-Poster-Template-A1-Portrait.pptx` — Poster summary: problem, goals, approach, technologies, and results. [file:1]
- `network_cost_report (2).pdf` — Enterprise network infrastructure cost analysis and breakdown. [file:3]

## Tools
- Cisco Packet Tracer (simulation/testing). [file:1]

## Credits
Course poster includes supervisor and project team details for “Network Design for Radeon Company Ltd.” [file:1]
