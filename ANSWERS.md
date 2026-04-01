# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer: A process is a stand-alone program that runs independently and has its own resources, memory, and system state, A thread, on the other hand, is a smaller execution unit that operates inside a process and shares resources and memory with other threads, Because they don't need separate memory allocation, threads are typically lighter and quicker to create than processes.
Since the CPU scheduler simulation needs several tasks to run and switch quickly, we used threads rather than processes in this assignment, Because of the expenses associated with memory segregation and context switching, creating several processes would result in significant overhead, In line with the ideas, threads enable the simulation to effectively depict CPU scheduling behavior while sharing the same application resources.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, the CPU stops running a process and puts it back at the end of the ready queue if it doesn't finish within the allotted time period This ensures that all processes are treated fairly by allowing other processes in the queue to obtain CPU time, Until every process has completed its execution, the scheduler keeps going through the queue.

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output: ▶ P1 executing quantum [3000ms] 
⚡ Quantum progress: [███████████████] 100%
⏸ P1 completed quantum 3000ms │ Overall progress: [██████████░░░░░░░░░░] 51%
Remaining time: 2806ms
↻ P1 yields CPU for context switch

➕ P1 added to ready queue │ Priority: 4 │ Burst time: 5806ms
┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P1]
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example: Process P1 in this instance was given the CPU and ran for the entire 3000 ms time quantum Nevertheless, there were still 2806 milliseconds left, indicating that the process was not complete, In order to give other processes a chance to run before P1 gets another turn, the scheduler took P1 off of the CPU and put it at the end of the ready queue, This illustrates the fundamental idea of Round-Robin scheduling, which guarantees equity by providing equal CPU usage opportunities to all processes.


---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer: 

During the simulation, each process thread moves through several thread states defined in Java. These states represent the lifecycle of a thread as it is created, scheduled, executed, and eventually finished. We can trace these states using process P1 from the program output and by understanding how the scheduler code operates.

New:
The thread enters the New state when it is created using new Thread(process) inside the addProcessToQueue() method. At this point, the thread object exists but has not started executing yet.
Runnable:
After the thread is added to the ready queue, it becomes Runnable. In this state, the thread is ready to run and waiting for the CPU scheduler to select it.
Running:
The thread enters the Running state when the scheduler calls currentThread.start(). At this moment the process begins executing the run() method. In the output we see this when P1 starts executing:
▶ P1 executing quantum [3000ms]
Waiting:
The main scheduler thread temporarily enters a Waiting state when it calls currentThread.join(). This causes the main thread to wait until the currently executing process finishes its quantum before continuing the scheduling cycle.
Terminated:
Finally, the thread enters the Terminated state when the process completes all its remaining burst time and exits the run() method. This is shown in the output when P1 finishes execution:
✓ P1 finished execution!

At this point, the thread has completed its lifecycle and will no longer participate in the scheduling process.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

Example 1: Web Server Request Handling

Description:
A web server often receives many user requests simultaneously, such as loading webpages or processing API calls. Each request can be handled by a separate thread.

Why Round-Robin works well here:
Round-Robin scheduling ensures that each request gets a fair amount of CPU time. This prevents one request from blocking others and improves the responsiveness of the server. It also allows multiple clients to be served efficiently.

Example 2: Time-Sharing Operating Systems

Description:
Modern operating systems like Linux and Windows allow multiple applications to run simultaneously on the same CPU.

Why Round-Robin works well here:
Round-Robin scheduling ensures that each running application receives a fair share of CPU time. This prevents long-running applications from monopolizing the processor and maintains system responsiveness for interactive users.

---

## Summary

**Key concepts I understood through these questions:**
1. The difference between processes and threads in operating systems.
2. How Round-Robin scheduling manages processes using a ready queue.
3. The lifecycle states of a thread during execution.

**Concepts I need to study more:**
1. Advanced CPU scheduling algorithms such as Priority Scheduling and Multilevel Queue Scheduling.
2. How context switching impacts CPU performance and system efficiency.
