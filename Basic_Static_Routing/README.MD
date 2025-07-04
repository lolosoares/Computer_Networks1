# Basic Static Routing with IPv4 and IPv6

This project demonstrates a simple static routing setup using both IPv4 and IPv6 in a small network topology. The goal is to understand manual IP configuration and routing table entries in dual-stack networks.

## 🛠️ Topology Overview

- 2 Routers (R1 and R2)
- Each router is connected to:
  - 2 Switches
  - Each switch is connected to 1 PC


## 🔧 Configuration Details

### IPv4
- IPs are **manually assigned** to all interfaces and PCs.
- Static routes are added to each router to ensure full end-to-end connectivity.

### IPv6
- Global unicast addresses (GUAs) are **manually configured**.
- Static IPv6 routes are added to enable inter-network communication.

## 📘 Objectives

- Practice manual IP addressing (IPv4 and IPv6)
- Understand and configure static routing on Cisco routers
- Verify end-to-end connectivity using `ping`

## ✅ Success Criteria

- All PCs should be able to ping each other via IPv4 and IPv6.
- Routers must have correct static route entries for each network.

## 🧪 Testing Commands

On each PC:
```bash
ping <destination IPv4>
ping <destination IPv6>
