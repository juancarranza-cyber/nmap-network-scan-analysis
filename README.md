                                                  Nmap Network Scan Analysis

Introduction

This project demonstrates a basic virtual SOC lab focused on network reconnaissance and traffic analysis using Kali Linux, Windows, Nmap, and Wireshark.

The objective of the lab was to simulate reconnaissance activity, capture generated traffic, analyze TCP behavior, and understand how network scanning can be identified from a defensive cybersecurity perspective.

The environment was built using VirtualBox with a Host-Only virtual network configuration to allow direct communication between virtual machines in a controlled environment.

Lab Environment

* Kali Linux
* Windows
* Nmap
* Wireshark
* VirtualBox

Network Topology

Kali Linux → Windows Target


# 1. Windows Network Configuration

![Windows IP](Screenshots/Capture1.PNG)

The Windows virtual machine was configured inside a Host-Only virtual network using VirtualBox.

Using the `ipconfig` command, the assigned IP address was identified and later used as the target for network reconnaissance and traffic analysis performed from Kali Linux.

The identified IP address was `192.168.56.102`.

The Host-Only configuration allowed direct communication between virtual machines while keeping the lab isolated from external networks.


# 2. Kali Linux Network Configuration

![Kali IP](Screenshots/Capture2.PNG)

The Kali Linux virtual machine was configured within the same Host-Only virtual network as the Windows target machine.

Using the `ip a` command, the assigned IP address `192.168.56.101` was identified.

Having both systems inside the same isolated virtual network allowed direct communication between the attacker and target machines, enabling traffic analysis, reconnaissance activities, and packet capture in a controlled cybersecurity lab environment.






