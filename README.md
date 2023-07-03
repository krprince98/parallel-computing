# Parallel Computing
Parallel computing refers to the concept of performing multiple computational tasks simultaneously by dividing them into smaller subtasks that can be executed concurrently. It involves utilizing multiple computing resources, such as multiple CPU cores or computers, to solve a problem more quickly or efficiently. The goal is to divide the workload among these resources and coordinate their execution to achieve faster execution times or handle larger and more complex computations.
We will discuss this topic with a focus on CPU.

## Find CPU specifications on a Linux machine
Run `lscpu` in a terminal window. It would produce a result like this:

![image](https://github.com/krprince98/parallel-computing/assets/96859685/916474cc-69de-4141-9686-87da74a29e00)

Here the number of processors or CPUs is 8.

`CPU(s):                  8`

This can be calculated from:
```
Thread(s) per core:  2
Core(s) per socket:  4
Socket(s):           1
```
CPU(s) = Thread(s) per core x Core(s) per socket x Socket(s) = 2 x 4 x 1 = 8

## Threads, Cores & Sockets
**Sockets**- A CPU socket is a physical connector on a motherboard that allows the installation of a central processing unit (CPU), providing the necessary electrical connections and mechanical support for the CPU. Most personal devices will have only one.

**Cores**- Cores in a CPU (Central Processing Unit) are individual processing units within the same physical chip. Each core is capable of independently executing instructions, performing calculations, managing tasks, and handling I/O (Input/Output) operations. Multiple cores in a CPU enable parallel processing, allowing for simultaneous execution of multiple tasks, including both computational and I/O-related operations. These are physical constructs within the CPU chip.  
&emsp;It is notable that they share certain resources like Cache Memory, Memory Bus, Power Management etc.
  
**Threads**- Theads are essentially a software concept. Threads are independent sequences of instructions within a program that can execute concurrently and share the same resources. The question arises here is what would it mean by *threads per core*? Here is the answer:  
&emsp;In modern CPUs, the term "threads per core" refers to a hardware feature called simultaneous multithreading (SMT) or hyper-threading. It allows each physical CPU core to handle multiple software threads simultaneously, improving resource utilization and potentially enhancing performance.
