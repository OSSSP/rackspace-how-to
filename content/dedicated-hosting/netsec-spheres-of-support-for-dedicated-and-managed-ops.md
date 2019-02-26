---
permalink: netsec-spheres-of-support-for-dedicated-and-managed-ops
title: NetSec Spheres of Support
type: article
created_date: '2019-02-25'
created_by: Adrian Bekele
last_modified_date: '2019-02-25'
last_modified_by: Adrian Bekele
product: Dedicated Hosting
product_url: dedicated-hosting
---

The Spheres of Support lists the technologies and features in the Network Security domain and defines support level for each item. It a pplies to Enterprise, SMB, US, International, unless otherwise noted.

Note that International NetSec also supports devices and technologies that are maintained by Security Support in the US. The support level of these features is described separately in Security Support Spheres of Support.


### Terminology

*  Supported - setup, configuration and troubleshooting.
*  Partial - setup, limited types of configuration and full troubleshooting of the supported configurations.
*  Reasonable endeavor - setup, attempt of configuration and attempt of troubleshooting.
   *   Use warning below when configuring a reasonable endeavor feature. 
*  Not supported - no setup or configuration provided.
   *   If an unsupported feature has to be supported on a device, this one-off has to be mentioned in the DMG by the Account Manager or the Lead Tech.
    
    
### Firewalls

|   | Feature | Cisco ASA | Juniper SRX |
| :---: |:--- | :--- | :--- |
| **Interfaces** |VLAN tagged (Cisco trunk)| Yes | Yes |
||VLAN untagged (Cisco access)| Yes | Yes |
||LACP bundling with number of interfaces is a power of 2| Yes | Yes |
| **Routing** |Static routing| Yes | Yes |
||Static routing with IP SLA tracking| Yes |  |
| **IPv6** |Static routing| Yes | Yes |
||Static routing with IP SLA tracking| Yes |  |
| **NAT** |Static (one-to-one)| Yes | Yes |
||PAT (NAT overloading)| Yes | Yes |
||Policy NAT/PAT| Yes | Yes |
||DNS Doctoring| Yes | Yes |
||Connection limits via static NAT| Yes | N/A |
| **Packet filtering** |Layer 3/4 filtering ingress/egress| Yes | Yes |
||FQDN based filtering| Yes | Yes |
||Outbound ACL| Yes | N/A |
| **DDoS Mitigation** |Connection limiting (Embryonic and/or established)  |Yes| Yes|
||Connection timeouts |Yes| Yes|
||TCP normalization modification  || Yes|
||Application inspection  || Yes|
| **VPN** |Route-based VPNs - BGP  |Yes| Yes|
||Route-based VPNs - Static |Yes| Yes|
||IPsec - IKEv2 L2L with PSK  |Yes| Yes|
||IPsec LAN-to-LAN Layer 3/4 filtering  |Yes| Yes|
||IPsec LAN-to-LAN Pre-shared keys authentication |Yes| Yes|
||IPsec LAN-to-LAN Hub and spoke configuration  |Yes| Yes|
||IPsec remote access with group authentication |Yes| |
||IPsec remote access with group and user authentication  |Yes| |
||IPsec remote access with two-factor authentication  |Yes| |
||IPsec remote access - Multiple VPN groups |Yes| |
||IPsec remote access with layer 3/4 filtering  |Yes| |
||IPsec remote access - Split-tunneling |Yes| |
||IPsec remote access - all traffic through VPN (tunnel all)  |Yes| |
||IPsec remote access - DNS server assignment |Yes| |
||IPsec remote access - Client certificate-based authentication || |
||SSL VPN AnyConnect Plus |Yes|N/A|
||SSL VPN - Mobile client (Plus license feature)  |Yes|N/A|
||SSL VPN - Two-factor authentication |Yes|N/A|
| **Management** |  Buffered Logging  |Yes| Yes|
||Log shipping to log correlation device within customer's account  |Yes| Yes|
||SNMP read-only for customer |Yes| Yes|
| **High Availability (HA)** |  Active/Standby (stateful and non-stateful) (clustering - SRX)<Br/>ASA 5510 and above, ASA-X 5508, 5515 and above |Yes|Yes|
| **Modes and modules** | Mode - Multi-Context Routed |Yes|N/A|
||Mode - Routed |Yes| Yes|
| **RackConnect** | RackConnect VLANs termination |Yes| |
| **RackConnect Global** |  RackConnect Global Classic Static |Yes| Yes|
||RackConnect Global 2.0 Static - BGP |Yes| |
||RackConnect Global 2.1 Static - BGP (with TOR)  |Yes| |


