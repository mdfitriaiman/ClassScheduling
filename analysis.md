# Introduction

In CPU scheduling, it is important to choose the right algorithm, so that it will take a shorter time to execute all the processes in a queue.  
In this context, choosing the right solution to schedule the classes is essential to save resources.

The chosen algorithms are:

1. **First Come First Serve (FCFS) Scheduling**

	This algorithm executes processes based on which process comes first in the queue.


2. **Shortest Job First (SJF) Scheduling**

	This algorithm executes processes based on which process in the queue has a shorter burst time. In this case, the duration of the class.


3. **Priority Scheduling**

	This algorithm executes processes based on which process in the queue has a higher priority (lower integer = higher priority).


# Consideration

For this analysis, we considered a few scenarios that would provide more clarity for each scheduling algorithm and made our input accordingly.

* For FCFS scheduling, it only depends on which class comes first in the array.
* For SJF scheduling, we considered classes that have the same duration.
* As for priority scheduling, we considered classes that have the same priority.

Hence, the input is as follows: 

| Process | Duration | Priority | Arrival time |
| :---: | :---: | :---: | :---: |
| 2201 | 3 | 2 | 1 |
| 3401 | 2 | 3 | 2 |
| 1103 | 1 | 1 | 3 |

*Do note that the arrival time for the classes are neglected, as the algorithms chosen are non-preemptive.*

# Analysis

## FCFS

For priority FCFS, the data is as follows:

| Process | Burst Time | Waiting Time | Turnaround Time | 
| :---: | :---: | :---: | :---: | 
| 2201 | 3 | 0 | 3 | 
| 3401 | 2 | 3 | 5 |
| 1103 | 1 | 5 | 6 |

**Average waiting time = 2.67**
**Average turnaround time = 4.67**

From the averages provided, FCFS is the least efficient algorithm because the waiting time is the longest overall. In this algorithm, some processes have to wait a long time to be executed, although they have shorter durations than others. It only runs the process in chronological order, so if an longer class arrives earlier in the queue, this will take time. So why is FCFS slower than SJF and Priority Scheduling.
 
## SJF

For SJF scheduling, the data is as follows:

| Process ID | Arrival Time | Burst Time | Waiting Time | Turnaround Time | 
| :---: | :---: | :---: | :---: | 
| 2201 | 1 | 3 | 0 | 3 |
| 3401 | 2 | 2 | 0 | 0 |
| 1103 | 3 | 1 | 0 | 0 |

**Average waiting time = 0**
**Average turnaround time = 1**

From the averages provided, SJF is the most efficient algorithm because the waiting time for the process is overall shortest compared to FCFS and Priority Scheduling. In this algorithm, It implements processes according to the duration, so it is the most effective process. However, the duration of each class must be known before this algorithm can be used.

## Priority Scheduling

For priority scheduling, the data is as follows:

| Process | Priority | Burst Time | Waiting Time | Turnaround Time | 
| :---: | :---: | :---: | :---: |
| 3401 | 1 | 2 | 0 | 2 |
| 2201 | 2 | 3 | 2 | 5 |
| 1103 | 3 | 1 | 5 | 6 |

**Average waiting time = 2.33**
**Average turnaround time = 4.33**



# Conclusion

From the analysis, it is shown that **Shortest Job First (SJF)** algorithm is the best non-preemptive algorithm to implement class scheduling.

It is the most efficient algorithm time-wise, based on the constraints given. Arrival time is neglected as it will only be considered in preemptive scheduling algorithms, as mentioned.

However, it is important to note again that the durations for the classes must be known beforehand, so that the algorithm can be used.  

# Group Members
* Mohammad Fitri Aiman bin Mohammad Azli (1810925)
* Muhammad Owish bin Muhammad Rizal(1816401)
* Syed Muhammad Aiman bin Syed Mohd Azmi (1727935)
