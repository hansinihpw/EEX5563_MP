# EEX5563_MP
# Multilevel Queue Scheduler

A Python module for implementing a multilevel queue scheduler with a graphical user interface using Tkinter.

## Overview

This module provides classes for a multilevel queue scheduler, which organizes processes into different priority queues. The scheduler uses a round-robin approach with a specified time quantum and incorporates an aging mechanism to boost the priority of processes.

## Classes

### `Process`

Represents a process with attributes such as Process ID (`pid`), priority, burst time, remaining time, and wait time.

#### Methods

- `__init__(self, pid, priority, burst_time)`: Initializes a process with the given parameters.

### `MultilevelQueueScheduler`

Implements the multilevel queue scheduler with a specified number of queues and aging threshold.

#### Methods

- `__init__(self, num_queues, aging_threshold)`: Initializes the scheduler with the number of queues and aging threshold.

- `enqueue_process(self, process)`: Adds a process to the scheduler's queue based on its priority.

- `run_scheduler(self)`: Runs the multilevel queue scheduler, executing processes based on their priorities and utilizing round-robin scheduling with the specified time quantum.

- `boost_priority(self, process)`: Increases the priority of a process, capped at the highest priority.

### `SchedulerApp`

Provides a graphical user interface for interacting with the multilevel queue scheduler.

#### Methods

- `__init__(self, master)`: Initializes the GUI for the scheduler application.

- `create_widgets(self)`: Creates widgets for the GUI, including process entry, queue settings, and run button.

- `run_scheduler(self)`: Runs the scheduler based on user inputs, parsing processes, setting up the scheduler, and displaying results.

- `display_results(self, total_time_elapsed)`: Displays scheduling results in a new window.

