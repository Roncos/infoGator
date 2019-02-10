# infoGator
Linux Information Gatherer

This script offers two operationg modes: Enumeration & Machine Inspection

The Enumeration mode is based on the common commands that need to be run on a Linux machine in a post-exploitation environment, reccomended for performing a local privilege escalation process.

The Machine Inspection mode automates the process of retriving information from a specified web site. It analyzes the site with Nmap, extract the open ports found and executes different tests. 

Current version: 
* tests on port 80 - Download entire site, enumerate files and directories with Dirb



USAGE:

* ./infoGator.sh -a
* ./infoGator.sh -n 192.168.10.11
* ./infoGator.sh -d -s -n 192.168.10.11
* ./infoGator.sh -g -w /usr/share/dirb/wordlist/big.txt -p /man -n 192.168.10.11 

 OPTIONS:
* -a  Run all tests on host
* -h  Displays usage info
* -v  Print current version
* -n [IP] Machine Inspection Mode - scan given IP and run tests on open ports
	  	 
* -s  Machine Inspection Mode - saves the scan in the current directory
* -d  Machine Inspection Mode - download entire site in the current directory
* -g  Machine Inspection Mode - enables Dirb to scan the site searching for common directories
	  	  IMPORTANT Dirb executable required to run the script in this mode
* -w [PATH] Machine Inspection Mode - specify a custom path to the wordlist for the scan
* -p [PATH] Machine Inspection Mode - specify a custom site path where Dirb will launch the scan

IMPORTANT Nmap and Dirb executable required to run the script in the Machine Inspection mode

WARNING use Machine Inspection Mode options BEFORE specifing -n

Running with no options = Less Tests Executed

Sources:
* https://github.com/rebootuser/LinEnum
* https://github.com/sleventyeleven/linuxprivchecker/blob/master/linuxprivchecker.py
* https://github.com/Arr0way/linux-local-enumeration-script
* https://sushant747.gitbooks.io/total-oscp-guide/privilege_escalation_-_linux.html
* https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/
* https://github.com/mubix/post-exploitation/wiki/Linux-Post-Exploitation-Command-List 


The project is part of the final essay for my graduation. 
It is meant for learning purposes only.
