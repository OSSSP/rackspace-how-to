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
||LACP bundling with number of interfaces is not a power of 2| RE | RE |
| **Routing** |Static routing| Yes | Yes |
||Static routing with IP SLA tracking| Yes | RE |
||Dynamic routing protocols OSPF, EIGRP, BGP| RE | RE |
| **IPv6** |Static routing| Yes | Yes |
||Static routing with IP SLA tracking| Yes | RE |
||Dynamic routing protocols| No | No |
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
||TCP normalization modification  |RE| Yes|
||QoS |No |RE|
||regex HTTP inspection |No| No|
||Application inspection  |RE| Yes|
| **VPN** |Route-based VPNs - BGP  |Yes| Yes|
||Route-based VPNs - Static |Yes| Yes|
||IPsec - IKEv2 L2L with PSK  |Yes| Yes|
||IPsec LAN-to-LAN Layer 3/4 filtering  |Yes| Yes|
||IPsec LAN-to-LAN Pre-shared keys authentication |Yes| Yes|
||IPsec LAN-to-LAN Hub and spoke configuration  |Yes| Yes|
||IPsec LAN-to-LAN Cert-based authentication  |RE|N/A|
||IPsec DMVPN |No| No|
||IPSec remote access - Juniper |N/A|N/A|
||IPsec remote access with Cisco Client |No|N/A|
||IPsec remote access with Apple OS X native IPsec client |RE| No|
||IPsec remote access with Shrew Soft client  |RE| No|
||IPsec remote access with group authentication |Yes| No|
||IPsec remote access with group and user authentication  |Yes| No|
||IPsec remote access with two-factor authentication  |Yes| No|
||IPsec remote access - Multiple VPN groups |Yes| No|
||IPsec remote access with layer 3/4 filtering  |Yes| No|
||IPsec remote access - Split-tunneling |Yes| No|
||IPsec remote access - all traffic through VPN (tunnel all)  |Yes| No|
||IPsec remote access - DNS server assignment |Yes| No|
||IPsec remote access - Client certificate-based authentication |RE| No|
||IPsec remote access on Windows 8  |RE| No|
||SSL VPN - Juniper |N/A|N/A|
||SSL VPN AnyConnect Plus |Yes|N/A|
||SSL VPN AnyConnect Apex |No|N/A|
||SSL VPN - Mobile client (Plus license feature)  |Yes|N/A|
||SSL VPN - Certificate authentication  |RE|N/A|
||SSL VPN - Two-factor authentication |Yes|N/A|
||SSL VPN - Clientless SSL VPN  |No|N/A|
||SSL VPN - Secure desktop  |No|N/A|
| **Management** |  Buffered Logging  |Yes| Yes|
||Log shipping to log correlation device within customer's account  |Yes| Yes|
||Custom logging, logging lists |RE| RE|
||Log retention by Rackspace  |No| No|
||Log analysis, outside of troubleshooting an issue |No| No|
||Direct customer access if firewall is on TACACS |No| No|
||SNMP read-only for customer |Yes| Yes|
| **High Availability (HA)** |  Active/Standby (stateful and non-stateful) (clustering - SRX)<Br/>ASA 5510 and above, ASA-X 5508, 5515 and above |Yes|Yes|
||ASA 5505|No|N/A|
||Active/Active (stateful and non-stateful) |No| No|
||Clustering of more than two units |No| No|
| **Modes and modules** | Mode - Multi-Context Routed |Yes|N/A|
||Mode - Routed |Yes| Yes|
||Mode - Transparent  |No| No|
||Modules/Configs - Threat-detection  |RE|N/A|
||Modules/Configs - IPS Module  |No|N/A|
||Modules/Configs - Cisco Unified Communications Proxy  |No|N/A|
| **RackConnect** | RackConnect VLANs termination |Yes| No|
| **RackConnect Global** |  RackConnect Global Classic Static |Yes| Yes|
||RackConnect Global 2.0 Static - BGP |Yes| RE|
||RackConnect Global 2.0 Dynamic - BGP  |RE| RE|
||RackConnect Global 2.1 Static - BGP (with TOR)  |Yes| RE|
||RackConnect Global 2.1 Static - BGP (without TOR) |RE| RE|
||RackConnect Global 2.1 Dynamic - BGP  |RE| RE|
||RackConnect Global Public |RE| RE|
||RackConnect Global IPv6 |RE| RE|
||RackConnect Global - Server→SVI (bypass FW) |RE| RE|
| **Geolocation** | Block by Country  |RE| RE|
| **DHCP** |    |No|No|


### Load balancers

