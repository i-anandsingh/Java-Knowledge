# Java-Knowledge

## Final Keyword
Final keyword is a non-access modifier used for classes, attributes & methods, which makes them non-changeable (impossible to inherit/reassign/override).

### Classes 
Classes marked as final cannot be extended (inherited).

### Variables
Variables marked as final connot be reassigned.

### Methods
Methods marked as final cannot be overriden.


## Threading
Allows us to do multiple things at once.
When multiple threads are executed at the same time. Then it is called as multi-threading.

### Multitasking in Java
They are of two type:-
1. Processed-bases multitasking: This type is heavy and requires a lot of time. This is because the program takes a lot of time to switch between differenct processes.

2. Thread-based multitasking: These are light-weight and require short time to switch between the processes.

### Thread life-cycle
A thread always remains in one of the few states.
The thread model consists of various states.

1. New: The model is in the new state when the code is not yet running.
2. Running stage or active stage: This is the state when the program is under execution or in ready to execute stage.
3. Suspended Stage: This is the state when the process is paused (temporarily) due to some reasons.
4. Blocked Stage: This is the state when thread is waiting for some resources. In the blocked state, the thread scheduler clears the queue by rejecting unwanted threads which are present.
5. Terminated Stage: This state stops a thread's execution immediately. A terminated thread means that it is dead and is no longer available for use.

## String, StringBuffer, StringBuilder


## Mutable & Immutable
