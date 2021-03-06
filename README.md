03_Queue_Lab
============

Implement an array-based queue in C++

Requirements
------------

1. remove takes O(1) time
2. add takes O(1) time, unless it calls grow (in that case O(n) is okay)
3. grow is only called if the number of items == backingArraySize, and the size of the array is doubled during grow
4. grow takes O(n) time
5. Do not leak memory (make sure grow and the destructor do the right thing)
6. getNumItems is O(1) time
7. add and remove throw excpetions as appropriate
8. You must use the array in a circular fashion. If you don't do this you probably won't be able to get #1, #2 and #3 to all be true.

Reading
=======
"Open Data Structures," Chapter 2, up through section 2.4 (ArrayDequeue). http://opendatastructures.org/ods-cpp/2_Array_Based_Lists.html

Questions
=========

#### 1. Which of the above requirements work, and which do not? For each requirement, write a brief response.

1. remove() takes O(1) time.
2. add() takes O(1) time, unless it calls grow, then it will be O(n). 
3. NOT WORKING
4. NOT WORKING
5. All the memories have been allocated properly.
6. getNumItems is O(1) time.
7. add and remove throw exceptions as appropriate.
8. I have a circular array implemented. 

#### 2. If we did a Stack instead of a Queue, which of the private methods and variables would we need to keep, and which could we get rid of? Explain your answer.

#### 3. What is one question that confused you about this excercise, or one piece of advice you would share with students next semester?
NO idea how to implement grow().
#### 4. In Java you might write "class ArrayQueue extends Queue" ... how do you write the same thing in C++?
ArrayQueue::Queue
#### 5. What is the purpose of "templates" in C++?
To make code reusable.
#### 6. What would the syntax be for dynamically allocating an array of 10 ints, in C++?
Delete[] a; // a is the pointer to memory address where 10 ints are stored
#### 7. What is the purpose of a class destructor in C++? Why don't you need them in Java?
The purpose of having a class destructor in c++ is to deallocate dynamic memory. The reason I don't need them is Java has garbage collector, so it automatically deallocates the memory where no pointer points
