# Network-Admnistration-WEEK7_Secure_Access_ITsimplera
This repository contains the complete network aThe project simulates a secure site-to-site WAN deployment connecting **Headquarters** and **Branch** routers, implementing advanced routing, VPN encryption, zone-based firewalls, AAA security, and network management services.

Enterprise Secure Network Architecture & Verification Lab
Overview
This repository contains the complete network architecture, troubleshooting documentation, and verification reports for a two-site enterprise topology built using GNS3. The project simulates a secure site-to-site WAN deployment connecting Headquarters and Branch routers, implementing advanced routing, VPN encryption, zone-based firewalls, AAA security, and network management services.

Key Architecture & Features
1. Secure Site-to-Site VPN
IPsec & ISAKMP (Phase 1 / Phase 2): Configured cryptographic parameters with alignment on transform-sets and ACLs to ensure secure, encrypted communication between sites (QM_IDLE state verified).

LAN-to-LAN Reachability: Full encrypted packet transit between internal subnets (192.168.1.0/24 and 192.168.2.0/24).

2. Perimeter Security & Zone-Based Firewall (ZBF)
Zone Separation: Configured INSIDE-ZONE and OUTSIDE-ZONE on the Headquarters router.

Traffic Inspection: Implemented inspection policies (ZP-INSIDE-TO-OUTSIDE) targeting ICMP, TCP, UDP, and OSPF traffic.

Default Deny Policy: Enforced strict perimeter rules where uninspected or unsolicited incoming traffic from the WAN is automatically dropped by the implicit class-default rule.

3. Routing & Device Hardening
OSPFv2 Routing: Established dynamic routing across Area 0 using MD5 authentication on point-to-point serial/WAN interfaces.

AAA & Secure Access: Secured administrative remote management via SSH version 2, backed by local user accounts and AAA authentication frameworks to mitigate lockout risks.

4. Management, Monitoring & Time Synchronization
NTP Master/Client Hierarchy: Configured Headquarters as an authoritative NTP master (ntp master 3), with the Branch router actively synchronizing time across the WAN.

Comprehensive Syslog Logging: Enabled local buffer logging (65535 buffer size), console logging, and monitor logging at the informational level on both routers.

SNMPv3 Management: Defined secure SNMPv3 groups (ITAdminGroup), views (AllView), and administrative user bindings supporting authentication and privacy (priv).

Verification & Testing
The project includes a formal verification matrix covering:

IPsec Security Associations & Encapsulation/Decapsulation counters.

Zone-Based Firewall packet inspection and class-default drop verification.

OSPF neighbor state convergence (FULL).

End-to-end encrypted ping tests and NTP clock synchronization.
