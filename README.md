# CS350-Homework-5-solved

Download Here: [CS350 Homework #5 solved](https://jarviscodinghub.com/assignment/homework-5-solution-2/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Write a simulator that would evaluate the performance of a round-robin scheduler.
Notice that (unlike the simulators you developed for M/M/1), in this simulator you will need to keep track of various parameters for the various requests in the system. Specifically, for each request in the system, you will need to record the current arrival time of the request, the requested service time for that request, and the service time already given to that request. For a round-robin scheduler, every time the request is assigned to the resource, one must check if the request will be done if it is given up to one quantum (time slice). If so, the “death” event (signifying the completion of service) can be added to the simulation calendar, otherwise a “timeout” event (signifying the expiration of a quantum) can be added to the simulation calendar. Of course, what happens as a result of “death” versus “timeout” is different.

Test your simulator using the following parameters:

Arrival rate of new requests is Lambda = 30 requests/second
Requested service time is exponentially-distributed with a mean = Ts = 30 milliseconds
The fixed time slice (quantum) of the RR scheduler is c milliseconds
Total simulation time = 100 seconds

Measure the average response time for requests submitted to your round-robin scheduler when c = 1, 10, 30, and 60 milliseconds. Compare the results from your simulator to those you calculate using an M/M/1 approximation [Note: Check the notes in “From M/M/1 to GPS”]. What conclusions can you make?
To show the relative performance for different types of requests, generate a bar chart (e.g., using excel) showing the average slowdown (on the Y axis) for different ranges of requested service times (on the X axis). In particular, use the following ranges (in milliseconds): 0-10; 10-20; 20-30; 30-40; 40-50; 50-60; 60-70+. What conclusions can you make? Does your answer depend on c?

Write a simulator that would evaluate the performance of a scheduler with the following characteristics:
Selection Function: Select the request with the minimum remaining service time
Decision Mode: Preemptive at timeout using a fixed quantum of c milliseconds
Test your simulator using the following parameters (same as round-robin problem above):

Arrival rate of new requests is Lambda = 30 requests/second
Requested service time is exponentially-distributed with a mean = Ts = 30 milliseconds
The fixed time slice (quantum) of the RR scheduler is c milliseconds
Total simulation time = 100 seconds

Measure the average response time and the slowdown for requests submitted to your scheduler when c = 1, 10, 30, and 60 milliseconds.
To show the relative performance for different types of requests, generate a bar chart (e.g., using excel) showing the average slowdown (on the Y axis) for different ranges of requested service times (on the X axis). In particular, use the following ranges (in milliseconds): 0-10; 10-20; 20-30; 30-40; 40-50; 50-60; 60-70+. What conclusions can you make? Does your answer depend on c?
Comment on differences between the observed slowdown profile of this scheduler and that of the round-robin scheduler (in the above problem).

Three processes A, B, and C are submitted for execution at time 0 (with A ahead of B, which in turn is ahead of C in the ready queue). Processes A and B are CPU bound and each need the CPU for a total of 1 second. Process C is I/O bound. It uses the CPU for 10 milliseconds and then waits for I/O to complete for 100 milliseconds. It needs to go through this CPU-I/O cycle for 5 times.
Compute the slowdown for jobs A, B, and C for the following algorithms:

FIFO
Shortest-Remaining-Time-First
Round Robin with a 200-milliseconds quantum
Virtual Round Robin with 200-milliseconds quantum

There are 3 classes of jobs in a computer system. Jobs of class A arrive to the system very infrequently, but are of the highest possible priority. Jobs of class C arrive to the system very infrequently and have the lowest possible priority. Jobs of class B arrive to the system quite frequently and have medium priority. Assume that all three classes of processes need the CPU. To manage the CPU, priority scheduling is used, whereby the highest priority Job that needs the CPU is scheduled (preempting any other job of lower priority that may be using the CPU, if necessary). Ties are broken arbitrarily. Answer the following questions:
Is starvation possible? Which of the three classes of jobs is most susceptible to starvation?
Assume that jobs of class A arrive periodically every minute (i.e. exactly every minute a job of class A arrives) and that each such job needs the CPU for exactly 5 seconds. Also, assume that jobs of class B arrive periodically every second and that each such job needs the CPU for exactly 0.5 seconds. Finally, assume that jobs of class C arrive periodically every 5 minutes.

Assuming that jobs of class C need the CPU for exactly 20 seconds. Answer the following questions:
What is the worst-case response time for jobs of class A?
What is the worst-case response time for jobs of class B?
What is the worst-case response time for jobs of class C?

What is the maximum amount of CPU time per period for jobs of class C beyond which the system will never reach steady state? In other words, what is the maximum amount of CPU time per period of jobs of class C that would make the worst-case response time for some jobs in the system grow infinitely large over time…
As it turns out, jobs from class A and class C need another resource R. R is a resource which cannot be shared. In other words, if a job starts using resource R, then R cannot be released to another job until that process is done—think of a printer, for example. Thus, if a job needs resource R and that resource is “busy” then that job must block waiting for the resource. When the resource R is released, it is given to the highest-priority job waiting for it with ties broken arbitrarily.

Assume that a job from classes A or C needs the resource R concurrently with the CPU (i.e. R will be “busy” as long as the job is not done with the CPU). Notice that if a job cannot get a hold of R, then it cannot compete for the CPU (it has no use for the CPU without having R).

Explain why the priority scheme devised for managing the CPU is not adequate when sharing resources such as R. In particular, show that under the above conditions, it is possible for a job from class A (which is presumably of the highest-priority) to be waiting for a job from class C (which is presumably of the lowest-priority) to release the shared resource R.
What is the worst-case response time for jobs of class A?
Read the article on “What Really Happened on Mars?” and answer the following:

Define what is meant by priority inversion.
Define what is meant by priority inheritance.
Assuming that priority inheritance is used to schedule the CPU for jobs of classes A, B, and C. What is the worst-case response time for jobs of class A?
