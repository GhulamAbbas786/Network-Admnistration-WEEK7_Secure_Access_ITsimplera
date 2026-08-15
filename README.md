
🌐 Enterprise Secure Network Architecture & Verification Lab

📌 Overview

This repository contains the complete network architecture, troubleshooting documentation, and verification reports for a two-site enterprise topology built using GNS3. The project simulates a secure site-to-site WAN deployment connecting Headquarters and Branch routers.

🚀 Key Architecture & Features
🛡️ 1. Secure Site-to-Site VPN
IPsec & ISAKMP: Configured cryptographic parameters with alignment on transform-sets and ACLs to ensure secure, encrypted communication.

Connectivity: Full encrypted packet transit between internal subnets.

🧱 2. Perimeter Security & ZBF
Zone Separation: Configured INSIDE and OUTSIDE zones.

Traffic Inspection: Implemented inspection policies (ZP-INSIDE-TO-OUTSIDE) and enforced a Default Deny policy to drop unsolicited incoming traffic.

⚙️ 3. Routing & Hardening
OSPFv2 Routing: Established dynamic routing with MD5 authentication.

AAA & SSHv2: Secured administrative access to mitigate lockout risks.

⏱️ 4. Monitoring & Management
NTP: Headquarters as Master time source; Branch as client.

Syslog: Comprehensive informational-level logging.

SNMPv3: Secure administrative group and view definitions.

📊 Verification & Testing
The project includes a formal verification matrix covering:

✅ IPsec SA and Encapsulation counters.

✅ Zone-Based Firewall packet inspection.

✅ OSPF neighbor convergence.

✅ NTP clock synchronization.
