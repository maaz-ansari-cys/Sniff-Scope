# SniffScope

**Educational Network & DNS Traffic Viewer for Windows**

SniffScope is a Windows desktop application designed for **educational network discovery and traffic analysis in authorized laboratory environments**.

It provides a graphical interface for discovering devices on a local network, viewing network information, analyzing DNS activity, and inspecting captured traffic during authorized security testing.

> **⚠ Authorized Use Only**
>
> SniffScope is intended for networks, systems, and devices that you own or have explicit permission to test.
>
> Do **not** use the software for unauthorized interception, surveillance, credential collection, traffic manipulation, or disruption of networks.
>
> You are responsible for complying with applicable laws, regulations, and network policies.

---

## ◆ Download

The SniffScope installer is distributed through **GitHub Releases** rather than being stored directly in the repository.

**→ [Download the latest SniffScope Release](../../releases/latest)**

From the latest release, download:

```text
SniffScope-Setup.exe
```

For detailed installation and usage instructions:

**→ [Sniff Scope Installation Guide](./Sniff%20Scope%20Installation%20Guide.pdf)**

### Repository Contents

```text
Sniff-Scope/
│
├── README.md
├── Sniff Scope Installation Guide.pdf
│
└── Releases
    └── SniffScope-Setup.exe
```

> **Why isn't the `.exe` visible in the repository?**
>
> The installer is distributed through GitHub Releases instead of being stored as a regular repository file. Open the **Releases** section above to download the latest Windows installer.

---

## ◆ Features

SniffScope provides an educational environment for studying:

* Local network device discovery
* ARP-based network scanning
* IP and MAC address identification
* Hardware/vendor identification
* DNS traffic and domain-resolution analysis
* Network device status monitoring
* Authorized traffic interception for laboratory testing
* Target host analysis
* DNS resolution visibility
* Application and HTTP payload inspection where technically available
* CSV export of scan results

---

# ◆ Prerequisites

Before installing SniffScope, ensure that the following requirements are available.

### Required

* Windows operating system
* Administrator privileges when required by the installer
* **Npcap**

SniffScope uses Npcap for packet capture and network traffic analysis.

### Npcap

Download Npcap from the official source:

