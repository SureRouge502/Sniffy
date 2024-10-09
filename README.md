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

# Usage
-------
The program is purely a proof of work intended for educational purposes. Sniffy is used to arp poison a target router
in order to get target device's network traffic which we will then analyze using wireshark , which is found using the network scan using the tool Nmap.

**NOTE**: You must be connected to the network you're targetting prior to usage of the program to sniff packets.

### Scanning Network :
-----------------------
We will be doing that with the help of nmap. First we must give the program executable permissions in order to run on our system which can be done by the following command : 
```
chmod +x install.sh sniffy.sh
```

Running the installer using the code :
``` 
./install.sh
```

Running the program itself :
```
./sniffy
```

Once you run the program , the first question you'll be asked is for your routers IP address.
**Note** : You must include the '/24' at the end of your ip.
The program will then use NMAP to scan the target network for connected devices' IP addresses.  We will select one of those as our target systems.

### Arp poisoning
------------------
After we have our target's IP address, armed with this information , we can now poision the router using ARP (address resolution protocol) posioning in order to initiate a 'man-in-the-middle' attack. This will misinform the router about the destination of targets device to the router - and the routers destination to the target - putting yourself in the middle so you can sniff packets and gather intel regarding the target

This is done using a program called Ettercap. We will be using the CLI only version of it (There is a GUI version available). 

### Analyze packets 
--------------------
As soon as the arp poisoning is compltete , a wireshark window with root privilages will open up. You will then select your Network card and proceed to perfrom network analysis of the on coming traffic.

