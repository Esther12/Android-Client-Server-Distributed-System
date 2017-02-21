# Android-Client-Server-Process-Management
https://docs.google.com/document/d/1Dqhsl8mBaC_kw02APLBqE5KbM7Pbk60SYF3gviZf9yM/edit


implement a distributed application with a server process accepting multiple client processes to perform a certain task.


The server side must be written in C and implement a remote connection providing an service to the client process.



The client process, running on a different machine from the server, 


must be implemented using a C program running from a shell as a command line utility, 


and another version running from an Android device using a graphical interface. 


The communication between the two processes (Server-Client) must be achieved using Sockets.



The server task can be summarized as follows:


 The server must start running before any client and waits for connections.


 When the server gets a client, forks and, 


let the child process take care of the client while the parent process goes back to wait for the next client.


 The server’s child process gets in an infinite loop then reads commands from the client’s socket, 



executes them, by the fork/exec mechanism, and sends all their outputs to the client side.


When the client sends CTR-D, then the server’s child quits.

Server: wait for Child processes and perform a service (based on your business plan/vision)

Client A: shell utility version that is text based and interactive.

Client B: Android based version, graphical interface and interactive.
