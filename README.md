```
  _   _            _    _                ____ _                _       _               _   
 | | | | __ _  ___| | _(_)_ __   __ _   / ___| |__   ___  __ _| |_ ___| |__   ___  ___| |_ 
 | |_| |/ _` |/ __| |/ / | '_ \ / _` | | |   | '_ \ / _ \/ _` | __/ __| '_ \ / _ \/ _ \ __|
 |  _  | (_| | (__|   <| | | | | (_| | | |___| | | |  __/ (_| | |_\__ \ | | |  __/  __/ |_ 
 |_| |_|\__,_|\___|_|\_\_|_| |_|\__, |  \____|_| |_|\___|\__,_|\__|___/_| |_|\___|\___|\__|
                                |___/                                                      
```

#    Attention - IMPORTANT
Only attack systems for which you have a (written!) permission or that are available for learning. (e.g. learn platforms like THM/HTB)
Attacking systems without premission is *illegal* und can lead in worst case to jail time.

# Websites for Challenge Boxes
* TryHackMe (THM): https://tryhackme.com (my recommendation to get into IT Security, you are guided during the learn process!)
* HackTheBox (HTB): https://www.hackthebox.com

# TryHackMe OpenVPN Guide  
TryHackMe OpenVPN Guide:
Get the IP of the OpenVPN connection:

Search for the following line in the connection log, which contains the string `net_addr_v4_add`:  
`2022-12-29 06:17:28 net_addr_v4_add: 13.37.40.4/16 dev tun0`

The IP address before /16 is your assigned IP address in the network of THM. So in this case --> `13.37.40.4`

Alternative: Access the Access page (https://tryhackme.com/access) of THM, there is in the field "Internal Virtual IP Address" your assigned IP address.

Other possibility: You can do the TryHackMe OpenVPN room, to find the IP address: https://tryhackme.com/room/openvpn

# Challenge Box Recommendations  
https://tryhackme.com/room/basicpentestingjt -> My recommendation for geuided hacking for beginners.

# Website Recommendations  
CyberChef: https://gchq.github.io/CyberChef/

Hacktricks: https://book.hacktricks.xyz/welcome/readme

OWASP Cheat Sheet Series: https://cheatsheetseries.owasp.org/index.html

GTFO Bins: https://gtfobins.github.io/

# Tool Recommendations   
Burp Suite Community Edition: https://portswigger.net/burp/communitydownload  
Usually installable with your package manager (apt, yum etc.) on Linux or installer downloadable for Windows.  
Is included in Kali linux.

man - Man Pages - Collection of help and documentationpages. Invoke: `man <program name>`  
Example: `man nmap`

nmap - Port Scanning Tool with a lot of functions

ffuf (integrated in Kali) - Fuzzing/Bruteforcing Tool: https://github.com/ffuf/ffuf

SecLists - useful lists (fuzzing, credentials, etc.): https://github.com/danielmiessler/SecLists

Scripts for automted reconnaissance on systems (developed by the person behind Hacktricks): https://github.com/carlospolop/PEASS-ng

# Methodology Recommendations for Linux

Things you can easily check fast (on Linux systems):
* Files in the home directories
* Bash history
* Permissions in the home directories
* Cronjobs incl. permissions for the files
* Binaries with SUID Bit set (check GTFO Bins)

Search for SUID Binaries with find: `find <DIRECTORY> -perm -4000`  
Example: `find /bin -perm -4000 `  
See also: https://linux-audit.com/finding-setuid-binaries-on-linux-and-bsd/
