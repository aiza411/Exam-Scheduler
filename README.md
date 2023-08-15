# Exam-Scheduler

There are N courses to be scheduled and K exam halls available. Each course has a specific set of time slots available for scheduling its exam, and each exam hall can be used for a certain number of hours per day. In addition, some pairs of courses have conflicting students, meaning that they cannot be scheduled at the same time.


## Requirements

1. Define a representation for a solution to the scheduling problem. This could be a list of tuples, where each tuple represents an exam and contains information about its course, time slot, and exam hall.
2. Write a function to calculate the fitness of a solution. The fitness function should take a solution as input and output a score indicating how good the solution is. A good solution is one that satisfies all the constraints of the problem and minimizes the total number of conflicts between exams.
3. Implement a genetic algorithm to search for a good solution. Your implementation should include functions for initializing a population of solutions, selecting parents for crossover, performing crossover and mutation, and evaluating the fitness of the resulting offspring. You should experiment with different parameter settings to find the best combination.
4. Test your implementation on a set of sample problems with varying difficulty levels. You should report the results in terms of the fitness score achieved and the running time of the algorithm. You should also discuss the advantages and disadvantages of using a genetic algorithm for this type of problem compared to other optimization techniques. You are tasked with optimizing the scheduling of exams for a university.

## Explanation

Suppose we have 5 courses (C1, C2, C3, C4, C5) and 2 exam halls (H1, H2). Each course has 3 time slots available (T1, T2, T3), and each exam hall can be used for a maximum of 6 hours per day. In addition, there are some pairs of courses with conflicting students: 
-> C1 and C2 have 10 common students. 
-> C1 and C4 have 5 common students. 
-> C2 and C5 have 7 common students. 
-> C3 and C4 have 12 common students.
-> C4 and C5 have 8 common students.

We can use a genetic algorithm to search for other good solutions, and compare their fitness scores with the optimal solution found. For Example the algorithm starts with an initial population of 100 schedules, using tournament selection, single-point crossover, and mutation over 100 generations. A fitness function, accounting for time slot and hall constraints, as well as penalties for exceeding hall usage and scheduling conflicting student pairs together, guides the search. The best solution found schedules exams with minimized penalties and optimal resource utilization, leading to a fitness score of 20 i.e [(C1, T1, H1), (C2, T3, H1), (C3, T2, H2), (C4, T1, H2), (C5, T3, H2)]. This solution distributes exams across time slots and halls to meet constraints and minimize penalties.
