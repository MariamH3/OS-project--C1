# CPU Scheduling Comparison Project: Priority vs SRTF

## Project Description

This project is an Operating Systems CPU Scheduling simulator that compares two scheduling algorithms:

1. Priority Scheduling
2. Shortest Remaining Time First (SRTF)

The goal is to compare how both algorithms affect waiting time, turnaround time, response time, fairness, starvation risk, and process execution order.

---

## Algorithms Implemented

### Priority Scheduling

- Type: Preemptive
- Priority rule: Lower number means higher priority
- Example: Priority 1 is higher than Priority 5
- Tie-breaking rule: FCFS based on arrival time
- Aging mechanism: Every 5 waiting time units, the waiting process priority is improved by decreasing its priority value by 1.

### Shortest Remaining Time First

- Type: Preemptive
- Selection rule: The process with the shortest remaining burst time is selected.
- A newly arrived shorter process can preempt the currently running process.
- Tie-breaking rule: FCFS based on arrival time.

---

## Features

- JavaFX GUI
- User-defined process input
- Input validation
- Process table
- Separate Gantt chart for Priority Scheduling
- Separate Gantt chart for SRTF
- Separate result table for each algorithm
- Waiting Time, Turnaround Time, and Response Time calculation
- Average WT, average TAT, and average RT calculation
- Comparison table
- Preset test scenarios
- Validation error handling

---

## Input Fields

Each process requires:

- Process ID
- Arrival Time
- Burst Time
- Priority Value

The program rejects invalid input such as:

- Empty fields
- Negative arrival time
- Zero or negative burst time
- Zero or negative priority
- Duplicate process ID
- Non-numeric input

---

## Technologies Used

- Java
- JavaFX
- Maven

---

## How to Run

Make sure Java and Maven are installed.

Run the following command from the project folder:

```bash
mvn clean javafx:run
