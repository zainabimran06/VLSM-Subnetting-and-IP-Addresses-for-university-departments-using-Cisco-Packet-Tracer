# VLSM-Subnetting-and-IP-Addresses-for-university-departments-using-Cisco-Packet-Tracer
Designed a complete VLSM subnetting scheme for 8 departments within a 192.168.0.0/22 block (1,024 addresses) ,8 optimized subnets with zero overlap. Reserved 176 addresses for future growth, eliminating wastage compared to fixed-length subnetting, Reduced address wastage by 55% compared to a fixed /24 approach
#  University Network Design — IP Addressing & Subnet Management

> A complete VLSM-based network design and simulation for a mid-sized university,
> built as part of the Networking course at the University of Management & Technology (UMT).

---

## Project Overview

This project presents a fully planned and simulated campus network for a university
with 8 departments, using Variable Length Subnet Masking (VLSM) to efficiently
allocate IP addresses from a single 192.168.0.0/22 block (1,024 addresses).

The network was designed, documented, and simulated end-to-end — from subnetting
calculations to live ping verification between departments in Cisco Packet Tracer 9.0.

---

## Departments Covered

| # | Department | Subnet | Prefix | Usable Hosts |
|---|---|---|---|---|
| 1 | Computer Science (CS) | 192.168.0.0 | /24 | 254 |
| 2 | Hostel | 192.168.1.0 | /24 | 254 |
| 3 | Software Engineering (SE) | 192.168.2.0 | /25 | 126 |
| 4 | Faculty Block | 192.168.2.128 | /26 | 62 |
| 5 | Informatics Systems (INFS) | 192.168.2.192 | /26 | 62 |
| 6 | Civil Engineering | 192.168.3.0 | /27 | 30 |
| 7 | Admin Office | 192.168.3.32 | /27 | 30 |
| 8 | Library | 192.168.3.64 | /28 | 14 |
| — | Reserved (Future Growth) | 192.168.3.80–3.255 | — | 176 addr |

---

## Technologies & Protocols

- **IPv4 Addressing** — RFC 1918 private address space
- **VLSM** — Variable Length Subnet Masking for efficient allocation
- **CIDR Notation** — /24 through /28 prefix lengths
- **IEEE 802.1Q** — VLAN trunking between switches and router
- **Inter-VLAN Routing** — Router-on-a-Stick via subinterfaces
- **Cisco IOS CLI** — Router and switch configuration
- **ICMP** — Connectivity verification via ping

---

## Tools Used

| Tool | Purpose |
|---|---|
| Cisco Packet Tracer 9.0 | Network simulation & topology |
| Cisco 2911 Router | Central inter-VLAN routing |
| Cisco 2960-24TT Switch ×8 | Per-department Layer 2 switching |
| Cisco IOS CLI | Device configuration |
| Python (ReportLab) | PDF report generation |

---

## Repository Structure
##  Results

| Metric | Value |
|---|---|
| Total IP block | 192.168.0.0/22 (1,024 addresses) |
| Addresses allocated | 848 (82.8%) |
| Addresses reserved | 176 (17.2%) |
| Subnets created | 8 |
| Address utilization | 82.8% |
| Wastage vs fixed /24 | ~55% reduction |
| Inter-dept connectivity |  Verified via ping |




