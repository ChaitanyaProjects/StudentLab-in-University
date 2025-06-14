# StudentLab-in-University
# 🎓 University Student Lab Network (Cisco Packet Tracer)

This project simulates a university computer lab network using Cisco Packet Tracer. It is designed for learning and practicing VLANs, inter-VLAN routing (Router-on-a-Stick), and basic networking services like DNS.

---

## 🏗️ Topology Overview

- 3 Switches
- 1 Router (Router-on-a-Stick)
- Multiple PCs connected to VLANs
- DNS Server (simulated as 8.8.8.8)
- Trunk links between switches and router
- Internet access simulation (wired only)

---

## 📁 File Information

| File Name | Description |
|-----------|-------------|
| `labsetup.pkt` | Packet Tracer project file containing full network setup |
| `screenshot.png` | Network topology diagram (optional) |
| `README.md` | This documentation |

---

## 🌐 Network Configuration Summary

### VLANs

| VLAN ID | Name     | Purpose              |
|---------|----------|----------------------|
| 10      | LAB1-1   | Department Lab 1     |
| 20      | VLAN20   | Department Lab 2     |
| 30      | VLAN30   | Department Lab 3     |

> VLANs are created and assigned to ports on all switches.

---

### Router Configuration (Router-on-a-Stick)

Router uses subinterfaces for inter-VLAN routing:

```bash
interface Gig0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0

interface Gig0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0

interface Gig0/0.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0
