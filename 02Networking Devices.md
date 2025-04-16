# Networking Devices

Understanding these devices like hub, switch and router is fundamental to understanding how networks function.

---

## Hubs

A **Hub** is a basic networking device that connects multiple Ethernet devices, making them act as a single network segment.

### Key Functions:
- Operates at **Layer 1 (Physical Layer)** of the OSI model.
- Forwards data to **all connected devices** (broadcasting) regardless of destination.
- Cannot filter or intelligently direct traffic.
- Increases the chance of collisions in larger networks.

### Example:
In older home or office networks, hubs were used to connect PCs, though switches have largely replaced them due to higher efficiency.

---

## Switches

A **Switch** is a device that connects multiple devices (computers, printers, servers) within the same **Local Area Network (LAN)** and forwards data only to the intended recipient.

`VLANs` and `subnets` are configured on switches 


### Key Functions:
- Operates at **Layer 2 (Data Link Layer)** of the OSI model.
- Uses **MAC addresses** to make forwarding decisions.
- Reduces unnecessary traffic compared to a hub.
- Improves network efficiency by creating **collision domains** per port.

- Switches and Hubs transfer frames 

### Example:
If PC1 sends a file to PC2 and their MAC addresses and ports have already record on the Mac address table, the switch ensures only PC2 receives the data, not all devices on the network.

---

## Routers

A **Router** connects different networks together and forwards data packets between them.

### Key Functions:
- Operates at **Layer 3 (Network Layer)** of the OSI model.
- Uses **IP addresses** to route data.
- Can connect a LAN to another LAN, or a LAN to the Internet.
- Performs **packet forwarding** and sometimes **Network Address Translation (NAT)**.
- **Broadcast domain** created on this layer(device)
- Routers transfer packet. 

### Example:
A home router connects your local Wi-Fi or Ethernet network to your Internet Service Provider (ISP).

---



## Access Points (AP)

An **Access Point** is a device that allows **wireless devices** to connect to a wired network.

### Key Functions:
- Operates at **Layer 2 (Data Link Layer)**.
- Extends wired LANs to wireless devices.
- Supports Wi-Fi standards (802.11a/b/g/n/ac/ax).
- Provides **wireless coverage** and handles **authentication and encryption**.

### Example:
A wireless access point in a café allows customers to connect to the internet over Wi-Fi.

---

## Modems

A **Modem** (Modulator-Demodulator) converts digital data from a computer to a signal suitable for a transmission medium and vice versa.

### Key Functions:
- Converts digital signals to analog for transmission over telephone lines or cable systems, and vice versa.
- Bridges **your ISP and your home network**.
- Essential for internet access over DSL, cable, or fiber connections.

### Example:
A cable modem converts digital data from a router to a signal that travels over coaxial cables to your ISP.

---

## Firewalls

A **Firewall** is a network security device that monitors and controls incoming and outgoing network traffic based on predefined security rules.

- Packet filter: Set of rules to handle specified packets
- Stateful firewall: Packet inspection for incoming network traffic
- Next-generation firewall(NGFW), OSI Layer7/application layerfirewall

### Key Functions:
- Operates at **Layer 3 (Network Layer)** or higher.
- Filters traffic based on **IP address, port numbers, or application-level data**.
- Prevents unauthorized access to private networks.
- Can be hardware, software, or a combination of both.

### Example:
A firewall blocks external threats from accessing internal systems while allowing safe web traffic.

---

## Gateways

A **Gateway** is a network node that acts as an interface between two different networks, often operating at multiple OSI layers.

### Key Functions:
- Translates data formats or protocols between networks.
- Can handle **protocol conversions, data encoding/decoding, and packet reformatting**.
- Acts as an entry and exit point for a network.

### Example:
A router that connects a local network to the Internet often acts as the gateway, translating internal private IP addresses to public ones.

---

## Summary Table

| Device         | OSI Layer               | Purpose                                      |
|----------------|--------------------------|----------------------------------------------|
| Switch         | Layer 2 (Data Link)      | Forwards frames within LAN using MAC addresses. |
| Router         | Layer 3 (Network)        | Routes packets between different networks.  |
| Hub            | Layer 1 (Physical)       | Broadcasts data to all connected devices.   |
| Access Point   | Layer 2 (Data Link)      | Connects wireless clients to wired networks. |
| Modem          | Physical/Data Link       | Converts digital and analog signals for WAN connections. |
| Firewall       | Layer 3+ (Network and above) | Filters and secures network traffic.     |
| Gateway        | Multiple layers          | Interfaces between different networks/protocols. |

---

## In summary

Each networking device has a specific role in the communication process:

- **Switches** handle internal LAN communication.
- **Routers** connect different networks.
- **Hubs** simply broadcast (rarely used today).
- **Access Points** enable wireless connectivity.
- **Modems** connect your network to your ISP.
- **Firewalls** protect your network.
- **Gateways** translate between different systems.

