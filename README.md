# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM

### CLIENT
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUTPUT

### CLIENT
![1](https://github.com/saieswar1607/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/93427011/a107bc7c-ca6c-417a-b0c3-e5d86077a212)

### SERVER
![2](https://github.com/saieswar1607/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/93427011/74d53c79-5c6c-417b-b571-b91146dd1ba1)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
