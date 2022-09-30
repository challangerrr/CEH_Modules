**Module 10** 

**Denial Of Service**

**What is Denial os service?**

Dos attack is attack in which attacker overload the legitimate user system resource.

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.001.png)

**What is DDos (distributed denial of service)?**

A DDoS attack use many computer to launch a coordinate dos attack against one or more targets

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.002.png)

**Types of DoS & DDoS attack** 

**UDP flood attack:-** An attacker send spoofed UDP packet to the victim system to overload the resources of victim system . victim lost the legitimate application access

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.003.png)

Lets see the practical of udp flood DoS attack

` `we will  use hping3 tool 

Command:- hping3 -2 –-flood [ip]

This will send high rate of udp packets

**ICMP flood attack:-** In this attack attacker send ping packet with high rate, cause website become stuck , system become lagy .

Command :- hping3 -1 --flood [IP]

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.004.png)

**Zero Day DoS attack:-** This attack means vulnerability which is not patched and not aware of this weakness , but hacker got this vulnerability and Exploit this. Similarly in Dos  zeroday attack patch is not available, attacker effectively block all the mechanism and steal the sensitive data.

**Ping of death attack:-** An Attacker want to crash, destabilize or freeze the Target system by sending large size of packets . 

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.005.png)

**Performing PoD attack :**

Command :- ping -l 65540 [IP]

`              `Ping [IP]-l 65500 -w 1 -n 1

**Smurf attack**:- Attacker spoof the victim ip address and send the echo of icmp packets to the IP broadcast network, and all the request are sent to the victim machine because attacker spoof the victim Ip address

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.006.png)

**Fragmantation Attack :-**  In this attack attacker want from victim to reassemble the fragment packet which is a combination of data segment with Ip header , But attacker send large no of fragmented packet to victim web server  with very small packet rate.

Because the protocol allows the fragmentation , these packet easly pass without any inspection through the network component  such as router , firewall. 

All small fragmantaion packet take large space of the resource and make system crash.

![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.007.png) 

**SYN flood attack:-**  In this attack , attacker send the syn packet, syn(synchronise) is TCP packet which is used in three way handshake, with fake IP to the target IP. The target ip response with SYN/ACK packet and wait for the ACK packets to complete the session but target machine did not get a response because it get request with fake IP.

Here attacker take advantage , because when target send syn packet to the victim. Victim host keep tracking and keep its connection partially open and keep listening in queue for atleast 75 second . Attacker exploit this small listening queue by sending multiple syn requests but never replying with syn-ack packet.


`  `![](Aspose.Words.b867f034-488b-4058-8217-d4c7e2c6a62a.008.png)

**Perform SYN flood attack** 

Command :- msfconsole (open Metasploit)

Command:- use auxiliary/dos/tcp/synflood

Command :- set rhost[target ip] && set rport 21 && set host [local IP]

` `Exploit  done

Through hping3 tool also syn flood can be done

` `Command :- hping3 -p 21 --flood [IP]

Backend activity can be seen in wireshark .

One tool is good for Dos attack 

Source :- <https://github.com/gkbrk/slowloris>

Command :- python3 slowloris.py -p 21 [IP]

Another tool is Goldeneye, a python language based tool

Command:- ./goldeneye.py <http://testphp.vulnweb.com/>  -w 100 -s 1000 -m random

LOIC- low orbit canon

1st source:- <https://github.com/nicolargo/loicinstaller>

