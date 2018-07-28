## Answers

1. List all of the main states a process may be in at any point in time on a
   standard Unix system. Briefly explain what each of these states mean.

   * State - This is the initial state when a process is first started/created.

   * Ready - The process is waiting to be assigned to a processor. Ready processes are waiting to have the processor allocated to them by the operating system so that they can run. Process may come into this state after Start state or while running it by but interrupted by the scheduler to assign CPU to some other process.

   * Running - Once the process has been assigned to a processor by the OS scheduler, the process state is set to running and the processor executes its instructions.

   * Waiting - Process moves into the waiting state if it needs to wait for a resource, such as waiting for user input, or waiting for a file to become available.

   * Exit or Terminated - Once the process finishes its execution, or it is terminated by the operating system, it is moved to the terminated state where it waits to be removed from main memory. 

2. What is a Zombie Process? How does it get created? How does it get destroyed?

    * On Unix and Unix-like computer operating systems, a zombie process or defunct process is a process that has completed execution (via the exit system call) but still has an entry in the process table: it is a process in the "Terminated state". This occurs for child processes, where the entry is still needed to allow the parent process to read its child's exit status: once the exit status is read via the wait system call, the zombie's entry is removed from the process table and it is said to be "reaped". A child process always first becomes a zombie before being removed from the resource table. In most cases, under normal system operation zombies are immediately waited on by their parent and then reaped by the system – processes that stay zombies for a long time are generally an error and cause a resource leak.


3. Describe the job of the Scheduler in the OS in general.

    * Long Term Scheduler. It is also called a job scheduler. A long-term scheduler determines which programs are admitted to the system for processing. It selects processes from the queue and loads them into memory for execution. Process loads into the memory for CPU scheduling.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.

    * MLFQ used priority levels to determine which job should run at a given time. High priorities run first and multiple jobs can run at the same time.