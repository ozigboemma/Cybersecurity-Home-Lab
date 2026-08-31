# Lab 01 – Windows 11 Security Endpoint Deployment

## Overview

This lab documents the deployment and initial configuration of a Windows 11 virtual endpoint using VMware Workstation.

The purpose of this lab was to build a controlled Windows 11 environment that can serve as a foundation for future cybersecurity, endpoint security, SOC, threat detection, and incident response exercises.

## Objectives

- Deploy a Windows 11 virtual machine
- Configure the virtual machine using VMware Workstation
- Verify Windows 11 installation and system configuration
- Configure network connectivity
- Verify basic Windows services and system functionality
- Establish a stable endpoint for future cybersecurity exercises

## Lab Environment

| Component | Configuration |
|---|---|
| Hypervisor | VMware Workstation |
| Virtual Machine | Security-Endpoint-01 |
| Operating System | Windows 11 Pro |
| Architecture | x64 |
| CPU | 4 cores |
| Memory | 6 GB RAM |
| Disk | 80 GB |
| Network | NAT |
| Firmware | UEFI |

## Deployment Process

1. Created the Windows 11 virtual machine in VMware Workstation.
2. Configured virtual hardware and networking.
3. Installed Windows 11 Pro.
4. Verified the operating system and system configuration.
5. Verified network connectivity.
6. Reviewed Windows services and endpoint functionality.
7. Created a VMware snapshot to preserve the working baseline.

## Security Considerations

The endpoint was configured as a controlled lab environment that will be used for future security testing and monitoring exercises.

The VM snapshot provides a known-good baseline that can be restored before conducting future experiments.

## Evidence

Screenshots documenting the deployment and configuration process are available in the [`screenshots`](./screenshots/) directory.

## Status

**Completed** ✅

## Next Steps

Future labs will build upon this Windows 11 endpoint and introduce additional cybersecurity technologies and scenarios, including:

- Endpoint security
- Security monitoring
- SIEM
- Threat detection
- Incident response
- Vulnerability management
- Network security
