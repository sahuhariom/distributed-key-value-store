# Distributed Key-Value Store

## Project Overview
This project implements a **Distributed Key-Value Store** in C using **TCP and UDP sockets**. It demonstrates a basic distributed system where nodes communicate to process `PUT` and `GET` requests for key-value pairs. The system handles node-to-node communication, request forwarding, and hash table storage with collision handling.

## Features
- **PUT(key, value)**: Store a key-value pair in the appropriate node.
- **GET(key)**: Retrieve the value of a given key from the distributed system.
- **UDP Forwarding**: Requests are forwarded between nodes to reach the correct node.
- **TCP Response**: Nodes respond to the original requester with the value or confirmation.
- **Hash Table Implementation**: Handles collisions using linked lists.
- **Interactive Console**: Accepts commands and displays hash table contents.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/sahuhariom/distributed-key-value-store.git
2. Navigate to the project directory:
  cd distributed-key-value-store/src

3. Compile the C program:
   gcc node.c -o node

## Usage
1.Run a node:
  ./node

2.Follow the instructions:
PUT(<key>,<value>) to insert a value

GET(<key>) to retrieve a value

r to display the current node's hash table

##Project Structure
distributed-key-value-store/
├── README.md
└── src/
    └── node.c
## Sample Commands
PUT(10,200)
GET(10)
r

##Author
Hariom Sahu 

##Notes

This project demonstrates basic distributed systems concepts including request forwarding, node communication, and hash table storage.

For simplicity, all nodes are run locally (127.0.0.1) and use consecutive ports.

The program uses gets() for input, which is unsafe for production. For production-grade systems, use fgets() instead.
