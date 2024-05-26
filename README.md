# Concurrent Event-Driven Microservices
his project was developed as part of a university course on System Programming Language (SPL).
This project consists of two main sections:

## Section 1: Framework Development

In the first part, I developed a framework of microservices implemented using threads. Each thread performs actions according to its definition and communicates with other threads via various types of messages. Threads register for specific message types and receive tasks while maintaining a round-robin order. Each thread is runnable, meaning it can operate as a thread and includes a `run` function as its execution loop.

Communication is managed by a common object—a singleton class—ensuring a single instance is used throughout the system. We utilized three concurrent hashmaps to store all necessary information, ensuring thread safety in the data structure. This entire section is designed to be non-blocking. For each message type, a corresponding callback is saved to determine the appropriate action when such a message is received.

## Section 2: System Implementation

In the second part, I implemented a system on top of the developed framework. This system handles the execution of attacks, manages the resources needed to respond to these attacks, and maintains a communication log, also designed as a singleton.

## Project Goals

The goal of this project was to practice concurrent programming within the Java 8 environment. This assignment required a strong understanding of Java Threads, Java Synchronization, Lambdas, and Callbacks.
