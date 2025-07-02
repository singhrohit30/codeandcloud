# 🌐 Networking Concepts — Core Basics

This document covers the essential networking concepts that every cloud or DevOps engineer should understand: **IP addresses, subnets & CIDR, and ports.**

---

## 📍 IP Addresses

An **IP address** is like a postal address for your device on a network — it uniquely identifies where to send data.

### Types of IP addresses

| Type      | Example            | Where Used         |
|-------------|----------------|----------------|
| Public IP | 142.250.190.78 | Internet servers, websites (e.g., google.com) |
| Private IP | 192.168.1.10    | Home or office networks (LAN) |

---

### IPv4 vs IPv6

- **IPv4**: Most common, e.g., `192.168.0.1`.  
- **IPv6**: Newer, longer addresses (e.g., `2001:0db8:85a3::8a2e:0370:7334`) — designed to solve IPv4 exhaustion.

---

## 🗺️ Subnets & CIDR

### What is a subnet?

A **subnet** divides a big network into smaller parts to:

- Reduce congestion
- Improve security
- Better manage IP allocation

---

### CIDR notation

**CIDR** = Classless Inter-Domain Routing

Format: 192.168.1.0/24


- `192.168.1.0` → Network address
- `/24` → Number of bits used for network prefix (remaining bits for hosts)

---

### How to calculate usable IPs

Usable IPs = 2^(32 - subnet bits) - 2


#### Example: `/24`

- Host bits: 32 - 24 = 8
- Usable IPs: 2^8 - 2 = **254**

---

### Visual diagram of `/24` subnet

192.168.1.0/24
├─ Network address: 192.168.1.0
├─ First usable: 192.168.1.1
├─ Last usable: 192.168.1.254
└─ Broadcast: 192.168.1.255


---

#### Common subnet sizes

| CIDR  | Host bits | Usable IPs |
|---------|-----------|-------------|
| /30    | 2       | 2           |
| /29    | 3       | 6           |
| /24    | 8       | 254        |
| /16    | 16     | 65,534  |

---

## 🚪 Ports

A **port** is like a door or channel on your device used by different services to communicate.

---

### Common ports

| Service | Port number |
|-----------|-----------|
| HTTP     | 80        |
| HTTPS    | 443     |
| SSH       | 22       |
| DNS      | 53       |
| MySQL  | 3306    |

---

### Why do we need ports?

A single machine can run multiple services simultaneously — each service listens on a **different port**, so the OS knows where to route the incoming data.

---

### Example

ssh user@203.0.113.5

- Uses **port 22** by default for SSH.

https://example.com


- Uses **port 443** (HTTPS).

---

## 💡 Quick Recap

✅ **IP address**: Your device's address on the network.  
✅ **Subnet & CIDR**: Divide networks and define IP ranges.  
✅ **Ports**: Entry points for specific services.

---

### 📖 Further reading

- [IANA Service Name and Port Number Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)
- [CIDR to IP Range Calculator](https://www.ipaddressguide.com/cidr)

---

⭐ *Keep this as your quick networking cheat sheet!*


