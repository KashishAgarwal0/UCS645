# UCS645
Parallel and Distributed Computing
# CUDA Assignments – UCS645 (Parallel and Distributed Computing)

This repository contains my completed assignments for UCS645 – Parallel and Distributed Computing, focused on CUDA programming, performance profiling, and parallel algorithm design using NVIDIA GPUs.

---

## 🚀 Assignment 1: Multi-threaded Task Execution in CUDA

### Problem
Implement a CUDA program where each thread performs a different task:
- **Thread 0** computes the sum of the first `N = 1024` integers *iteratively*.
- **Thread 1** computes the same sum *using the direct formula*.

### Key Concepts
- Thread-level parallelism
- Host-to-device memory management
- Simple GPU task branching

### Output Sample
Iterative sum (Thread 0): 524800 Formula sum (Thread 1): 524800


## ⚡ Assignment 2: Merge Sort — Pipelined vs CUDA Parallel

### Part A: Merge Sort using Pipelining on CPU
- Implements standard merge sort with pipelined stages.
- Simulates overlapping stages to mimic parallel flow.

### Part B: Parallel Merge Sort using CUDA
- Sorts a large array using GPU kernels.
- Measures and compares execution time with pipelined CPU sort.

### Part C: Performance Comparison
- **Input Size:** `N = 1000`
- **Metrics Tracked:** Execution time (ms), Speedup
- **Output:** Console output + timing data

### Output Sample
CPU Time: 4.32 ms CUDA Time: 0.68 ms Speedup: ~6.35x


## 🧮 Assignment 3: Performance Profiling & Bandwidth

### Task
1. Implement basic **vector addition** using CUDA.
2. Use **statically defined global memory** (no cudaMalloc).
3. Measure:
   - **Kernel execution time**
   - **Theoretical memory bandwidth** (from device props)
   - **Measured bandwidth** based on reads/writes

### Extra Task
- Compute **vector square roots** over increasing array sizes:
  - `N = 50K`, `500K`, `5M`, `50M`
  - Measure kernel time for each
  - Plot timing results using matplotlib

## 📈 Technologies & Tools
- CUDA C++ (compiled with `nvcc`)
- Google Colab (with T4 GPU)
- `cudaEvent` for profiling
- `cudaDeviceProp` for hardware queries
- Python + matplotlib for plotting

---



## ✅ How to Run

In Google Colab (with GPU enabled):

```bash
!nvcc filename.cu -o output
!./output
Or in local terminal (if CUDA is installed).

📌 Author
Kashish Agarwal, 3rd Year Computer Engineering
Thapar Institute of Engineering & Technology
Learning CUDA to conquer data-heavy computation one kernel at a time ⚡

📘 License
This project is submitted as part of coursework for UCS645. Not intended for redistribution.

