# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**
This assignment taught me how multithreading enables several jobs to run simultaneously within a single program I comprehended how Java's Thread class is used to build threads and how each simulation process operates as a separate thread. The lifecycle of a thread, which includes phases like new, runnable, running, waiting, and terminated, was one important idea I noticed Time quantums were used by the Round-Robin scheduler to show how threads split CPU time I also discovered that controlling the order of execution requires thread synchronization Controlling when threads execute and the scheduler waits was made easier by using methods like join() and start() In general, this task improved my comprehension of how operating systems effectively handle multiple processes at once.

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**
Understanding how the scheduler manages several threads throughout execution was the most difficult aspect of this project. When a time quantum ended, it was initially challenging to understand how processes moved between the ready queue and the CPU. A close examination of the code structure was necessary to understand how the scheduler thread interacted with the process threads. Making changes to the program to incorporate the new feature while maintaining the proper behavior presented another difficulty Small errors could result in unexpected output or improper scheduling behavior when numerous threads were involved It was also necessary to interpret the program's output and make sure it matched the anticipated Round-Robin behavior I gained a better understanding of the connection between thread execution and scheduling methods thanks to this challenge.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

In order to overcome the difficulties in this project, I first thoroughly examined the beginning code that was supplied in order to comprehend the interactions between the scheduler and process threads I examined the procedures in charge of running each process and overseeing the ready queue I was able to see the results and comprehend the scheduling sequence by running the application several times I also tracked the flow of processes across the system by using debugging techniques like publishing intermediate messages The implementation was easier to handle when the issue was divided into smaller components A number of concepts were also made clearer by going over the course materials on thread states and scheduling techniques I was able to effectively finish the necessary changes thanks to this methodical approach.

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

In practical applications, multithreading is frequently employed to enhance responsiveness and performance For instance, several threads are used concurrently by contemporary web browsers to load webpages, execute scripts, and handle user interactions Multithreading is also used in video games to manage player input, physics computations, and graphics rendering simultaneously Threads enable background operations in mobile applications, including processing photos or downloading data, without causing the user interface to freeze Multithreading is used by operating systems to effectively handle several processes The ideas covered in this assignment, like CPU sharing and thread scheduling, have a direct bearing on how these systems function Developers can create faster and more responsive systems by having a better understanding of multithreading.

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
