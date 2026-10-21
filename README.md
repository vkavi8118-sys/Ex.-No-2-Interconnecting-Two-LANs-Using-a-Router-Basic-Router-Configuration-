# Date :21.10.2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
<img width="1920" height="1080" alt="Screenshot (232)" src="https://github.com/user-attachments/assets/77e254ab-0df0-4df2-bd7c-a60b1462a227" />

•	IP configurations on PCs<br>
<img width="1920" height="1080" alt="Screenshot (229)" src="https://github.com/user-attachments/assets/c5855931-62ee-42b6-be2a-1878f1927550" />
<img width="1920" height="1080" alt="Screenshot (230)" src="https://github.com/user-attachments/assets/91052dea-ea03-4ada-ae34-9c4b4752c1ea" />

•	Successful ping between PC0 and PC1<br>
<img width="1920" height="1080" alt="Screenshot (239)" src="https://github.com/user-attachments/assets/e21cf380-0691-4aa6-83ef-a88c51651ab8" />

<img width="1920" height="1080" alt="Screenshot (234)" src="https://github.com/user-attachments/assets/6bb65b03-3109-4152-abe5-26f920d7c1dd" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

