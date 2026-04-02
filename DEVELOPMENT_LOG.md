# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 28,2026,9:37pm]
**What I did**: Set up the project and ran the initial scheduler simulation.

**Details**: I launched the beginning code in my IDE after downloading it.
examined the program's architecture, particularly the SchedulerSimulation and Process classes.
I changed the code's student ID to my real ID, 445050253.
Java SchedulerSimulation was used to run the program after it was compiled using JavaC.
confirmed that the scheduling simulation operated well and generated the anticipated

**Challenges**: At first the program did not run because I forgot to compile the file before executing it.

**Solution**: I compiled the program first using javac SchedulerSimulation,java and then ran it again successfully.

**Time spent**: 50 minutes 

---

### Entry 2 - [march 29,2026,9:00pm]
**What I did**: Analyzed the code to understand how the Round-Robin scheduling algorithm was implemented.

**Details**: examined the process of adding processes to the ready queue.
saw how the simulation's processes are represented by threads.
adhered to the scheduler loop, which selects a thread from the queue, runs it for a certain amount of time, and then adds it again if there is still time left.
examined how Thread and Thread.start() work.To manage execution, join() is utilized.

**Challenges**: Understanding how the queue and the process map worked together to track processes and threads.

**Solution**: I traced the code step by step and added small print statements to observe how processes moved in the ready queue.

**Time spent**: 1 hour 30 hours 

---

### Entry 3 - [march 30,2026,11:18pm]
**What I did**: Implemented Feature 1 (Process Priority).

**Details**: The Process class now has a priority variable.
For every process, a random priority between 1 and 5 was generated.
To store the priority value, the constructor was updated.
When a process is added to the ready queue, the output message is changed to show the process priority.

**Challenges**: Ensuring that the priority value was passed correctly when creating each process.

**Solution**: I updated the constructor parameters and verified that the priority was printed correctly in the output.

**Time spent**: 1 hour 10 minutes 

---

### Entry 4 - [march 30,2026,8:35pm]
**What I did**: Implemented Feature 2 (Context Switch Counter).

**Details**: To track the number of times the CPU changes between processes, a static variable called contextSwitchCount was added.
Each time the scheduler chooses a new thread from the ready queue, the counter is increased.
At the conclusion of the simulation, the total number of context switches was shown.

**Challenges**: Determining the correct place in the scheduler loop to increment the counter.

**Solution**: I added the counter increment right after the scheduler retrieves the next thread from the ready queue.

**Time spent**: 1 hour  40 minutes 

---

### Entry 5 - [April 1 , 2026, 8:45pm]
**What I did**: Implemented Feature 3 (Waiting Time Calculation).

**Details**: StartTime and completionTime variables were added to the Process class.
When the process object is built, the process creation time is recorded.
recorded the time it took for the process to finish running.
To determine waiting time, a getWaitingTime() method was implemented utilizing the 
At the conclusion of the simulation, a summary table was printed and a list of completed processes was created.

**Challenges**: Tracking when processes finished and storing them correctly for the final summary table.

**Solution**: I added a list called finishedProcesses and inserted processes into the list when they completed execution.

**Time spent**: 1 hour 15 minutes 

---

### Entry 6 - [april 1,2026,9:58pm]
**What I did**: Tested the program and prepared the assignment documentation.

**Details**: To ensure the scheduler functioned properly, the program was run several times.
verified that the waiting table was printed accurately and that all procedures were finished.
checked the output to make sure the Round-Robin algorithm's ready queue behavior matched.
finished the answers file and recorded the process of development.

**Challenges**: Ensuring the output matched the requirements of the assignment and clearly demonstrated the scheduling behavior.

**Solution**: Carefully reviewed the output and compared it with the assignment instructions to confirm that all features were implemented correctly.

**Time spent**: 2 hours

---

## Summary

**Total time spent on assignment**: 8 hours 25 minutes 

**Most challenging part**: Tracking process completion times and calculating accurate waiting times for Feature 3.

**Most interesting learning**:Understanding how Round-Robin scheduling works in practice and how context switching occurs between processes. 

**What I would do differently next time**: I would plan the implementation of features earlier and test each feature immediately after adding it to reduce debugging time.
