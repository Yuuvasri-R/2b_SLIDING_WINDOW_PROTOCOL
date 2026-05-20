# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL
## AIM
To implement a program to illustrate the mechanism of sliding window protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM

Developed by : **Yuuvasri R**

Reg no : **212225230313**

### Client
```python
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
size=int(input("Enter number of frames to send : ")) 
l=list(range(size)) 
s=int(input("Enter Window Size : ")) 
st=0 
i=0 
while True: 
    while(i<len(l)): 
        st+=s 
        c.send(str(l[i:st]).encode()) 
        ack=c.recv(1024).decode() 
        if ack: 
            print(ack) 
            i+=s
```

### Server
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000))  
while True: 
    print(s.recv(1024).decode()) 
    s.send("acknowledgement recived from the server".encode())
```
## OUPUT
<img width="930" height="949" alt="Screenshot 2026-05-19 151319" src="https://github.com/user-attachments/assets/26fe4207-5c58-4893-9d08-44cedb6774ed" />
<img width="938" height="948" alt="Screenshot 2026-05-19 151330" src="https://github.com/user-attachments/assets/6fe5cdce-4e9e-4931-97af-1e0a3d9f82ef" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed



























































.


































































.



























































































































.





























































.













.
































.
.
