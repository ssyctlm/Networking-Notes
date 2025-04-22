# Network Addressing

In networking, **addressing** is the system used to identify devices so they can communicate with each other. Every device on a network must have a unique address at each layer of the communication process.

---

## IP Addressing

An **IP address** (Internet Protocol Address) is a logical identifier assigned to each device on a network, used for identifying the sender and receiver of packets.

There are two major versions of IP addressing:

---

### IPv4

**IPv4 (Internet Protocol version 4)** is the most widely used version of IP addressing.

- **Address Length:** 32 bits.
- **Format:** Written as 4 decimal numbers separated by dots.
- **Example:** `192.168.1.10`

### IPv4 Address Classes:

| Class  | Address Range         | Default Subnet Mask  | Usage                    |
|--------|------------------------|-----------------------|---------------------------|
| A      | 1.0.0.0 – 126.255.255.255 | 255.0.0.0         | Large networks           |
| B      | 128.0.0.0 – 191.255.255.255 | 255.255.0.0      | Medium networks          |
| C      | 192.0.0.0 – 223.255.255.255 | 255.255.255.0    | Small networks           |
| D      | 224.0.0.0 – 239.255.255.255 | N/A              | Multicast                |
| E      | 240.0.0.0 – 255.255.255.255 | N/A              | Reserved for research    |

---

### IPv6

**IPv6 (Internet Protocol version 6)** was introduced to solve IPv4's exhaustion problem.

- **Address Length:** 128 bits.
- **Format:** Written as 8 groups of hexadecimal numbers, separated by colons.
- **Example:** `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

### IPv6 Advantages:

- Vastly larger address space.
- Simplified packet header.
- Built-in security (IPSec).
- Improved support for mobile devices.
- Eliminates need for NAT (Network Address Translation) in most cases.

---

## Subnetting & CIDR

### Subnetting

**Subnetting** is the process of dividing a larger network into smaller, more efficient sub-networks.

### Why Subnet?

- Efficient IP address usage.
- Improved network performance.
- Simplified management and isolation.

Example:
A company has `192.168.1.0/24` and splits it into two subnets:

| Subnet           | Range                    | Usable Hosts |
|------------------|---------------------------|--------------|
| `192.168.1.0/25` | `192.168.1.1` – `192.168.1.126` | 126          |
| `192.168.1.128/25` | `192.168.1.129` – `192.168.1.254` | 126      |

---

### CIDR (Classless Inter-Domain Routing)

**CIDR** notation replaces class-based addressing by using the **prefix length** to define the network portion.

Format: `IP_address/Prefix_length`

Example:
- `192.168.1.0/24` → First 24 bits are the network part.
- `2001:db8::/32` → First 32 bits are the network part in IPv6.

CIDR allows flexible allocation of IP addresses, improving routing efficiency and reducing wasted IP space.

---

## MAC Address

A **MAC Address (Media Access Control Address)** is a physical address assigned to a device’s network interface card (NIC).

### Characteristics:

- **Length:** 48 bits.
- **Format:** Six groups of two hexadecimal digits, separated by colons.
- **Example:** `00:1A:2B:3C:4D:5E`

### Purpose:

- Uniquely identifies hardware at **Layer 2 (Data Link Layer)**.
- Used in local communication within the same network segment.
- Assigned by the manufacturer (burned into the NIC).

---

## Address Resolution Protocol (ARP)

**ARP** is a protocol used to map **IP addresses** to **MAC addresses** on a local network.

### How ARP Works:

1. Device A wants to send a packet to an IP address.
2. Device A checks its ARP table for the corresponding MAC address.
3. If the MAC address isn’t known:
   - Device A broadcasts an **ARP Request**:  
     "Who has IP `192.168.1.20`? Tell `192.168.1.10`."
4. Device B (if it's `192.168.1.20`) replies with an **ARP Reply**.
5. Device A stores the response in its ARP table for future use.

---

## Summary Table

| Concept               | Purpose                                      | Layer         |
|------------------------|----------------------------------------------|---------------|
| IPv4 Addressing        | Logical addressing (32-bit)                  | Layer 3 (Network) |
| IPv6 Addressing        | Logical addressing (128-bit)                 | Layer 3 (Network) |
| Subnetting & CIDR      | Network segmentation, efficient allocation   | Layer 3 (Network) |
| MAC Address            | Physical hardware address                    | Layer 2 (Data Link) |
| ARP                    | Resolves IP to MAC for local delivery        | Between Layer 2 & 3 |




