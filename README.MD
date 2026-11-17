Name : Hima Sai Chandana
Roll Number : 2401MC37
Set Number : 1
Date : 17/11/2026

Question 1: Counting Semaphores for Process Synchronization
sem.c : created new file sem.c and wrote semaphore functions for question 1
defs.h : added declarations for sem_init, sem_wait, sem_post
main.c : initialized semaphore lock using seminit
syscall.h : assigned system call numbers for sem_init, sem_wait, sem_post
syscall.c : mapped syscall numbers in array from syscall.h for sem_init, sem_wait, sem_post
sysproc.c : implemented syscall wrapper functions for sem_init, sem_wait, sem_post
user.h : added user system call prototypes int sem_init(int, int); int sem_wait(int); int sem_post(int);
usys.S : added SYSCALL(sem_init), SYSCALL(sem_wait), SYSCALL(sem_post)
Makefile : added sem.o and synctest to build
synctest.c : created user C program to test question 1

Question 2: Memory Statistics and Address Translation
defs.h : added declarations for freepages, va2pa
syscall.h : assigned system call numbers for freepages, va2pa
syscall.c : mapped syscall numbers in array from syscall.h for freepages, va2pa
sysproc.c : implemented syscall wrapper functions for freepages, va2pa
user.h : added user system call prototypes int freepages(void); int va2pa(int);
usys.S : added SYSCALL(freepages), SYSCALL(va2pa)
Makefile : added memtest to build
kalloc.c : added freepages count and updated kfree, kalloc
vm.c : implemented address translation function int va2pa(uint)
memtest.c : created user C program to test question 2