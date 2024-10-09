# Sniffy
---------
Arp poisoning packet sniffer

# Installation
--------------
Runs on linux systems , debian since it uses apt repository for installation of packagaes/dependencies
If you're on another flavour of linux, you can still use the program with manual installation of 3 tools :
```
1. Wireshark
2. Nmap
3. Ettercap-text-only
```

#Usage
-------
The program is purely a proof of work intended for educational purposes. Sniffy is used to arp poison a target router
in order to get target device's network traffic which we will then analyze using wireshark , which is found using the network scan using the tool Nmap.

**NOTE**: You must be connected to the network you're targetting prior to usage of the program to sniff packets.

#### Scanning Network :
