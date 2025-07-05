# Basic VLAN Configuration with IPv4, IPv6, and DHCP

This project demonstrates how to configure two VLANs using both IPv4 and IPv6, with dynamic address assignment via DHCP. It is designed to introduce network segmentation, VLAN routing, and dual-stack addressing in a small topology.

## 🧱 Topology Overview

- 1 Router (R1)
- 1 Switch (S1)
- 2 PCs (PC0 and PC1)
- 2 VLANs:
  - VLAN 1 (DEEL)
  - VLAN 3 (DEC)

📷 The topology diagram is included in the repository as `topology.png`.


## 📘 Objectives

- Segment the network using VLANs
- Assign IPv4 and IPv6 addresses using DHCP
- Configure router-on-a-stick (subinterfaces with 802.1Q encapsulation)
- Enable inter-VLAN routing and test communication

## 🔧 Configuration Summary

### VLANs
- VLAN 1: Assigned to PC0
- VLAN 3: Assigned to PC1

### ROUTERS  
- DHCPv4 and DHCPv6 pools configured for both VLANs
- `ipv6 unicast-routing` enabled

### PCs
- Set to obtain both IPv4 and IPv6 via DHCP
- Should receive correct IP, gateway, and DNS addresses

## ✅ Testing

- Verify PC1 and PC2 receive correct IP configurations.
- Use `ping` to test:
  - Inter-VLAN communication (e.g., PC0 ↔ PC1)
  - Connectivity to router’s interfaces (default gateways)

### Commands

On each PC:
```bash
ipconfig /all    # View IP configuration
ping <other PC IPv4>
ping <other PC IPv6>

