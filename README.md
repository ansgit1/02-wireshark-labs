Wireshark Labs — SOC Practice

Purpose

This repository contains Wireshark labs to practice network analysis and SOC detection. Each lab shows normal or suspicious network behavior to help learn how to spot attacks.

Labs
1. Baseline Browsing - Open YouTube → DNS → TLS/QUIC → streaming
2. Follow a TCP Conversation - tcp.stream == 5 shows GET → 200 OK
3. Cleartext Credential Leak - POST to http://insecure.example/login with username & password
4. SYN Scan (scanning) - Many SYNs, few ACKs
5. SMB / RDP Detection - Connections on TCP/445 or TCP/3389 with repeated failed logins
6. Noisy / Exfil DNS - Many queries for long/random subdomains

Tools Used

Wireshark / tshark
Nmap
Kali Linux (attacker VM)
Windows RDP / SMB clients
Browser for HTTP/HTTPS tests

How to Run

1. Set up attacker and target VMs on a test network
2. Capture traffic with Wireshark/tshark
3. Perform the activity (browse, scan, login, etc.)
4. Open the capture in Wireshark and inspect

What I Learned From This Lab

Web / Streaming - Watch known domains and protocols (QUIC/UDP or TCP)
TCP Streams - Follow streams to see full requests and responses
HTTP POSTs - Cleartext POSTs can leak passwords. Alert on unexpected HTTP logins
SYN Scans - Many SYNs with few ACKs usually mean scanning
SMB / RDP - Unexpected sessions or repeated failed logins may indicate lateral movement
DNS - Lots of queries to long/random subdomains may indicate beaconing or data exfiltration

Display & Capture Filters

Display Filters (Wireshark, after capture)
tls || quic - show web traffic (HTTPS / QUIC)
http.request.method == "POST" - show HTTP POSTs
tcp.stream eq 5 - follow a specific TCP conversation
tcp.flags.syn == 1 && tcp.flags.ack == 0 - show SYN scans
tcp.port == 445 - SMB traffic
tcp.port == 3389 - RDP traffic
dns - DNS queries

Capture Filters (BPF, when recording)

tcp port 443 or udp port 443 - capture web traffic
tcp port 80 - capture HTTP
udp port 53 - capture DNS
tcp port 445 or tcp port 3389 - capture SMB/RDP
