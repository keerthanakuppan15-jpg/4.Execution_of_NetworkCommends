# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
All commands related to Network configuration which includes how to switch to privilege mod
and normal mode and how to configure router interface and how to save this configuration to
flash memory or permanent memory.
This commands includes
• Configuring the Router commands

• General Commands to configure network

• Privileged Mode commands of a router 

• Router Processes & Statistics

• IP Commands

• Other IP Commands e.g. show ip route etc.

## PROGRAM:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
hostname=c.recv(1024).decode() 
try: 
c.send(str(ping(hostname, verbose=False)).encode()) 
except KeyError: 
c.send("Not Found".encode())
SERVER 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
ip=input("Enter the website you want to ping ") 
s.send(ip.encode()) 
print(s.recv(1024).decode())

TRACEROUTE COMMAND:
 from scapy.all import*     
target = ["www.google.com"]     
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## Output
<img width="1475" height="797" alt="Screenshot 2026-05-26 120103" src="https://github.com/user-attachments/assets/1ec66c09-928b-4d3e-909a-61f2574982b2" />
<img width="1491" height="804" alt="Screenshot 2026-05-26 120152" src="https://github.com/user-attachments/assets/4e244a4c-3b6b-4955-988f-a9bb714611b2" />

## Result
Thus Execution of Network commands Performed 
