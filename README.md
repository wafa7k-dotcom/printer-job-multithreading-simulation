````markdown
# Printer Job Multithreading Simulation

## Project Overview

This project simulates a printer system using Java Multithreading concepts. The system models print jobs being submitted and processed through a shared buffer using the Producer-Consumer pattern.

Multiple writer threads generate print jobs and place them into the buffer, while multiple reader threads retrieve and process the jobs one at a time. Synchronization mechanisms ensure safe access to shared resources and prevent concurrency issues.

---

## Objectives

- Simulate printer job scheduling using multithreading.
- Implement a shared buffer with a maximum capacity of 20 jobs.
- Allow multiple writer threads to add print jobs.
- Allow multiple reader threads to process print jobs.
- Prevent reading from an empty buffer.
- Prevent writing to a full buffer.
- Handle race conditions.
- Avoid deadlocks.
- Ensure the buffer is empty before program termination.

---

## Features

- Shared Buffer implementation
- Producer-Consumer Model
- Multiple Writer Threads
- Multiple Reader Threads
- Synchronization using `synchronized`
- Thread communication using `wait()` and `notifyAll()`
- Deadlock prevention
- Race condition handling

---

## System Components

### Buffer
A shared object that stores print jobs.

- Maximum capacity: 20 jobs
- Supports safe read and write operations
- Blocks writers when full
- Blocks readers when empty

### Writer Threads
Producer threads that:

- Generate print jobs
- Add jobs to the buffer
- Wait 0.5 seconds between jobs

### Reader Threads
Consumer threads that:

- Read print jobs from the buffer
- Simulate printing
- Wait 1 second between jobs

---

## Technologies Used

- Java
- Multithreading
- Synchronization
- Producer-Consumer Pattern
- Object-Oriented Programming

---

## Concurrency Techniques

### Race Condition Prevention

The shared buffer is protected using synchronized methods to ensure only one thread accesses critical sections at a time.

### Deadlock Avoidance

The program uses:

- `wait()`
- `notifyAll()`

to coordinate thread execution and prevent deadlocks.

---

## Project Structure

```text
PrinterSimulation.java
│
├── Buffer
├── Writer
├── Reader
└── Main Program
````

---

## Expected Output

Example:

```text
Written: Writer 1 - Job 1
Written: Writer 2 - Job 1
Printed: Writer 1 - Job 1
Printed: Writer 2 - Job 1
...
Program finished. Buffer is empty.
```

---

## Learning Outcomes

Through this project, students learn:

* Thread creation and management
* Synchronization techniques
* Shared resource protection
* Producer-Consumer implementation
* Deadlock prevention strategies
* Concurrent programming concepts

---

## Author

Wafaa Aluhaidan
and other student 

Information Technology Department

Qassim University

```
```
