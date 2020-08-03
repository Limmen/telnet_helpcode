# Telnet Server/Client Lab Help code

## Description

Some help code to get started with socket programming in C, useful for the Telnet lab.

## How To Run

### Build
Build all:
```
make all
```
Build client:
```
make client
```
Build server:
```
make server
```

### Run

Run server:
```bash
./server
```

Run client:
```bash
./client
```

### Cleanup
```bash
make clean
```

### Example Output
Server:
```bash
kim@kim-vox:/home/kim/telnet_helpcode$ make clean
rm -rf server client
kim@kim-vox:/home/kim/telnet_helpcode$ make all
gcc -o server server.c
gcc -o client client.c
kim@kim-vox:/home/kim/telnet_helpcode$ ./server
Telnet Server Starting
[Server] Listening to port 9999
[Server] Waiting for incoming connections..
[Server] Accepted client connection
[Server] Reading from socket..
[Server] Read 27 bytes successfully
[Server] Read the message: Hello from Enköping/Client
[Server] Sending msg: Hello from Stockholm/Server , of length: 27
[Server] Message sent successfully
[Server] Closing the client connection and waiting for the next connection
[Server] Waiting for incoming connections..
```

Client:
```bash
kim@kim-vox:/home/kim/telnet_helpcode$ ./client
Telnet Client Starting
[Client] Configuring server to connect to, address: 127.0.0.1, port: 9999
[Client] Connecting to server
[Client] Connected successfully with server
[Client] Sending msg: Hello from Enköping/Client , of length: 27
[Client] Message sent successfully
[Client] Reading from socket..
[Client] Read 27 bytes successfully
[Client] Read the message: Hello from Stockholm/Server
[Client] Closing the socket and exiting
```
