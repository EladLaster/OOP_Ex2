# Object_Oriented_Programming_2

*presenters:*

            elad laster 208968636

            david stern 315556308
            
*subject:*
          
            1)In the first part we will create several text files, and count the number of lines created in several different ways:
              normal method without the use of threads,method using threads, and and method using threadpool.
             
            2)In the second part we will create a new "Task" type that consists of an asynchronous operation and priority,
              and in addition we will also create a new  "ThreadPool" type that will prioritize the type of new tasks we built 
              - according to their priority.
            
## Get start 
1) Clone the repository:

                        git clone https://github.com/EladLaster/OOP_Ex2.git   
                                               
2) Open in any Java IDE.
 
3) In part 1: Create a number of new text files with a random number of lines and get the total number of lines of the texts
            by one of four existing methods/functions present in the class.

   In part 2: Bulid a new CustomExecutor and a new task with/without priority, send the task to the new CustomExecutor , submit the task         
           u create in the CustomExecutor and get the result of the task you sent to the program by considering the priority of the task.

4) Enjoy!!!


## Adapter design pattern
the adapter pattern is a software design pattern that allows the interface of an existing class to be used as another interface.
It is often used to make existing classes work with others without modifying their source code.




## Classes part1


### *Ex2:*


### *Ex2_1:*

- _createTextFiles()_- 

- _getNumOfLines()_- 

- _getNumOfLinesThreads()_- 

- _getNumOfLinesThreadPool()_-


### *Thread_Ex2:*

- _run()_ -


### *ThreadP_Ex2:*

- _call()_ -

## Classes part2


### *Adapter:*

- _Adapter()_ -

- _compareTo()_ -


### *CustomExecutor:*

- _CustomExecutor()_ -

- _exe()_ -

- _submit()_ - 2 func

- _getCurrentMax()_ -

- _gracefullyTerminate()_ -

### *Task:*

- _createTask()_ - 2 func

- _get_priority()_ -

- _call()_ -

- _compareTo()_ -

### *TaskType:*


## Tests

### *part1 test:*

### *part2 test:*


## Uml

### *part1 uml:*

### *part2 uml:*
