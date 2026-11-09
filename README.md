# Router-on-a-stick
Configure inter-VLAN routing using a single router.  Enabling router sub-interfaces.
#STATIC ROUTING 

This repository contains the configuration files and documentation for setting up **Inter-VLAN Routing** using a single router (Router-on-a-Stick method) connected to Cisco switches and multi-VLAN end devices in Cisco Packet Tracer.

Topology Overview
Router - 1x Cisco 1941, Configured with 802.1Q sub-interfaces
Switches - 2x Managed Layer 2 Switches, Configured with VLANs and Trunk ports
End Devices -  2x PCs and Printers distributed across VLAN 10 and VLAN 20

IP Addressing Table
VLAN 10 - switch0 
        interface gigabitethernet0/1
        ip address - 192.168.1.30/24
        gateway - 192.168.10.1 
 VLAN 20
         interface gigabitethernet0/1
        ip address - 192.168.1.32
        gateway - 192.168.20.1
Router - 
        gigabitethernet0/0.10
                192.168.10.1
        gigabitethernet0/0.20
                192.168.20.1
End points - Ip address changes for end devices - gateways stay the same, depending on VLAN
        interface fastethernet0/1-3
        Ip address - 192.168.10.x or 192.168.20.x
        gateway - 192.168.10.1 or 192.168.20.1
        



