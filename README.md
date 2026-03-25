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

client

    import socket
    s=socket.socket()
    s.connect(('localhost',8001))
    while True:
        msg=input("Client > ")
        s.send(msg.encode())
        print("Server > ",s.recv(1024).decode())

server

    import socket
    s=socket.socket()
    s.bind(('localhost',8001))
    s.listen(5)
    c,addr=s.accept()
    while True:
         ClientMessage=c.recv(1024).decode()
         c.send(ClientMessage.encode())
## OUPUT

<img width="1646" height="263" alt="image" src="https://github.com/user-attachments/assets/0bb5eebc-2611-4d8c-b6fe-071e8a13bed4" />

<img width="1615" height="266" alt="image" src="https://github.com/user-attachments/assets/82d4e957-6f2e-45a4-a290-7eef48336c83" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
