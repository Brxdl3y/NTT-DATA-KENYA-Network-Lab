**NTTT DATA KENYA** – Enterprise Network Topology

**Summary**

This project presents a sophisticated enterprise-grade network design for **NTTT Data Kenya**. The architecture demonstrates not only technical proficiency in Cisco networking but also the pragmatic principles of **redundancy, scalability, and cost efficiency**; essential for real-world enterprise deployments.

The design includes multiple departments **(Sales, Finance, HR, Help Desk, Data Center, and Network Operations Center)** with logical VLAN segmentation, trunking, secure routing to the ISP, and robust Layer 3 switching for inter-VLAN routing. Security is elevated using MD5 authentication on routing protocols, while redundancy and resilience are factored into the distribution-core-access hierarchy.

This configuration highlights a professional yet creative approach, balancing theoretical best practices with practical deployment strategies.


**Design Goals & Rationale**

**Availability & Redundancy**: EtherChannel between Distribution and Core, HSRP for gateway redundancy, and IP SLA checks for failover of ISP links. These choices reduce single points of failure while staying cost-sensitive.

**Scalability**: Hierarchical design (Core → Distribution → Access). VLANs mapped to functional groups (Sales, Finance, HR, Ops, Data Center) so growth is predictable.

**Security & Segmentation**: ACLs at the edge and inter‑VLAN ACLs where necessary; port‑security on access ports; routed boundaries for sensitive segments (Data Center, NOC, Ops).

**Manageability & Observability**: SNMP, NTP, Syslog centralized to a logging host; descriptive interface names and a consistent addressing/naming scheme.

**Cost‑Effective**: Start with WISP/fiber mix for last‑mile if needed; minimize expensive licensed features; use standard commodity devices for access and push complexity to distribution/core.


**Technical Highlights**

**Trunk and Access Port Design**: Access ports tied to specific VLANs; trunks interconnect switches for VLAN propagation.

**VLANs**: Logical segmentation for Sales, Finance, HR, Data Center, Help Desk, and Operations Center.

**ROAS (Router-on-a-Stick)**: Sub-interfaces configured for each VLAN on the router.

**Inter-VLAN Routing**: Layer 3 Switch SVIs with IP routing enabled.

**MD5 Authentication**: Secure routing sessions with neighbor routers.

**Default Routes**: Gateway to ISP for external connectivity.

**IP Subnetting**: Optimized addressing plan for departmental isolation.

**Serial Interface**: Configured serial interfaces with a clockrate of 64000 at the DCE and PPP encapsulation; this boosts the performance and efficiency. 


**Creative additions I added**

**HSRP** on core SVIs for gateway redundancy (shows enterprise awareness).

EtherChannel (LACP) between Core and Distribution to increase throughput and simplify STP.

**IP SLA + Track** on ISP links so default route failover is graceful (useful for recruiters wanting high‑availability thinking).

ACL templates for east‑west and internet filtering with explicit allow/deny rationale—practical and interview‑ready.

Netflow/sFlow placeholder config note: easy to add if the company wants traffic analytics — demonstrates telemetry awareness.


**Conclusion**

This project is more than a lab topology — it’s a case study in enterprise network design thinking. By blending **VLAN segmentation, secure routing, redundancy, and scalability** into one architecture, the design demonstrates a **holistic engineering mindset.**

For recruiters: this showcases not only the ability to configure devices but also to **design resilient, efficient, and cost-effective networks** in line with modern enterprise demands.

AUTHOR - **BRADLEY GIOVANNI** | **ASPIRING NEWTORK ENGINEER**  |  **NETWORK ADMINISTRATOR**  |

EMAIL - **giovanniibradley@gmail.com**

 [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/bradley-giovanniii293) 
