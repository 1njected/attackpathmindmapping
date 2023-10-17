---
alias: M1037
---

## M1037

Use network appliances to filter ingress or egress traffic and perform protocol-based filtering. Configure software on endpoints to filter network traffic.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Port Knocking\|T1205.001]] | Port Knocking | Mitigation of some variants of this technique could be achieved through the use of stateful firewalls, depending upon how it is implemented. |
| [[Adversary-in-the-Middle\|T1557]] | Adversary-in-the-Middle | Use network appliances and host-based security software to block network traffic that is not necessary within the environment, such as legacy protocols that may be leveraged for AiTM conditions. |
| [[Protocol Tunneling\|T1572]] | Protocol Tunneling | Consider filtering network traffic to untrusted or known bad domains and resources.  |
| [[Application Exhaustion Flood\|T1499.003]] | Application Exhaustion Flood | Leverage services provided by Content Delivery Networks (CDN) or providers specializing in DoS mitigations to filter traffic upstream from services.(Citation: CERT-EU DDoS March 2017) Filter boundary traffic by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport. |
| [[DHCP Spoofing\|T1557.003]] | DHCP Spoofing | Consider filtering DHCP traffic on ports 67 and 68 to/from unknown or untrusted DHCP servers. Additionally, port security may also be enabled on layer switches. Furthermore, consider enabling DHCP snooping on layer 2 switches as it will prevent DHCP spoofing attacks and starvation attacks. Consider tracking available IP addresses through a script or a tool. <br /><br />Additionally, block DHCPv6 traffic and incoming router advertisements, especially if IPv6 is not commonly used in the network.(Citation: ntlm_relaying_kerberos_del) |
| [[Reflection Amplification\|T1498.002]] | Reflection Amplification | When flood volumes exceed the capacity of the network connection being targeted, it is typically necessary to intercept the incoming traffic upstream to filter out the attack traffic from the legitimate traffic. Such defenses can be provided by the hosting Internet Service Provider (ISP) or by a 3rd party such as a Content Delivery Network (CDN) or providers specializing in DoS mitigations.(Citation: CERT-EU DDoS March 2017)<br /><br />Depending on flood volume, on-premises filtering may be possible by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport.(Citation: CERT-EU DDoS March 2017)<br /><br />As immediate response may require rapid engagement of 3rd parties, analyze the risk associated to critical resources being affected by Network DoS attacks and create a disaster recovery plan/business continuity plan to respond to incidents.(Citation: CERT-EU DDoS March 2017) |
| [[DNS\|T1071.004]] | DNS | Consider filtering DNS requests to unknown, untrusted, or known bad domains and resources. Resolving DNS requests with on-premise/proxy servers may also disrupt adversary attempts to conceal data within DNS packets.  |
| [[Multi-hop Proxy\|T1090.003]] | Multi-hop Proxy | Traffic to known anonymity networks and C2 infrastructure can be blocked through the use of network allow and block lists. It should be noted that this kind of blocking may be circumvented by other techniques like [Domain Fronting](https://attack.mitre.org/techniques/T1090/004). |
| [[BITS Jobs\|T1197]] | BITS Jobs | Modify network and/or host firewall rules, as well as other network controls, to only allow legitimate BITS traffic. |
| [[Traffic Signaling\|T1205]] | Traffic Signaling | Mitigation of some variants of this technique could be achieved through the use of stateful firewalls, depending upon how it is implemented. |
| [[Exfiltration Over Symmetric Encrypted Non-C2 Protocol\|T1048.001]] | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Enforce proxies and use dedicated servers for services such as DNS and only allow those systems to communicate over respective ports/protocols, instead of all systems within a network.  |
| [[VNC\|T1021.005]] | VNC | VNC defaults to TCP ports 5900 for the server, 5800 for browser access, and 5500 for a viewer in listening mode. Filtering or blocking these ports will inhibit VNC traffic utilizing default ports. |
| [[Network Denial of Service\|T1498]] | Network Denial of Service | When flood volumes exceed the capacity of the network connection being targeted, it is typically necessary to intercept the incoming traffic upstream to filter out the attack traffic from the legitimate traffic. Such defenses can be provided by the hosting Internet Service Provider (ISP) or by a 3rd party such as a Content Delivery Network (CDN) or providers specializing in DoS mitigations.(Citation: CERT-EU DDoS March 2017)<br /><br />Depending on flood volume, on-premises filtering may be possible by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport.(Citation: CERT-EU DDoS March 2017)<br /><br />As immediate response may require rapid engagement of 3rd parties, analyze the risk associated to critical resources being affected by Network DoS attacks and create a disaster recovery plan/business continuity plan to respond to incidents.(Citation: CERT-EU DDoS March 2017) |
| [[Verclsid\|T1218.012]] | Verclsid | Consider modifying host firewall rules to prevent egress traffic from verclsid.exe. |
| [[Service Exhaustion Flood\|T1499.002]] | Service Exhaustion Flood | Leverage services provided by Content Delivery Networks (CDN) or providers specializing in DoS mitigations to filter traffic upstream from services.(Citation: CERT-EU DDoS March 2017) Filter boundary traffic by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport. |
| [[Endpoint Denial of Service\|T1499]] | Endpoint Denial of Service | Leverage services provided by Content Delivery Networks (CDN) or providers specializing in DoS mitigations to filter traffic upstream from services.(Citation: CERT-EU DDoS March 2017) Filter boundary traffic by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport. To defend against SYN floods, enable SYN Cookies. |
| [[Lateral Tool Transfer\|T1570]] | Lateral Tool Transfer | Consider using the host firewall to restrict file sharing communications such as SMB. (Citation: Microsoft Preventing SMB) |
| [[Unsecured Credentials\|T1552]] | Unsecured Credentials | Limit access to the Instance Metadata API. A properly configured Web Application Firewall (WAF) may help prevent external adversaries from exploiting Server-side Request Forgery (SSRF) attacks that allow access to the Cloud Instance Metadata API.(Citation: RedLock Instance Metadata API 2018) |
| [[Application or System Exploitation\|T1499.004]] | Application or System Exploitation | Leverage services provided by Content Delivery Networks (CDN) or providers specializing in DoS mitigations to filter traffic upstream from services.(Citation: CERT-EU DDoS March 2017) Filter boundary traffic by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport. |
| [[Exfiltration Over Alternative Protocol\|T1048]] | Exfiltration Over Alternative Protocol | Enforce proxies and use dedicated servers for services such as DNS and only allow those systems to communicate over respective ports/protocols, instead of all systems within a network. Cloud service providers support IP-based restrictions when accessing cloud resources. Consider using IP allowlisting along with user account management to ensure that data access is restricted not only to valid users but only from expected IP ranges to mitigate the use of stolen credentials to access data. |
| [[Remote Access Software\|T1219]] | Remote Access Software | Properly configure firewalls, application firewalls, and proxies to limit outgoing traffic to sites and services used by remote access tools. |
| [[Forced Authentication\|T1187]] | Forced Authentication | <br />Block SMB traffic from exiting an enterprise network with egress filtering or by blocking TCP ports 139, 445 and UDP port 137. Filter or block WebDAV protocol traffic from exiting the network. If access to external resources over SMB and WebDAV is necessary, then traffic should be tightly limited with allowlisting. (Citation: US-CERT SMB Security) (Citation: US-CERT APT Energy Oct 2017) |
| [[Socket Filters\|T1205.002]] | Socket Filters | Mitigation of some variants of this technique could be achieved through the use of stateful firewalls, depending upon how it is implemented. |
| [[Direct Network Flood\|T1498.001]] | Direct Network Flood | When flood volumes exceed the capacity of the network connection being targeted, it is typically necessary to intercept the incoming traffic upstream to filter out the attack traffic from the legitimate traffic. Such defenses can be provided by the hosting Internet Service Provider (ISP) or by a 3rd party such as a Content Delivery Network (CDN) or providers specializing in DoS mitigations.(Citation: CERT-EU DDoS March 2017)<br /><br />Depending on flood volume, on-premises filtering may be possible by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport.(Citation: CERT-EU DDoS March 2017)<br /><br />As immediate response may require rapid engagement of 3rd parties, analyze the risk associated to critical resources being affected by Network DoS attacks and create a disaster recovery plan/business continuity plan to respond to incidents.(Citation: CERT-EU DDoS March 2017) |
| [[Network Device Configuration Dump\|T1602.002]] | Network Device Configuration Dump | Apply extended ACLs to block unauthorized protocols outside the trusted network.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[Non-Application Layer Protocol\|T1095]] | Non-Application Layer Protocol | Filter network traffic to prevent use of protocols across the network boundary that are unnecessary. |
| [[Exfiltration Over Unencrypted Non-C2 Protocol\|T1048.003]] | Exfiltration Over Unencrypted Non-C2 Protocol | Enforce proxies and use dedicated servers for services such as DNS and only allow those systems to communicate over respective ports/protocols, instead of all systems within a network.  |
| [[Proxy\|T1090]] | Proxy | Traffic to known anonymity networks and C2 infrastructure can be blocked through the use of network allow and block lists. It should be noted that this kind of blocking may be circumvented by other techniques like [Domain Fronting](https://attack.mitre.org/techniques/T1090/004). |
| [[OS Exhaustion Flood\|T1499.001]] | OS Exhaustion Flood | Leverage services provided by Content Delivery Networks (CDN) or providers specializing in DoS mitigations to filter traffic upstream from services.(Citation: CERT-EU DDoS March 2017) Filter boundary traffic by blocking source addresses sourcing the attack, blocking ports that are being targeted, or blocking protocols being used for transport. To defend against SYN floods, enable SYN Cookies. |
| [[Transfer Data to Cloud Account\|T1537]] | Transfer Data to Cloud Account | Implement network-based filtering restrictions to prohibit data transfers to untrusted VPCs. |
| [[Data from Configuration Repository\|T1602]] | Data from Configuration Repository | Apply extended ACLs to block unauthorized protocols outside the trusted network.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[Network Boundary Bridging\|T1599]] | Network Boundary Bridging | Upon identifying a compromised network device being used to bridge a network boundary, block the malicious packets using an unaffected network device in path, such as a firewall or a router that has not been compromised.  Continue to monitor for additional activity and to ensure that the blocks are indeed effective. |
| [[SMB／Windows Admin Shares\|T1021.002]] | SMB／Windows Admin Shares | Consider using the host firewall to restrict file sharing communications such as SMB. (Citation: Microsoft Preventing SMB) |
| [[ARP Cache Poisoning\|T1557.002]] | ARP Cache Poisoning | Consider enabling DHCP Snooping and Dynamic ARP Inspection on switches to create mappings between IP addresses requested via DHCP and ARP tables and tie the values to a port on the switch that may block bogus traffic.(Citation: Cisco ARP Poisoning Mitigation 2016)(Citation: Juniper DAI 2020) |
| [[Data from Cloud Storage\|T1530]] | Data from Cloud Storage | Cloud service providers support IP-based restrictions when accessing cloud resources. Consider using IP allowlisting along with user account management to ensure that data access is restricted not only to valid users but only from expected IP ranges to mitigate the use of stolen credentials to access data. |
| [[Exfiltration Over Asymmetric Encrypted Non-C2 Protocol\|T1048.002]] | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Enforce proxies and use dedicated servers for services such as DNS and only allow those systems to communicate over respective ports/protocols, instead of all systems within a network.  |
| [[SNMP (MIB Dump)\|T1602.001]] | SNMP (MIB Dump) | Apply extended ACLs to block unauthorized protocols outside the trusted network.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[Network Address Translation Traversal\|T1599.001]] | Network Address Translation Traversal | Block Traffic	Upon identifying a compromised network device being used to bridge a network boundary, block the malicious packets using an unaffected network device in path, such as a firewall or a router that has not been compromised.  Continue to monitor for additional activity and to ensure that the blocks are indeed effective. |
| [[LLMNR／NBT-NS Poisoning and SMB Relay\|T1557.001]] | LLMNR／NBT-NS Poisoning and SMB Relay | Use host-based security software to block LLMNR/NetBIOS traffic. Enabling SMB Signing can stop NTLMv2 relay attacks.(Citation: byt3bl33d3r NTLM Relaying)(Citation: Secure Ideas SMB Relay)(Citation: Microsoft SMB Packet Signing) |
| [[Cloud Instance Metadata API\|T1552.005]] | Cloud Instance Metadata API | Limit access to the Instance Metadata API. A properly configured Web Application Firewall (WAF) may help prevent external adversaries from exploiting Server-side Request Forgery (SSRF) attacks that allow access to the Cloud Instance Metadata API.(Citation: RedLock Instance Metadata API 2018) |
| [[LLMNR／NBT-NS Poisoning and Relay\|T1171]] | LLMNR／NBT-NS Poisoning and Relay | Use host-based security software to block LLMNR/NetBIOS traffic. Enabling SMB Signing can stop NTLMv2 relay attacks.(Citation: byt3bl33d3r NTLM Relaying)(Citation: Secure Ideas SMB Relay)(Citation: Microsoft SMB Packet Signing) |
| [[Custom Command and Control Protocol\|T1094]] | Custom Command and Control Protocol | Filter network traffic to look for unusual or non-standard protocols. |
| [[Multi-hop Proxy\|T1188]] | Multi-hop Proxy | Traffic to known anonymity networks and C2 infrastructure can be blocked through the use of network black and white lists. It should be noted that this kind of blocking may be circumvented by other techniques like [Domain Fronting](https://attack.mitre.org/techniques/T1172). |
| [[Cloud Instance Metadata API\|T1522]] | Cloud Instance Metadata API | Limit access to the Instance Metadata API using a host-based firewall such as iptables.(Citation: RedLock Instance Metadata API 2018) A properly configured Web Application Firewall (WAF) may help prevent external adversaries from exploiting Server-side Request Forgery (SSRF) attacks that allow access to the Cloud Instance Metadata API. |
| [[Valid Accounts\|T1078]] | Valid Accounts | Cloud service providers support IP-based restrictions when accessing cloud resources. Consider using IP whitelisting on cloud-based systems along with user account management to ensure that data access is restricted not only to valid users but only from expected IP ranges to mitigate the use of stolen credentials to access data. |