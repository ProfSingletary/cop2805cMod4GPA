# cop2805cMod4GPA

A queue is an abstract data type similar to the stack we discuss in the lecture slides, but it is a FIFO (first-in, first-out) structure as compared to the stack, which is LIFO (last-in, first-out). Think of it as waiting in line for a movie ticket (the British word for line is "queue"). As the line grows, the first person in the line is "removed" to buy a ticket, while the end of the line continues to grow. So the first person in line is the first person to leave, the second in line is second to leave, and so on.

Modify the GenericStack class provided in this modules's lecture source code (GenericStack.java) to implement a generic queue. You may use the original source file and just make necessary changes (including the class names). The push and pop methods will need to be changed to enque (adds an element to the end of the queue) and deque (removes an element from the front of the queue). You can retain the getSize, peek, isEmpty, and toString methods from the GenericStack class; some of them will need to be tweaked, some can be used as is.

Change the "TestGenericStack" class in that file to  "TestGenericQueue" ; here is the main method to use in your TestGenericQueue class which will test your GenericQueue class:

    public static void main(String[] args)
    {
        GenericQueue queue1 = new GenericQueue<>();
        queue1.enque("London");
        queue1.enque("Paris");
        queue1.enque("Berlin");
        log(queue1);
        log(queue1.deque());
        log(queue1.deque());
        log(queue1.deque());
       
        GenericQueue queue2 = new GenericQueue<>();
        queue2.enque(1);
        queue2.enque(2);
        queue2.enque(3);
        log(queue2);
        log(queue2.deque());
        log(queue2.deque());
        log(queue2.deque());     
    }

Expected Output -- note that elements are removed in the same order as they are inserted (FIFO), compared to the TestGenericStack program output which removes them in reverse order (LIFO):

queue: [London, Paris, Berlin]
London
Paris
Berlin
queue: [1, 2, 3]
1
2
3
