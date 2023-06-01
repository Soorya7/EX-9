# APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
# EXP: 9
# DATE:04-05-2023
# AIM:
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1.Import the necessary modules in python <br>
2.Create a socket connection to using the socket module. <br>
3.Send message to the client and receive the message from the client using the Socket module in server <br>
4.Send and receive the message using the send function in socket. <br>
## PROGRAM:
## CLIENT:
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
## SERVER:
```py
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
## OUTPUT :
## Client:
![image](https://github.com/Bhargava-123/EX-9/assets/85554376/c7aadacd-2bbe-4dbb-89d4-47adde25f125)


## Server:
![image](https://github.com/Bhargava-123/EX-9/assets/85554376/3581a70e-ded6-4b63-b648-6769ed32de6d)


## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
