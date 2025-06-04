# SPANNING TREE PROTOCOL (SPF)
### Introduction: Understanding Redundancy in Networks
In modern computer networks, redundancy is crucial for maintaining **high availability** and fault tolerance. Redundant links and devices are intentionally added to prevent single points of failure. However, while redundancy ensures reliability, it also introduces the risk of layer 2 switching loops, which can flood the network and disrupt communication.

To address this, network protocols like Spanning Tree Protocol (STP) were developed. STP prevents loops by dynamically analyzing the network topology and blocking redundant paths, only activating them if the primary path fails. This allows networks to maintain resilience without compromising stability

---
### Project Summary: Simulating STP Failover in Cisco Packet Tracer
This project demonstrates how Spanning Tree Protocol (802.1D / PVST+) operates in a simulated network built using Cisco Packet Tracer. The core goal was to implement redundancy with intelligent loop prevention and automatic failover, using a simple network of three switches (S1, S2, S3) and four PCs (PC1–PC4).

**Desired Network Behavior:**
* Primary Path (Normal Operation):
_PC1/2/3 → S1 → S3 → PC4_

* Backup Path (If S1–S3 link fails):
_PC1/2/3 → S1 → S2 → S3 → PC4_

**Loop Prevention:**
STP should block the S1–S2 link under normal conditions to prevent loops from forming. If the S1–S3 link goes down, STP reconverges and unblocks S1–S2 to maintain connectivity.

**Key Implementation Details:**
* S3 is manually set as the Root Bridge to ensure it's the central point for STP calculations.
* STP determines the optimal path, placing unnecessary paths in a blocking state.
* Upon failure of a forwarding link, STP dynamically unblocks alternate links to restore network communication.
* CLI commands and verification steps (show spanning-tree) are used to monitor STP behavior.

🏁 Achievements:
1. Successfully simulated STP behavior and convergence in a redundant network.
2. Validated automatic failover and loop prevention using Cisco Packet Tracer.
3. Gained practical experience with STP configurations, port roles, and port states (forwarding, blocking, etc.).
4. Demonstrated how redundant topology can remain loop-free and resilient using STP.

---

### Step-by-Step Implementation
1. Add 3 switches: S1, S2, and S3
2. Add 4 PCs: PC1, PC2, PC3 (connected to S1) and PC4 (connected to S3)
3. Connect the switches in a triangle:
* S1 ↔ S2
* S2 ↔ S3
* S1 ↔ S3
4. Connect PCs to switches:
* PC1–3 → S1
* PC4 → S3

![image](https://github.com/user-attachments/assets/804d2380-81a9-49ed-81f1-01850822ef2b)
