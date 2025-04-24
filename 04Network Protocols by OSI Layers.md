# Network Protocols by OSI Layers

Network protocols are standardized rules that define how data is transmitted and received across networks. These protocols operate at different layers of the OSI model. Below is a breakdown of key protocols categorized by their respective OSI layers.

---

## Application Layer Protocols

These protocols operate at the top of the OSI model (Layer 7) and directly interface with end-user applications. They define how application processes communicate over a network.

### 1. HTTP (Hypertext Transfer Protocol)
- **Purpose:** Transfers web pages over the internet.
- **Port:** 80 (TCP)
- **Characteristics:**
  - Stateless
  - Plaintext (not secure)
- **Used for:** Web browsing, REST APIs.

### 2. HTTPS (Hypertext Transfer Protocol Secure)
- **Purpose:** Secure version of HTTP using SSL/TLS encryption.
- **Port:** 443 (TCP)
- **Used for:** Secure web communication (banking, e-commerce, etc.).

### 3. FTP (File Transfer Protocol)
- **Purpose:** Transfers files between client and server.
- **Ports:** 20 (data), 21 (control) (TCP)
- **Used for:** Uploading/downloading files to/from servers.

### 4. SFTP (SSH File Transfer Protocol)
- **Purpose:** Secure file transfer over SSH.
- **Port:** 22 (TCP)
- **Used for:** Secure file management and transfers.

### 5. DNS (Domain Name System)
- **Purpose:** Translates human-readable domain names into IP addresses.
- **Port:** 53 (UDP/TCP)
- **Used for:** Website access (e.g., converting `google.com` to `142.250.190.14`).

### 6. DHCP (Dynamic Host Configuration Protocol)
- **Purpose:** Automatically assigns IP addresses and other network settings to devices.
- **Ports:** 67 (server), 68 (client) (UDP)
- **Used for:** Simplified IP management in dynamic networks.

---

## Transport Layer Protocols

These protocols work at OSI Layer 4, providing reliable or unreliable data delivery between hosts.

### 1. TCP (Transmission Control Protocol)
- **Type:** Connection-oriented
- **Features:**
  - Ensures data delivery
  - Performs error checking
  - Supports flow control and congestion control
- **Used for:** HTTP/HTTPS, FTP, email.

### 2. UDP (User Datagram Protocol)
- **Type:** Connectionless
- **Features:**
  - Fast but unreliable
  - No error checking or delivery guarantee
- **Used for:** Streaming, VoIP, DNS, gaming.

---

## Network Layer Protocols

Protocols here work at OSI Layer 3 and deal with logical addressing and routing of packets.

### 1. IP (Internet Protocol)
- **Purpose:** Provides logical addressing and routes packets between networks.
- **Versions:**
  - IPv4: 32-bit addressing
  - IPv6: 128-bit addressing
- **Key Feature:** Stateless protocol used for best-effort delivery.

### 2. ICMP (Internet Control Message Protocol)
- **Purpose:** Used for network diagnostics and error reporting.
- **Used by:** Tools like `ping` and `traceroute`.
- **Example:** If a packet can't reach its destination, ICMP may send a "destination unreachable" message.

---

## Data Link Layer Protocols

These protocols operate at OSI Layer 2, ensuring reliable transmission between directly connected nodes.

### 1. Ethernet
- **Purpose:** Standard protocol for wired LANs.
- **Functionality:**
  - Uses MAC addresses for addressing
  - Supports speeds from 10 Mbps to 100 Gbps+
- **Frame structure includes:** Header, payload, trailer (with CRC).

### 2. ARP (Address Resolution Protocol)
- **Purpose:** Maps IP addresses to MAC addresses.
- **Layer:** Interface between Layer 3 (IP) and Layer 2 (MAC).
- **Functionality:** Sends a broadcast to find the MAC address associated with a known IP.

---

## Summary Table

| Layer         | Protocols                                      | Key Functions                                         |
|---------------|------------------------------------------------|------------------------------------------------------|
| Application   | HTTP, HTTPS, FTP, SFTP, DNS, DHCP              | Web, file transfer, name resolution, IP assignment   |
| Transport     | TCP, UDP                                       | Reliable/unreliable data delivery                    |
| Network       | IP, ICMP                                       | Logical addressing, routing, diagnostics             |
| Data Link     | Ethernet, ARP                                  | Physical addressing, MAC-to-IP mapping               |

---

## Summary

- Each protocol operates at a specific OSI layer but often interacts with others.
- Understanding the role of each helps in diagnosing network problems.
- For practical use: knowing ports, function, and behavior is essential (e.g., firewalls, security settings, protocol sniffing with Wireshark).

