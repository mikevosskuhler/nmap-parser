# nmap-parser
Nmap XML output parser written in python

## Installation
Clone the repo
```
cd /tmp
git clone git@github.com:mikevosskuhler/nmap-parser.git
```
Copy the nmap-parser python script to the `/usr/local/bin` directory, you will have to restart the teminal for tab completion to work.
```
cd nmap-parser
sudo cp nmap-parser /usr/local/bin
sudo chmod +x /usr/local/bin/nmap-parser
```
## Usage
```
└─$ nmap-parser -h                                                             2 ⨯
usage: nmap-parser [-h] [--script SCRIPT] [--ips IPS] nmap_file

positional arguments:
  nmap_file        Nmap XML formatted output file

optional arguments:
  -h, --help       show this help message and exit
  --script SCRIPT  Specify which filter script to use
  --ips IPS        filter on ip or cidr block, specify single ip or a cidr range
```
## Example
```
nmap-parser nmap --ips 10.0.0.0/8 --script get_services
```
