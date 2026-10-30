# ARP-Attack-and-Network-Sniffing

# Explore Network Sniffing and ARP Attacks

### AIM:

To explore network sniffing and ARP attacks using Parrot OS and various network analysis tools.

### STEPS:

### Step 1:

Install Parrot Security OS either in a partition, VirtualBox or in live mode.

### Step 2:

Investigate the various categories of network security tools available in Parrot OS, such as:

* arpspoof
* dsniff
* Metasploit Framework
* Wireshark
* Ettercap
* tcpdump

### Step 3:

Open the terminal and execute some Parrot OS commands.

```bash
cat /etc/os-release
ip addr
ip route
ip neigh
ifconfig
```

### ARP Attacks:

ARP spoofing is an attack in which an attacker sends forged ARP packets that associate the attacker's MAC address with the IP address of another computer on a local network.

Boot Parrot OS and Windows 7 virtual machines.

In Windows 7, open Command Prompt and execute:

```cmd
ipconfig
arp -a
```

### OUTPUT:

<img width="813" height="607" alt="Screenshot 2026-10-30 114933" src="https://github.com/user-attachments/assets/7a099951-152c-4fa4-ba9e-1ec2be4f98f5" />


From Parrot OS, identify the active network interface using:

```bash
ifconfig
```
### OUTPUT:
<img width="945" height="533" alt="image" src="https://github.com/user-attachments/assets/bc2dd013-6d1d-4ca4-ad36-9c1426ea540c" />


Examine the ARP neighbor table using:

```bash
ip neigh
```
### OUTPUT:
<img width="771" height="136" alt="Screenshot 2026-10-30 115829" src="https://github.com/user-attachments/assets/2f3ca43e-55a7-45f1-86e4-37d8a3bbcb16" />


Check the routing information using:

```bash
ip route
```
### OUTPUT:
<img width="883" height="115" alt="image" src="https://github.com/user-attachments/assets/0b084da7-2b19-4575-a6ee-2fa8cc20342f" />







ARP spoofing concepts and their effects on IP-to-MAC address mappings were studied in an isolated virtual network.

### dsniff:

dsniff is a collection of network auditing and traffic analysis tools used to examine network traffic.

Install dsniff using:

```bash
sudo apt update
sudo apt install dsniff -y
```

Check the available utilities using:

```bash
dsniff -h
dpkg -L dsniff
```

### OUTPUT:
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/ff60489d-9ca2-47b9-b5e3-1cc59bc01947" />


### Metasploit Framework:

Metasploit is a penetration-testing framework used for security testing and vulnerability assessment.

Open Metasploit using:

```bash
msfconsole
```

Search for FTP-related auxiliary modules using:

```text
search type:auxiliary ftp
```

Examine FTP service identification modules.

### OUTPUT:

[Paste Screenshot – Metasploit FTP modules]

### Wireshark:

Wireshark is a network protocol analyzer used to capture and examine network packets.

Invoke Wireshark using:

```bash
sudo wireshark
```
<img width="941" height="851" alt="image" src="https://github.com/user-attachments/assets/0a5616bd-b9c2-42a0-b923-428de1a8b28d" />


Examine the various menus, controls, packet details and protocol information available in Wireshark.

### OUTPUT:

<img width="1110" height="692" alt="Screenshot 2026-10-30 120638" src="https://github.com/user-attachments/assets/cc237a5a-8b0a-4460-9073-86c804199dc2" />


### Ettercap:

Ettercap is a network security tool that supports active and passive network analysis and host discovery.

Open Ettercap using:

```bash
sudo ettercap -G
```

Explore the following menus:

* Sniff
* Hosts
* Targets
* View
* Plugins

Examine the graphical interface and network analysis features.

### OUTPUT:
<img width="1157" height="836" alt="Screenshot 2026-10-30 122812" src="https://github.com/user-attachments/assets/0e7f049e-4aa7-46da-9916-e41870e7274f" />




### tcpdump:

tcpdump is a command-line network packet analyzer used to capture and examine network traffic.

Check the installed version using:

```bash
tcpdump --version
```

Examine the available network interfaces using:

```bash
sudo tcpdump -D
```
### OUTPUT:

<img width="833" height="548" alt="image" src="https://github.com/user-attachments/assets/28edbb66-780e-495f-853d-0c65169081ec" />


Capture ARP packets on the active interface using:

```bash
sudo tcpdump -i enp0s3 arp
```

Stop packet capturing using `Ctrl + C`.

### OUTPUT:
<img width="780" height="422" alt="image" src="https://github.com/user-attachments/assets/4a1c27ee-5d23-4d31-a160-6ba9faee8532" />




### RESULT:

Thus, the network security and network sniffing tools available in Parrot OS, including arpspoof, dsniff, Metasploit, Wireshark, Ettercap and tcpdump, were explored successfully. The concepts of ARP attacks, ARP tables, network interfaces and packet analysis were studied.
