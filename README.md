
# CLI Chat Room Application

This is a basic client-server chat room project built using Java. The project allows multiple clients to connect to a server, exchange messages in real-time, and see notifications when someone enters or leaves the chat room. It demonstrates fundamental concepts such as Sockets and Threads.


## Features

- Clients can connect to the server using a socket and enter their username.
- The server broadcasts messages from one client to all other connected clients.
- When a client joins or leaves, the server sends a message to notify all other clients.



## Concepts Used

### Sockets
A socket is the mechanism that allows communication between the client and server over the network. The server opens a socket and waits for clients to connect. Once connected, the socket allows the exchange of messages.

### Threads
A thread allows multiple tasks to run concurrently. In this project:

- The server creates a separate thread for each client connection using the ClientHandler.java class. This way, multiple clients can be connected and handled simultaneously without blocking each other.
- Each client uses two threads: one for sending messages and another for listening to messages.

If the server is running and three clients are connected, the total number of threads in the system is 10:

4 threads on the server (1 main thread + 3 client-handling threads).
6 threads on the clients (2 threads per client for sending and receiving messages).
## Installation


```bash
  npm install my-project
  cd my-project
```
Clone the repository or download the project files.

Make sure Java is installed on your system.

Open a terminal window and navigate to the project folder.

Compile the server code:

```bash
  javac Server.java
```

Run the server:

```bash
  java Server.java
```

The server will start and begin listening for client connections on a specific port (e.g., localhost:8010).

Open another terminal window to run the client code.

Compile and run the client code:

```bash
  javac Client.java
```
```bash
  java Client.java
```

The client will connect to the server, ask for a username, and start sending/receiving messages.

Repeat the above step for each additional client in separate terminal windows to allow multiple clients to connect and communicate.

## Project Flow

- Server starts: The server begins listening for clients on localhost:8010.
- Client connects: When a client connects, they are asked for a username, and a message is broadcast to all clients.
- Messaging: Clients can send and receive messages in real-time.
- Client disconnects: When a client leaves, the server broadcasts a message to the remaining clients.
## Requirements

Java (JDK) installed on your system.
## License

This project is for educational purposes and open to use.
## Future Scope

This project was build on a previous project I uploaded on github called WebServer where I build Single Threaded, Multithreaded and ThreadPool.

This project is a work in progress and I intend to make this a full fledged social media app. 

My long term goal in doing this is to get a grasp on Java fundamentals and DSA.