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


## 5. Initial Nmap Scan and Firewall Filtering

![Filtered Ports](Screenshots/Capture5.PNG)

An initial network scan was performed against the Windows target machine using Nmap.

During the scan, all TCP ports appeared in a filtered state, indicating that the target system was blocking or filtering incoming connection attempts.

This behavior is commonly associated with defensive security mechanisms such as Windows Defender Firewall, which restrict unauthorized access and reduce the visibility of exposed services.

From a defensive cybersecurity perspective, filtered ports can make reconnaissance activities more difficult for attackers by preventing accurate service enumeration.

This step demonstrated how firewall protections can significantly affect network reconnaissance results and how security controls influence the visibility of systems during scanning activities.














