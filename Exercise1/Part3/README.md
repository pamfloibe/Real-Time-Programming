# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Parallelism: A process in which at least two threads are being executed simultaneusly.*

 > *Concurrency: A process in which two threads are being executed in overlapping time periods.*

 > *The difference between concurrency and parallelism is that concurrency manages access to shared state from different threads, like multitasking on a single-core machine, and parallelism uses multiple processors in order to improve the performance of a computation.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *Before the past decade, the number of transistors that could be placed in the same area of the one-core processors kept growing exponentially, meaning that the number of processes that could take place kept growing as well. At some point, the energy needed to supply ALL these transistors was not enough, meaning that it would be easier to split them up into multi-core processors in order to feed all of the transistors and keep up with the amount of processes that could be made.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *As concurrency results in increased performance, it is helpful even for every 'simple' thing done in a computer. As simple as using or running two programs at the same time, without having to exit one first in order to use the second one. Most of things used in a computer a concurrent.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *I would say both, as it would make it a bit more difficult for the programmer to think about the solution and how to implement it, but once the programmer has got that part it will make the process of developing and testing easier.*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Processes: They are OS-managed. A process is the instance of a computer program that is being executed. It may be made up of multiple threads in order to execute instructions concurrently.*

 > *Threads: They are OS-managed. They are the smallest sequence of programmed instructions that can be managed independently.*

 > *Green threads: They are NOT OS-managed as they are used by a virtual machine instead of the operating system itself.*

 > *Coroutines: They are NOT OS-managed. They are computer-program components that generalize subroutines for non-preemptive multitasking, as they allow multiple entry points for suspending and resuming execution at certain locations.*

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *pthread_create() - Starts a new thread*
 > *threading.Thread() - Starts a coroutine*
 > *go - Starts a green thread*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *As GIL protects access to Python objects and prevents multiple threads, it prevents programs from taking full advantage of multiprocessors.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *You can use another Python module that doesn't use GIL, such as JYTHON.*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *It can change the limit of threads that can be executed simultaneously.*
