# Answers

## 1. Thread vs Process

A process is an independent program that has its own memory space, while a thread is a smaller unit of execution inside a process that shares memory with other threads. Threads are more lightweight and faster to create compared to processes. Communication between threads is easier because they share the same memory, while processes require inter-process communication mechanisms.

In this assignment, threads were used instead of processes because the simulation requires fast switching between tasks and shared data structures like the ready queue. For example, in SchedulerSimulation.java, each process is executed using a Thread object, which allows efficient scheduling and context switching.

---

## 2. Ready Queue Behavior

In Round-Robin scheduling, if a process does not finish within its time quantum, it is placed back into the ready queue. This behavior is clearly implemented in the code where the process is re-added using addProcessToQueue().

Example from the program output:
P1 (Priority: 3) added to ready queue
▶ P1 executing quantum [2000ms]
⏸ P1 completed quantum 2000ms │ Remaining time: 1500ms
↻ P1 yields CPU for context switch

Since P1 still has remaining time, it is re-enqueued into the ready queue. This ensures fairness because all processes get equal CPU time and no process can monopolize the CPU.

---

## 3. Thread Lifecycle

A thread goes through several states during execution. First, it is in the New state when the Thread object is created. When Thread.start() is called, it moves to the Runnable state. Then it enters the Running state when the CPU executes the run() method.

In the code, Thread.sleep() is used to simulate execution time, which puts the thread into a Waiting state temporarily. After completing execution, the thread moves to the Terminated state.

For example, process P1 is created, started using start(), executes run(), waits during sleep(), and finally terminates when remainingTime becomes zero.

---

## 4. Real-World Applications

One real-world application is a web server, where multiple user requests are handled using threads. Round-Robin scheduling ensures fairness so all users are served without delay.

Another example is a media player, where different threads handle video playback, buffering, and user interaction. The scheduling ensures smooth performance and responsiveness.

In this assignment, similar concepts are applied where each process is treated as a thread, and the scheduler distributes CPU time fairly among them.
