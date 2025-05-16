# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME : STEFFI J
## REGISTER NUMBER : 212224220107
## DATE : 16/05/2025

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
~~~
client.py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
~~~
~~~
server.py
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
~~~
## OUPUT
![WhatsApp Image 2025-05-15 at 11 14 45_6e2a469a](https://github.com/user-attachments/assets/fc05f37e-15a3-4faa-8539-8f65ab219123)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
