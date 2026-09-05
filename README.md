# VLSM-Subnetting-and-IP-Addresses-for-university-departments-using-Cisco-Packet-Tracer
Designed a complete VLSM subnetting scheme for 8 departments within a 192.168.0.0/22 block (1,024 addresses) ,8 optimized subnets with zero overlap. Reserved 176 addresses for future growth, eliminating wastage compared to fixed-length subnetting, Reduced address wastage by 55% compared to a fixed /24 approach
#  University Network Design — IP Addressing & Subnet Management

> A complete VLSM-based network design and simulation for a mid-sized university,
> built as part of the Networking course at the University of Management & Technology (UMT).

Project Overview

This project presents a fully planned and simulated campus network for a university
with 8 departments, using Variable Length Subnet Masking (VLSM) to efficiently
allocate IP addresses from a single 192.168.0.0/22 block (1,024 addresses).

The network was designed, documented, and simulated end-to-end — from subnetting
calculations to live ping verification between departments in Cisco Packet Tracer 9.0.

Departments Covered

| # | Department | Subnet | Prefix | Usable Hosts |

| 1 | Computer Science (CS) | 192.168.0.0 | /24 | 254 |
| 2 | Hostel | 192.168.1.0 | /24 | 254 |
| 3 | Software Engineering (SE) | 192.168.2.0 | /25 | 126 |
| 4 | Faculty Block | 192.168.2.128 | /26 | 62 |
| 5 | Informatics Systems (INFS) | 192.168.2.192 | /26 | 62 |
| 6 | Civil Engineering | 192.168.3.0 | /27 | 30 |
| 7 | Admin Office | 192.168.3.32 | /27 | 30 |
| 8 | Library | 192.168.3.64 | /28 | 14 |
| — | Reserved (Future Growth) | 192.168.3.80–3.255 | — | 176 addr |



 Technologies & Protocols

- **IPv4 Addressing** — RFC 1918 private address space
- **VLSM** — Variable Length Subnet Masking for efficient allocation
- **CIDR Notation** — /24 through /28 prefix lengths
- **IEEE 802.1Q** — VLAN trunking between switches and router
- **Inter-VLAN Routing** — Router-on-a-Stick via subinterfaces
- **Cisco IOS CLI** — Router and switch configuration
- **ICMP** — Connectivity verification via ping


Tools Used

| Tool | Purpose |
|---|---|
| Cisco Packet Tracer 9.0 | Network simulation & topology |
| Cisco 2911 Router | Central inter-VLAN routing |
| Cisco 2960-24TT Switch ×8 | Per-department Layer 2 switching |
| Cisco IOS CLI | Device configuration |
| Python (ReportLab) | PDF report generation |



Repository Structure
Results

| Metric | Value |
|---|---|
| Total IP block | 192.168.0.0/22 (1,024 addresses) |
| Addresses allocated | 848 (82.8%) |
| Addresses reserved | 176 (17.2%) |
| Subnets created | 8 |
| Address utilization | 82.8% |
| Wastage vs fixed /24 | ~55% reduction |
| Inter-dept connectivity |  Verified via ping |

Network Topology

PC_CS ── SW_CS ──┐
PC_Hostel ── SW_Hostel ──┤
PC_SE ── SW_SE ──┤
PC_Faculty ── SW_Faculty ──┼── Router2 (2911) — Gi0/0 subinterfaces
PC_INFS ── SW_INFS ──┤ (802.1Q VLANs 10–80)
PC_Civil ── SW_Civil ──┤
PC_Admin ── SW_Admin ──┤
PC_Library ── SW_Library ──┘
Star topology** — all switches connect to a central Cisco 2911 router via
GigabitEthernet subinterfaces using 802.1Q VLAN encapsulation.


How to Run the Simulation

1. Install [Cisco Packet Tracer 9.0](https://www.netacad.com/courses/packet-tracer)
2. Open `simulation/University_Network.pkt`
3. If configs are missing, paste from `configs/Cisco_PT_Configs.txt` into each device CLI
4. Verify connectivity:
   - Click any PC → Desktop → Command Prompt
   - `ping <gateway>` — test local subnet
   - `ping <cross-dept IP>` — test inter-VLAN routing

Report Includes

- IP addressing fundamentals & binary conversion
- CIDR reference table (/22 through /30)
- Full VLSM calculations per department
- Master subnetting table
- Address space utilization diagrams
- Growth & scalability planning
- VLSM vs Fixed-Length subnetting comparison
- Challenges & mitigations


Author
Zainab Imran
School of Systems and Technology
University of Management & Technology (UMT)

License
This project is submitted for academic purposes at UMT.
Feel free to reference the methodology for educational use.



