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
