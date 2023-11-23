# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here

## A1
- b. A Unix-like operating system
## A2
 - b. Linux
## A3
- d. simple
## A4
- d. As external programs
## A5
- a. 128
## A6
- c. Sh
## A7
- a. Round-robin scheduling
## A8
- a. Paging
## A9
- d. Both b and c
## A10
- b. No
## A11
- c. MIT
## A12
These are the following states a process can take
1.Running: currently being executed.
2.Runnable: Ready to run but is waiting for CPU allocation. 
3. Sleeping: Waiting for a particular event or condition.
4. Zombie: Execution completed . Waiting for parent to call for results
## A13
- XV6 has an heirarchial file system structure,consisting of directories, files, and inodes similar to Linux. Inodes  store metadata about files and their data block locations. Directories correspond to folders where other directories of files are located.
## A14
- System calls are interfaces provided by the operating system that allow user-level processes to request services from the kernel. eg. kill, which can be used to kill a particular process.
- Library functions are sets of pre-compiled routines provided by libraries that applications can link to. eg printf() which may use some write() system call to do its stuff.
- Library Functions are usually at a higher level of abstractions than system calls
## A15
In XV6, memory paging is a technique used for virtual memory management. Memory paging in XV6 divides physical memory into fixed-size pages and maps virtual pages of a process to physical pages via page tables. On a memory access, the CPU consults the page table; if the required page isn't in physical memory, a page fault triggers the OS to load the page. Paging offers benefits like virtual memory expansion beyond physical limits, memory protection, simplified management, non-contiguous memory allocation, and support for sharing via copy-on-write. This technique facilitates efficient memory utilization, security, and simpler memory handling in the operating system, enabling processes to access larger virtual memory spaces without requiring contiguous physical memory.
## A16
-ls : lists all directories and files in the current working directory
-echo : Used to print something directly to the terminal
-mkdir : Used to make a new Directory
## A17

## A18
In the XV6 operating system, interrupts play a crucial role in managing system events and ensuring timely responses to them. When hardware or software triggers an interrupt (such as a timer, I/O operation completion, or hardware error), the processor suspends its current execution, saves its state, and jumps to a predefined interrupt handler. This handler processes the interrupt, performs necessary actions (like servicing I/O requests), and resumes the interrupted task. Interrupts enhance system efficiency by enabling multitasking, allowing the system to promptly handle external events without wasting CPU cycles constantly checking for them.
## A19
Virtual memory is a memory management technique that extends physical memory by using disk space as an extension. In XV6, virtual memory is implemented through memory paging, dividing both physical and virtual memory into fixed-size pages and mapping them via page tables. XV6 handles page faults, loading required pages from disk to memory. Advantages of virtual memory include efficient memory utilization, memory protection, larger address spaces for processes, and simplified memory management.
## A20
