# Practice 1 - Circular Queue with Array

**Course:** Concurrent and Distributed Programming (Programación Concurrente y Distribuida)\
**Practice:** Practice 1 - Introduction to Java\
**University:** Universidad de Huelva\
**Year:** 2026-2027

## 📄 Description

Implementation of a **circular queue** backed by a fixed-size array, as a first contact
with Java and NetBeans. When the tail reaches the end of the array, new elements are
stored again at the beginning, reusing the slots freed by previously removed elements.

This queue is the base structure for later practices, where it will be extended for
concurrent access.

## 🎯 Learning Objectives

- Getting started with Java and the NetBeans environment
- Defining a contract with an **interface** and implementing it in a class
- Implementing a circular buffer with modular arithmetic
- Handling error cases (full / empty queue) with exceptions

## 🧩 Classes Implemented

- **ICola**: Interface with the queue operations: `acola`, `desacola`, `primero`, `getNum`
- **Cola**: Circular queue implementation. `head` points to the first element and `tail` to the next free slot; both advance with `(pos + 1) % capacidad`. An element counter distinguishes the full and empty states (in both cases `head == tail`)
- **UsaCola**: Test program: a queue of capacity 4 and a 10-iteration loop that randomly inserts the iteration number (1) or removes the first element (0)

## 💻 Technologies Used

- **Language:** Java
- **IDE:** NetBeans
- **Package:** practica1

## 🚀 How to Run

1. Clone the repository
2. Open the folder in NetBeans (*File → Open Project*)
3. Run `UsaCola.java`

Example of using the queue through its interface:

```java
ICola cola = new Cola(4);
cola.acola(5);                  // insert
Object first = cola.primero();  // peek without removing
Object out = cola.desacola();   // remove the first element
```

## 🔜 Used In

- Upcoming PCD practices: this queue will be reused and extended with concurrency support
