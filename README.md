# CatSec-PortScan-Blocker
 tool to detect port scans on a host machine and block IPs

### Python Dependencies
`pip3 install scapy`
`pip3 install python_iptables`

### Linux Dependencies
`sudo apt-get install iptables`
   
### Usage
`sudo python3 catsec_portscan_blocker.py`

#### Usage Options
```-h, --help            show this help message and exit
  -H HOSTIP, --hostIP HOSTIP
                        Specify your host inet address. Will default to the
                        inet address of default interface.
  -i INTERFACE, --interface INTERFACE
                        Specify an interface to sniff for port scans on. Will
                        default to system default.
  -c, --clear           Use this flag to clear all blocked IPs before running. 
```
 `sudo python3 catsec_portscan_blocker.py -i ens4 -H 10.138.0.27` 
 
 #### Clear out iptable rule chain 
 `sudo python3 catsec_portscan_blocker.py -c`  
 or  
 ``` 
 sudo iptables -F
 sudo iptables -X 
 ```  
 #### View Blocked IP Addresses
 `Ctrl + C` while running  
 or  
 `sudo iptables -n -L` 
 
