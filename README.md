<div align="center">
  
# NETWORKWALKS-B084-WEEK1-PM1
This project involves establishing a virtualised cybersecurity laboratory using VirtualBox, Kali Linux and a private NAT Network.
</div>

## Project Overview
This project documents the deployment and configuration of a Kali Linux virtual machine within Oracle VirtualBox. The objective was to establish a functional and reproducible cybersecurity laboratory environment for future networking and security exercises. The implementation involved importing a prebuilt Kali Linux virtual machine, configuring a dedicated NAT Network, manually assigning IPv4 network settings, verifying connectivity and creating a recovery snapshot. The resulting environment provides a controlled foundation for future cybersecurity activities without requiring additional physical hardware.

## Objectives
- Install and configure VirtualBox and import a prebuilt Kali Linux virtual machine.
- Establish a dedicated private NAT Network for the virtual laboratory.
- Configure Kali Linux with a static IPv4 address, subnet prefix, default gateway and DNS server.
- Verify connectivity between the virtual machine, its default gateway and an external IP address.
- Create a VirtualBox snapshot to preserve the initial configuration and provide a recovery point.
- Document the configuration process and verification results to support reproducibility and troubleshooting.

## Lab Architecture
| Component | Configuration |
| --------- | -------------- |
| Host OS | Windows 11 |
| Virtualisation Platform | Oracle VirtualBox |
| Lab OS | Kali Linux 2026.3 |
| Network Type | NAT Network |
| Network Name | NatNetwork |
| Network Prefix | 10.0.0.0/24 |
| Kali IP Address | 10.0.0.2 |
| Subnet Mask | 255.255.255.0 (/24) |
| Default Gateway | 10.0.0.1 |
| DNS Server | 8.8.8.8 |
| DHCP | Enabled |

The laboratory uses a private IPv4 subnet (`10.0.0.0/24`) to provide a shared network environment for virtual machines connected to the `NatNetwork` interface.

Kali Linux uses a manually assigned static IPv4 address (`10.0.0.2`), while DHCP remains enabled to accommodate additional virtual machines. This provides predictable addressing for the primary security testing machine while maintaining flexibility for future laboratory expansion.

# Lab Setup Procedure

## Step 1 - Preparing VirtualBox and Kali Linux


