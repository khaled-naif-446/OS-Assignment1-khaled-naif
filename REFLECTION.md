# Reflection

## 1. What did you learn about multithreading from this assignment?

In this assignment, I learned how to implement multithreading in Java using the Runnable interface. I understood how multiple threads can run concurrently and simulate CPU scheduling. I also learned how to control thread execution using Thread.start(), Thread.join(), and Thread.sleep(). The assignment helped me understand how threads share resources and how scheduling works in practice. Additionally, I learned how Round-Robin scheduling ensures fairness between processes. Overall, this assignment gave me practical experience with thread management.

---

## 2. What was the most challenging part of this assignment and why?

The most challenging part was implementing the waiting time calculation. It was difficult because I had to track time accurately while processes were moving in and out of the ready queue. Another challenge was updating the waiting time at the correct moment before execution. Also, understanding how context switching affects waiting time was not easy. The timing logic required careful attention to detail. Debugging this feature took extra effort.

---

## 3. How did you overcome the challenges you faced?

I overcame these challenges by carefully analyzing the flow of the program. I used System.currentTimeMillis() to track when a process enters and leaves the queue. I also created helper methods like updateWaitingTime() and setLastReadyTime() to organize the logic. Testing each feature separately helped me ensure correctness. I also reviewed the code multiple times to fix mistakes. This step-by-step approach helped me solve the problem.

---

## 4. How can multithreading concepts be applied in real-world applications?

Multithreading is widely used in real-world systems such as web servers and operating systems. For example, a web server can handle multiple client requests simultaneously using threads. It is also used in applications like games and video streaming, where different tasks run at the same time. In this assignment, the scheduler distributes CPU time among processes, similar to real operating systems. This improves performance and responsiveness. These concepts are essential in modern software development.
