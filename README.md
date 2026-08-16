# Enterprise VLAN Architecture Lab
Documentation Attached as a PDF

A hands-on Cisco Packet Tracer enterprise networking lab focused on VLAN design, network segmentation, access ports, trunking, voice VLANs, IP addressing, and collapsed-core switching architecture.

## Project Overview

This project was created to gain practical experience designing and configuring a VLAN-based enterprise network using Cisco Packet Tracer.

Before completing this lab, I already understood the basic concept of VLANs and had read about how they are used in networking. However, I wanted to move beyond theory and actually build, configure, test, troubleshoot, and verify a network myself.

The lab focuses on how VLANs can be used to divide a physical network into multiple logical networks while still allowing those networks to operate across a shared switching infrastructure.

The project uses a **collapsed-core network architecture**, with Cisco switches providing the core and access functions of the simulated enterprise network.

The main technologies explored in this project are:

- VLANs
- VLAN segmentation
- Access ports
- Trunk ports
- IEEE 802.1Q
- Native VLANs
- Voice VLANs
- Static IPv4 addressing
- Layer 3 switching
- Collapsed-core architecture
- Network verification
- Connectivity testing
- Network troubleshooting

---

# Project Objectives

The main objectives of this lab were to:

- Design an enterprise VLAN structure
- Create and configure multiple VLANs
- Assign end devices to the correct VLANs
- Configure access ports
- Configure trunk ports
- Configure native VLANs
- Configure voice VLANs
- Configure trunk links between switches
- Configure the core switching infrastructure
- Understand the difference between Cisco 2960 and Cisco 3560 switch configuration
- Configure IEEE 802.1Q trunking
- Restrict the VLANs allowed across trunk links
- Assign static IP addresses to network devices
- Test connectivity between devices
- Verify VLAN and trunk configurations
- Troubleshoot configuration problems
- Understand how VLANs and trunking work together in an enterprise network

---

# Network Architecture

The network was designed using a **collapsed-core architecture**.

A collapsed-core design combines core and distribution functions into the same switching infrastructure.

The access switches connect end devices to the network, while the core switches provide the infrastructure needed to connect the different network segments.

The design allows multiple VLANs to operate across the same physical switching infrastructure while keeping the different logical networks separated.

### High-Level Design

```text
                    +----------------------+
                    |     Core Switch 01   |
                    |     Cisco 3560       |
                    +----------+-----------+
                               |
                               |
                    +----------+-----------+
                    |     Core Switch 02   |
                    |     Cisco 3560       |
                    +----------+-----------+
                         /            \
                        /              \
                       /                \
              +-------+------+    +-----+-------+
              | Access Switch |    | Access      |
              | Cisco 2960   |    | Switch 2960 |
              +------+-------+    +------+-------+
                     |                   |
               +-----+-----+       +-----+-----+
               | End       |       | End       |
               | Devices   |       | Devices   |
               +-----------+       +-----------+