**→ [Npcap Official Website](https://npcap.com/)**

The installer may have a versioned filename such as:

```text
npcap-1.89.exe
```

The exact filename may change with newer Npcap releases.

---

# ◆ Installation

## 1. Download SniffScope

Open the:

**→ [Latest SniffScope Release](../../releases/latest)**

Download:

```text
SniffScope-Setup.exe
```

> Windows may display a security warning because the installer may not have an established code-signing reputation. Make sure the installer was downloaded from the intended SniffScope GitHub Release.

---

## 2. Start the Installer

Run:

```text
SniffScope-Setup.exe
```

Follow the installation wizard.

---

## 3. Select Installation User

When prompted, select the appropriate installation option/user and click:

**Next**

---

## 4. Select Installation Directory

Choose the directory where SniffScope should be installed.

You can:

* Keep the default directory, or
* Select a custom installation directory.

Click:

**Next**

---

## 5. Install Npcap

SniffScope may detect that Npcap is not installed.

If prompted:

1. Open the official Npcap website.
2. Download the Windows installer.
3. Right-click the installer.
4. Select **Run as administrator**.
5. Complete the Npcap installation.
6. Restart Windows if requested.

Return to the SniffScope installer and select:

**Retry**

---

## 6. Finish Installation

Once all required components have been detected, complete the installation.

Click:

**Finish**

SniffScope is now installed.

---

# ◆ First-Time Setup

Launch SniffScope and open:

**Access Command Center**

The first launch requires local application credentials.

### 1. Choose Your Name

Enter the name you want to use for the local application profile.

### 2. Create an 8-Character Password

Create the required 8-character password.

### 3. Initialize System Administrator

Select:

**Initialize System Administrator**

SniffScope will initialize the local system configuration.

Wait while the application loads the required network information and credentials.

---

# ◆ Network Discovery

After initialization, SniffScope can be used to discover devices visible on the local network.

## Trigger ARP Scan

Select:

**Trigger ARP Scan**

SniffScope performs an ARP-based discovery process.

Depending on the network configuration, discovered information may include:

| Information | Description                                |
| ----------- | ------------------------------------------ |
| IP Address  | Network address assigned to the device     |
| MAC Address | Network interface hardware address         |
| Vendor      | Manufacturer information when identifiable |
| Status      | Current discovery/status information       |

### Discovery Process

```text
ARP Scan
   │
   ├── Discover devices
   ├── Identify IP addresses
   ├── Identify MAC addresses
   └── Determine vendor information
```

The device list will populate as hosts are discovered.

---

# ◆ Network Status

After scanning, SniffScope displays the discovered devices in the network interface.

This information can be used for educational exercises involving:

* Network inventory
* Network discovery
* Asset identification
* IP/MAC analysis
* Basic network monitoring

---

# ◆ Authorized Traffic Interception

> **⚠ Authorization Required**
>
> Only perform traffic interception against systems and networks where you have explicit authorization.
>
> A controlled laboratory containing your own virtual machines is recommended for testing.

To begin an authorized interception session:

1. Select a device from the discovered-device list.

2. Review the target information.

3. Select:

   **Begin MITM (Man-in-the-Middle) Interception**

4. Follow any permission or authorization prompts displayed by the application.

SniffScope will begin the configured traffic-analysis process.

---

# ◆ Network Limitations & Enterprise Firewalls

SniffScope's MITM interception functionality has **important limitations in enterprise and organizational networks**.

### Enterprise Firewall Restrictions

Organizations implementing **ISO 27001, ISO 27002, and privacy compliance standards** typically deploy advanced firewall configurations and network security controls that prevent Man-in-the-Middle attacks:

#### Restrictions That Block MITM:

* **Next-Generation Firewalls (NGFW)** — inspect and block ARP spoofing attempts
* **Dynamic ARP Inspection (DAI)** — prevents ARP-based MITM attacks
* **DHCP Snooping** — validates ARP packets against DHCP bindings
* **Network Access Control (NAC)** — monitors and restricts unauthorized device activity
* **Encrypted DNS (DoH/DoT)** — prevents DNS interception and analysis
* **TLS/SSL Inspection** — decrypts and re-encrypts traffic (blocks passive capture)
* **Port Security & MAC Filtering** — restricts ARP on protected ports
* **Intrusion Detection/Prevention (IDS/IPS)** — detects MITM signatures
* **VPN Requirements** — forces encrypted tunnels that bypass local interception
* **Endpoint Detection & Response (EDR)** — detects SniffScope packet capture and MITM processes

### When MITM Will Not Work:

✗ Large organizations with enterprise security policies  
✗ Corporate networks with compliance requirements (ISO standards)  
✗ Networks with stateful firewall inspection  
✗ Networks requiring VPN access  
✗ Educational institutions with robust network security  
✗ Any network restricting unauthorized ARP or DNS activity  

### When MITM May Work:

✓ Small isolated lab networks (Virtual machines)  
✓ Home networks without advanced firewalls  
✓ Networks you own with no security controls  
✓ Authorized penetration testing environments  
✓ Controlled lab environments with explicit permission  

### Recommendation

**SniffScope MITM functionality is designed for isolated laboratory testing only.**

For enterprise network analysis, organizations should:

* Use authorized network monitoring tools approved by IT/Security teams
* Work with network administrators within compliance frameworks
* Conduct authorized security testing through formal channels
* Respect organizational security policies and privacy standards

---

# ◆ DNS & Traffic Analysis

During an authorized analysis session, SniffScope can display information associated with observed network traffic.

Depending on the captured traffic, this may include:

* Source and destination IP addresses
* Domain information
* DNS resolutions
* Target host information
* Application-related traffic
* HTTP payload information where applicable

The purpose is to provide a practical environment for understanding how network and DNS activity appears during security analysis.

---

# ◆ DNS Resolution Analysis

SniffScope can help associate observed network activity with domain names and DNS resolutions.

A simplified example:

```text
Device
   │
   ▼
DNS Query
   │
   ▼
example.com
   │
   ▼
Resolved IP Address
   │
   ▼
Network Connection
```

This allows students to study the relationship between:

```text
Device → DNS Query → Domain → IP Address → Network Traffic
```

---

# ◆ Application & HTTP Payload Analysis

Where supported by the captured traffic and protocol conditions, SniffScope can provide application-level traffic information.

HTTP payload information may also be available when the captured traffic is actually using HTTP and the relevant data is visible.

> **Note:** HTTPS encrypts application traffic. SniffScope cannot simply display encrypted HTTPS contents. Visibility depends on the protocol, encryption, capture conditions, and traffic available to the application.

---

# ◆ Export Scan Results

After a network scan, SniffScope provides an option to export collected results.

Select:

**Download CSV**

The exported CSV can be used for:

* Lab reports
* Network inventory
* Documentation
* Further analysis
* Record keeping

### Workflow

```text
ARP Scan
   │
   ▼
Device Discovery
   │
   ▼
Review Results
   │
   ▼
Export CSV
   │
   ▼
Analyze / Document
```

---

# ◆ Targeted Host Analysis

After selecting a target during an authorized analysis session, SniffScope can provide additional information related to that host.

Depending on the available traffic, this may include:

* Target IP address
* DNS resolutions
* Observed domains
* Application traffic
* HTTP information
* Network activity

This functionality is intended for controlled network-security experiments.

---

# ◆ Permissions & Authorization

SniffScope may display permission or authorization prompts during operation.

Always verify that you have permission before continuing with scanning or interception activities.

### Recommended Lab

A controlled virtual environment can be used for testing:

```text
             Isolated Lab Network
                     │
          ┌──────────┼──────────┐
          │          │          │
       Windows     Linux     SniffScope
       Test VM    Test VM       Host
```

Virtual machines allow network-security experiments to be performed without intentionally affecting unrelated systems.

---

# ◆ Trial Usage

SniffScope provides:

**3 free attempts**

These attempts cover the application's scanning and MITM interception functionality.

After the available free attempts are used, additional usage requires credits/license activation.

---

# ◆ Licensing & Credits

To request additional usage credits:

### 1. Copy Your Machine ID

Open the relevant licensing/access section in SniffScope and copy your:

```text
Machine ID
```

### 2. Contact the Developer

**→ [SniffScope Licensing / Contact](https://maazansari.vercel.app/contact)**

Use a valid email address and include your Machine ID in the request.

### 3. Request Credits

Eligible users can request:

**$100 worth of free scanning and MITM interception credits**

> Credit availability and licensing terms may change.

---

# ◆ Troubleshooting

## Npcap is required

Install Npcap from:

**→ [Npcap Official Website](https://npcap.com/)**

Run the installer as administrator and restart Windows if requested.

Then return to SniffScope and select:

**Retry**

---

## Npcap is installed but SniffScope does not detect it

Try:

```text
1. Close SniffScope
2. Confirm Npcap is installed
3. Restart Windows
4. Launch SniffScope
5. Provide required Windows permissions
```

---

## ARP Scan does not discover devices

Possible causes include:

* The target is not on the same local network.
* Network isolation is enabled.
* The network restricts ARP-based discovery.
* The wrong network interface is being used.
* Windows permissions or packet-capture configuration are incomplete.

Testing on a controlled LAN or virtual lab is recommended.

---

## DNS information is not appearing

DNS visibility depends on the network and the way the target performs DNS resolution.

Possible reasons include:

* DNS caching
* Encrypted DNS
* DNS-over-HTTPS
* DNS-over-TLS
* Traffic occurring outside the captured interface
* Insufficient capture permissions

Therefore, the absence of a DNS entry does not necessarily mean that a domain was not accessed.

---

## MITM Interception is not working

See the **Network Limitations & Enterprise Firewalls** section for details about firewall restrictions that may prevent MITM functionality.

If you are testing in an enterprise or organizational network, MITM interception may be blocked by:

* Firewall policies
* ARP inspection
* Network access controls
* Compliance-related security measures

For MITM testing, use isolated laboratory networks (virtual machines) where you have full control.

---

# ◆ Recommended Educational Lab

SniffScope can be tested using an isolated virtual network.

A simple setup:

```text
                  Isolated Network
                         │
             ┌───────────┼───────────┐
             │           │           │
        Windows VM    Linux VM    SniffScope
        Test Host    Test Host      Machine
```

Use only systems that you own or have explicit authorization to monitor.

The environment can be used to study:

```text
ARP
 ├─ MAC Addresses
 ├─ IP Addresses
 └─ Device Discovery

DNS
 ├─ Queries
 ├─ Domains
 └─ Resolutions

Traffic
 ├─ Packet Capture
 ├─ Application Traffic
 └─ HTTP Analysis
```

---

# ◆ Responsible Use

SniffScope is an educational security tool.

It must not be used to:

* Intercept networks without authorization
* Monitor devices without permission
* Collect credentials
* Capture private communications
* Disrupt network availability
* Circumvent security controls
* Conduct unauthorized surveillance

Use the software only within an authorized environment.

The developer does not authorize misuse of the software.

---

# ◆ Disclaimer

SniffScope is provided for educational and authorized security-testing purposes.

The software is provided **without warranty**. Users are responsible for ensuring that their use of SniffScope complies with applicable laws, regulations, organizational policies, and network-owner requirements.

The developer assumes no responsibility for unauthorized or unlawful use of the software.

---

# ◆ Copyright

Copyright © 2026 **Maaz Ansari**

This notice covers SniffScope's original code and assets distributed with:

```text
SniffScope-Setup.exe
```

Bundled third-party components, including Npcap, remain subject to their respective licenses and terms.

---

# ◆ Developer

**Maaz Ansari**

Cybersecurity Student | Security Research & Development

**Portfolio:**
https://maazansari.vercel.app

**Licensing / Contact:**
https://maazansari.vercel.app/contact

---

## ◆ Quick Start

For experienced users:

```text
1. Open GitHub Releases
        │
        ▼
2. Download SniffScope-Setup.exe
        │
        ▼
3. Install SniffScope
        │
        ▼
4. Install Npcap if required
        │
        ▼
5. Launch SniffScope
        │
        ▼
6. Access Command Center
        │
        ▼
7. Create local credentials
        │
        ▼
8. Initialize System Administrator
        │
        ▼
9. Trigger ARP Scan
        │
        ▼
10. Review discovered devices
        │
        ▼
11. Select an authorized test device
        │
        ▼
12. Begin authorized traffic interception
        │
        ▼
13. Analyze DNS / traffic information
        │
        ▼
14. Export results to CSV
```

---

> **⚠ Final Reminder**
>
> Only scan, monitor, or intercept devices and networks that you own or have explicit authorization to test.
>
> SniffScope is intended as a learning tool for understanding network discovery, DNS activity, packet capture, and traffic analysis in controlled cybersecurity environments.
