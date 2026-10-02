
# 🔎 SniffScope

### Educational Network & DNS Traffic Viewer for Windows

**SniffScope** is a Windows desktop application designed for **educational network discovery and traffic analysis in authorized laboratory environments**.

It provides a graphical interface for discovering devices on a local network, viewing network information, analyzing DNS activity, and inspecting captured traffic during authorized security testing.

> ⚠️ **Authorized Use Only**
>
> SniffScope is intended for networks, systems, and devices that you own or have explicit permission to test.
>
> Do **not** use the software for unauthorized interception, surveillance, credential collection, traffic manipulation, or disruption of networks.
>
> You are responsible for complying with applicable laws, organizational policies, and network-usage rules.

---

## ✨ Features

SniffScope provides an educational environment for studying:

* 🌐 Local network device discovery
* 📡 ARP-based network scanning
* 💻 Device IP and MAC address identification
* 🏷️ Hardware/vendor identification
* 🔎 DNS traffic and domain-resolution analysis
* 📊 Network device status monitoring
* 🧪 Authorized traffic interception for laboratory testing
* 📋 Target host analysis
* 🌍 Domain/DNS resolution visibility
* 📦 Application and HTTP payload inspection where technically available
* 📁 CSV export of collected scan results

---

# 📋 Prerequisites

Before installing SniffScope, make sure your Windows system meets the following requirements.

### Required

* Windows operating system
* Administrator privileges when required by the installer
* **Npcap**

SniffScope requires Npcap for packet capture and network traffic analysis.

### Npcap

Download Npcap from its official website:

