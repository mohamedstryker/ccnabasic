CCNA Network Design & Implementation

📌 Overview :

This project is a CCNA-level network design that demonstrates advanced LAN switching and routing techniques.
It covers VLAN segmentation, IP routing, HSRP, ACLs, DHCP services, and security mechanisms to ensure high availability and secure communication between different departments.

The network is divided into multiple VLANs, each representing a different department (IT, HR, Finance, Healthcare, Production, Call Center).
Only the IT department is allowed to access switches for management purposes, while inter-VLAN communication is restricted by ACLs.


⚙️ Features & Technologies Used :

✅ VLAN Segmentation (Departments: IT, HR, Finance, Healthcare, Production, Call Center)

✅ IP Routing enabled on multilayer switches

✅ HSRP (Hot Standby Router Protocol) for redundancy and high availability

✅ DHCP Server for dynamic IP allocation

✅ DHCP Snooping and ARP Inspection for security

✅ Access Control Lists (ACLs) to restrict VLAN communication

✅ Spanning Tree Protocol (STP) to prevent switching loops

✅ Switch Security (Port Security, MAC Filtering, Double Tagging Protection)



## 🖥️ Network VLANs & IP Schema :

| Department      | VLAN | Network          | Gateway       |
|-----------------|------|------------------|---------------|
| IT Dept         | 10   | 192.168.10.0/24  | 192.168.10.1  |
| HR              | 20   | 192.168.20.0/24  | 192.168.20.1  |
| Finance         | 30   | 192.168.30.0/24  | 192.168.30.1  |
| Healthcare      | 40   | 192.168.40.0/24  | 192.168.40.1  |
| Production (PD) | 50   | 192.168.50.0/24  | 192.168.50.1  |
| Call Center     | 60   | 192.168.60.0/24  | 192.168.60.1  |


🔒 Note: Only VLAN 10 (IT Dept) can access switches (management IPs):

Switch1 → 192.168.10.10

Switch2 → 192.168.10.11

Switch3 → 192.168.10.20

Credentials:

username: admin
password: 123456



🚀 How to Run :

Open the project in Cisco Packet Tracer (or GNS3 if adapted).

Load the provided .pkt topology file.

Verify VLAN configuration on switches:

show vlan brief

Test inter-VLAN connectivity with:

ping 192.168.x.1

Check HSRP redundancy with:

show standby brief



🔐 Security Measures Implemented :

DHCP Snooping to prevent rogue DHCP servers

Dynamic ARP Inspection (DAI) against ARP spoofing

Port Security to limit MAC addresses per port

ACLs to restrict unauthorized VLAN access

STP Root Guard & BPDU Guard to protect spanning tree topology



📈 Future Enhancements :

Implement Syslog + SNMP monitoring

Add NAT + Internet Access simulation

Configure VPN tunnels for remote access

Deploy AAA authentication (TACACS+/RADIUS) for advanced security


📸 Photos :
<img width="1752" height="635" alt="d2f95bc8-a8a7-401d-afa2-c81cb50943b4" src="https://github.com/user-attachments/assets/2032f5be-2951-480b-acf0-9a875d705efb" />

👨‍💻 Author
Mohamed Ahmed Metwally
