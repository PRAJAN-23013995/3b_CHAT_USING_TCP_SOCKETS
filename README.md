# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
Server:
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
```
## OUPUT
client:

![323091977-1c0d469d-5779-465a-904c-24a6e04c9963](https://github.com/user-attachments/assets/987fed09-4739-42b5-bc1e-b520cc80ffe6)

server:

![323091994-39b048b9-d353-4a6e-b84c-5322edc700af](https://github.com/user-attachments/assets/8580a776-9cf2-477b-a558-561e578c4546)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
