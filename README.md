# Distributed Key-Value Store

## Project Overview
This project implements a **Distributed Key-Value Store** in C using **TCP and UDP sockets**.  
It allows multiple nodes to communicate, store, and retrieve key-value pairs in a distributed environment.  
The project demonstrates concepts of **distributed systems**, **hash tables**, **collision handling**, and **network programming**.

## Features
- Handles multiple nodes with **UDP forwarding** and **TCP connections**.
- Implements a **hash table** with chaining to resolve collisions.
- Supports `PUT(key, value)` and `GET(key)` operations.
- Each node can forward requests to the correct node based on the key.
- Real-time interaction via console with instructions for usage.

## Folder Structure
distributed-key-value-store/
├── README.md # Project description
└── src/
└── node.c # Main C source file implementing the project


## How to Compile and Run
1. Navigate to the `src` directory:
```bash
