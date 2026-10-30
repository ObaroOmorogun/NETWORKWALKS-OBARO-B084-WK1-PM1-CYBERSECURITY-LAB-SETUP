# NETWORKWALKS-OBARO-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP

**NetworkWalks Cybersecurity Training — Week 1 Assignment**

**Project:** Cybersecurity Lab Setup Using Kali Linux and Oracle VirtualBox

## 1. Project Overview

This project documents the installation, configuration, and verification of a cybersecurity testing lab using Oracle VirtualBox and Kali Linux on a Windows host computer.

The objective is to establish a functional virtualized environment for practical cybersecurity training, networking, and security testing.

## 2. Lab Environment

**Component Configuration:**

Host Operating System - Windows
Virtualization Platform - Oracle VirtualBox 7.2.22
Guest Operating System - Kali Linux 2026.3 (64-bit)
Host RAM - 32 GB
Network Type - NAT Network
Network Name - CyberLab-NAT
Network Subnet - 10.0.0.0/24
Kali Linux IP - 10.0.0.2/24
Default Gateway - 10.0.0.1
DNS Servers - 1.1.1.1, 8.8.8.8
Shared Folder - /downloads

## 3. Implementation Steps

**Step 1: Oracle VirtualBox Installation**

Installed Oracle VirtualBox on the Windows host computer.

**Step 2: Kali Linux Installation**

Downloaded the preconfigured Kali Linux 2026.3 VirtualBox image, extracted the files, and registered the virtual machine in VirtualBox Manager.

**Step 3: NAT Network Configuration**

Created a NAT Network named CyberLab-NAT using subnet 10.0.0.0/24, with DHCP disabled.

**Step 4: Static IP Configuration**

Configured Kali Linux with static IP address 10.0.0.2/24, default gateway 10.0.0.1, and DNS servers.

**Step 5: Internet Connectivity Verification**

Successfully tested connectivity using ping commands to 1.1.1.1 and google.com.

**Step 6: Shared Folder Configuration**

Configured the Windows folder C:\CyberLab\Downloads to be accessible within Kali Linux at /downloads.

Successfully verified file transfer in both directions.

**Step 7: Clipboard and Drag-and-Drop**

Enabled bidirectional clipboard and drag-and-drop in VirtualBox.

Bidirectional clipboard functionality was successfully verified.

Windows-to-Kali drag-and-drop worked, but Kali-to-Windows drag-and-drop remained unsuccessful despite troubleshooting.

**Step 8: Recovery Snapshot**

Created a VirtualBox snapshot to preserve the working lab configuration before updating Guest Additions.

## 4. Challenges Encountered

Read-Only Filesystem Issue

During static IP configuration, Kali Linux returned a read-only filesystem error that prevented NetworkManager from saving the configuration.

The filesystem was successfully restored to read/write mode, allowing the network configuration to be completed.

VirtualBox Drag-and-Drop Issue

Guest-to-host drag-and-drop failed with VERR_TIMEOUT and VERR_IPE_UNINITIALIZED_STATUS errors.

Troubleshooting included updating Guest Additions, restarting VBoxClient, verifying the X11/XFCE session, and checking kernel modules.

The issue remains unresolved. However, bidirectional file transfer through the shared folder works successfully.

## 5. Verification Results

**Requirement & Result**

VirtualBox installation - Passed
Kali Linux installation - Passed
NAT Network configuration - Passed
Static IP configuration - Passed
Internet connectivity - Passed
Shared folder access - Passed
Bidirectional file transfer - Passed
Bidirectional clipboard - Passed
Windows-to-Kali drag-and-drop - Passed
Kali-to-Windows drag-and-drop - Unresolved

## 6. Lessons Learned

This assignment strengthened my practical understanding of:

- Virtualization using Oracle VirtualBox.
- Kali Linux installation and administration.
- NAT networking and static IP configuration.
- Linux filesystem troubleshooting.
- VirtualBox Guest Additions.
- Shared-folder configuration and file transfers.
- Troubleshooting virtualization integration issues.

## 7. Screenshots

Screenshots documenting the installation, configuration, troubleshooting, and verification processes are available in the screenshots directory.

## 8. Acknowledgement

Special appreciation to Waqas Karim and the NetworkWalks team for their guidance and support throughout this practical assignment.

## 9. Conclusion

The Week 1 cybersecurity lab environment was successfully established, with the essential networking, internet access, clipboard, and shared-folder functionality verified.

Guest-to-host drag-and-drop remains an outstanding limitation, but the lab is operational for subsequent cybersecurity exercises.
