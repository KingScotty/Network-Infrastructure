# Network-Infrastructure
A combined repo for my IT2035C – Networking Infrastructure Management class labs (Cisco Packet Tracer).
Lab 2 – Basic routed network with DHCP
Lab 3 – Routed network with DHCP, DNS, and HTTP (PCs resolve soit.edu to the DMZ web server)

**Lab 2 – DHCP (overview)**
Single router with multiple LANs
Server provides DHCP scopes for each LAN
PCs obtain addresses dynamically (no static IPs on clients)
Validation checklist
PCs show DHCP-assigned IP, mask, gateway, DNS
ping between subnets succeeds
Router interfaces are up/up

**Lab 3 - DHCP, DNS and HTTP (overview)**
Single router, 3 user LANs + DMZ with a server
Server static IP: 192.168.231.254/21, GW 192.168.224.1
Services enabled on the server:
DHCP (3 scopes: LAN1/LAN2/LAN3; DNS = 192.168.231.254)
DNS (A record: soit.edu → 192.168.231.254)
HTTP (index.html contains student name + greeting)
Router interfaces (example mapping):
192.168.248.1/21 (LAN3)
192.168.240.1/21 (LAN2)
192.168.232.1/21 (LAN1)
192.168.224.1/21 (DMZ)
Each L3 interface has: ip helper-address 192.168.231.254
Validation checklist
PC gets DHCP lease (correct mask/gateway/DNS)
nslookup soit.edu returns 192.168.231.254
Browser loads http://soit.edu (shows name/greeting)
Diagram annotated with all static addresses + name/lab number

**How to open**
Open .pkt files in Cisco Packet Tracer (v8.x+).
Wait a few seconds for links to come up, then verify:
Lab 2: DHCP leases on PCs.
Lab 3: Open PC browser → soit.edu.

