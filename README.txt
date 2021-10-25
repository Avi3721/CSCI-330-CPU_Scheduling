------------------------------------------------------------------------
This is the project README file. Here, you should describe your project.
Tell the reader (someone who does not know anything about this project)
all he/she needs to know. The comments should usually include at least:
------------------------------------------------------------------------

PROJECT TITLE:.........................Round Robin CPU scheduling
PURPOSE OF PROJECT:....................Final class project
VERSION or DATE:.......................04/21/2021
HOW TO START THIS PROJECT:.............steps provided below 
AUTHORS:...............................AVIVARTTA KRISHNA (1261351)
USER INSTRUCTIONS:.....................Steps provided below 

The following submitted java file consists of the final project, where the objective was to create a program that would simulate Round Robin CPU scheduling. 

program requirements:

1). Generate a schedule process
2). Plaintext file for the stored processes 
3). Accepts 2 parameters (Path/time quantum)
4). Simulation which includes (clock/process creator/CPU/queue/procss arrival time/process service time/time quantum/context switch)
5). Program uotput should print the performance evaluation criteria, which includes (CPU utilization/throughput/waiting time/turnaround time)

understanding the working of the program:

The term CPU scheduling is a cycle that permits one cycle to utilize the CPU while the execution of another cycle is on hold because of inaccessibility of any asset like I/O and so forth, in this manner utilizing CPU. The point of the CPU scheduling is to make the framework productive, quick, and reasonable. There are 3 types of CPU scheduling:
- When a process switches from the running state to the waiting state.
- When a process switches from the running state to the ready sate.
- When a process switches from the waiting state to the ready state.

Round Robin Scheduling
-The name of this algorithm comes from the round-robin principle, where each person gets an equal share of something in turns. It is the oldest, simplest scheduling algorithm, which is mostly used for multitasking.
-In Round-robin scheduling, each ready task runs turn by turn only in a cyclic queue for a limited time slice. This algorithm also offers starvation free execution of processes.
-Round Robin is the preemptive process scheduling algorithm.
-Each process is provided a fix time to execute, it is called a quantum.
-Once a process is executed for a given time period, it is preempted and other process executes for a given time period.
-Context switching is used to save states of preempted processes.

I started working on the java code by firstly by creating an array to keep track of the remaining burst time of the processes, which is initially a copy of the bursts time array. Then I created another array to store the waiting time of the processes and initialize it as 0. I then transversed all the processes one by one again and again. After completing that I then worked on calculating the turn around time, avarage time, waiting time. Stated below are the java code comments for a better understnding of the entire working of the program. 
All of this I made in a seperate Java Package which I name CSCI_330.
The Code was made in Five Parts:
1.RoundRobinSimulation - Main Code
2.Simulation - Constructors for the Simulation
3.CPU - Constructors for Time Process and Time Quantum
4.Clock - Constructors for wait time process and ready queue
5.Process - Contians all of the process for the working of the code

Resulting Output of Program Using Five Different Time Quantums Using Sample Input Give - cfg.txt flie (Path - C:\Users\avivk\OneDrive\Desktop\cfg.txt)

Enter time quantum for processes: 5
Enter Config File Name: C:\Users\avivk\OneDrive\Desktop\cfg.txt
Average wait time: 11.0
Average turnaround time: 22.0
Throughput: 9.615384615384617%
CPU utilization: 86.53846153846155%
END of simulation

Enter time quantum for processes: 10
Enter Config File Name: C:\Users\avivk\OneDrive\Desktop\cfg.txt
Average wait time: 6.0
Average turnaround time: 16.0
Throughput: 9.615384615384617%
CPU utilization: 96.15384615384616%
END of simulation

Enter time quantum for processes: 20
Enter Config File Name: C:\Users\avivk\OneDrive\Desktop\cfg.txt
Average wait time: 4.0
Average turnaround time: 14.0
Throughput: 9.615384615384617%
CPU utilization: 100.0%
END of simulation

Enter time quantum for processes: 30
Enter Config File Name: C:\Users\avivk\OneDrive\Desktop\cfg.txt
Average wait time: 4.0
Average turnaround time: 14.0
Throughput: 9.615384615384617%
CPU utilization: 100.0%
END of simulation

Enter time quantum for processes: 40
Enter Config File Name: C:\Users\avivk\OneDrive\Desktop\cfg.txt
Average wait time: 4.0
Average turnaround time: 14.0
Throughput: 9.615384615384617%
CPU utilization: 100.0%
END of simulation


