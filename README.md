# Distributed Key-Value Store

## Project Overview
This project implements a Distributed Key-Value Store in C using TCP and UDP sockets. It demonstrates a basic distributed system where nodes communicate to process PUT and GET requests for key-value pairs. The system handles node-to-node communication, request forwarding, and hash table storage with collision handling.

## Features
- **PUT(key, value):** Store a key-value pair in the appropriate node.  
- **GET(key):** Retrieve the value of a given key from the distributed system.  
- **UDP Forwarding:** Requests are forwarded between nodes to reach the correct node.  
- **TCP Response:** Nodes respond to the original requester with the value or confirmation.  
- **Hash Table Implementation:** Handles collisions using linked lists.  
- **Interactive Console:** Accepts commands and displays hash table contents.  

## Installation
```bash
# Clone the repository
git clone https://github.com/sahuhariom/distributed-key-value-store.git

# Navigate to the src directory
cd distributed-key-value-store/src

# Compile the C program
gcc node.c -o node



# Run a node
./node

# Follow the instructions in the console:
# PUT(10,200)  --> To insert a key-value pair
# GET(10)      --> To retrieve a value
# r            --> To display the current node's hash table



distributed-key-value-store/
├── README.md
└── src/
    └── node.c



PUT(10,200)
GET(10)
r


Notes

This project demonstrates basic distributed systems concepts including request forwarding, node communication, and hash table storage.

For simplicity, all nodes are run locally (127.0.0.1) and use consecutive ports.

The program uses gets() for input, which is unsafe for production. For production-grade systems, use fgets() instead.
