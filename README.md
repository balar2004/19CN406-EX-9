# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
# AIM:
To write a python program for creating Chat using TCP Sockets Links.
# ALGORITHM:
1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it
will sendNACK signal to client.
6. Stop the program
# PROGRAM:
# CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
# SERVER:
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
# OUTPUT:
# CLIENT SIDE:
![Client-6](https://github.com/balar2004/19CN406-EX-9/assets/118791778/0fd7d3b6-8653-47a7-9fc9-24776c342308)
# SERVER SIDE:
![Server-6](https://github.com/balar2004/19CN406-EX-9/assets/118791778/e6195276-792c-4b0e-8acc-13e306812c12)
# RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
