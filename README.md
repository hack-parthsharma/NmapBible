# Nmap-Bible

All information in this repo is presented for research and learning purpose. No warranty or guarantee is provided and the owner and publisher shall not be held liable for any loss or damage.


# Introduction

`Nmap is an open source program released under the GNU General Public License (see www.gnu.org/copyleft/gpl.html). It is an evaluable tool for network administrators which can be used to discover, monitor, and troubleshoot TCP/IP systems. Nmap is a free cross-platform network scanning utility created by Gordon
“Fyodor” Lyon and is actively developed by a community of volunteers.`

A typical Nmap scan Nmap’s award-winning suite of network scanning utilities has been in constant development since 1997 and continually improves with each new release. Version 5.00 of Nmap (released in July of 2009) adds many new features and enhancements
including:
 Improved service and operating system version detection.
 Improved support for Windows and Mac OS X.
 Improved Nmap Scripting Engine (NSE) for performing complex scanning
tasks.
 Addition of the Ndiff utility which can be used to compare Nmap scans.
 Ability to graphically display network topology with Zenmap.
 Additional language localizations including German, French, and
Portuguese.
 Better overall performance.

The Nmap project relies on volunteers to support and develop this amazing tool. If you would like to help improve Nmap, there are several ways to get involved:
Promote Nmap.

Nmap is a wonderful tool that every administrator network should know about. Despite its popularity, Nmap isn’t widely known outside of technically elite circles. Promote Nmap by introducing it to your friends or write a blog entry about it and help spread the word.

# Report Bugs
You can help improve Nmap by reporting any bugs you discover to the Nmap developers. The Nmap project provides a mailing list for this which can be found online at www.seclists.org/nmap-dev.

# Note
Thousands of people worldwide use Nmap. Additionally, Nmap developers are very busy people. Before reporting a bug, or asking for assistance, you should search the Nmap website at www.insecure.org/search.html to make sure your problem hasn’t already been reported or resolved.

# Contribute Code
If you’re a hacker with some spare time on your hands, you can get involved with Nmap development. To learn more about contributing code to the Nmap project visit www.nmap.org/data/HACKING.

The Nmap project does not accept donations. If, however, you have a security related service you would like promote, you can sponsor Nmap by purchasing an
advertising package on the insecure.org website. For more information visit www.insecure.org/advertising.html.

  # Installing Nmap 
  
## Step 1
Download the Windows version of Nmap from www.nmap.org.
## Step 2
Launch the Nmap setup program. Select the default installation (recommended) which will install the entire Nmap suite of utilities. During installation, a helper program called WinPcap will also be installed. WinPcap is required for Nmap to function properly on the Windows platform so do not skip this step.                       

## Step 3
Once Nmap has been successfully installed you can verify it is working correctly by
executing nmap scanme.insecure.org on the command line (located in Start >Programs > Accessories > Command Prompt).

## C:\>nmap scanme.insecure.org
`Starting Nmap 5.00 ( http://nmap.org ) at 2022-08-09 09:36 Central`
`Daylight Time`
`Interesting ports on scanme.nmap.org (00.00.000.00):`
`Not shown: 994 filtered ports`
PORT STATE SERVICE
25/tcp closed smtp
70/tcp closed gopher
80/tcp open http
110/tcp closed pop3
113/tcp closed auth
31337/tcp closed Elite
Nmap done: 1 IP address (1 host up) scanned in 9.25 seconds
C:\>

# ---- Nmap test scan on Microsoft Windows ( ͡❛ ͜ʖ ͡❛)----

## Installing Nmap on Unix and Linux systems: 
Most popular Linux distributions provide binary Nmap packages which allow for simple installation. Installation on Unix systems requires compiling Nmap from source code.

### Installing Precompiled Packages for Linux For Debian and Ubuntu based systems
 `apt-get install nmap`
### For Red Hat and Fedora based systems
` yum install nmap`
### For Gentoo Linux based systems
 `emerge nmap`
### To check which version of Nmap you are running, type the following command on
the command line:
 `nmap -V`
`Nmap version 8.00 ( http://nmap.org )`

