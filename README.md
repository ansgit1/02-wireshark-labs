# Wireshark Lab Collection

This repository contains packet-capture labs and notes from hands-on exercises (Wireshark + network labs).  
**Open `.pcapng` files locally with Wireshark** for full analysis.

> **Repo layout:** (clickable links is not working ,consider its as a map)

- [wireshhark-lab](wireshhark-lab/)
  - [Lab-Purposes.txt](wireshhark-lab/Lab-Purposes.txt)
  - [lab-01-baseline-browse](wireshhark-lab/lab-01-baseline-browse/)
    - [baseline_browse%20(DNS%20queries,%20TLS%20handshakes).png](wireshhark-lab/lab-01-baseline-browse/baseline_browse%20(DNS%20queries,%20TLS%20handshakes).png)
    - [baseline_browse.pcapng](wireshhark-lab/lab-01-baseline-browse/baseline_browse.pcapng)
    - [win11_baseline_stream1.txt](wireshhark-lab/lab-01-baseline-browse/win11_baseline_stream1.txt)
  - [lab-2-follow-stream](wireshhark-lab/lab-2-follow-stream/)
    - [win11_post_stream.txt](wireshhark-lab/lab-2-follow-stream/win11_post_stream.txt)
  - [lab-03-http-credential-leak](wireshhark-lab/lab-03-http-credential-leak/)
    - [Lab%203%20Simulated%20HTTP%20Credential%20Leaak%20summary.txt](wireshhark-lab/lab-03-http-credential-leak/Lab%203%20Simulated%20HTTP%20Credential%20Leaak%20summary.txt)
    - [lab-03_http-credential-leak.png](wireshhark-lab/lab-03-http-credential-leak/lab-03_http-credential-leak.png)
    - [tcp_8000_traffic.pcapng](wireshhark-lab/lab-03-http-credential-leak/tcp_8000_traffic.pcapng)
    - [win11_cleartext_post.pcapng](wireshhark-lab/lab-03-http-credential-leak/win11_cleartext_post.pcapng)
    - [win11_to_win10_http_post_capture.pcapng](wireshhark-lab/lab-03-http-credential-leak/win11_to_win10_http_post_capture.pcapng)
  - [lab-04-syn-scan](wireshhark-lab/lab-04-syn-scan/)
    - [lab-04_synscan.pcapng](wireshhark-lab/lab-04-syn-scan/lab-04_synscan.pcapng)
    - [lab-04_synscan_tcpflags.png](wireshhark-lab/lab-04-syn-scan/lab-04_synscan_tcpflags.png)
    - [Lab4-Port-Scan-Observations.txt](wireshhark-lab/lab-04-syn-scan/Lab4-Port-Scan-Observations.txt)
    - [nmap%20-sS-192.168.1.100-scan-result.png](wireshhark-lab/lab-04-syn-scan/nmap%20-sS-192.168.1.100-scan-result.png)
    - [tcp.flags.syn==1%20&&%20tcp.flags.ack==1.png](wireshhark-lab/lab-04-syn-scan/tcp.flags.syn==1%20&&%20tcp.flags.ack==1.png)
  - [lab-05-SMB & RDP Lateral Movement Lab](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/)
    - [lab-05 RDP Internal Access Lab.txt](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/lab-05%20RDP%20Internal%20Access%20Lab.txt)
    - [RDP_Internal_Access from kali.png](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/RDP_Internal_Access%20from%20kali.png)
    - [RDP_Internal_Access kali to windows.png](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/RDP_Internal_Access%20kali%20to%20windows.png)
    - [smb_explorer_win10.png](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/smb_explorer_win10.png)
    - [SMB_Lab_Capture.txt](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/SMB_Lab_Capture.txt)
    - [smb_lab_traffic.png](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/smb_lab_traffic.png)
    - [smblab.pcapng](wireshhark-lab/lab-05-SMB%20&%20RDP%20Lateral%20Movement%20Lab/smblab.pcapng)
  - [lab-6-DNS-Noisy](wireshhark-lab/lab-6-DNS-Noisy/)
    - [dns_noisy_lab%20radnomdns.pcapng](wireshhark-lab/lab-6-DNS-Noisy/dns_noisy_lab%20radnomdns.pcapng)
    - [dns_noisy_lab.png](wireshhark-lab/lab-6-DNS-Noisy/dns_noisy_lab.png)
    - [Lab6_DNS_Noisy_Overview.txt](wireshhark-lab/lab-6-DNS-Noisy/Lab6_DNS_Noisy_Overview.txt)
# Wireshark Lab Collection
This repository contains packet-capture labs and notes from hands-on exercises (Wireshark + network labs).  
**Open `.pcapng` files locally with Wireshark** for full analysis.

> **Repo layout:** (file tree)
```
wireshhark-lab/
├─ Lab-Purposes.txt
├─ lab-01-baseline-browse/
│ ├─ baseline_browse (DNS queries, TLS handshakes).png
│ ├─ baseline_browse.pcapng
│ └─ win11_baseline_stream1.txt
├─ lab-2-follow-stream/
│ └─ win11_post_stream.txt
├─ lab-03-http-credential-leak/
│ ├─ Lab 3 Simulated HTTP Credential Leaak summary.txt
│ ├─ lab-03_http-credential-leak.png
│ ├─ tcp_8000_traffic.pcapng
│ ├─ win11_cleartext_post.pcapng
│ └─ win11_to_win10_http_post_capture.pcapng
├─ lab-04-syn-scan/
│ ├─ lab-04_synscan.pcapng
│ ├─ lab-04_synscan_tcpflags.png
│ ├─ Lab4-Port-Scan-Observations.txt
│ ├─ nmap -sS-192.168.1.100-scan-result.png
│ └─ tcp.flags.syn==1 && tcp.flags.ack==1.png
├─ lab-05-SMB & RDP Lateral Movement Lab/
│ ├─ lab-05 RDP Internal Access Lab.txt
│ ├─ RDP_Internal_Access from kali.png
│ ├─ RDP_Internal_Access kali to windows.png
│ ├─ smb_explorer_win10.png
│ ├─ SMB_Lab_Capture.txt
│ ├─ smb_lab_traffic.png
│ └─ smblab.pcapng
└─ lab-6-DNS-Noisy/
├─ dns_noisy_lab radnomdns.pcapng
├─ dns_noisy_lab.png
└─ Lab6_DNS_Noisy_Overview.txt
```
