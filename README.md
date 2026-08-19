ITEP 414 Week 3 — Enterprise Server Deployment

Project Overview
This portfolio project documents the deployment of the first Linux server for ABC Startup Solutions using Ubuntu Server in a virtual machine. The server is planned for file sharing, remote administration, database hosting, web hosting, and internal services.

Learning Objectives
- Explain the purpose of operating systems in enterprise environments.
- Differentiate BIOS and UEFI.
- Explain the computer boot process.
- Compare Ubuntu Server, Windows Server, and Rocky Linux.
- Install and configure Ubuntu Server in a VM.
- Enable SSH and verify server functionality.
- Produce professional technical documentation.

Virtual Machine Specifications
| Component | Requirement |
|---|---|
| Name | Ubuntu-Server-Week03 |
| RAM | 4 GB |
| CPU | 2 virtual processors |
| Storage | 40 GB VDI/VMDK |
| Network | NAT or Bridged if instructed |
| ISO | Ubuntu Server LTS |

Installation Summary
Ubuntu Server is configured with English language, an appropriate keyboard layout, DHCP networking, hostname `server01`, a non-root administrative account, guided whole-disk installation, and OpenSSH Server.

Configuration Summary
- Hostname: `server01`
- Network: DHCP unless instructed otherwise
- Disk: Guided – Use Entire Disk
- SSH: OpenSSH Server enabled
- Additional packages: none unless instructed

Verification Results
Run and capture evidence for:
- `hostname`
- `ip addr`
- `ping -c 4 google.com`
- `sudo apt update`
- `sudo apt upgrade -y`
- `systemctl status ssh`

BIOS vs UEFI Highlights
UEFI is the modern firmware standard and is commonly used with GPT and Secure Boot. BIOS is a legacy firmware approach commonly associated with MBR. UEFI provides better support for modern storage, security, and boot management.

Embedded Boot Process Flowchart
![Ubuntu Boot Process](diagrams/boot_process_flowchart.png)

Windows Server Activity
Install Windows Server Evaluation in a separate VM, assign a computer name, create an administrator password, log in, and capture installation screenshots.

## OS Comparison
The project compares Windows Server, Ubuntu Server, and Rocky Linux based on licensing, interface, package management, security, performance, use cases, advantages, and disadvantages.

## Challenges Encountered
The major challenge is connecting the installation steps and verification commands into a repeatable deployment procedure and understanding how firmware, GRUB, the Linux kernel, systemd, and services work together.

Reflection
This project taught me that deploying a server is more than installing an operating system. A system administrator must plan the virtual machine resources, configure the operating system consistently, secure remote access, verify every major service, and document the result. The Ubuntu Server laboratory made the relationship between hardware resources, networking, users, storage, and services more practical for me. I learned why a non-root administrative account is preferred and why SSH is important for remote administration. I also learned that verification commands such as hostname, ip addr, ping, apt update, apt upgrade, and systemctl status ssh provide direct evidence that the server is ready for its next stage of deployment. The most challenging part was understanding the boot process and connecting firmware, the boot loader, kernel, systemd, and services into one sequence. Comparing BIOS and UEFI helped me understand why modern computers use UEFI and GPT more often. The Windows Server comparison also showed me that operating system selection depends on licensing, management tools, security, performance, and the workload that the organization needs to support. Planning and documentation are important because another administrator should be able to reproduce the deployment without guessing. This project will help me become a better System Administrator by improving my troubleshooting, documentation, virtualization, Linux administration, and technical communication skills. It also showed me that screenshots and command results are valuable evidence rather than decoration. Overall, Week 3 gave me a practical foundation for deploying and validating a server in a controlled environment.

## References
- LSPU ITEP 414 Week 3 Self-Paced Learning Module
- https://ubuntu.com/server/docs
- https://documentation.ubuntu.com/
- https://learn.microsoft.com/windows-server/
- https://docs.rockylinux.org/
