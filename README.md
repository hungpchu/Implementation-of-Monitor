# Implementation-of-Monitor


NAME: HUNG CHU
NUID: 95060612

## 1 Compile, Run, and Test program:

### 1.1 Compile and Run


	a/ To run the program part1.cpp:

make
./part1 -b 10 -p 1 -c 10 -i 20


## 2 Specification:	


(a) How would you guarantee that only one thread is inside the monitor at one time?

Answer: in my code, to guarantee that only one thread is inside the monitor at one time, i use a semaphore named mutex, which will signal and wait properly to ensure the mutual exclusion between threads


(b) Will your monitor follow the signal and wait or signal and continue discipline?

Answer: My monitor will follow signal and wait discipline

(c) How would you make sure that a suspended thread (due to wait) resumes where it left off?

Answer:  in my code, signal and wait function will be placed properly so that a suspended thread (due to wait) can resume where it left off

(d) How would you initialize the necessary data structures to support your monitor and make them visible to all threads?

Asnwer: I create a struct cond as implement of condition variables, which will support my monitor. Moreover, my own make function wait and signal is made in the local library named cond.cpp so that when i declare in my part2.cpp, all my thread can use those 2 functions.
