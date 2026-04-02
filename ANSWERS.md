# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?


**Your Answer:**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

A process is an entity with it's own address space and a thread is also an entity that is a part of a process. a thread provides advantages over the process first being that it's a lightweight meaning that it's much faster and more responsive than a process, and threads allow for creating multiple threads under the same address space without having to create multiple processes and they are much cheaperto create and allowes for resource sharing.
---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]
when using a Round Robin scheduling when a process goes into the CPU and starts executing it has a certain time period to finish, but if the time period expire before the process finishes while there's another process in the ready queue, then the process leaves from the CPU and waits at the ready queue while another process takes it place in the CPU.
Example from my output:
```
 ? P1 executing quantum [3000ms]
  ? Quantum progress: [███████████████] 100%
  ? P1 completed quantum 3000ms │ Overall progress: [████████░░░░░░░░░░░░] 42%
     Remaining time: 4031ms
  ? P1 yields CPU for context switch

[Paste a relevant snippet from your program output here showing a process being re-queued]
```
│ [P2 ? P3 ? P4 ? P5 ? P6 ? P7 ? P8 ? P9 ? P10 ? P11 ? P12 ? P13 ? P14 ? P15] P2 waiting for p1 time quantum to end

│ [P3 ? P4 ? P5 ? P6 ? P7 ? P8 ? P9 ? P10 ? P11 ? P12 ? P13 ? P14 ? P15 ? P1] p1 time quantum ends and gets requeued while p2 uses the CPU

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]
p1 goes to the CPU first and starts executing until the time quantum ends then it yields the CPU for the next process to take it's place being p2 in this case then p1 gets re-queued into the ready queue again.
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?] when it's beign created

2. **Runnable**: [When does P1 become Runnable?] when it's added to the ready queue

3. **Running**: [When is P1 Running?] when it's executing in the CPU

4. **Waiting**: [When/why would P1 be Waiting?] When it's waiting for a specific thing

5. **Terminated**: [When is P1 Terminated?] When it finished execution

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]
a web server that recieves multiple requests from mulitple users 
**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
it's suitable mainly because it provides fairness to all of the users meaning that all the users will get a chance load a page or download some files 
### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]
a video game engine has mulitple tasks that need to be dealt with at once such detecting player input graphics rendering playing audio
**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
Round Robin with a good time quantum can provide high responsivness for the player
---

## Summary

**Key concepts I understood through these questions:**
1. threading vs process and the difference between them
2. Round-Robin scheduling and it affects
3. thread states

**Concepts I need to study more:**
1. real world application on threads
2. how do threads deal with using the same resource by two threads 
