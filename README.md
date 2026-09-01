# 🏢 Enterprise Campus Network Architecture & Simulation

## Overview

This project details the comprehensive design and simulation of a scalable, reliable, and cost-effective Local Area Network (LAN) infrastructure intended for a 20-25 year deployment lifespan at the University of Moratuwa[cite: 4]. 

The design is split into two primary phases: a robust **Backbone Network** interconnecting all university faculties via the Center for Information Technology Services (CITeS), and a detailed **Internal LAN Structure** specifically tailored for the Electronic and Telecommunication Engineering (ENTC) building[cite: 4].

![Network Topology Placeholder](media/network_topology.png)

---

## ✨ Core Network Features

*   **Hierarchical Architecture:** Utilizes a highly efficient Core, Distribution, and Access layer model to isolate faults and manage traffic seamlessly[cite: 4].
*   **High Availability & Redundancy:** The central core deploys two redundant Cisco Catalyst 3650-24PS multilayer switches, eliminating single points of failure[cite: 4].
*   **Optimized Bandwidth Allocation:** Implements 10 Gbps Single Mode Fiber (SMF) links between the core and distribution layers, scaling down to 1 Gbps fiber or copper depending on specific department data loads[cite: 4].
*   **Dual-Stack IP Addressing:** 
    *   **IPv4:** Hierarchical `/24` subnets (e.g., `192.168.1.0/24`) for department isolation and `/30` subnets for point-to-point backbone routing[cite: 4].
    *   **IPv6:** Future-proofed with standard `/64` prefix subnets assigned to every building[cite: 4].
*   **Structured Internal LAN (ENTC):** Integrates wired laboratory workstations and wireless access points (AP-PT) managed through patch panels and 24-port access switches connected via fiber uplinks[cite: 4].

---

## 🛠️ Simulation & Verification

The entire network architecture was mapped, configured, and tested using **Cisco Packet Tracer**[cite: 4]. 

### Testing Parameters:
*   **Intra-VLAN Communication:** Verified zero packet loss for devices communicating within the same department switch (e.g., between ENTC laboratory PCs)[cite: 4].
*   **Inter-VLAN Routing:** Successfully simulated packet routing across the campus backbone, verifying connectivity between isolated subnets (e.g., from the ENTC network to the Electrical and Civil Engineering networks) with optimal average Round Trip Times (RTT) of under 10ms[cite: 4].

---

## 📦 Bill of Quantities (BOQ) Summary

A production-ready hardware list was generated for the deployment[cite: 4]:
*   **Active Components:** 13x Cisco 3650-24PS Multilayer Switches, 16x Access Switches, 15x Wireless Access Points[cite: 4].
*   **Passive Components:** ~5km Single Mode Fiber, ~5km Copper UTP (Cat5e/Cat6), 40x Patch Panels, and 40x Network Racks[cite: 4].

---

## 👥 Team Contributions

*Note: Update names and index numbers as necessary.*

| Name | Index |
| :--- | :--- |
| **A.H.D. Karunanayake** | 230321P[cite: 4] |
| **H.H. Palihena** | 230458P[cite: 4] |
| **N.P.P. Piyumal** | 230493R[cite: 4] |
| **M.N.N. Shehan** | 230613M[cite: 4] |

---

## 📂 Repository Contents

```text
/PacketTracer_Simulations # .pkt files containing the full campus topology
/Documentation            # Detailed design report and BOQ breakdown
README.md                 # Project overview and topology details
