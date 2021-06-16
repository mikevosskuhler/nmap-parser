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
└─$ nmap-parser -h
usage: nmap-parser [-h] [--script {get_ports,get_hosts,get_services,get_http_urls}] [--ips IPS] nmap_file

positional arguments:
  nmap_file             Nmap XML formatted output file.

optional arguments:
  -h, --help            show this help message and exit
  --script {get_ports,get_hosts,get_services,get_http_urls}, -s {get_ports,get_hosts,get_services,get_http_urls}
                        Specify which filter script to use. Default is get_ports.
  --ips IPS, -i IPS     Filter on IP or CIDR block, specify single IP or a CIDR range.
```
## Example
```
nmap-parser nmap --ips 10.0.0.0/8 --script get_services
```
