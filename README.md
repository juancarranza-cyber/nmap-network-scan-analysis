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


# 3. Connectivity Verification Using ICMP

![Ping Test](Screenshots/Capture3.PNG)

Connectivity between Kali Linux and the Windows target machine was verified using the `ping` command.

The ICMP protocol allowed successful communication testing between both virtual machines inside the Host-Only virtual network configured in VirtualBox.

Successful Echo Reply responses confirmed that the lab environment was correctly configured and ready for traffic analysis and reconnaissance testing.

This step is important in cybersecurity labs because it validates network reachability before performing scanning, monitoring, or offensive security activities.


# 4. ICMP Traffic Capture Using Wireshark

![Wireshark ICMP](Screenshots/Capture4.PNG)

Wireshark was used to capture and analyze ICMP traffic generated during the connectivity verification process.

The packet capture displayed Echo Request and Echo Reply packets associated with the `ping` command executed from Kali Linux toward the Windows target machine.

This analysis demonstrates how network communication can be monitored in real time and how packet analysis tools are used by SOC analysts and cybersecurity professionals to investigate traffic behavior, detect anomalies, and monitor suspicious activity inside enterprise environments.

Packet analysis is a fundamental skill in defensive cybersecurity operations because it provides visibility into communication patterns and network-level activity.


# 5. Successful Nmap Port Scan

![Filtered Ports](Screenshots/Capture5.PNG)

A network scan was performed against the Windows target machine using Nmap.

The scan successfully identified accessible TCP ports and active network services running on the target system.

Nmap is a widely used reconnaissance and enumeration tool in cybersecurity that allows analysts and penetration testers to identify exposed services, discover accessible systems, and analyze potential attack surfaces.

During the scan, multiple TCP connection attempts were generated toward the target machine, allowing further traffic analysis using Wireshark.

From a defensive cybersecurity perspective, network scans are considered reconnaissance activity and may represent an early stage of an attack lifecycle.


# 6. TCP Traffic Analysis During Nmap Scan

![Wireshark TCP Scan](Screenshots/Capture6.PNG)

During the Nmap scan, Wireshark was used to capture and analyze the TCP traffic generated between Kali Linux and the Windows target machine.

The packet capture revealed multiple TCP connection attempts directed toward different ports on the target system, behavior that is characteristic of network reconnaissance activity.

Traffic analysis allowed observation of how Nmap interacts with remote systems by sending TCP packets to identify accessible services and determine port states.

From a defensive cybersecurity perspective, this type of activity can be monitored by SOC analysts to detect reconnaissance attempts, suspicious scanning behavior, and potential early stages of an attack lifecycle.

Packet-level visibility is essential for incident detection, traffic analysis, and network monitoring operations.










