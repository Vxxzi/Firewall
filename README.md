# Firewall Deployment and Configuration 

## Objective

The objective of this project is to implement and demonstrate effective techniques for configuring a firewall using UFW and detecting network vulnerabilities with Nmap.

By exploring and applying these tools, the project aims to enhance understanding of network security principles, improve defensive measures against potential threats, and develop practical skills in monitoring and managing network traffic. 

Through hands-on experience, the project seeks to empower users with the knowledge to create secure environments and respond effectively to security incidents.

## Pre-requisites
- Basic understanding of networking concepts
- Familiarity with the Linux command line
- Knowledge of common network protocols (HTTP, TCP/IP, etc.)
- A computer with at least 8GB of RAM and 20GB of free disk space
- Virtualization software (VirtualBox, VMware, etc.)

## Lab Set-up and Tools
### Lab Set-up
1. **Virtual Machines**:
   - **VM**: Ubuntu Virtual Machine

2. **Admin Configuration**:
Root Access or Sudo Privileges: You need administrative rights to install and configure UFW.
Debian-Based Linux Distribution: UFW is designed for use on Debian-based systems (e.g., Ubuntu, Linux Mint).
Installation of UFW: Ensure UFW is installed on your system (usually pre-installed on many distributions).

Prerequisites for Nmap:

**Root Access or Sudo Privileges**: Some Nmap functionalities require elevated privileges to gather detailed information about network services.

**Debian-Based Linux Distribution**: Nmap should be installed on a compatible Linux system.

**Installation of Nmap**: Make sure Nmap is installed (use sudo apt install nmap if it’s not).

**Network Access**: Ensure you have the appropriate permissions to scan the target IP addresses or networks to avoid legal issues.

   

### Tools
- **Uncomplicated Firewall**: A user-friendly interface for managing firewall rules on Debian-based systems, allowing for easy configuration of network traffic permissions.
- **Nmap**: A powerful network scanning tool used for discovering hosts, services, and vulnerabilities on a network. It provides various scanning techniques and detailed information about the scanned targets.
- **Terminal/Command Line Interface**: The primary environment for executing commands related to UFW and Nmap, where users input commands to manage firewall settings and perform network scans.
- **SSH Client (e.g., OpenSSH)**: For managing remote systems securely via SSH, which is commonly allowed through UFW.



## Steps used throughout the project


![sudo apt update](https://github.com/user-attachments/assets/4aa6bd63-c52c-4f3e-9a90-aaee1a0a4bf8)

*Ref 1: Execution of "sudo apt update"*

The command sudo apt update updates the package index on the Ubuntu Virtual Machine, ensuring that the system has the latest information on available software packages and their versions from the repositories.



![sudo apt upgrade -y](https://github.com/user-attachments/assets/493ef5f7-2f8c-4b89-a84c-e9970d2950ba)

*Ref 2: Execution of "sudo apt upgrade -y"*

The command "sudo apt upgrade -y" upgrades all installed packages on the linux system to their latest available versions without prompting for confirmation, ensuring that the system is up to date.



![sudo ufw enable](https://github.com/user-attachments/assets/4e218eb9-4a2d-447a-a29f-6bb003fa8257)

*Ref 3: Execution of "sudo ufw enable"*

The command "sudo ufw enable" activates the Uncomplicated Firewall (UFW) on a Linux system, enabling firewall rules to enhance security by controlling incoming and outgoing network traffic.

![sudo multiple rules](https://github.com/user-attachments/assets/ad7f2650-9fcc-42d5-a1b0-2972d9b3d20a)

*Ref 4: Execution of multiple commands*

- sudo ufw allow ssh: Allows incoming SSH (Secure Shell) connections on port 22, enabling remote access to the system.

- sudo ufw allow http: Permits incoming HTTP traffic on port 80, allowing web traffic to reach web servers hosted on the system.

- sudo ufw allow https: Allows incoming HTTPS (Hypertext Transfer Protocol Secure) traffic on port 443, enabling secure web traffic to reach the system.

- sudo ufw allow 8080/tcp: Opens port 8080 for TCP traffic, commonly used for alternative web servers or applications.

- sudo ufw allow 1000:2000/tcp: Allows TCP traffic on all ports within the range of 1000 to 2000, enabling connections for various services that may be using these ports.

Each of these commands configures the firewall to accept specific types of traffic, enhancing the system's accessibility while maintaining security.

![sudo ufw status verbose](https://github.com/user-attachments/assets/ea54eeb7-8096-4455-bf95-931b9d0b4a5b)

*Ref 5: Execution of "sudo ufw status verbose"*

The command `sudo ufw status verbose` displays the current status of the Uncomplicated Firewall (UFW), providing detailed information about the active firewall rules, including the specific ports and protocols that are allowed or denied.



![sudo apt install nmap](https://github.com/user-attachments/assets/d899ded7-2d1f-4931-ac8e-ade0ca42698d)

*Ref 6: Execution of "sudo apt install nmap"*

The command sudo apt install nmap installs Nmap, a powerful network scanning tool enabling users to discover hosts and services on a network, as well as to assess security vulnerabilities.





![nmap ip address](https://github.com/user-attachments/assets/f746e876-f44a-4be1-b75f-b09e76671ff5)

*Ref 7: Execution of "nmap -v -A 127.0.0.1"*

The command "nmap -v -A 127.0.0.1" performs a detailed scan on the local host (localhost) with verbose output, enabling service detection, operating system identification, and script scanning to gather comprehensive information about the services running and their configurations on the specified IP address.




![sudo ufw status numbered](https://github.com/user-attachments/assets/9634e3b7-3f4e-4f61-83cd-929613127771)

*Ref 8: Execution of "sudo ufw status numbered"*

The command "sudo ufw status numbered" displays the current status of the Uncomplicated Firewall (UFW) with each rule listed alongside a number, making it easier to reference and manage specific rules for modification or deletion.



![sudo ufw delete 2](https://github.com/user-attachments/assets/8db5bd6d-59e2-43cc-886c-b2045ef9d366)

*Ref 9: Execution of "sudo ufw delete 2"*

The command `sudo ufw delete 2` removes the firewall rule associated with the specified number (in this case, rule number 2) from the Uncomplicated Firewall (UFW), effectively updating the firewall configuration by eliminating that particular rule.


![nmap ip address 2 0](https://github.com/user-attachments/assets/040b52f4-7299-4506-92e6-9af7329634bc)

*Ref 10: Execution of " nmap -v -A 10.0.2.15"*


The command nmap -v -A 10.0.2.15 performs a comprehensive scan on the target IP address (10.0.2.15) with verbose output, enabling features such as service detection, operating system identification, and script scanning to gather detailed information about the services and configurations running on that specific host.


