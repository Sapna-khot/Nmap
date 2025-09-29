# Cybersecurity-
# nmap

What is this?
Nmap is a tool to discover open ports and services on computers/networks. Use it only on systems you own or have permission to test.

Quick setup:
Install Nmap: https://nmap.org

Basic commands:
Scan common ports on one host:
  nmap -sV target.example.com

Scan all TCP ports (slower):
  nmap -p- -sV target.example.com

Save output as XML (good for scripts):
  nmap -sV -oX scans/output.xml target.example.com

Example (pseudo):
 uses lxml or xml.etree
 read scans/output.xml → write ip,port,state,service to results.csv

 **Tips :

* Always get permission before scanning.
* Start small: one host, fewer ports.
* Use -sV to see service names/versions.
* Keep XML (-oX) if you want to automate parsing later.
