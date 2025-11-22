# Workshop-Cisco Packet Tracing
## Date:22.11.25
## Name :Kishore K
## Reg No :212223040101
## AIM:
To design a multi-router enterprise network using Cisco Packet Tracer.

To assign proper LAN and WAN IP addressing for all network devices.

To configure router-to-router communication using serial or Ethernet links.

To implement static or dynamic routing to enable inter-network connectivity.

To verify successful end-to-end communication using ping and simulation mode.

TOPOLOGY DIAGRAM :

<img width="942" height="490" alt="image" src="https://github.com/user-attachments/assets/27ce499d-67f6-4b51-88fa-0e67038463cf" />

## DESCRIPTION:

This topology represents a small enterprise network built using Cisco Packet Tracer. The design includes three routers (Router0, Router1, and Router2) linked through a serial WAN configuration. Each router provides connectivity to a local network via a switch, and each LAN contains two end devices (PCs).

Each LAN operates on its own IPv4 addressing scheme:

LAN 1 (Router0): 192.168.0.0/24 and 192.168.1.0/24

LAN 2 (Router1): 192.168.1.0/24 and 10.10.1.0/24

LAN 3 (Router2): 192.168.10.0/24 and 10.10.2.0/24

The WAN connections between routers use point-to-point networks:

12.12.0.0/30 → Router0 ↔ Router1

15.15.0.0/30 → Router1 ↔ Router2

The goal of this configuration is to ensure full communication between all devices by applying correct addressing, interface configuration, and routing.

## PROCEDURE:

Step 1: Build the Network Layout

Add three Cisco 2911 routers

Connect each router to a 2960 switch

Attach two PCs to each switch

Link the routers using serial DCE/DTE connections

Step 2: Configure Addressing

Assign IP addresses to all PCs

Configure LAN interfaces on routers (GigabitEthernet0/0)

Assign /30 subnet addresses to the WAN serial links

Step 3: Implement Routing
Routing can be done through Static Routing or RIP/OSPF.

Example using Static Routes (Router0):

ip route 192.168.1.0 255.255.255.0 12.12.0.2
ip route 192.168.10.0 255.255.255.0 12.12.0.2
ip route 10.10.1.0 255.255.255.0 12.12.0.2
ip route 10.10.2.0 255.255.255.0 12.12.0.2

Step 4: Verify Connectivity

Use the ping command (example: PC0 → PC4)

Ensure all devices can communicate successfully

Switch to Simulation Mode to observe the packet path and routing behavior

## Output

<img width="975" height="500" alt="image" src="https://github.com/user-attachments/assets/cbaa6f3d-996e-4894-8edb-0d4dccd87775" />
<img width="972" height="497" alt="image" src="https://github.com/user-attachments/assets/810c5a12-b9c9-466f-87d0-a92becf61542" />
<img width="1036" height="300" alt="image" src="https://github.com/user-attachments/assets/081df394-f4bc-455e-b2c5-09ef9e50d57f" />
<img width="495" height="481" alt="image" src="https://github.com/user-attachments/assets/ac2d70b0-2890-40e5-a6e0-af00f0fb45d8" />
<img width="500" height="497" alt="image" src="https://github.com/user-attachments/assets/31a4adfb-8a32-4849-92a5-0312143aa504" />

## Result
All routers and end devices were successfully configured, and full connectivity was achieved across the network. Ping tests confirmed that communication between all LANs and across WAN links was functioning correctly.