[Npcap Official Website](https://npcap.com/?utm_source=chatgpt.com)

The installer may have a versioned filename such as:

```text
npcap-1.89.exe
```

The exact filename may change as newer Npcap releases become available.

---

# 🚀 Installation

## Step 1 — Download SniffScope

Download the latest:

```text
SniffScope-Setup.exe
```

from the **GitHub Releases** section of this repository.

> Windows may display a security warning because the installer may not have a widely recognized code-signing reputation.

If Windows shows a warning, verify that you downloaded the installer from the intended official repository/release before proceeding.

---

## Step 2 — Start the Installer

Run:

```text
SniffScope-Setup.exe
```

Follow the installation wizard.

---

## Step 3 — Select Installation User

When prompted, select the appropriate installation option/user and click:

**Next**

---

## Step 4 — Select Installation Directory

Choose where SniffScope should be installed.

You can either:

* Keep the default installation directory, or
* Select a custom directory.

Then click:

**Next**

---

## Step 5 — Install Npcap

During installation, SniffScope may detect that Npcap is not installed.

If prompted:

1. Visit the official Npcap website.
2. Download the **Windows installer**.
3. Right-click the Npcap installer.
4. Select **Run as administrator**.
5. Complete the Npcap installation.
6. Restart Windows if Npcap requests it.

After Npcap has been installed, return to the SniffScope installer and click:

**Retry**

---

## Step 6 — Finish Installation

Once all prerequisites have been detected successfully, complete the SniffScope installation.

Click:

**Finish**

SniffScope is now installed.

---

# 🔐 First-Time Setup

After launching SniffScope, open:

### Access Command Center

You will be asked to configure your local SniffScope access credentials.

### 1. Choose Your Name

Enter the name you want to use for the local application profile.

### 2. Create an 8-Character Password

Create the required 8-character password.

### 3. Initialize System Administrator

Click:

**Initialize System Administrator**

SniffScope will initialize the local system configuration.

Wait while the application loads the required network information and credentials.

---

# 🌐 Network Discovery

Once initialization is complete, you can begin discovering devices on the local network.

## Step 1 — Trigger ARP Scan

Click:

**Trigger ARP Scan**

SniffScope will perform an ARP-based discovery process to identify devices visible on the local network.

Depending on the network configuration, discovered information may include:

| Information | Description                                |
| ----------- | ------------------------------------------ |
| IP Address  | Network address assigned to the device     |
| MAC Address | Hardware/network interface address         |
| Vendor      | Manufacturer information when identifiable |
| Status      | Current discovery/status information       |

---

## Step 2 — Wait for Discovery

SniffScope will begin scanning the network.

The application will populate the device list as devices are discovered.

You can use this information to study:

* Local network topology
* Connected devices
* IP addressing
* MAC addresses
* Hardware vendors
* Device visibility on the network

---

# 📊 Network Status

After the scan completes, the discovered devices will be displayed in the SniffScope interface.

The device list provides an overview of hosts detected during the scan.

This can be useful for educational exercises involving:

* Network inventory
* Network discovery
* Asset identification
* Basic network analysis

---

# 🧪 Authorized Traffic Interception

> ⚠️ **IMPORTANT**
>
> Only perform interception or traffic-analysis activities against systems where you have explicit authorization.
>
> For example, use a controlled laboratory environment containing your own virtual machines or devices.

To begin an authorized interception session:

1. Select the target device from the discovered-device list.

2. Review the target information.

3. Click:

   **Begin MITM (Man-in-the-Middle) Interception**

4. Follow any permission or authorization prompts shown by the application.

SniffScope will then begin the configured traffic-analysis process.

---

# 🔎 DNS & Traffic Analysis

During an authorized analysis session, SniffScope can display network information associated with observed traffic.

The interface may show:

* Source/target IP addresses
* Domain information
* DNS resolutions
* Target host information
* Application-related traffic information
* HTTP payload information where applicable

The purpose of this functionality is to provide a practical environment for learning how network traffic and DNS activity can appear during security analysis.

---

# 🌍 DNS Resolution Analysis

One of SniffScope's main educational features is examining DNS activity.

The application can help associate observed network activity with domain names and DNS resolutions.

For example, during an authorized lab session, you may observe:

```text
Device
   ↓
DNS Query
   ↓
example.com
   ↓
Resolved IP Address
   ↓
Network Connection
```

This allows students to study the relationship between:

**Device → DNS Query → Domain → IP Address → Network Traffic**

---

# 📦 Application & HTTP Payload Analysis

Where supported by the captured traffic and protocol conditions, SniffScope provides application-level traffic information.

You may also encounter:

**HTTP Payload Data**

This can be useful when studying how application-layer traffic appears during controlled network-security experiments.

> **Important:** Encrypted protocols such as HTTPS generally prevent the application from simply displaying the contents of encrypted traffic. Visibility depends on the protocol, encryption, capture conditions, and the specific traffic being analyzed.

---

# 📥 Export Scan Results

After completing a network scan, SniffScope provides an option to export the collected results.

Click:

**Download CSV**

The exported CSV can be used for:

* Documentation
* Lab reports
* Network inventory
* Further analysis
* Record keeping

Example workflow:

```text
ARP Scan
   ↓
Device Discovery
   ↓
Review Results
   ↓
Export CSV
   ↓
Analyze / Document
```

---

#  Targeted Host Analysis

After selecting a target during an authorized analysis session, SniffScope can provide additional information related to that host.

Depending on the available traffic, this may include:

* Target IP address
* DNS resolutions
* Domains observed
* Application traffic
* HTTP information
* Network activity

This section is intended for studying how a particular host communicates across a network during a controlled laboratory exercise.

---

# ⚠️ Permissions & Authorization

During operation, SniffScope may display permission or authorization-related prompts.

Always verify that you have permission before proceeding.

### Recommended Lab Environment

For learning and testing, use an isolated environment such as:

```text
┌──────────────────────┐
│   Your Test Network  │
└──────────┬───────────┘
           │
     ┌─────┴─────┐
     │            │
┌────▼────┐  ┌────▼────┐
│ Windows │  │  Linux  │
│ Victim  │  │  Tester │
└─────────┘  └─────────┘
```

Virtual machines are particularly useful because they allow you to create a controlled environment without affecting unrelated devices.

---

# 🆓 Trial Usage

SniffScope provides:

### **3 Free Attempts**

The application provides **3 free tries for scanning and MITM interception functionality**.

After the available free attempts have been used, additional usage requires credits/license activation.

---

# 🔑 Licensing & Credits

To request additional usage credits:

### Step 1 — Copy Your Machine ID

Open the relevant licensing/access section of SniffScope and copy your:

```text
Machine ID
```

### Step 2 — Contact the Developer

Visit:

[SniffScope Licensing / Contact](https://maazansari.vercel.app/contact?utm_source=chatgpt.com)

Use a valid email address and include your Machine ID when requesting a license.

### Step 3 — Request Credits

Once the request is processed, eligible users can receive:

**$100 worth of free scanning and MITM interception credits**

> Credit availability and licensing terms may be subject to change.

---

# 🛠️ Troubleshooting

## SniffScope asks me to install Npcap

Install Npcap from:

[Npcap Official Website](https://npcap.com/?utm_source=chatgpt.com)

Run the installer as administrator and restart Windows if requested.

Then return to SniffScope and select:

**Retry**

---

## Npcap is installed but SniffScope does not detect it

Try the following:

1. Close SniffScope.
2. Confirm Npcap is installed.
3. Restart Windows.
4. Launch SniffScope again.
5. Run SniffScope with the required Windows permissions.

---

## ARP Scan does not discover devices

Possible causes include:

* The device is not on the same local network.
* Network isolation is enabled.
* The network blocks or restricts ARP-based discovery.
* The interface selected by the system is not the expected network adapter.
* Windows permissions or packet-capture configuration are incomplete.

Test first in a controlled LAN/lab environment.

---

## DNS information is not appearing

DNS visibility depends on how the target system and network handle DNS.

Possible reasons include:

* Encrypted DNS
* DNS caching
* DNS-over-HTTPS / DNS-over-TLS
* Traffic occurring outside the captured interface
* Insufficient capture permissions

Therefore, absence of a DNS entry does not necessarily mean that the device did not access a domain.

---

# 🧪 Recommended Educational Lab

For cybersecurity students, SniffScope can be tested safely using an isolated virtual network.

A simple setup could contain:

```text
              Isolated Lab Network
                     │
        ┌────────────┼────────────┐
        │            │            │
   Windows VM    Linux VM    SniffScope
    Test Host    Test Host     Machine
```

Use only systems that you control or have explicit authorization to monitor.

This provides a practical environment for studying:

* ARP
* MAC addresses
* IP addressing
* DNS
* Network discovery
* Packet capture
* Traffic analysis
* HTTP
* Network monitoring
* Security testing concepts

---

# 🛡️ Responsible Use

SniffScope is an educational security tool.

It should **not** be used to:

* Intercept networks without authorization
* Monitor other people's devices without permission
* Collect credentials
* Capture private communications
* Disrupt network availability
* Circumvent security controls
* Conduct unauthorized surveillance

Use the software only within an authorized environment.

The developer does not authorize misuse of the software.

---

# 📄 Disclaimer

SniffScope is provided for educational and authorized security-testing purposes.

The software is provided **without warranty**. Users are solely responsible for ensuring that their use of SniffScope complies with applicable laws, regulations, organizational policies, and network-owner requirements.

The developer assumes no responsibility for unauthorized or unlawful use of the software.

---

# 📜 Copyright

Copyright © 2026 **Maaz Ansari**

This copyright notice covers SniffScope's original code and assets distributed with:

```text
SniffScope-Setup.exe
```

Bundled third-party components, including Npcap, remain subject to their respective licenses and terms.

---

# 👨‍💻 Developer

**Maaz Ansari**

Cybersecurity Student | Security Research & Development

🌐 Portfolio:

[maazansari.vercel.app](https://maazansari.vercel.app?utm_source=chatgpt.com)

📩 Licensing & Contact:

[Contact / Licensing](https://maazansari.vercel.app/contact?utm_source=chatgpt.com)

---

## 📌 Quick Start

For experienced users, the complete workflow is:

```text
1. Download SniffScope
        ↓
2. Install SniffScope
        ↓
3. Install Npcap if required
        ↓
4. Restart Windows if requested
        ↓
5. Launch SniffScope
        ↓
6. Access Command Center
        ↓
7. Create local credentials
        ↓
8. Initialize System Administrator
        ↓
9. Trigger ARP Scan
        ↓
10. Review discovered devices
        ↓
11. Select an authorized test device
        ↓
12. Begin authorized traffic interception
        ↓
13. Analyze DNS / traffic information
        ↓
14. Export results to CSV
```

---

### ⚠️ Final Reminder

**Only scan, monitor, or intercept devices and networks that you own or have explicit authorization to test.**

Use SniffScope as a learning tool to understand how network discovery, DNS activity, and traffic analysis work in controlled cybersecurity environments.
