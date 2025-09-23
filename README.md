# Cybersecurity-
# Day-1
A tiny starter guide to run Nmap and turn results into basic CSV for beginners.

What is this?

Nmap is a tool to discover open ports and services on computers/networks. Use it only on systems you own or have permission to test.

Quick setup

Install Nmap: https://nmap.org

(Optional) Python 3 installed to parse XML.

Basic commands

Scan common ports on one host:

nmap -sV target.example.com


Scan all TCP ports (slower):

nmap -p- -sV target.example.com


Save output as XML (good for scripts):

nmap -sV -oX scans/output.xml target.example.com

Simple parse idea (convert XML → CSV)

Save scans/output.xml then use a small Python script to extract IP, port, state, service into results.csv.

Example (pseudo):

# uses lxml or xml.etree
# read scans/output.xml → write ip,port,state,service to results.csv

Tips (beginner-friendly)

Always get permission before scanning.

Start small: one host, fewer ports.

Use -sV to see service names/versions.

Keep XML (-oX) if you want to automate parsing later.
