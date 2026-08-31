# Lab 01 – Windows 11 Security Endpoint Deployment

## Overview

This lab documents the deployment and initial security configuration of a Windows 11 endpoint in VMware Workstation.

The objective was to build a controlled Windows 11 virtual machine that can be used as a foundation for future cybersecurity, SOC, endpoint security, and incident-response labs.

---

## Lab Environment

| Component | Configuration |
|---|---|
| Hypervisor | VMware Workstation Pro |
| Virtual Machine | Security-Endpoint-01 |
| Operating System | Windows 11 Pro |
| Architecture | x64 |
| Virtual CPU | 4 cores |
| Memory | 6 GB RAM |
| Virtual Disk | 80 GB |
| Network | NAT |
| Firmware | UEFI |
| Installation Media | Windows 11 ISO |

---

## Objectives

- Deploy a Windows 11 virtual endpoint using VMware Workstation.
- Configure appropriate virtual hardware resources.
- Install Windows 11 Pro from an ISO image.
- Configure network connectivity using NAT.
- Verify the Windows installation and system configuration.
- Create a VMware snapshot after the base installation.
- Prepare the endpoint for future cybersecurity security labs.

---

## 1. Virtual Machine Creation

A new virtual machine was created in VMware Workstation.

### Hardware Configuration

The virtual machine was configured with:

- **6 GB RAM**
- **4 CPU cores**
- **80 GB virtual disk**
- **NAT networking**
- Windows 11 ISO connected through the virtual CD/DVD drive.

The virtual disk was configured as a single virtual disk file.

---

## 2. Windows 11 Installation

Windows 11 was installed using the Windows 11 ISO image.

During installation:

1. Windows 11 Setup was launched.
2. Windows 11 Pro was selected.
3. The 80 GB unallocated virtual disk was selected as the installation destination.
4. Windows installation completed successfully.
5. The system rebooted into Windows 11.

---

## 3. Windows 11 Initial Configuration

After installation, the virtual machine successfully booted into the Windows 11 desktop.

The system was configured as a standalone laboratory endpoint.

The Windows installation was verified using **System Information**.

### Verification

The following system information was confirmed:

- Operating System: **Microsoft Windows 11 Pro**
- System Type: **x64-based PC**
- BIOS Mode: **UEFI**
- System Manufacturer: **VMware, Inc.**
- System Model: **VMware20,1**

---

## 4. Network Configuration

Windows network connectivity was verified through Network Connections.

The virtual machine was configured using VMware's **NAT** network mode.

The Windows endpoint detected the virtual network adapter successfully.

---

## 5. Service Verification

Windows Services was opened to review the installed and running Windows services.

This provides an initial understanding of the services operating on the endpoint and establishes a baseline for future security investigations.

---

## 6. VMware Snapshot

After completing the initial Windows installation and configuration, a VMware snapshot was created.

### Purpose of the Snapshot

The snapshot provides a restore point for the virtual machine.

This allows the lab environment to be returned to a known-good baseline before performing future cybersecurity experiments.

For example, future labs may involve:

- Installing security tools
- Generating security events
- Testing endpoint detection
- Malware-analysis simulations
- Network-security experiments
- Incident-response exercises

If a future experiment damages or changes the environment, the virtual machine can be reverted to the clean snapshot.

---

## 7. Troubleshooting During Installation

During the installation process, the VM initially encountered an EFI/network boot timeout.

The VMware boot manager was then used to select the appropriate virtual CD/DVD device containing the Windows 11 installation media.

Windows Setup subsequently loaded successfully and installation continued.

This demonstrated basic troubleshooting of:

- VMware boot configuration
- UEFI boot options
- Virtual CD/DVD devices
- Windows installation media

---

## 8. Lab Outcome

The Windows 11 security endpoint was successfully deployed and verified.

The resulting virtual machine provides a clean baseline environment for future cybersecurity exercises.

### Current Baseline

**Security-Endpoint-01**

- Windows 11 Pro
- 6 GB RAM
- 4 CPU cores
- 80 GB virtual disk
- NAT networking
- UEFI
- VMware Workstation
- Clean snapshot created

---

## Skills Demonstrated

- VMware Workstation administration
- Virtual machine deployment
- Windows 11 installation
- Windows system administration
- Basic endpoint configuration
- Network configuration
- UEFI/boot troubleshooting
- Windows service inspection
- System verification
- Virtual machine snapshot management
- Cybersecurity lab environment preparation

---

## Cybersecurity Relevance

This endpoint will serve as the foundation for future hands-on cybersecurity labs involving:

- Endpoint security
- Security monitoring
- SOC operations
- Threat detection
- Incident response
- Windows event logging
- Network security
- Vulnerability assessment

---

## Evidence

Screenshots documenting the lab configuration and installation process are included in this repository.

---

## Next Lab

The next phase will build security monitoring and detection capabilities on this Windows endpoint.
