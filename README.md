# DATE:
# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME:HARSSHITHA LAKSHMANAN
## RENO: 212223230075
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
SERVER:
```
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
```
## OUTPUT
CLIENT:

![WhatsApp Image 2024-09-19 at 10 52 46_6ae7e25b](https://github.com/user-attachments/assets/bb93fddf-83f1-4709-a879-4f2838799751)

SERVER:

![WhatsApp Image 2024-09-19 at 10 53 09_96433ed5](https://github.com/user-attachments/assets/2b1af081-481e-4113-bf94-e85fe63811a2)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
