# Basic-LAN-Static-IP-Router-Configuration

## 📌 Project Overview
This project demonstrates a **Basic LAN network simulation** built in Cisco 
Packet Tracer connecting three separate LAN segments through three routers 
using **Serial WAN links**. All devices including routers, PCs, and laptops 
are configured with **Static IP addresses manually** no DHCP is used 
anywhere in this topology.

---

## 🖧 Network Topology Summary

| Router   | LAN Interface | LAN Network       | WAN Interface | WAN IP  |
|----------|---------------|-------------------|---------------|---------|
| Router 1 | Fa0/0         | 192.168.50.0/24   | Se0/0/0       | 52.1    |
| Router 2 | Fa0/0         | 192.168.60.0/24   | Se0/0/0       | 52.2    |
| Router 2 | Fa0/1         | —                 | Se0/0/1       | 63.1    |
| Router 3 | Fa0/0         | 192.168.70.0/24   | Se0/0/0       | 63.2    |

### 🔗 WAN Serial Links
| Link              | Subnet            |
|-------------------|-------------------|
| Router1 ↔ Router2 | 192.168.52.0/30   |
| Router2 ↔ Router3 | 192.168.63.0/30   |

---

## 📋 LAN Network Details

### 🔵 LAN 1 — Router 1
| Device   | IP Address      | Subnet Mask     | Default Gateway |
|----------|-----------------|-----------------|-----------------|
| Router 1 | 192.168.50.1    | 255.255.255.0   | —               |
| PC0      | 192.168.50.2    | 255.255.255.0   | 192.168.50.1    |
| Laptop0  | 192.168.50.3    | 255.255.255.0   | 192.168.50.1    |

### 🟢 LAN 2 — Router 2
| Device   | IP Address      | Subnet Mask     | Default Gateway |
|----------|-----------------|-----------------|-----------------|
| Router 2 | 192.168.60.1    | 255.255.255.0   | —               |
| Laptop1  | 192.168.60.2    | 255.255.255.0   | 192.168.60.1    |
| PC1      | 192.168.60.3    | 255.255.255.0   | 192.168.60.1    |

### 🔴 LAN 3 — Router 3
| Device   | IP Address      | Subnet Mask     | Default Gateway |
|----------|-----------------|-----------------|-----------------|
| Router 3 | 192.168.70.1    | 255.255.255.0   | —               |
| PC2      | 192.168.70.2    | 255.255.255.0   | 192.168.70.1    |
| PC3      | 192.168.70.3    | 255.255.255.0   | 192.168.70.1    |

---

## ⚙️ Configuration Details

### ✅ IP Assignment Method
| Method    | Status          |
|-----------|-----------------|
| Static IP | ✔ Yes — All devices |
| DHCP      | ✘ Not used      |

### 🔧 Router Configuration Applied
- Static IP on all FastEthernet LAN interfaces
- Static IP on all Serial WAN interfaces
- Static routing configured for inter-network communication
- No dynamic routing protocol used
- Clock rate configured on Serial DCE interfaces

---

## 🛠️ Devices Used
| Device              | Model        | Quantity |
|---------------------|--------------|----------|
| Router              | Cisco 2811   | 3        |
| Switch              | Cisco 2960-24TT | 3     |
| PC                  | PC-PT        | 4        |
| Laptop              | Laptop-PT    | 2        |

---

## 🔌 Interface Summary
| Router   | LAN Port | WAN Port(s)        |
|----------|----------|--------------------|
| Router 1 | Fa0/0, Fa0/1 | Se0/0/0        |
| Router 2 | Fa0/0, Fa0/1 | Se0/0/0, Se0/0/1|
| Router 3 | Fa0/0, Fa0/1 | Se0/0/0        |

---

## 🧠 Concepts Covered
- Basic LAN design and setup
- Static IP addressing and subnetting
- Point-to-point Serial WAN links (/30 subnetting)
- Inter-router static routing
- Default gateway configuration on end devices
- FastEthernet and Serial interface configuration on Cisco routers

---

## 📂 Project File
| File | Description |
|------|-------------|
| `Static-LAN-Network.pkt` | Cisco Packet Tracer simulation file |

---

## 🚀 How to Run
3. Open the `.pkt` file in Cisco Packet Tracer
4. Go to **Simulation Mode** to observe packet flow
5. Test connectivity using `ping` command between PCs across different LANs




1. Install **Cisco Packet Tracer** (version 7.x or above)
2. Clone this repository:
