# NAME: S.KAVIYA
# RESIGTER NO: 212223040090
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

CLIENT:

    import socket
    
    s=socket.socket()
    
    s.connect(('localhost',800))
    
    while True:
    
       msg=input("Client > ")
       
       s.send(msg.encode())
       
       print("Server > ",s.recv(1024).decode())


SERVER:

     import socket
     
     s=socket.socket()
     
     s.bind(('localhost',800))
     
     s.listen(5)
     
     c,addr=s.accept()
     
     while True:
     
         ClientMessage=c.recv(1024).decode()
         
         print("Client > ",ClientMessage)
         
         msg=input("Server > ")
         
         c.send(msg.encode()) 
         


## OUPUT:

CLIENT

![Screenshot 2024-04-29 141707](https://github.com/KAVIYASHANMUGAM19/3b_CHAT_USING_TCP_SOCKETS/assets/155141139/7e6de406-3f57-4a06-89d4-e2f2925d143e)


SERVER

![Screenshot 2024-04-29 141711](https://github.com/KAVIYASHANMUGAM19/3b_CHAT_USING_TCP_SOCKETS/assets/155141139/54b8dad1-9bd3-49ca-b6b5-1f3cc1192f07)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
