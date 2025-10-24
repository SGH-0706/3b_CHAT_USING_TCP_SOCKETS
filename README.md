# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
client
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',8081)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
server
```
import socket 
s=socket.socket() 
s.bind(('localhost',8081)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
<img width="1850" height="1072" alt="3b cn" src="https://github.com/user-attachments/assets/be8af7e4-4a30-49d0-8b41-8f0960005270" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
