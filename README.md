# *Tugas 2 Cisco Packet Tracer*

# Diagram 1 & 2
## Router0
```bash
enable
configure terminal
interface FastEthernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
interface FastEthernet0/1
ip address 192.168.2.1 255.255.255.0
no shutdown
exit
```

# Diagram 3 & 4
## Router0 Command
```bash
enable
configure terminal

interface fastethernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

interface fastethernet0/1
ip address 10.10.10.1 255.255.255.252
no shutdown
exit

ip route 192.168.2.0 255.255.255.0 10.10.10.2
exit
```

## Router1 Command
```bash
enable
configure terminal

interface fastethernet0/0
ip address 192.168.2.1 255.255.255.0
no shutdown
exit

interface fastethernet0/1
ip address 10.10.10.2 255.255.255.252
no shutdown
exit

ip route 192.168.1.0 255.255.255.0 10.10.10.1
exit
```

# Diagram 5
## Router0
```bash
enable
configure terminal

interface f0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

interface f0/1
ip address 10.10.10.1 255.255.255.252
no shutdown
exit

ip route 10.10.20.0 255.255.255.252 10.10.10.2
ip route 192.168.2.0 255.255.255.0 10.10.10.2
```
## Router1
```bash
enable
configure terminal

interface f0/0
ip address 10.10.10.2 255.255.255.252
no shutdown
exit

interface f0/1
ip address 10.10.20.1 255.255.255.252
no shutdown
exit

ip route 192.168.1.0 255.255.255.0 10.10.10.1
ip route 192.168.2.0 255.255.255.0 10.10.20.2
```
## Router2
```bash
enable
configure terminal

interface f0/0
ip address 192.168.2.1 255.255.255.0
no shutdown
exit

interface f0/1
ip address 10.10.20.2 255.255.255.252
no shutdown
exit

ip route 192.168.1.0 255.255.255.0 10.10.20.1
ip route 10.10.10.0 255.255.255.252 10.10.20.1
```

# Test Router
```bash
show ip interface brief
```
