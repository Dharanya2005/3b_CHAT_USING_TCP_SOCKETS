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
# client:
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
# server:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUTPUT:
# client:
![Screenshot 2024-04-10 123725](https://github.com/Dharanya2005/3b_CHAT_USING_TCP_SOCKETS/assets/145742468/145a7164-af4c-476b-98b3-f4b4aeeb6033)
# server:
![image](https://github.com/Dharanya2005/3b_CHAT_USING_TCP_SOCKETS/assets/145742468/8b25bb69-bc20-4afd-9222-c54428b2d20c)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
