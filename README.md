# -MULTITHREADED-CHAT-APPLICATION

*Company*: CODTECH IT SOLUTIONS

*Name*: G Sai Jaswanth

*Intern ID*:CT06DY237

*Domain*: Java Programming

*Duration*:6 weeks

*Mentor*:NEELA SANTOSH

##Description:

*Platform*: Eclipse

Task 3: Client–Server Chat Application using Java Sockets and Multithreading

In this task, the objective was to design and implement a real-time chat application that enables communication between multiple users through a client–server model. The system was developed in Java, using sockets for network communication and multithreading to handle multiple clients simultaneously.

Understanding the Problem

In real-world applications like WhatsApp, Messenger, or Slack, multiple users communicate in real time. To achieve this, messages are not sent directly between clients but are first routed through a server. The server manages all connections and ensures that messages typed by one client are distributed to all other connected clients. This model is reliable, centralized, and scalable.

Task 3 required us to build a simplified version of such a system:

A server program that listens for incoming client connections on a specified port.

A client program that connects to the server and allows users to send and receive chat messages.

Multithreading on the server side, so that many clients can connect and chat simultaneously without blocking one another.

How the System Works

Server Initialization
The server uses a ServerSocket to listen on a fixed port. When a new client connects, the server accepts the connection and creates a new thread (ClientHandler) to handle communication with that specific client. This ensures multiple clients can be served concurrently.

Client Connection
Each client connects to the server using a Socket. After connecting, the client can send messages to the server and receive messages from other clients via the server.

Message Broadcasting
Whenever the server receives a message from a client, it logs the message for monitoring and then broadcasts it to all connected clients. This is achieved by maintaining a collection (Set<PrintWriter>) of client output streams and iterating over them to send the same message.

Multithreading
Every client is handled in its own thread. This prevents one client’s message sending or disconnection from affecting the rest of the system. The use of threads makes the chat system responsive and scalable.

Features

Multiple clients can join the chat room at the same time.

Messages typed by one client are instantly visible to all other connected clients.

The server continuously logs all received messages for monitoring purposes.

The architecture can be extended to support usernames, private chats, or even a graphical user interface (GUI).

Output :
