#🚀 GNS3-pfSense-Firewall-Project

A hands-on implementation of a virtualized enterprise-grade network security solution using **pfSense** and **GNS3**. This project demonstrates core networking concepts including WAN/LAN segmentation, automated IP management, and content filtering.

## 🛠 Project Overview & Technologies
* **Virtualization Platform:** GNS3 (Graphical Network Simulator-3)
* **Firewall/Router:** pfSense 2.7+ (FreeBSD-based)
* **Client Node:** Docker Webterm (Linux-based testing environment)
* **Key Skills:** Network Topology Design, DHCP Configuration, DNS Filtering, Troubleshooting.

## 🌐 Network Configuration Details
* **pfSense LAN IP:** `192.168.1.1/24`
* **DHCP Address Pool:** `192.168.1.100` – `192.168.1.200`
* **Client Assignment:** Dynamically leased IP `192.168.1.100` via DHCP.

## 🔑 Core Features & Implementation

### 1. Gateway & DHCP Configuration
- Established a stable WAN-LAN bridge to provide internet connectivity to internal nodes.
- Configured a **DHCP Server** on the LAN interface to automate IP, Gateway, and DNS assignment, ensuring seamless device onboarding.

### 2. DNS-Based Content Control
- Implemented **DNS Resolver Host Overrides** to enforce security policies.
- Successfully restricted access to specific domains (e.g., `facebook.com`) by redirecting traffic to a local loopback address (`127.0.0.1`).
- Verified policy enforcement via the client-side browser while maintaining access to authorized resources.

## 📸 Lab Demonstration
*Insert your screenshots here:*
1. **GNS3 Topology Diagram**
2. **Webterm `ip a` output (Confirming 192.168.1.100)**
3. **pfSense Web GUI Dashboard**
4. **Site Blocking Result (Denied Access vs. Successful Google Search)**
