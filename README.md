# Redundant-OSPF-HSRP-Infrastructure

![Complete Network Topology](./Images/TOPOLOGY.png)

A simulated enterprise LAN/WAN built in Cisco Packet Tracer, demonstrating routing, switching, redundancy, and security fundamentals.

## Topology Overview

- **3x Access Switches** (2960-24TT) – SW1, SW2, SW3, each serving one department VLAN
- **2x Distribution Layer 3 Switches** (3560-24PS) – L3-SW1, L3-SW2, running redundant gateways
- **1x Core Router** (R1) – routes between the internal network and the ISP
- **1x ISP Router** – simulates the internet edge
- **6x PCs** – two per department (IT, HR, Sales), mixed static/DHCP

## Key Features Implemented

- **VLAN Segmentation** – IT (VLAN 10), HR (VLAN 20), Sales (VLAN 30)
- **Inter-VLAN Routing** via SVIs on two Layer 3 switches
- **First-Hop Redundancy** – HSRP (active/standby) across L3-SW1 and L3-SW2, with priorities tuned so each switch is active for different VLANs (load sharing)
- **Spanning Tree Tuning** – per-VLAN root priority aligned with HSRP active paths
- **Dynamic Routing** – OSPF between distribution switches, core router, and ISP
- **DHCP Services** – centralized DHCP pools for IT, HR, and Sales, relayed via `ip helper-address`
- **Security ACL** – extended ACL blocking direct traffic between HR (VLAN 20) and Sales (VLAN 30)
- **Internet Edge Simulation** – static default routing between the core router and ISP router

## Skills Demonstrated

`Switching` · `VLANs` · `Inter-VLAN Routing` · `OSPF` · `HSRP` · `DHCP` · `Access Control Lists` · `Network Redundancy` · `Cisco IOS Configuration`

---
*Built and documented as part of a personal network engineering practice project.*
