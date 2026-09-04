# Arkham General Hospital Infrastructure

A simulated enterprise hospital infrastructure project designed for approximately 200 employees operating in a 24/7 environment.

The project demonstrates hands-on implementation across Cisco networking and Windows Server administration. The Cisco and Windows environments were implemented separately: Cisco networking was simulated in Packet Tracer, while the Windows infrastructure was implemented using VirtualBox.

## Technologies

- Cisco IOS / Cisco Packet Tracer
- VLANs and Layer 3 inter-VLAN routing
- Switch Virtual Interfaces (SVIs)
- HSRP gateway redundancy
- EtherChannel
- Windows Server 2022
- Active Directory Domain Services
- DNS
- DHCP
- SMB file services
- Active Directory security groups / AGDLP
- Group Policy Preferences
- Automated network-drive mapping
- PowerShell
- VirtualBox

## Key Implementations

- Departmental VLAN segmentation
- Layer 3 inter-VLAN routing
- HSRP redundant default gateways
- EtherChannel link aggregation and redundancy
- `arkham.local` Active Directory domain
- DNS and DHCP services on DC01
- Departmental SMB shares on FILE01
- OU and security-group architecture
- AGDLP-style resource access
- GPO-based automated Clinical drive mapping
- PowerShell user provisioning
- DNS/connectivity validation
- Network-drive troubleshooting
- NTFS permissions investigation and remediation
- Authorized vs. unauthorized file-share access testing

## Network Segmentation

| VLAN | Department | Subnet | Virtual Gateway |
|---:|---|---|---|
| 10 | Administration | 192.168.10.0/24 | 192.168.10.1 |
| 20 | IT | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Clinical Services | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Emergency | 192.168.40.0/24 | 192.168.40.1 |
| 50 | Research | 192.168.50.0/24 | 192.168.50.1 |
| 60 | Server Farm | 192.168.60.0/24 | 192.168.60.1 |
| 70 | Management | 192.168.70.0/24 | 192.168.70.1 |
| 80 | Guest Wi-Fi | 192.168.80.0/24 | 192.168.80.1 |

## Windows Server Infrastructure

| Server | Address | Role |
|---|---|---|
| DC01 | 192.168.60.10 | Active Directory, DNS, DHCP |
| FILE01 | 192.168.60.20 | SMB departmental file shares |

## Repository Structure

```text
01-Architecture/       Network architecture and addressing
02-Cisco-Network/       Packet Tracer work, configurations, verification
03-Windows-Server/      Windows Server infrastructure
04-Active-Directory/    OUs, security groups, access model
05-Group-Policy/        GPO and automated drive mapping
06-PowerShell/          Automation scripts
07-Troubleshooting/     Troubleshooting scenarios and remediation
08-Validation/          Test results and validation
screenshots/            Selected implementation evidence
documentation/          Detailed project report
```

## Detailed Documentation

See `documentation/ARKHAM-GENERAL-HOSPITAL-INFRASTRUCTURE-DESIGN.pdf` for the full implementation report and evidence.

## Project Notes

This is a lab environment built for learning and portfolio demonstration. The Cisco Packet Tracer environment and VirtualBox Windows environment are separate implementations; the documentation reflects that distinction.