## Once Nmap has been successfully installed, you can verify it is working correctly by executing nmap localhost on the command line.
`$ nmap localhost`
Starting Nmap 8.00 ( http://nmap.org ) at 2022-08-07 00:42 CDT
Warning: Hostname localhost resolves to 2 IPs. Using 127.0.0.1.
Interesting ports on e6400 (127.0.0.1):
Not shown: 993 closed ports
PORT STATE SERVICE
22/tcp open ssh
25/tcp open smtp
111/tcp open rpcbind
139/tcp open netbios-ssn
445/tcp open microsoft-ds
631/tcp open ipp
2049/tcp open nfs

Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds

# Nmap test scan on Unix/Linux ( ͡👁️ ͜ʖ ͡👁️)


## Basic Scanning Techniques

## Basic Scanning Overview
This section covers the basics of network scanning with Nmap. Before we begin it is
important to understand the following concepts:

### Firewalls, routers, proxy servers, and other security devices can skew the results of an Nmap scan. Scanning remote hosts that are not on your local network may provide misleading information because of this.

### Some scanning options require elevated privileges. On Unix and Linuxsystems you may be required to login as the root user or to execute Nmap using the sudo command.

### There are also several warnings to take into consideration:
Scanning networks that you do not have permission to scan can get you in trouble with your internet service provider, the police, and possibly even the
government. Don’t go off scanning the FBI or Secret Service websites unless you want to get in trouble.

Aggressively scanning some systems may cause them to crash which can lead to undesirable results like system downtime and data loss. Always scan mission critical systems with caution.


# Nmap Online Resources
Fyodor’s Nmap Book
www.nmap.org/book/man.html




Nmap Install Guide
www.nmap.org/book/install.html




Nmap Scripting Engine Documentation
www.nmap.org/nsedoc/




Zenmap Reference Guide
www.nmap.org/book/zenmap.html




Nmap Change Log
www.nmap.org/changelog.html




Nmap Mailing Lists
www.seclists.org




Nmap Online Scan
www.nmap-online.com




Security Tools
www.sectools.org




Nmap Mailing Lists
www.seclists.org




Nmap Facebook
www.nmap.org/fb




Nmap Twitter
www.twitter.com/nmap




Nmap Cookbook
www.nmapcookbook.com

#                                                                Nmap Cheat Sheet

## Basic Scanning Techniques 

Scan a Single Target                         `nmap [target]`




Scan Multiple Targets                        `nmap [target1, target2, etc]`




Scan a List of Targets                       `nmap -iL [list.txt]`




Scan a Range of Hosts                        `nmap [range of ip addresses]`




Scan an Entire Subnet                        nmap [ip address/cdir]




Scan Random Hosts                            nmap -iR [number]Crop a circle in image online - free 




Excluding Targets from a Scan                nmap [targets] --exclude [targets]




Excluding Targets Using a List               nmap [targets] --excludefile [list.txt]




Perform an Aggressive Scan                   nmap -A [target]




Scan an IPv6 Target                          nmap -6 [target]





## Discovery Options 

|rform a Ping Only Scan                     nmap -sP [target]




|on’t Ping                                   nmap -PN [target]




|CP SYN Ping                                 nmap -PS [target]




|CP ACK Ping                                 nmap -PA [target]




|DP Ping                                     nmap -PU [target]




|CTP INIT Ping                               nmap -PY [target]




|CMP Echo Ping                               nmap -PE [target]




|CMP Timestamp Ping                          nmap -PP [target]




|CMP Address Mask Ping                       nmap -PM [target]




|P Protocol Ping                             nmap -PO [target]




|ARP Ping                                     nmap -PR [target]




|Traceroute                                   nmap --traceroute [target]




|Force Reverse DNS Resolution                 nmap -R [target]




|Disable Reverse DNS Resolution               nmap -n [target]




|Alternative DNS Lookup                       nmap --system-dns [target]




|Manually Specify DNS Server(s)               nmap --dns-servers [servers] [target]




|Create a Host List                           nmap -sL [targets]





## Advanced Scanning Functions

|TCP SYN Scan                                  nmap -sS [target]




|TCP Connect Scan                              nmap -sT [target]




|UDP Scan                                      nmap -sU [target]




|TCP NULL Scan                                 nmap -sN [target]




|TCP FIN Scan                                  nmap -sF [target]




|Xmas Scan                                     nmap -sX [target]




|TCP ACK Scan                                  nmap -sA [target]




|Custom TCP Scan                               nmap --scanflags [flags] [target]




|IP Protocol Scan                              nmap -sO [target]




|Send Raw Ethernet Packets                     nmap --send-eth [target]




|Send IP Packets                               nmap --send-ip [target]




## Port Scanning Options
Perform a Fast Scan                           nmap -F [target]
Scan Specific Ports                           nmap -p [port(s)] [target]
Scan Ports by Name                            nmap -p [port name(s)] [target]
Scan Ports by Protocol                        nmap -sU -sT -p U:[ports],T:[ports] [target]
Scan All Ports                                nmap -p "*" [target]
Scan Top Ports                                nmap --top-ports [number] [target]
Perform a Sequential Port Scan                nmap -r [target]

## Version Detection

Operating System Detection                     nmap -O [target]
Submit TCP/IP Fingerprints                     www.nmap.org/submit/
Attempt to Guess an Unknown                    nmap -O --osscan-guess [target]
Service Version Detection                      nmap -sV [target]                    
Troubleshooting Version Scans                  nmap -sV --version-trace [target]
Perform a RPC Scan                             nmap -sR [target]

## Timing Options
Timing Templates                               nmap -T[0-5] [target]
Set the Packet TTL                             nmap --ttl [time] [target]
Minimum # of Parallel Operations               nmap --min-parallelism [number] [target]
Maximum # of Parallel Operations               nmap --max-parallelism [number] [target]
Minimum Host Group Size                        nmap --min-hostgroup [number] [targets]
Maximum Host Group Size                        nmap --max-hostgroup [number] [targets]
Maximum RTT Timeout                            nmap --initial-rtt-timeout [time] [target]
Initial RTT Timeout                            nmap --max-rtt-timeout [TTL] [target]
Maximum Retries                                nmap --max-retries [number] [target]
Host Timeout                                   nmap --host-timeout [time] [target]
Minimum Scan Delay                             nmap --scan-delay [time] [target]
Maximum Scan Delay                             nmap --max-scan-delay [time] [target]
Minimum Packet Rate                            nmap --min-rate [number] [target]
Maximum Packet Rate                            nmap --max-rate [number] [target]
Defeat Reset Rate Limits                       nmap --defeat-rst-ratelimit [target]

## Firewall Evasion Techniques
Fragment Packets                                nmap -f [target]
Specify a Specific MTU                          nmap --mtu [MTU] [target]
Use a Decoy                                     nmap -D RND:[number] [target]
Idle Zombie Scan                                nmap -sI [zombie] [target]
Manually Specify a Source Port                  nmap --source-port [port] [target]
Append Random Data                              nmap --data-length [size] [target]
Randomize Target Scan Order                     nmap --randomize-hosts [target]
Spoof MAC Address                               nmap --spoof-mac [MAC|0|vendor] [target]
Send Bad Checksums                              nmap --badsum [target]

## Output Options
Save Output to a Text File                      nmap -oN [scan.txt] [target]
Save Output to a XML File                       nmap -oX [scan.xml] [target]
Grepable Output                                 nmap -oG [scan.txt] [targets]
Output All Supported File Types                 nmap -oA [path/filename] [target]
Periodically Display Statistics                 nmap --stats-every [time] [target]
133t Output                                     nmap -oS [scan.txt] [target]

## Troubleshooting and Debugging

Getting Help                                    nmap -h
Display Nmap Version                            nmap -V
Verbose Output                                  nmap -v [target]
Debugging                                       nmap -d [target]
Display Port State Reason                       nmap --reason [target]
Only Display Open Ports                         nmap --open [target]
Trace Packets                                   nmap --packet-trace [target]
Display Host Networking                         nmap --iflist
Specify a Network Interface                     nmap -e [interface] [target]

## Nmap Scripting Engine
Execute Individual Scripts                      nmap --script [script.nse] [target]




Execute Multiple Scripts                        nmap --script [expression] [target]




Script Categories                               all, auth, default, discovery, external,
intrusive, malware, safe, vuln
Execute Scripts by Category                     nmap --script [category] [target]
Execute Multiple Script Categories              nmap --script [category1,category2,etc]
Troubleshoot Scripts                            nmap --script [script] --script-trace [target]
Update the Script Database                      nmap --script-updatedb

## Ndiff
Comparison Using Ndiff                          ndiff [scan1.xml] [scan2.xml]




Ndiff Verbose Mode                              ndiff -v [scan1.xml] [scan2.xml]




XML Output Mode                                 ndiff --xml [scan1.xml] [scan2.xml]





## Nmap Port States

### open
An open port is a port that actively responds to an incoming connection.
### closed
A closed port is a port on a target that actively responds to a probe but does not
have any service running on the port. Closed ports are commonly found on systems
where no firewall is in place to filter incoming traffic.
### filtered
Filtered ports are ports that are typically protected by a firewall of some sort that
prevents Nmap from determining whether or not the port is open or closed.
### unfiltered
An unfiltered port is a port that Nmap can access but is unable to determine
whether it is open or closed.
#### open|filtered
An open|filtered port is a port which Nmap believes to be open or filtered but
cannot determine which exact state the port is actually in.
### closed|filtered
A closed|filtered port is a port that Nmap believes to be closed or filtered but
cannot determine which respective state the port is actually in

## CIDR Cross Reference
Subnet Mask          CIDR




000.000.000.000      /0



128.000.000.000      /1




192.000.000.000      /2




224.000.000.000      /3




240.000.000.000      /4




248.000.000.000      /5




252.000.000.000      /6




254.000.000.000      /7




255.000.000.000      /8




255.128.000.000      /9




255.192.000.000      /10




255.224.000.000      /11




255.240.000.000      /12




255.248.000.000      /13




255.252.000.000      /14




255.254.000.000      /15




255.255.000.000      /16




255.255.128.000      /17




255.255.192.000      /18




255.255.224.000      /19




255.255.240.000      /20




255.255.248.000      /21




255.255.252.000      /22




255.255.254.000      /23




255.255.255.000      /24




255.255.255.128      /25




255.255.255.192      /26




255.255.255.224      /27




255.255.255.240      /28




255.255.255.248      /29




255.255.255.252      /30




255.255.255.254      /31




255.255.255.255      /32





# Common TCP/IP Ports
Port   Type     Usage
20   TCP FTP    Data
21   TCP FTP    Control
22   TCP|UDP    Secure Shell (SSH)
23   TCP        Telnet
25   TCP        Simple Mail Transfer Protocol (SMTP)
42   TCP|UDP    Windows Internet Name Service (WINS)
53   TCP|UDP    Domain Name System (DNS)
67   UDP        DHCP Server
68   UDP        DHCP Client
69   UDP        Trivial File Transfer Protocol (TFTP)
80   TCP|UDP    Hypertext Transfer Protocol (HTTP)
110  TCP       Post Office Protocol 3 (POP3)
119  TCP       Network News Transfer Protocol (NNTP)
123  UDP       Network Time Protocol (NTP)
135  TCP|UDP   Microsoft RPC
137  TCP|UDP   NetBIOS Name Service
138  TCP|UDP   NetBIOS Datagram Service
139  TCP|UDP   NetBIOS Session Service
143  TCP|UDP   Internet Message Access Protocol (IMAP)
161  TCP|UDP   Simple Network Management Protocol (SNMP)
162  TCP|UDP   Simple Network Management Protocol (SNMP) Trap
389  TCP|UDP   Lightweight Directory Access Protocol (LDAP)
443  TCP|UDP   Hypertext Transfer Protocol over TLS/SSL (HTTPS)
445  TCP       Server Message Block (SMB)
636  TCP|UDP   Lightweight Directory Access Protocol over TLS/SSL (LDAPS)
873  TCP       Remote File Synchronization Protocol (rsync)
993  TCP       Internet Message Access Protocol over SSL (IMAPS)
995  TCP       Post Office Protocol 3 over TLS/SSL (POP3S)
1433 TCP      Microsoft SQL Server Database
3306 TCP      MySQL Database
3389 TCP      Microsoft Terminal Server/Remote Desktop Protocol (RDP)
5800 TCP      Virtual Network Computing (VNC) web interface
5900 TCP      Virtual Network Computing (VNC) remote desktop
