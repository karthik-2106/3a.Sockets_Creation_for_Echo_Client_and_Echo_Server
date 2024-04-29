# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
### server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT
### client
![Screenshot 2024-04-29 131903](https://github.com/karthik-2106/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150319557/0ac9b430-739f-44ff-b39f-53776119bba5)
### server
![Screenshot 2024-04-29 131903](https://github.com/karthik-2106/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150319557/87934f22-e3c5-4df2-b0a4-503287e10726)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
