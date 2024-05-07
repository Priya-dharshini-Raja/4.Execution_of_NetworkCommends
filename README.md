# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PROGRAM:
DEVELOPED BY:PRIYADHARSHINI RAJA
REGISTER NUMBER: 212223230160

## PING COMMAND

## CLIENT:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```

## SERVER:

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
## TRACEROUTE COMMAND:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```


## Output:
## PING COMMAND:

 ## Client:
 ![image](https://github.com/Priya-dharshini-Raja/4.Execution_of_NetworkCommends/assets/148514803/8fd951ec-767e-4b60-ab6c-adebd77fa6a6)

 ## Server:
 ![image](https://github.com/Priya-dharshini-Raja/4.Execution_of_NetworkCommends/assets/148514803/2d300766-bb3d-41e1-a63d-e5b9ba9dcce6)


 ## TRACEROUTE COMMAND:

 ![image](https://github.com/Priya-dharshini-Raja/4.Execution_of_NetworkCommends/assets/148514803/4e07ff7d-9693-43d5-8234-2f45d909aeaf)




## Result
Thus Execution of Network commands Performed 
