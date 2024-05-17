# 3b.CREATION FOR CHAT USING TCP SOCKETS

### Name : Surendhar A
### Reg. No. : 212222110049

## AIM
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
   
## PROGRAM
### Client 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### Server 
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
### Client 
![image](https://github.com/Surendhar6/3b_CHAT_USING_TCP_SOCKETS/assets/118352907/868b35cb-63e3-4fcd-96a4-b966c1c8136c)

### Server
![image](https://github.com/Surendhar6/3b_CHAT_USING_TCP_SOCKETS/assets/118352907/687918fe-597b-4e1e-88b8-1f70df7bc28b)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
