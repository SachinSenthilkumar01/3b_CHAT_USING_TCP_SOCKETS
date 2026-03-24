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
### Server
```python
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
### Client 
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
### Server
<img width="1920" height="1080" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/494e4f02-7354-4de6-874e-88e2e8f37083" />


### Client 
<img width="1920" height="1080" alt="Screenshot (69)" src="https://github.com/user-attachments/assets/e565aae2-b63f-47a1-805b-390c958b4385" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
