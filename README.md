# 🌐 Communication Network Diagnostics and Analysis

## Overview
This project is a comprehensive practical analysis of real-world telecommunication network performance, routing behaviors, and latency metrics. The study explores how packets traverse hierarchical networks—specifically the Access, Distribution, and Core layers—across global ISPs. By leveraging command-line diagnostic tools, the project investigates physical packet routing, bandwidth constraints, and severe latency issues such as bufferbloat under varying network loads.

## ✨ Key Features
* **Path Mapping:** Traced physical packet routes from local nodes to international servers using `traceroute` and geolocated intermediate ISP routers.
* **Latency Analysis:** Calculated Theoretical vs. Practical Round Trip Time (RTT), accounting for submarine cable routing, transmission, processing, and queuing delays.
* **Bandwidth Profiling:** Measured and compared network throughput during peak and off-peak hours using `iperf3`.
* **Bufferbloat Diagnostics:** Evaluated oversized network buffer congestion resulting in severe latency increases (Grade F) using Waveform and `Flent` Real-time Response Under Load (RRUL) tests.
* **Protocol Inspection:** Outlined the step-by-step connection lifecycle, including DNS resolution, TCP 3-way handshakes, and TLS secure connections.

## 🛠️ Technical Implementation
The analysis relies entirely on robust network diagnostic software to map and stress-test infrastructure.
* **Core Tools:** `ping`, `traceroute`, `iperf3`, `Flent`, Waveform.
* **Protocols Investigated:** TCP, UDP, ICMP, HTTP/HTTPS, DNS, and BGP routing decisions.
* **Methodology:** Network load was tested across different environments (University vs. Home ISP) to isolate the variables that increase queuing time and degrade the overall Quality of Experience.

## 📂 Repository Contents
**Sole Contributor:** Palihena H.H. (Index: 230458P)

```text
/Diagnostic_Logs        # Raw output data from iperf3 and Flent RRUL tests
/Geolocation_Maps       # Mapped traceroute paths and physical router locations
/Documentation          # Full network analysis report (PDF)
README.md               # Project overview and testing methodology
