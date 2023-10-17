---
alias: APT41, Wicked Panda
---

## G0096

[APT41](https://attack.mitre.org/groups/G0096) is a threat group that researchers have assessed as Chinese state-sponsored espionage group that also conducts financially-motivated operations. Active since at least 2012, [APT41](https://attack.mitre.org/groups/G0096) has been observed targeting healthcare, telecom, technology, and video game industries in 14 countries. [APT41](https://attack.mitre.org/groups/G0096) overlaps at least partially with public reporting on groups including BARIUM and [Winnti Group](https://attack.mitre.org/groups/G0044).(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021)



### Techniques Used

| ID | Name | Use |
| --- | --- | --- |
| [[Valid Accounts\|T1078]] | Valid Accounts | [APT41](https://attack.mitre.org/groups/G0096) used compromised credentials to log on to other systems.(Citation: FireEye APT41 Aug 2019)(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[Compromise Software Supply Chain\|T1195.002]] | Compromise Software Supply Chain | [APT41](https://attack.mitre.org/groups/G0096) gained access to production environments where they could inject malicious code into legitimate, signed files and widely distribute them to end users.(Citation: FireEye APT41 Aug 2019) |
| [[PowerShell\|T1059.001]] | PowerShell | [APT41](https://attack.mitre.org/groups/G0096) leveraged PowerShell to deploy malware families in victims’ environments.(Citation: FireEye APT41 Aug 2019)(Citation: FireEye APT41 March 2020) |
| [[Rootkit\|T1014]] | Rootkit | [APT41](https://attack.mitre.org/groups/G0096) deployed rootkits on Linux systems.(Citation: FireEye APT41 Aug 2019)(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[Match Legitimate Name or Location\|T1036.005]] | Match Legitimate Name or Location | [APT41](https://attack.mitre.org/groups/G0096) attempted to masquerade their files as popular anti-virus software.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[Windows Service\|T1543.003]] | Windows Service | [APT41](https://attack.mitre.org/groups/G0096) modified legitimate Windows services to install malware backdoors.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) [APT41](https://attack.mitre.org/groups/G0096) created the StorSyncSvc service to provide persistence for Cobalt Strike.(Citation: FireEye APT41 March 2020) |
| [[File Transfer Protocols\|T1071.002]] | File Transfer Protocols | [APT41](https://attack.mitre.org/groups/G0096) used exploit payloads that initiate download via [ftp](https://attack.mitre.org/software/S0095).(Citation: FireEye APT41 March 2020) |
| [[Mitre Att&ck/techniques/Code Signing|T1553.002]] | Code Signing | [APT41](https://attack.mitre.org/groups/G0096) leveraged code-signing certificates to sign malware when targeting both gaming and non-gaming organizations.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[Tool\|T1588.002]] | Tool | [APT41](https://attack.mitre.org/groups/G0096) has obtained and used tools such as [Mimikatz](https://attack.mitre.org/software/S0002), [pwdump](https://attack.mitre.org/software/S0006), [PowerSploit](https://attack.mitre.org/software/S0194), and [Windows Credential Editor](https://attack.mitre.org/software/S0005).(Citation: FireEye APT41 Aug 2019) |
| [[Account Manipulation\|T1098]] | Account Manipulation | [APT41](https://attack.mitre.org/groups/G0096) has added user accounts to the User and Admin groups.(Citation: FireEye APT41 Aug 2019)  |
| [[SMB／Windows Admin Shares\|T1021.002]] | SMB／Windows Admin Shares | [APT41](https://attack.mitre.org/groups/G0096) has transferred implant files using Windows Admin Shares.(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[Local Account\|T1136.001]] | Local Account | [APT41](https://attack.mitre.org/groups/G0096) has created user accounts.(Citation: FireEye APT41 Aug 2019)  |
| [[Bootkit\|T1542.003]] | Bootkit | [APT41](https://attack.mitre.org/groups/G0096) deployed Master Boot Record bootkits on Windows systems to hide their malware and maintain persistence on victim systems.(Citation: FireEye APT41 Aug 2019) |
| [[Web Protocols\|T1071.001]] | Web Protocols | [APT41](https://attack.mitre.org/groups/G0096) used HTTP to download payloads for CVE-2019-19781 and CVE-2020-10189 exploits.(Citation: FireEye APT41 March 2020)  |
| [[Clear Windows Event Logs\|T1070.001]] | Clear Windows Event Logs | [APT41](https://attack.mitre.org/groups/G0096) attempted to remove evidence of some of its activity by clearing Windows security and system events.(Citation: FireEye APT41 Aug 2019) |
| [[Network Share Discovery\|T1135]] | Network Share Discovery |  [APT41](https://attack.mitre.org/groups/G0096) used the <code>net share</code> command as part of network reconnaissance.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[Environmental Keying\|T1480.001]] | Environmental Keying | [APT41](https://attack.mitre.org/groups/G0096) has encrypted payloads using the Data Protection API (DPAPI), which relies on keys tied to specific user accounts on specific machines. [APT41](https://attack.mitre.org/groups/G0096) has also environmentally keyed second stage malware with an RC5 key derived in part from the infected system's volume serial number.(Citation: Twitter ItsReallyNick APT41 EK) |
| [[Data from Local System\|T1005]] | Data from Local System | [APT41](https://attack.mitre.org/groups/G0096) has uploaded files and data from a compromised host.(Citation: Group IB APT 41 June 2021) |
| [[External Remote Services\|T1133]] | External Remote Services | [APT41](https://attack.mitre.org/groups/G0096) compromised an online billing/payment service using VPN access between a third-party service provider and the targeted payment service.(Citation: FireEye APT41 Aug 2019)<br /> |
| [[File Deletion\|T1070.004]] | File Deletion | [APT41](https://attack.mitre.org/groups/G0096) deleted files from the system.(Citation: FireEye APT41 Aug 2019)  |
| [[Spearphishing Attachment\|T1566.001]] | Spearphishing Attachment | [APT41](https://attack.mitre.org/groups/G0096) sent spearphishing emails with attachments such as compiled HTML (.chm) files to initially compromise their victims.(Citation: FireEye APT41 Aug 2019) |
| [[Scheduled Task\|T1053.005]] | Scheduled Task | [APT41](https://attack.mitre.org/groups/G0096) used a compromised account to create a scheduled task on a system.(Citation: FireEye APT41 Aug 2019)(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[Registry Run Keys ／ Startup Folder\|T1547.001]] | Registry Run Keys ／ Startup Folder | [APT41](https://attack.mitre.org/groups/G0096) created and modified startup files for persistence.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) [APT41](https://attack.mitre.org/groups/G0096) added a registry key in <code>HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Svchost</code> to establish persistence for Cobalt Strike.(Citation: FireEye APT41 March 2020) |
| [[Accessibility Features\|T1546.008]] | Accessibility Features | [APT41](https://attack.mitre.org/groups/G0096) leveraged sticky keys to establish persistence.(Citation: FireEye APT41 Aug 2019)  |
| [[Password Cracking\|T1110.002]] | Password Cracking | [APT41](https://attack.mitre.org/groups/G0096) performed password brute-force attacks on the local admin account.(Citation: FireEye APT41 Aug 2019) |
| [[Dynamic Linker Hijacking\|T1574.006]] | Dynamic Linker Hijacking | [APT41](https://attack.mitre.org/groups/G0096) has configured payloads to load via LD_PRELOAD.(Citation: Crowdstrike GTR2020 Mar 2020)	 |
| [[Windows Command Shell\|T1059.003]] | Windows Command Shell | [APT41](https://attack.mitre.org/groups/G0096) used <code>cmd.exe /c</code> to execute commands on remote machines.(Citation: FireEye APT41 Aug 2019)<br />[APT41](https://attack.mitre.org/groups/G0096) used a batch file to install persistence for the [Cobalt Strike](https://attack.mitre.org/software/S0154) BEACON loader.(Citation: FireEye APT41 March 2020) |
| [[Domain Generation Algorithms\|T1568.002]] | Domain Generation Algorithms | [APT41](https://attack.mitre.org/groups/G0096) has used DGAs to change their C2 servers monthly.(Citation: FireEye APT41 Aug 2019) |
| [[Service Execution\|T1569.002]] | Service Execution | [APT41](https://attack.mitre.org/groups/G0096) used  svchost.exe and [Net](https://attack.mitre.org/software/S0039) to execute a system service installed to launch a [Cobalt Strike](https://attack.mitre.org/software/S0154) BEACON loader.(Citation: FireEye APT41 March 2020)(Citation: Group IB APT 41 June 2021) |
| [[DNS\|T1071.004]] | DNS | [APT41](https://attack.mitre.org/groups/G0096) used DNS for C2 communications.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021)  |
| [[Network Service Discovery\|T1046]] | Network Service Discovery | [APT41](https://attack.mitre.org/groups/G0096) used a malware variant called WIDETONE to conduct port scans on specified subnets.(Citation: FireEye APT41 Aug 2019) |
| [[Archive via Utility\|T1560.001]] | Archive via Utility | [APT41](https://attack.mitre.org/groups/G0096) created a RAR archive of targeted files for exfiltration.(Citation: FireEye APT41 Aug 2019) |
| [[Rundll32\|T1218.011]] | Rundll32 | [APT41](https://attack.mitre.org/groups/G0096) has used rundll32.exe to execute a loader.(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[Dead Drop Resolver\|T1102.001]] | Dead Drop Resolver | [APT41](https://attack.mitre.org/groups/G0096) used legitimate websites for C2 through dead drop resolvers (DDR), including GitHub, Pastebin, and Microsoft TechNet.(Citation: FireEye APT41 Aug 2019) |
| [[Fallback Channels\|T1008]] | Fallback Channels | [APT41](https://attack.mitre.org/groups/G0096) used the Steam community page as a fallback mechanism for C2.(Citation: FireEye APT41 Aug 2019)  |
| [[Resource Hijacking\|T1496]] | Resource Hijacking | [APT41](https://attack.mitre.org/groups/G0096) deployed a Monero cryptocurrency mining tool in a victim’s environment.(Citation: FireEye APT41 Aug 2019) |
| [[System Network Connections Discovery\|T1049]] | System Network Connections Discovery | [APT41](https://attack.mitre.org/groups/G0096) has enumerated IP addresses of network resources and used the <code>netstat</code> command as part of network reconnaissance. The group has also used a malware variant, HIGHNOON, to enumerate active RDP sessions.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[Unix Shell\|T1059.004]] | Unix Shell | [APT41](https://attack.mitre.org/groups/G0096) executed <code>file /bin/pwd</code> in activity exploiting CVE-2019-19781 against Citrix devices.(Citation: FireEye APT41 March 2020) |
| [[Data Encrypted for Impact\|T1486]] | Data Encrypted for Impact | [APT41](https://attack.mitre.org/groups/G0096) used a ransomware called Encryptor RaaS to encrypt files on the targeted systems and provide a ransom note to the user.(Citation: FireEye APT41 Aug 2019) |
| [[DLL Side-Loading\|T1574.002]] | DLL Side-Loading | [APT41](https://attack.mitre.org/groups/G0096) used legitimate executables to perform DLL side-loading of their malware.(Citation: FireEye APT41 Aug 2019)  |
| [[System Network Configuration Discovery\|T1016]] | System Network Configuration Discovery | [APT41](https://attack.mitre.org/groups/G0096) collected MAC addresses from victim machines.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021)  |
| [[System Owner／User Discovery\|T1033]] | System Owner／User Discovery | [APT41](https://attack.mitre.org/groups/G0096) used the WMIEXEC utility to execute <code>whoami</code> commands on remote machines.(Citation: FireEye APT41 Aug 2019) |
| [[Ingress Tool Transfer\|T1105]] | Ingress Tool Transfer | [APT41](https://attack.mitre.org/groups/G0096) used [certutil](https://attack.mitre.org/software/S0160) to download additional files.(Citation: FireEye APT41 March 2020)(Citation: Crowdstrike GTR2020 Mar 2020)(Citation: Group IB APT 41 June 2021) |
| [[Exploitation for Client Execution\|T1203]] | Exploitation for Client Execution | [APT41](https://attack.mitre.org/groups/G0096) leveraged the follow exploits in their operations: CVE-2012-0158, CVE-2015-1641, CVE-2017-0199, CVE-2017-11882, and CVE-2019-3396.(Citation: FireEye APT41 Aug 2019)  |
| [[Compiled HTML File\|T1218.001]] | Compiled HTML File | [APT41](https://attack.mitre.org/groups/G0096) used compiled HTML (.chm) files for targeting.(Citation: FireEye APT41 Aug 2019)  |
| [[Modify Registry\|T1112]] | Modify Registry | [APT41](https://attack.mitre.org/groups/G0096) used a malware variant called GOODLUCK to modify the registry in order to steal credentials.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[Proxy\|T1090]] | Proxy | [APT41](https://attack.mitre.org/groups/G0096) used a tool called CLASSFON to covertly proxy network communications.(Citation: FireEye APT41 Aug 2019) |
| [[LSASS Memory\|T1003.001]] | LSASS Memory | [APT41](https://attack.mitre.org/groups/G0096) has used hashdump, [Mimikatz](https://attack.mitre.org/software/S0002), and the Windows Credential Editor to dump password hashes from memory and authenticate to other user accounts.(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[BITS Jobs\|T1197]] | BITS Jobs | [APT41](https://attack.mitre.org/groups/G0096) used [BITSAdmin](https://attack.mitre.org/software/S0190) to download and install payloads.(Citation: FireEye APT41 March 2020)(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[File and Directory Discovery\|T1083]] | File and Directory Discovery | [APT41](https://attack.mitre.org/groups/G0096) has executed <code>file /bin/pwd</code> on exploited victims, perhaps to return architecture related information.(Citation: FireEye APT41 March 2020) |
| [[Process Injection\|T1055]] | Process Injection | [APT41](https://attack.mitre.org/groups/G0096) malware TIDYELF loaded the main WINTERLOVE component by injecting it into the iexplore.exe process.(Citation: FireEye APT41 Aug 2019) |
| [[Remote Desktop Protocol\|T1021.001]] | Remote Desktop Protocol | [APT41](https://attack.mitre.org/groups/G0096) used RDP for lateral movement.(Citation: FireEye APT41 Aug 2019)(Citation: Crowdstrike GTR2020 Mar 2020) |
| [[Exploit Public-Facing Application\|T1190]] | Exploit Public-Facing Application | [APT41](https://attack.mitre.org/groups/G0096) exploited CVE-2020-10189 against Zoho ManageEngine Desktop Central, and CVE-2019-19781 to compromise Citrix Application Delivery Controllers (ADC) and gateway devices.(Citation: FireEye APT41 March 2020) |
| [[Obfuscated Files or Information\|T1027]] | Obfuscated Files or Information | [APT41](https://attack.mitre.org/groups/G0096) used VMProtected binaries in multiple intrusions.(Citation: FireEye APT41 March 2020) |
| [[Multi-Stage Channels\|T1104]] | Multi-Stage Channels | [APT41](https://attack.mitre.org/groups/G0096) used the storescyncsvc.dll BEACON backdoor to download a secondary backdoor.(Citation: FireEye APT41 March 2020) |
| [[Windows Management Instrumentation\|T1047]] | Windows Management Instrumentation | [APT41](https://attack.mitre.org/groups/G0096) used WMI in several ways, including for execution of commands via WMIEXEC as well as for persistence via [PowerSploit](https://attack.mitre.org/software/S0194).(Citation: FireEye APT41 Aug 2019)(Citation: Group IB APT 41 June 2021) |
| [[Keylogging\|T1056.001]] | Keylogging | [APT41](https://attack.mitre.org/groups/G0096) used a keylogger called GEARSHIFT on a target system.(Citation: FireEye APT41 Aug 2019) |
| [[Clear Command History\|T1070.003]] | Clear Command History | [APT41](https://attack.mitre.org/groups/G0096) attempted to remove evidence of some of its activity by deleting Bash histories.(Citation: FireEye APT41 Aug 2019) |
| [[Masquerade Task or Service\|T1036.004]] | Masquerade Task or Service | [APT41](https://attack.mitre.org/groups/G0096) has created services to appear as benign system tools.(Citation: Group IB APT 41 June 2021) |
| [[DLL Search Order Hijacking\|T1574.001]] | DLL Search Order Hijacking | [APT41](https://attack.mitre.org/groups/G0096) has used search order hijacking to execute malicious payloads, such as Winnti RAT.(Citation: Crowdstrike GTR2020 Mar 2020) |