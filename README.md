# 3b.CREATION FOR CHAT USING TCP SOCKETS
### Name: Rohith Prem S
### Register Number: 212223040172
## AIM
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM:
### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### Server:
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
## OUPUT:
### Client:
![Screenshot 2024-10-29 133116](https://github.com/user-attachments/assets/684ddd9a-687a-4de1-a334-90b60243f54f)

### Server:
![Screenshot 2024-10-29 133123](https://github.com/user-attachments/assets/1f4ba714-964d-4453-b964-f93c39a526a0)

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
