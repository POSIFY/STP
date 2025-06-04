# SPANNING TREE PROTOCOL (SPF)
### Introduction: Understanding Redundancy in Networks
In modern computer networks, redundancy is crucial for maintaining **high availability** and fault tolerance. Redundant links and devices are intentionally added to prevent single points of failure. However, while redundancy ensures reliability, it also introduces the risk of layer 2 switching loops, which can flood the network and disrupt communication.

To address this, network protocols like Spanning Tree Protocol (STP) were developed. STP prevents loops by dynamically analyzing the network topology and blocking redundant paths, only activating them if the primary path fails. This allows networks to maintain resilience without compromising stability

---
### Project Summary: Simulating STP Failover in Cisco Packet Tracer
