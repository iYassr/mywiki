
# nmap 
- host discovery
	  to ack discovery to make know if it's a statful or stateless firewall
	- even closed ports can be used on host discovery 
	- UDP closed ports are more likely to respond that open ports
	- DNS is a good option for udp discovery scan
	- closed? reset, open? syn-ack mostly 
	- 

$ source https://www.youtube.com/watch?v=Hk-21p2m8YY
$ nmap -sP -PE -PS21,22,23,25,80,113,31339 -PA80,113,44,10042 --source-\port 53 -T4 -iL ips.txt

| option         | use                                                             |
|----------------|-----------------------------------------------------------------|
| sP             | ping scan                                                       |
| n              | no reverse dns lookup                                           |
| PE/PP/PM       | ICMP echo, timestamp, and netmask request discovery probes      |
| PS             | Syn Packet Discovery  [ Stateful Firewalls ]                    |
| PA             | Ack Packet Discovery   [ Stateful Firewalls ]                   |
| top-ports 3674 | TCP scan the most common 3674 ports                             |
| top ports 1017 | UDP scan the most common  1017 ports                            |
| S              | spoof source address, works with TCP?                           |
| d              | debugging mode, every info you need                             |
| reason         | filtered, why?                                                  |
| packet-trace   | which host responded? is it the same or the firewall, remember? |
| source-port    | use DNS for Ex to bypass firewall                               |
| ndiff          | aweesome tool to compare scan results!                          |






