# 📡 Two-Way Paging System Using Software Defined Radio (SDR)

## Overview

This project implements a robust **two-way paging (text messaging) system** built entirely on **Software Defined Radio (SDR)** architecture. Designed to operate reliably in noisy RF environments, the system facilitates the exchange of short text messages between multiple discrete nodes. 

By prioritizing signal integrity and packet delivery, the design overcomes standard wireless communication challenges using a highly structured packet format, precise node addressing, and acknowledgment-based transmission protocols.

![System Architecture Placeholder](media/system_architecture.png)

---

## ✨ Key Features

*   **Multi-Node Communication:** Addressed packet structures allowing targeted, two-way short text messaging between specific nodes in a network.
*   **QPSK Modulation:** Utilizes Quadrature Phase Shift Keying (QPSK) for efficient data transmission over the RF spectrum.
*   **Guaranteed Delivery:** Implements a robust **Stop-and-Wait ARQ (Automatic Repeat reQuest)** protocol to ensure reliable message transmission and acknowledgment.
*   **Error Detection:** Integrates **CRC (Cyclic Redundancy Check)** to detect and discard corrupted packets.
*   **Noise Resiliency:** Features a robust receiver pipeline designed to maintain synchronization and decode signals accurately despite environmental RF noise and phase misalignment.
*   **Message Queuing:** Built-in queue management to handle concurrent message requests seamlessly.
*   **Interactive GUI:** A user-friendly Graphical User Interface for easy message composition, node selection, and real-time inbox monitoring.

---

## 🛠️ Technical Implementation

### Signal Processing Pipeline
The system's core digital signal processing (DSP) logic was designed and simulated using **GNU Radio** and deployed onto SDR hardware. The pipeline encompasses:
1.  **Transmitter:** Text encoding $\rightarrow$ Packet Framing (Address + Payload + CRC) $\rightarrow$ QPSK Constellation Modulation $\rightarrow$ SDR Sink.
2.  **Receiver:** SDR Source $\rightarrow$ Carrier/Timing Recovery $\rightarrow$ QPSK Demodulation $\rightarrow$ CRC Validation $\rightarrow$ Stop-and-Wait ACK Trigger $\rightarrow$ GUI Display.

### Graphical User Interface (GUI)
The user interface abstracts the complex RF backend, providing a simple chat-like interface for users to specify destination addresses and read incoming pages.

![GUI Screenshot Placeholder](media/gui_interface.png)

---

## 🎥 Project Demonstration

A demonstration of the working SDR paging system, including packet transmission and error handling in a noisy environment, can be viewed below:

👉 [Watch the Project Demo Video Here](ADD_VIDEO_LINK_HERE)

---

## 👥 Team Contributions

*Note: Update names and index numbers as necessary.*

| Name | Index |
| :--- | :--- |
| **Palihena H.H.** | 230458P |
| [Team Member 2] | [Index] |
| [Team Member 3] | [Index] |
| [Team Member 4] | [Index] |

**Key Personal Contributions (Palihena H.H.):**
*   Designed the QPSK modulation and demodulation flowgraphs.
*   Implemented the Stop-and-Wait ARQ logic and CRC packet validation.
*   Conducted system testing and parameter tuning for noise resiliency.

---

## 📂 Repository Contents

```text
/GNU_Radio_Flowgraphs   # .grc files for transmitter and receiver pipelines
/GUI_Source             # Source code for the user interface
/Simulations            # Baseline tests and noise environment simulations
/Documentation          # Project reports and system block diagrams
README.md               # Project overview and setup instructions