### Load balancers

| | Feature | F5 LTM | Brocade ADX | NetScaler VPX^ | NetScaler MPX^^|
| :---: |:--- | :--- | :--- | :--- | :--- |
| **Interfaces** |  VLAN tagged (Cisco trunk) |Yes|Yes||Yes|
||VLAN untagged (Cisco access)  |Yes|Yes|Yes|Yes|
| **Routing** | Static Routes |Yes|Yes|Default route|Yes|
| **IPv6** |  Static Routes |Yes|Yes| Default route|Yes|
| **Packet filtering** |  Layer 3/4 Ingress/Egress |US - Yes <Br/>Intl - |Yes|||
| **NAT** | Static (one-for-one)  |Yes|Yes|||
||PAT (NAT overload)  |Yes|Yes|||
||Source NAT pools on Virtual Servers |Yes|Yes|Yes|Yes|
| **Load balancing** |  Local Servers Servers behind the LB |Yes|Yes||Yes|
||Remote Servers in front of the LB |Yes|Yes|Yes|Yes|
||Parallel Servers sitting as a neighbor to the LB  |Yes|Yes|Yes|Yes|
||Algorithms - Static (Round Robin or Weighted Round Robin) |Yes|Yes|Yes|Yes|
||Algorithms - Dynamic (Least Connections)  |Yes|Yes|Yes|Yes|
||Healthchecks - ICMP echo  |Yes|Yes|Yes|Yes|
||Healthchecks - Layer 4 TCP (Port Socket Check) and UDP (Port Rejection) |Yes|Yes|Yes|Yes|
||Healthchecks - Layer 7 HTTP (Response Code, String Search, Checks on non well-known ports)  |Yes|Yes|Yes|Yes|
||Healthchecks - Layer 7 HTTPS (SSL hello, Response Code, String Search, Checks on non well-known ports)  |Yes|Yes|Yes|Yes|
||TCP/UDP Virtual Servers (Catchall, Single Port) |Yes|Yes|Yes|Yes|
||SNAT  |Yes|Yes|Yes|Yes|
||HTTP Redirects  |Yes|Yes|Yes|Yes|
||URI Load Balancing  |Yes|Yes|Yes|Yes|
||SSL Offloading  |Yes|Yes|Yes|Yes|
||Pools - Single Node: port combination (multiple ports on a server)  |Yes|Yes|Yes|Yes|
||Pools - Connection Limits (Pool, Node)  |Yes|Yes|Yes|Yes|
||LB - Pools - Group monitor applied to all pool members  |Yes|N/A|Yes|Yes|
||LB - Pools - Individual monitors applied to each pool member  |Yes|Yes|Yes|Yes| 
||LB - Pools - Combination of individual and group monitors across different pool members |Yes|N/A|Yes|Yes|
||LB - Application Profiles - HTTP (OneConnect, Custom HTTP Profile settings) |Yes|N/A|Yes|Yes|
||LB - Application Profiles - SSL (Client and Server) |Yes|Yes|Yes|Yes|
||LB - Application Profiles - FTP (Active and Passive)  |Yes|N/A|Yes|Yes|
||Persistence - TCP - Source IP |Yes|Yes|Yes|Yes|
||Persistence - HTTP cookie: LB generated, server generated |Yes|Yes|Yes|Yes|
||Persistence - HTTP Custom cookie name |Yes|N/A|Yes|Yes|
||Persistence - Cookie encryption |Yes|N/A|Yes|Yes|
||Persistence - UDP - Source IP |Yes|Yes|Yes|Yes|
||LB - Virtual Servers - SNAT Pools |Yes|Yes|Yes|Yes|
| **Scripting** | iRule 0006  |Yes||N/A|N/A|
| **Management** |  Logging - Local Buffered Logging  |Yes|Yes|Yes|Yes|
||Logging - Log shipping to log correlation device (Within customer's account)  |Yes|Yes|Yes|Yes|
||Management - SNMP read-only for customer  |Yes|Yes|Yes|Yes|
| **High availability (HA)** |  High availability |Yes 1600 and above  |Yes ADX 1000 only |Yes|Yes|
||HA - Active/Standby |Yes|Yes|Yes|Yes|
| **Modes and Modules** | Routed (Single and Multiple Route Domains) Default gateway for back end servers |Yes|Yes||Yes|
||Routed (Single and Multiple Route Domains) t the default gateway for back end servers |||||
||Multiple Segments behind LB |Yes|Yes||Yes<Br/>Interface filtering is |
| **RackConnect** | RackConnect VLANs termination |Yes| for RCV2<Br/>Yes for RCv3 |||
| **RackConnect Global** |  RackConnect Global Classic Static |Yes(AFM only)||||
| **SSL VPNs** |  SSL Client VPN on edge Big-IPs using APM module |Yes|N/A|||
| **SNI** | Server Name Indication  |Yes|Yes|Yes|Yes|

^ VPX - Product in EA soon to be LA

^^ MPX - Product not launched, supportability is only planned at this stage.
  
### Global load balancer

|| Feature | F5 GTM |  ADX GSLB | NetScaler VPX | NetScaler MPX|
| :--- |:--- | :--- | :--- | :--- | :--- |
| **Interfaces** |  VLAN tagged (Cisco trunk)|Yes|ALL GSLB currently reasonable endeavor|All GSLB currently unsupported|All GSLB currently unsupported|
||VLAN untagged (Cisco access)  |Yes| |||     
||LACP bundling with number of interfaces is a power of 2 |Yes|||| 
| **Routing** | Static routes |Yes||||
| **IPv6** |  Static routes |Yes||||
| **Load balancing** |  Single Listener Address |Yes||||
||Servers - BIG-IP System (Single)  |Yes||||
||Servers - BIG-IP System (Redundant pair)  |Yes||||
||Virtual Servers - Manual Configuration  |Yes||||
||Wide IPs - Standard FQDN Names  |Yes||||
||Wide IPs - Standard FQDN Alias Names  |Yes||||
||Wide IPs - Single Pool, Multiple Virtual Server Members |Yes||||
||Algorithms - Static - Round Robin, Ratio (Weighted Round Robin), Global Availability  |Yes||||
||Algorithms - Dynamic - Least Connections  |Yes||||
| **DNS** | Authoritative Name Server for Specific Subdelegated Domains |Yes||||
| **Management** |  Buffered Logging  |Yes||||
||Log shipping to log correlation device (Within customer's account)  |Yes||||
| **High availability (HA)** |  Synchronization Groups  |Yes||||
||Redundant GTM Devices specified as primary and secondary DNS servers  |Yes||||
| **Modes and modules** | Serial configuration  |Yes||||
||Paralled configuration  |Yes||||
||Standalone BigIP with GTM License |Yes||||


### Cisco CSS
End of support on September 30, 2014. Customers that continue using the platform will be in the Extended Lifecycle Support. All the support will be Reasonable endeavor.

### Redhill WebMux
End of support. Customers that continue using the platform will be in the Extended Lifecycle Support . All the support will be Reasonable endeavor.

### General topics
| Feature | Support le
| DDoS mitigation | Supported|
