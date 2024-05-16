## Developed By: Prasannalakshmi G
## Regno: 212222240075

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

## PROGRAM:
### CLIENT SIDE:
```
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### SERVER SIDE:
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUPUT:

### CLIENT SIDE:
![image](https://github.com/Prasannalakshmiganesan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118610231/225c74da-d14d-41b3-b5d2-363e60f55914)



### SERVER SIDE:
![image](https://github.com/Prasannalakshmiganesan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118610231/5132c67f-cb96-4fe7-af40-7f12b1deefbc)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
