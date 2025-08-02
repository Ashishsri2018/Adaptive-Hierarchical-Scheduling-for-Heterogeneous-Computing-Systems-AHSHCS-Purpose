# Adaptive-Hierarchical-Scheduling-for-Heterogeneous-Computing-Systems-AHSHCS-Purpose

Purpose
The Adaptive Hierarchical Scheduling for Heterogeneous Computing Systems (AHSHCS) algorithm optimizes task allocation in computing environments with diverse hardware components, such as CPUs, GPUs, and FPGAs. Unlike traditional scheduling algorithms, AHSHCS uses a hierarchical structure combined with reinforcement learning to dynamically adapt to workload patterns and hardware performance characteristics, maximizing system throughput in real-time.
Core Idea
The algorithm operates on two levels:

High-Level Scheduler: Analyzes historical and current workload patterns to make coarse-grained decisions about task distribution across hardware types.
Low-Level Agents: Each hardware type (e.g., CPU, GPU, FPGA) has a dedicated reinforcement learning (RL) agent that fine-tunes task execution based on real-time performance feedback.

The novelty lies in the specific integration of a hierarchical decision-making framework with per-hardware RL agents that cooperate to optimize global system performance, adapting dynamically to changing computational demands and hardware capabilities.
Why It’s Unique
While scheduling algorithms for heterogeneous systems exist (e.g., HEFT, ML-based schedulers), and reinforcement learning has been applied to scheduling, the combination of a hierarchical approach with dedicated RL agents per hardware type, focused on real-time adaptation in heterogeneous environments, appears to be a novel contribution. A search for "hierarchical scheduling with reinforcement learning for heterogeneous computing" revealed related concepts but no exact match for this specific design.
How It Works

Input: A set of tasks with dependencies (represented as a directed acyclic graph, DAG), hardware component specifications, and real-time performance metrics.
High-Level Scheduler: Uses a clustering technique (e.g., k-means) on historical task execution data to group tasks by hardware affinity, then assigns task clusters to hardware types.
Low-Level RL Agents: Each agent uses a Q-learning model to optimize task execution order and resource allocation within its assigned hardware, adjusting based on rewards (e.g., throughput, latency).
Feedback Loop: Agents report performance back to the high-level scheduler, which refines its clustering and allocation strategy over time.
Output: An optimized task schedule that maximizes system throughput.
