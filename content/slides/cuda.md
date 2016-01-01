+++
Categories = []
Tags = []  
Title = "CUDA Profile"  
date = "2015-12-31T10:30:25+08:00"  
+++

# CUDA Profile
---

## Profile Tool
- nvpp
  - GUI tool
- nvprof
  - Command line tool
---

## nvprof
- Basic
  - nvprof -o [GUI output file] -s [executable file] [arguments]
  - nvprof --log-file [output file]
- More
  - --print-gpu-trace
  - --events
  - --metrics
---

## Time
- CPU Timers
 ```
  t1 = myCPUTimer();
  launch <<< >>>;
  cudaDeviceSynchronize();
  t2 = myCPUTimer();
 ```
- CUDA Event
  ```
  cudaEvent_t start, stop;
  cudaEventCreate(&start);
  cudaEventCreate(&stop);
  cudaEventRecord(start);
  launch <<< >>>;
  cudaEventRecord(stop);
  cudaEventSynchronize(stop;
  float milliseconds = 0;
  cudaEventElapsedTime(&milliseconds, start, stop);
  cudaEventDestroy(&start);
  cudaEventDestroy(&stop);
  ```
- Profile Tool
---

## Memory Bandwidth(GB/s)

- Theoretical Bandwidth
 - BW = memory clock rate * 10^6(Hz) * n-bit wide memory interface / 8(byte) * 2(double data rate DDR) / 10^9 (s)
- Effective Bandwidth
 - BW = data number * data byte * (RB + WB) / (t * 10^9)
---

## Throughput(GFLOP)
- Giga-Floating-point Operations per second
- data number * float-point operations(add, mul)/ (t * 10^9)
---

## Reference
[How to implement Performance Metrics in CUDA](http://devblogs.nvidia.com/parallelforall/how-implement-performance-metrics-cuda-cc/)

