# promises_assignment


Description:
This a Nodejs function that process N number of task concurrently, until the tasklist is exhausted.
MORE_INFO
it means that suppose if there are 100 task in the task list and at a time only 10 task should be processed so the function will process first 10 task and if any task in these selected task is performed then the function should performed 11th task without waiting for all the task to end and then do next 10 task

LOGIC USE:
first there is async function init in this function we generates a task list arrayvof number of tasks we assign ,and each task has a random name consisting of lowercase letters.This  function initializes variables (counter,cocurrencyCurrent,concurrencyMax,numberOfTask, generates a task list, and logs relevant information to the console. It then calls an asynchoronous function name  manageConcurrency with the task list and other parameters.
In doTask function it takes the task as a parameter and creates a promise that represents the execution of a task. It uses a random delay to simulate the task execution time and logs the task's completion message to the console.
manageConcurrency:
this is a async function which takes the  four parameters taskList (array of tasks to execute), counter (current index of the task being executed), concurrencyMax (maximum number of tasks that can be executed concurrently), and concurrencyCurrent (current number of tasks being executed concurrently). In this function first there is a loop that checks rather our tasklist is exhausted it checks if the counter (task num)  is less that the length of taskList array. if it is then we move to another while loop that checks the concurrencyCurrent is less that MaxCurrency and the counter is less that length of Task list then we call doTask on the task  and plus one in currentCurrency indicating that a task has started executing. Information about the current concurrency and task count is logged to the console. 
if the  task is perform the promise is accepted/fullfilled  we use .then()and then minus the cocurrency number. and the loop ends  outside the loop 
the function awaits a promise that resolves after a short delay using setTimeout( in our case we are waiting till a promise is resolve)