| | Feature | F5 LTM | Brocade ADX | NetScaler VPX^ | NetScaler MPX^^|
| :---: |:--- | :--- | :--- | :--- | :--- |
| **Interfaces** |  VLAN tagged (Cisco trunk) |Yes|Yes|No|Yes|
||VLAN untagged (Cisco access)  |Yes|Yes|Yes|Yes|
||LACP bundling with number of interfaces is a power of 2 |RE MAN|RE MAN|No|RE MAN|
||LACP bundling with number of interfaces is not a power of 2 |No|No|No|No|
| **Routing** | Static Routes |Yes|Yes|Default route|Yes|
||Dynamic Routing Protocols |No|No|No|No|
| **IPv6** |  Static Routes |Yes|Yes| Default route|Yes|
||Dynamic Routing Protocols |No|No|No|No|
| **Packet filtering** |  Layer 3/4 Ingress/Egress |US - Yes <Br/>Intl - RE|Yes|No|RE|
||Layer 7 |No|No|No|No|
| **NAT** | Static (one-for-one)  |Yes|Yes|No|No|
||PAT (NAT overload)  |Yes|Yes|No|No|
||Source NAT pools on Virtual Servers |Yes|Yes|Yes|Yes|
||One-to-many policy NAT  |RE|No|No|No|
| **Load balancing** |  Local Servers Servers behind the LB |Yes|Yes|No|Yes|
||Remote Servers in front of the LB |Yes|Yes|Yes|Yes|
||Parallel Servers sitting as a neighbor to the LB  |Yes|Yes|Yes|Yes|
||Algorithms - Static (Round Robin or Weighted Round Robin) |Yes|Yes|Yes|Yes|
||Algorithms - Dynamic (Least Connections)  |Yes|Yes|Yes|Yes|
||Algorithms - All Other  |RE|RE|RE|RE|
||Algorithms - Custom |No|No|No|No|
||Healthchecks - ICMP echo  |Yes|Yes|Yes|Yes|
||Healthchecks - Layer 4 TCP (Port Socket Check) and UDP (Port Rejection) |Yes|Yes|Yes|Yes|
||Healthchecks - Layer 7 HTTP (Response Code, String Search, Checks on non well-known ports)  |Yes|Yes|Yes|Yes|
||Healthchecks - Layer 7 HTTPS (SSL hello, Response Code, String Search, Checks on non well-known ports)  |Yes|Yes|Yes|Yes|
||Healthchecks - All Other Healthchecks |RE|RE|RE|RE|
||Healthchecks - Scripted Healthchecks  |RE|No|No|No|
||TCP/UDP Virtual Servers (Catchall, Single Port) |Yes|Yes|Yes|Yes|
||SNAT  |Yes|Yes|Yes|Yes|
||HTTP Redirects  |Yes|Yes|Yes|Yes|
||URI Load Balancing  |Yes|Yes|Yes|Yes|
||SSL Offloading  |Yes|Yes|Yes|Yes|
||Application Specific Virtual Servers  |RE|RE|RE|RE|
||CSW |N/A|RE|N/A|N/A|
||Virtual Servers - Data Modification/Insertion/Deletion within the payload |No|No|No|No|
||Virtual Servers - Regex |No|No|No|No|
||Virtual Servers - Rate-Limiting |No|No|No|No|
||Pools - Single Node: port combination (multiple ports on a server)  |Yes|Yes|Yes|Yes|
||Pools - Priority Group Activation |Yes|N/A|N/A|N/A|
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
||Application Profiles - Statistics |RE|N/A|N/A|N/A|
||HTTP (HTTP classes, caching, compression) |RE|N/A|RE|RE|
||Application profiles not listed above |No|No|No|No|
||LB - Virtual Servers - SNAT Pools |Yes|Yes|Yes|Yes|
||LB - Virtual Servers - Traffic Cloning (client and server side) |RE|N/A|RE|RE|
||LB - Virtual Servers - Traffic Classification |No|No|No|No|
| **Scripting** | iRule 0006  |Yes|No|N/A|N/A|
||Standardized scripted rules (iRules, OpenScript, NetScaler policies)  |RE|No|RE|RE|
||Unstandardized scripted rules (iRules, OpenScript, NetScaler policies)  |RE|No|RE|RE|
| **Management** |  Logging - Local Buffered Logging  |Yes|Yes|Yes|Yes|
||Logging - Log shipping to log correlation device (Within customer's account)  |Yes|Yes|Yes|Yes|
||Logging - Custom Logging  |RE|RE|RE|RE|
||Logging - Log retention by Rackspace  |No|No|No|No|
||Logging - Log analysis (outside of troubleshooting) |No|No|No|No|
||Management - Direct customer access if load balancer is on TACACS |No|No|No|No|
||Management - SNMP read-only for customer  |Yes|Yes|Yes|Yes|
||Email Alerts |No|No|No|No|
| **High availability (HA)** |  High availability |Yes 1600 and above  |Yes ADX 1000 only |Yes|Yes|
||HA - Active/Standby |Yes|Yes|Yes|Yes|
||HA - Active/Active  |No|No|No|No|
||HA - Clustering |No|No|No|No|
| **Modes and Modules** | Mode - Edge Net Device |US - Yes<Br/>Intl - Yes with AFM |No|No|No|
||Multiple contexts |N/A|No|N/A|N/A|
||Route domains/Traffic domains |RE|N/A|No|No|
||Routed (Single and Multiple Route Domains) Default gateway for back end servers |Yes|Yes|No|Yes|
||Routed (Single and Multiple Route Domains) Not the default gateway for back end servers |RE|RE|No|RE|
||Mode - Out-of-Path - DSR (Direct Server Return) |RE|RE|RE|RE|
||Mode - Layer 2 Bridge |No|No|No|No|
||Multiple Segments behind LB |Yes|Yes|No|Yes<Br/>Interface filtering is RE|
| **RackConnect** | RackConnect VLANs termination |Yes|No for RCV2<Br/>Yes for RCv3  |No|No|
| **RackConnect Global** |  RackConnect Global Classic Static |Yes(AFM only)|No|No|No|
||RackConnect Global 2.0 Static - BGP |RE|No|No|No|
||RackConnect Global 2.0 Dynamic - BGP  |RE|No|No|No|
||RackConnect Global 2.1 Static - BGP |RE|No|No|No|
||RackConnect Global 2.1 Dynamic - BGP  |RE|No|No|No|
||RackConnect Global Public |RE|No|No|No|
||RackConnect Global IPv6 |RE|No|No|No|
| **IPSec VPNs** |  IPSec VPN tunnels on edge Big-IPs |RE|No|N/A|N/A|
| **SSL VPNs** |  SSL Client VPN on edge Big-IPs using APM module |Yes|N/A|No|No|
| **SNI** | Server Name Indication  |Yes|Yes|Yes|Yes|

^ VPX - Product in EA soon to be LA

^^ MPX - Product not launched, supportability is only planned at this stage.
  
### Global load balancer

|| Feature | F5 GTM |  ADX GSLB | NetScaler VPX | NetScaler MPX|
| :--- |:--- | :--- | :--- | :--- | :--- |
| **Interfaces** |  VLAN tagged (Cisco trunk)|Yes|ALL GSLB currently reasonable endeavor|All GSLB currently unsupported|All GSLB currently unsupported|
||VLAN untagged (Cisco access)  |Yes| |||     
||LACP bundling with number of interfaces is a power of 2 |Yes|||| 
||LACP bundling with number of interfaces is not a power of 2 |Reasonable endeavor||||
| **Routing** | Static routes |Yes||||
||Dynamic routing protocols |No||||
| **IPv6** |  Static routes |Yes||||
||Dynamic routing protocols |No||||
| **Load balancing** |  Single Listener Address |Yes||||
||Multiple Listener Addresses |Reasonable endeavor||||
||Servers - BIG-IP System (Single)  |Yes||||
||Servers - BIG-IP System (Redundant pair)  |Yes||||
||Servers - Limit connections Settings  |Reasonable endeavor||||
||Virtual Servers - Manual Configuration  |Yes||||
||Virtual Server Discovery  |Reasonable endeavor||||
||Wide IPs - Standard FQDN Names  |Yes||||
||Wide IPs - Standard FQDN Alias Names  |Yes||||
||Wide IPs - Single Pool, Multiple Virtual Server Members |Yes||||
||Wide IPs - Multiple Pools |Reasonable endeavor||||
||Algorithms - Static - Round Robin, Ratio (Weighted Round Robin), Global Availability  |Yes||||
||Algorithms - Dynamic - Least Connections  |Yes||||
||Algorithms - All Others |Reasonable endeavor||||
| **DNS** | Authoritative Name Server for Specific Subdelegated Domains |Yes||||
||Manual Modifying/adding DNS records via ZoneRunner  |Reasonable endeavor||||
||Authoritative Name Server for all DNS Queries |No||||
||Forwarding to another DNS Server  |No||||
| **Scripting** | Scripted rules (iRules) |Reasonable endeavor||||
| **Management** |  Buffered Logging  |Yes||||
||Log shipping to log correlation device (Within customer's account)  |Yes||||
||Custom Logging  |Reasonable endeavor||||
||Log retention by Rackspace  |No||||
||Logging - Log analysis (outside of troubleshooting) |No||||
| **High availability (HA)** |  Synchronization Groups  |Yes||||
||Redundant GTM Devices specified as primary and secondary DNS servers  |Yes||||
| **Modes and modules** | Serial configuration  |Yes||||
||Paralled configuration  |Yes||||
||Standalone BigIP with GTM License |Yes||||
||Shared BigIP with GTM and LTM Licenses  |Reasonable endeavor||||


### Cisco CSS
End of support on September 30, 2014. Customers that continue using the platform will be in the Extended Lifecycle Support. All the support will be Reasonable endeavor.

### Redhill WebMux
End of support. Customers that continue using the platform will be in the Extended Lifecycle Support . All the support will be Reasonable endeavor.

### General topics
| Feature | Support level | 
| :--- |:--- |
| DDoS mitigation | Supported|
