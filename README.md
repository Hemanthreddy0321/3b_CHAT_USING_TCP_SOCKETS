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

CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
SERVER
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

## OUPUT
CLIENT

![image](https://github.com/Hemanthreddy0321/3b_CHAT_USING_TCP_SOCKETS/assets/150005937/3c313344-da19-4a4a-af73-16ce14d8cf6d)

SERVER 

![image](https://github.com/Hemanthreddy0321/3b_CHAT_USING_TCP_SOCKETS/assets/150005937/f7411fc1-f873-4a35-b034-7278ff8a4805)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
