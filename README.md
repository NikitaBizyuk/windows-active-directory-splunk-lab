# windows-active-directory-splunk-lab
Windows Active Directory home lab with Splunk SIEM, Sysmon, and centralized endpoint logging
# Windows Active Directory & Splunk Home Lab

## Overview

This project demonstrates the deployment of a small Windows Active
Directory environment integrated with Splunk for centralized security
monitoring.

The lab was built using Oracle VirtualBox and consists of a Windows
Server 2022 Domain Controller, a Windows client endpoint, a Splunk
Enterprise server, and a Kali Linux system.

## Lab Architecture

| System | Purpose |
|---|---|
| Windows Server 2022 | Active Directory Domain Controller |
| Windows 10 | Domain-joined endpoint |
| Ubuntu Server | Splunk Enterprise server |
| Kali Linux | Security testing workstation |

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy
- Windows 10
- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- Ubuntu Server
- Kali Linux
- Oracle VirtualBox

## Active Directory Configuration

I installed Active Directory Domain Services on Windows Server 2022
and promoted the server to a Domain Controller.

Domain:

    mydfir.local

I then created Active Directory user accounts and joined a Windows
client machine to the domain.

I verified the configuration by successfully authenticating to the
Windows client using an Active Directory domain account.

[Screenshot of Active Directory Users and Computers]



[Screenshot of successful domain login]

## Security Monitoring

Sysmon was installed on Windows systems to provide additional endpoint
telemetry.

Splunk Universal Forwarder was configured to collect Windows Event
Logs and Sysmon logs and forward them to the Splunk Enterprise server.

Logs collected include:

- Windows Security logs
- Windows System logs
- Windows Application logs
- Sysmon Operational logs

The Splunk server receives forwarded events over TCP port 9997.

[Screenshot of Splunk showing both hosts]

## Skills Demonstrated

- Active Directory deployment
- Domain Controller configuration
- Windows domain administration
- User and account management
- Domain joining
- DNS configuration
- Windows Event Log analysis
- Sysmon configuration
- Splunk log ingestion
- Splunk Universal Forwarder configuration
- Virtual networking
- SIEM fundamentals
