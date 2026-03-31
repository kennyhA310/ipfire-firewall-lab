# IPFire Firewall Lab 🔥

## Overview
This project demonstrates building a segmented network using IPFire firewall in a virtual environment. The lab simulates real-world network security by separating LAN and wireless networks and enforcing firewall rules to control traffic flow.

## Lab Architecture

- **GREEN (LAN):** 192.168.XX.X
- **BLUE (Wireless):** 192.168.XX.X
- **RED (Internet):** DHCP (External Network)

## Tools Used
- IPFire Firewall
- Oracle VirtualBox
- Ubuntu (Target Machine)
- Windows Host Machine

## Network Configuration

| Interface | Purpose | IP Address |
|----------|---------------|------------------|
| GREEN | Internal LAN | 192.168.10.1 |
| BLUE | Wireless LAN | 192.168.20.1 |
| RED | Internet | DHCP Assigned |

## Firewall Rules Implemented

1. **Block Wireless to LAN**
- Source: BLUE (192.168.20.0/24)
- Destination: GREEN (192.168.10.0/24)
- Action: DROP

2. **Allow Wireless to Internet**
- Source: BLUE
- Destination: RED
- Action: ACCEPT

## Testing & Validation

- ✅ Verified internet access from BLUE network
- ❌ Blocked ICMP (ping) from BLUE to GREEN
- ✅ Confirmed LAN access remains functional

## Key Concepts Demonstrated

- Network Segmentation
- Firewall Rule Configuration
- Traffic Filtering
- Internal Network Protection
- Basic Security Architecture

## Screenshots
<img width="809" height="440" alt="Screenshot 2026-03-30 224902" src="https://github.com/user-attachments/assets/f090e826-08d9-43ba-a9ca-868c6b4c4c1d" />
<img width="1150" height="776" alt="Screenshot 2026-03-28 111805" src="https://github.com/user-attachments/assets/78a24b87-01e1-452c-abb7-7d7e01d83599" />
<img width="1109" height="618" alt="Screenshot 2026-03-28 111748" src="https://github.com/user-attachments/assets/8afed95e-5759-4b51-ba81-9d4b0558b64b" />

- IPFire dashboard & Firewall rules
- Network configuration
- Successful/failed ping tests

## Lessons Learned

- Proper segmentation prevents lateral movement
- Firewall rules must be tested to confirm effectiveness
- Virtual labs can simulate real enterprise environments

## 📌 Project Highlights

- Built a segmented virtual network using IPFire firewall
- Implemented access control policies between network zones
- Validated firewall behavior through real-world testing scenarios

