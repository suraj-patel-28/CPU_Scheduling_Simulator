
---

# CPU Scheduling Simulator

This repository contains a CPU scheduling simulator implemented in C++. The simulator supports various scheduling algorithms, including First-Come-First-Serve (FCFS), Round Robin (RR), Shortest Process Next (SPN), Shortest Remaining Time (SRT), Highest Response Ratio Next (HRRN), and Feedback Queues. The simulator can be used to trace the scheduling of processes and output statistics related to process execution times.

## Table of Contents

- [Features](#features)
- [Supported Algorithms](#supported-algorithms)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)

## Features

- Simulates various CPU scheduling algorithms.
- Outputs a timeline of process execution.
- Calculates and displays turnaround time and normalized turnaround time for each process.
- Handles edge cases such as different arrival times and varying service times.

## Supported Algorithms

The simulator currently supports the following CPU scheduling algorithms:

1. **First-Come-First-Serve (FCFS)**: Processes are executed in the order of their arrival.
2. **Round Robin (RR)**: Processes are executed in a cyclic manner with a fixed time quantum.
3. **Shortest Process Next (SPN)**: The process with the shortest service time is executed next.
4. **Shortest Remaining Time (SRT)**: The process with the shortest remaining service time is executed.
5. **Highest Response Ratio Next (HRRN)**: The process with the highest response ratio is executed next.
6. **Feedback Queue (FB-1)**: Uses feedback queues with fixed quantum.
7. **Feedback Queue (FB-2i)**: Feedback queue with dynamically increasing quantum.
8. **Aging**: Not yet implemented but can be added for simulating priority aging.

## Installation

To install and run this project locally, follow these steps:

1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/CPU-Scheduling-Simulator.git
   cd CPU-Scheduling-Simulator
   ```

2. Compile the code using a C++ compiler:

   ```sh
   g++ -o cpu_scheduling main.cpp
   ```

3. Run the simulator:

   ```sh
   ./cpu_scheduling.exe
   ```

## Usage

To use the simulator, you need to provide a configuration of processes, including their arrival times and service times. The simulator will then execute the selected scheduling algorithm and output the process execution timeline and related statistics.

### Command Line Arguments

- `trace`: Enables tracing of the process timeline.
- `stats`: Displays statistics such as turnaround time and normalized turnaround time for each process.
- `ALGORITHM`: Specify the scheduling algorithm to use (e.g., FCFS, RR, SPN, etc.).

Example:

## Example

```sh
./cpu_scheduling.exe
trace
1
20
5
A,0,3
B,2,6
C,4,4
D,6,5
E,8,2

```

Example Output:

```text
Algorithm: FCFS

FCFS  0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0
------------------------------------------------
A     |*|*|*| | | | | | | | | | | | | | | | | |
B     | | |.|*|*|*|*|*|*| | | | | | | | | | | |
C     | | | | |.|.|.|.|.|*|*|*|*| | | | | | | |
D     | | | | | | |.|.|.|.|.|.|.|*|*|*|*|*| | |
E     | | | | | | | | |.|.|.|.|.|.|.|.|.|.|*|*|
------------------------------------------------
```


---

