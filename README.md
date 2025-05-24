# Industrial-Network

# Project Title: Secure Virtual Network Infrastructure Simulation for a 50-User Enterprise

## Overview
This academic project simulates the design and implementation of a secure virtual network for a mid-sized enterprise of 50 users. It demonstrates core concepts in enterprise networking and cybersecurity, including VPN configuration, subnet design, firewall rules, access control, and network monitoring.

## Objectives
- Simulate a real-world enterprise network environment
- Demonstrate secure remote access via VPN
- Implement segmentation using subnets and VLANs
- Apply firewall rules and role-based access control (RBAC)
- Integrate basic monitoring and logging mechanisms
- Document and present the network professionally for academic and portfolio purposes

## Simulated Infrastructure
The project will be built using virtualized systems and open-source tools:
- VirtualBox or VMware Workstation for virtualization
- pfSense (or OPNsense) for firewall and VPN services
- A simulated directory service (mock AD or user roles)
- Zabbix or Nagios for monitoring (optional)
- Local Linux VMs for client/user simulation
- Optional: GNS3 or EVE-NG to simulate network topology

## Network Services
The network will include the following services:
- VPN Server (OpenVPN or WireGuard)
- DHCP and DNS Server (built-in or BIND)
- Role-Based Access Control (using groups)
- Network segmentation (Guest, Admin, Dev, etc.)
- Internal routing and NAT
- Centralized logging

## User Roles
Simulated users will be divided into:
- **Network Administrator** – Full control
- **IT Staff** – Access to infrastructure tools
- **Employees** – Standard access to work apps
- **Guests** – Internet-only access (segregated)

## Security Goals
- Encrypted VPN for remote users
- Network segmentation using firewall rules
- Use of strong authentication for admin access
- Simulated Intrusion Detection System (Snort or Suricata)
- Simulated patching and maintenance plan

## Monitoring Goals
- Uptime and traffic monitoring for virtual devices
- Bandwidth tracking and user activity simulation
- Alerting for anomalies (e.g., CPU usage, unauthorized access)

## Tools & Technologies
| Purpose            | Tool                  |
|--------------------|------------------------|
| Virtualization     | VirtualBox / VMware    |
| Firewall/VPN       | pfSense / OpenVPN      |
| OS for Clients     | Ubuntu / Debian VMs    |
| Monitoring         | Zabbix / Nagios        |
| Logging            | rsyslog / Graylog (optional) |
| Network Diagrams   | draw.io or Lucidchart  |

## Deliverables
- Network topology diagram
- Simulated configuration files (pfSense, VPN, users)
- Role descriptions and access rules
- Screenshots or demo video
- `README.md` and documentation
- Optional: blog post or LinkedIn write-up


