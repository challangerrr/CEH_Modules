# MODULE NO 02

## FootPrinting and Reconnaissance 

### What is footprinting ?
Footprint  is the process where attacker or intruder try to gain all possible information . It is first step of an ethical hacker , where attacker identify the risk.

Footprinting is a part of reconnaissance process which is used for gathering possible information about a target computer system or network.
Some of the tools used for Footprinting are :-
nslookup, traceroute , who is , Metasploit , nikto , Nmap etc

Footprinting Types: Active and Passive.
### ⦁	Passive –  
Passive footprinting means , an attacker gather information without coming in contact of victim or target . So we can gather info about target using search engine , social network sites, job site,  etc.
       e.g :- Websites, DNS records, .

### ⦁	Active – 
Active footprinting means , an attacker gather information by come in contact with target . Simple he do direct interaction with targets. HE will search digital files, harvesting email lists, perform Traceroute etc
                      e.g :- Social engineering, traceroute.



### During this phase, a hacker can collect the following information (only high-level information):
⦁	Domain name
⦁	IP Addresses
⦁	Namespaces
⦁	Employee information
⦁	Phone numbers
⦁	E-mails
⦁	Job Information

### Footprinting Threats

#### Social Engineering:-  
A Malicious link is send by attacker to the email of target , to compromise the system so he can collect the information . This activity easily can be done if the employee or any person cannot have knowledge of hacker intent or we can say Tactics and Techniques

#### System and Network :-  
An attacker can perform several attacks , as if they can collect information of organization like network configuration , os running on the machine . After collecting information , he start find vulnerability as soon as he get vulnerability he will do exploit work. May achieve the full control of network.

#### Information Leakage:- 
If any sensitive information are present in web search engine or any platform that can give a signal to attacker to perform attack . 

#### Privacy Loss:-
As if attacker gain access by the help of footprinting , and he will escalate previllage . so he can still the sensitive file ,  or delete the sensitive file which cause privacy loss. 

#### Corporate Espionage :-
Attacker approach is clear  corporate organization that just achieve the sensitive file , about Ideas , new steps of organization , by which they can demolise the competitor of any organization so competitor loose the market position , share prices. As if he got success to alter the price of product  of any organization this is great achievement of attacker. 

#### Business Loss :- 
Footprinting plays an major effect on organization like E-commerce website and online Business or Banking . If attacker or intruder get success of his goal than any business face the heavy loss.

### Footprinting Methodology 
At above you have seen the consequences of Footprinting , know lets see Methodology how an ethical hacker do Footprinting 

#### Footprinting Through Search Engines
Search engines are the main source of key information about the target Organization. 
Search  engines are like yahoo, google , Bing , Duck duckgo .


#### Google dorking :- 
####	Google search | Google dorks:

              ⦁	filetype: - looks for file types
              ⦁	index of - directory listings
              ⦁	info: - contains Google's information about the page
              ⦁	intitle: - string in title
              ⦁	inurl: - string in url
              ⦁	link: - finds linked pages
              ⦁	related: - finds similar pages
              ⦁	site: - finds pages specific to that site
              ⦁ intitle:password site:craw.in  
            
          
** Site:craw.in inurl:ceh filetype:pdf  **
 
#### Let see another Google Dork:-
inurl:adminpanel site:gov.*  inurl googel dork
 
After searching this we can see only admin page of gov site…
Another use of inurl , we can see live camera with the help of this GD
inurl view index.shtml   this is GD to view live camera 
intitle:"webcamXP" inurl:8080   

http://www.insecam.org/en/view/993071/
http://109.233.191.130:8080/  live camera
http://122.116.41.8:8080/   live camera
https://www.skylinewebcams.com/en/webcam/italia/lazio/roma/piazza-di-spagna.html   live camera

We can extract password if it is not kept safe in browser:
index of:"password" "wp-content"  use to see password directory

Gather information Through Video search Engines
 
 


All type of information about is given by youtube data viewer


#### Shodan 
Shodan Unlike traditional search engines such as Google, use Web crawlers to traverse your entire site, but directly into the channel behind the Internet, various types of port equipment audits, and never stops looking for the Internet and all associated servers, camera, printers, routers, and so on.
Basic search filters you can use:
⦁	city: find devices in a particular city
⦁	country: find devices in a particular country
⦁	geo: you can pass it coordinates
⦁	hostname: find values that match the hostname
⦁	net: search based on an IP or /x CIDR
⦁	os: search based on an operating system
⦁	port: find particular ports that are open
⦁	before/after: find results within a timeframe  Censys
Alternative for Shodan.
 


Perform Footprinting through Web Services
Hacker try to gain information from web services like :- job site, groups , social networks , forums , etc to gain sensitive information.
As an ethical hacker we can find Top level domain like Domain and subdomain 
We can do this with the help of Google Dorking also lets
 see:
site:craw.in -inurl:www
 


#### Another tool is Netcraft
Source :- https://sitereport.netcraft.com/
 
 (Demo of Microsoft) 

##### Another tool is which mostly used in web footprinting  , and it is popular , name is WHOIS
Source :- https://whois.domaintools.com/


We can use whois in CLI also , let see it
 
We can clearly say that we go gmail of owner , so with the help of whois we can do email harvesting , email footprinting .


Determine Target OS through passive footprinting 
This can be easily done by Censys tool as we had seen earlier . 



#### Perform Footprinting through Social Networking sites:
 
 Knowadays almost all people are highly active in social media networks , jobs sites, etc . People unaware they post every moment of his life without knowing that they are leaking himself info in internet.
An attacker all those information from internet like :- social media network,  
We use THE HARVESTER tool
Command :- theHarvester -d craw.in  -l 200 -b linkedin
 
 
#### Perform DNS footprinting 
DNS turn domain name into Ip address for the browser .
DNS or Domain Name System footprinting reveal the DNS zone data like :- DNS server name , DNS records, IP address , domain mail server , etc 
We use nslookup tool for DNS footprinting 
Source :- https://www.nslookup.io/
 
 
#### We can use it in linux terminal also in CLI mode 
Command :- nslookup [ domain ]
 

#### Perform Reverse DNS lookup using Reverse Domain Check and DNS recon
This task is performed to check the shared server of target . Means Target is hosted in whatever server there may be other domains are also hosted. 
If we able to compromise the any domain of that server we got server access and we can target the our victim .
Lets see how Reverse DNS footprinting is done :
Tool name is you get signal 
Source :- https://www.yougetsignal.com/ 

Go to the website and find Reverse IP domain check
 

#### Know lets see DNS recon tool , which is CLI tool
Command :- dnsrecon -d [domain name]


 
Above result we got shared server IP like cloudfare , alt3.aspmx etc .

#### Perform Network Footprinting 
We can perform network footprinting through traceroute tool
>Command :- traceroute [ ip or domain]  for linux  
Command:- tracert  [ip or domain]  for window


 