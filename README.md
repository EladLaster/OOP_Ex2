# Object_Oriented_Programming_2

*presenters:*

            elad laster 208968636

            david stern 315556308
            
*subject:*
          
            1)In the first part we will create several text files, and count the number of lines created in several different ways:
              normal method without the use of threads,method using threads and method using threadpool.
             
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

## Uml

### *part1 uml:*

![WhatsApp Image 2023-01-12 at 15 53 15](https://user-images.githubusercontent.com/118683420/212110815-09c3f479-e9ec-4db7-81f3-90782745d62d.jpeg)

### *part2 uml:*

![WhatsApp Image 2023-01-12 at 15 51 27](https://user-images.githubusercontent.com/118683420/212110544-3fc26566-0fce-4c10-b54e-3507ac94aa75.jpeg)

## RunTimes

We want to see that runtimes differ from method to method, and we want to understand which method is more efficient in terms of runtime
We can see that by running the ex2 program, it follows that working with Thrades and ThradePool is indeed faster than working without Thrades. This shows that indeed the calculation of lines of text in parallel is better than regular counting. This is obvious because counting rows performed all at once by several objects is faster than counting the lines one at a time.
You can also see that working with ThradePool is faster than working with Thrades, because when you create a Thradepool, he already produces a large number of Thrades himself that will be ready to receive tasks, instead of creating Thrades only when the task arrives.

In the following picture we can see the correctness of the claim by create a 5000 files.

![2023-01-12 (5)](https://user-images.githubusercontent.com/118683420/212140507-0337ede9-b666-46b3-a01c-c4f3982456e0.png)
![2023-01-12 (4)](https://user-images.githubusercontent.com/118683420/212140383-3dce131b-f0c0-46ae-8202-d8daabcca826.png)




## Adapter design pattern

the adapter pattern is a software design pattern that allows the interface of an existing class to be used as another interface.
It is often used to make existing classes work with others without modifying their source code.

Whenever we want to link an object to a task and there is no real connection between it and the object, we want to build an adapter that will cause an indirect connection between the object and the task that will pass through it. 
The correlation will make it possible to do this by inserting the values of the given object and adjusting them to the given task.


## Classes part1


### *Ex2:*
The main class in which we call the file creation function and the file line count function.
running it will show us the total number of lines in the files by one of the method that we defined, and the running times of each method.

### *Ex2_1:*
The class in which we build the function with which we create new files with a random number of lines.
We will also build in it the functions with which we count the total number of lines of the built files - this in one of the 3 ways we have defined:
normal method without the use of threads,method using threads and method using threadpool.

- _createTextFiles()_

- _getNumOfLines()_

- _getNumOfLinesThreads()_

- _getNumOfLinesThreadPool()_


### *Thread_Ex2:*

The class where we create a Thrade that has a name and a counter.
In this class we implement the run() function of the Thrade which in the future we will use to count the lines of the files.
The function getCounter() will return the number of lines that the specific Thrade found.

- _Thread_ex2()_

- _getCounter()_

- _run()_


### *ThreadP_Ex2:*

The class where we create a ThradePool that has a name and a counter.
In this class we implement the coll() function of the ThradePool which in the future we will use to count the lines of the files.
The call() function will itself send the number of lines that the ThreadePool found.

- _ThreadP_ex2()_

- _call()_

## Classes part2


### *Adapter:*

In this class we will use an Adapter() that will help us transfer the tasks with a call() function to the tasks with a run() function,
this is because later we will want to put them in a priority queue that only accepts tasks that implement a run() function.
We will also add a compareTo() function with which the priority queue will compare the tasks.

- _Adapter()_

- _compareTo()_


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

In this class, we will check the functions of the "Ex_1".
In the "createTextFiles" function, We would like to see that the number of files we asked a function to build has indeed been created.
In the "getNumOfLines" function, We would like to see that the number of rows in the created files does indeed match the number of rows that the function spends (normal method without the use of threads).
In the "getNumOfLinesThreads" function, We would like to see that the number of rows in the created files does indeed match the number of rows that the function spends (method using threads).
In the "getNumOfLinesThreadPool" function, We would like to see that the number of rows in the created files does indeed match the number of rows that the function spends (method using threadpool).

### *part2 test:*

In this class, we will check the functions of all the file we created.
We will introduce new "Tasks" that we have built into the new "CustomExecutor" that we have created, we will check that the results of the tasks are correct and that the "CustomeExecutor" perform the tasks according to the priority - from high to low.


