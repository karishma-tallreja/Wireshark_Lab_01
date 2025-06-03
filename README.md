# Wireshark_Lab_01 - Host-Only HTTP Traffic Capture

## Objective
To analyze HTTP traffic between a Windows host and a DSL virtual server using Wireshark on a Host-Only network (VMnet1).

### Tools and Setup
- Wireshark
- VMware Workstation
- DSL Linux Server
- Host-Only Network (VMnet1)
- PuTTY

### 🧾 Steps Performed
1. Set up a host-only network and verify connectivity using `ping`.
2. Captured packets using Wireshark on the VMnet1 adapter.
3. Accessed a web page hosted on the DSL server.
4. Filtered HTTP traffic and analyzed HTTP GET requests.

### 📌 Key Observations
- HTTP GET request successfully captured.
- TCP 3-way handshake observed.
- Protocols like ICMPv6, DNS, and TCP were also present.
- Confirmed browser caching behavior (e.g., HTTP 304 Not Modified).

https://imgur.com/a/6x8oMKN 

## 📸 Key Screenshots

### 1. Interface Detection by Wireshark
![Wireshark Interfaces](https://i.imgur.com/9hDwoci.png)
*Detected all active interfaces like Ethernet, VMnet1, VMnet8 before starting packet capture.*

---

### 2. Accessing Local Web Server (index page)
![Index Page Access](https://i.imgur.com/wBqNnIt.png)
*Accessed http://192.168.217.134/ — the default index page of the local server.*

---

### 3. Wireshark Capture of HTTP Traffic
![Wireshark HTTP](https://i.imgur.com/vwfuMWG.png)
*Captured packets while accessing INTRO-wireshark.html. Expanded HTTP layer to view GET request and headers.*

---

### 4. Wireshark-labs Directory Access
![Wireshark Labs Directory](https://i.imgur.com/Jd1h0I6.png)
*Browsed to http://192.168.217.134/wireshark-labs/ and observed server response in Wireshark.*

---

📂 **For more sequential screenshots and detailed steps, view the full album [here](https://imgur.com/a/6x8oMKN).**


### What I Learned / Skills
- Set up VMware Host-Only network (VMnet1)
- Verified connectivity using ping on Windows and Linux VMs
- Captured and filtered packets with Wireshark (focused on HTTP traffic)
- Analyzed HTTP GET requests and response codes (e.g., 304 Not Modified)
- Used Linux commands (ifconfig, ping) in DSL VM
- Interpreted Ethernet, IP, TCP, and HTTP packet details
- Cleared browser cache and restarted captures for accurate results
- Connected to Linux VM via PuTTY SSH terminal
