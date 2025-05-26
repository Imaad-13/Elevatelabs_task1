# 🕵️ Wireshark Packet Capture Notes

## 📍 Objective
Capture and analyze packet traffic on the local network using Wireshark to identify protocols in use, potential anomalies, and general network behavior.

---

## 🔧 Capture Details
- **Interface used**: wlan0 (WI-Fi)
- **Capture duration**: 3 minutes
- **Filters applied**: 
  - Display filter: `ip.addr == 192.168.1.10`
  - Protocol filter: `http`, `dns`, `tcp.port == 80`, etc.

---

## 🧪 Observations
- High number of DNS requests originating from one host.
- HTTP traffic with unencrypted GET requests observed.
- ICMP Echo Requests (ping) between two internal hosts.
- TCP handshake failures, possibly due to blocked ports or firewalls.

---
## 📦 Notable Protocols Seen
| Protocol | Description |
|----------|-------------|
| DNS      | Name resolution activity |
| HTTP     | Unencrypted web traffic |
| TCP      | Transport layer sessions |
| ICMP     | Ping requests/responses |

---

## ✅ Conclusion
The Wireshark capture gives visibility into real-time network activity. Further inspection of DNS and HTTP patterns may reveal risky behavior. The capture also helps verify which devices are actively communicating on the network.

