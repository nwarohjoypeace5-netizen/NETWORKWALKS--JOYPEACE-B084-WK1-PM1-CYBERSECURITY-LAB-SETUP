# Kali-Linux-lab-setup
Building an isolated virtual lab for penetration testing and ethical hacking process.
## Project overview 
This project focuses on setting up a VirtualBox cybersecurity and penetration-testing environment using VirtualBox, Kali Linux and a custom NATNetwork.
## PURPOSE of the Lab
This laboratory provides a secure, isolated, and controlled virtual environment for future cybersecurity projects and hands-on practice, using oracle VirtualBox and kali Linux.
The lab will only be used for personal systems or system with explicit permission to test. 
## Lab Configuration
* Host OS ----- Windows 11pro
* Host RAM ----- 8 GB
* Processor ----- Intel(R) Core(TM) i7
* Hypervisor ---- Oracle VIRTUALBOX
* Security OS --- Kali Linux 2026.3
* Kali RAM ---- 2048 MB
* Virtual Network ---- NAT Network ( NATNework')
* Kali IP Address ---- 10.0.0.0/24
## Objectives
* Install and confugure VirtualBox.
* Import Kali Linux as a virtual machine.
* Updating the Ip address to the Private NAT network address
* Configure a static IP address
* Verify network connectivity
* Document setup hurdles and solutions.
* Prepare the environment for Future Cybersecurity Projects
## Lab Setup Procedure
## Step 1. Install 7-Zip
I installed 7-Zip to extract the kali Linux Virtual machine archive.
## Step 2. Install VirtualBOX
I installed oracle VirtualBox as the hypervisor.
## Step 3. Create the NAT Network
A dedicated NAT Network was ("NATNetwork") was created with the IPv4 prefix '10.0.0.0/24' with DHCP enabled
## Step 4. Import Kali Linux
Kali Linux was imported into vitualBOX, assigned 2048 MB of RAM, and attached to the 'NATNetwork'.
## Verification of Connection
* I verified network connectivity to ensure the Kali Linux virtual machine could successfully communicate externally through the custom NAT Network:
* I Verified that the virtual machine successfully obtained an IP address (`10.0.0.3`) dynamically via the `NatNetwork` DHCP server.
* Internet & DNS Verification: I Opened a web browser inside Kali Linux and successfully loaded Google, confirming that DNS resolution, outbound routing, and NAT translation through the Windows host were functioning correctly.
### Problems Encountered & Solution
I faced some difficulties while trying to set up the virtual lab. I encountered a persistent "nested folder" file pathing issue that caused disk attachment errors, I had to manually relocate the .vdi file and cleared out duplicate ID conflicts in VirtualBox. Additionally, I also encountered a hardware virtualization error (VT-x is disabled in the BIOS) because I had to enable virtualization on my laptop's BIOS settings so that the VirtualBOX would have the necessary processor support to boost 64-bit virtual machines. 
