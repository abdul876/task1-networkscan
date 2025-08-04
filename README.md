 Task 1 - Local Network Port Scanning
 Objective
To scan the local network and identify active devices and their open ports using Nmap. Optionally, analyze the traffic with Wireshark to understand how port scanning looks at the packet level.

 Tools Used
1.Nmap
2.Wireshark

IP Range Used
My local IP was: `10.243.85.225`
Subnet: `255.255.255.0`
So I scanned the network range: `10.243.85.0/24`

 Command Used

nmap -sS 10.243.85.0/24 > portscan.txt
This performed a TCP SYN scan to check which ports are open on devices in the local network.

 Scan Result Summary
Host: 10.243.85.207
53/tcp open — domain (DNS)

Host: 10.243.85.225 (my own device)
135/tcp open — msrpc

139/tcp open — netbios-ssn

445/tcp open — microsoft-ds

6881/tcp open — bittorrent-tracker

Full results are in portscan.txt.

Wireshark Packet Analysis
I used Wireshark to capture packets during the Nmap scan.

Key Observations:
Captured SYN and SYN-ACK packets used during the TCP SYN scan

Saw traffic to devices in my subnet

Observed protocols such as:

Ethernet II

IPv4

TCP

TLS 

Wireshark capture file: nmap_scan_capture.pcapng (added in this repo)

 What I Learned:
1.How to scan a local network using Nmap

2.How SYN scan works at the packet level

3.Identified services exposed on local devices

Understood how tools like Wireshark help visualize network behavior

 Files in This Repo
1.portscan.txt 

2.README.md 

3.nmap.pcapng 

4.screenshots
