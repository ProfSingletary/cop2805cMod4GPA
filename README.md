# cop2805cMod3GPA
# COP2805C Module 3 Graded Programming Assignment

Write a multi-threaded Java program named "EchoMachine" which prompts the user for a sentence, a time increment in seconds, and a number of repetitions. The program should split the sentence into separate words and spawn one thread for each word which echoes the word, sleeps for the specified time increment in seconds, and repeats the process for the specified number of repetitions. Use a "join" statement in your main method which joins each thread to verify they have exited before exiting your main method.

Hints:

- The "split" method in the String class will split a sentence into an array of Strings consisting of the words.
- For example, given String s = "This is a test"; calling s.split("\\s") will return an array of Strings containing "This", "is", "a", "test".
- Define a class which extends the Thread class so you can store the word associated with that thread.
- Define a member variable in that class which stores a single word, which can be passed via the constructor.
- Override the run method in your extended class to perform the echo/delay/repeat operations.
- The constructor for your subclass starts the thread
- Store the instantiated thread objects (your extended class) in an array of Threads in your main method.
- You can call join() on the elements of this array using a for loop.
- Remember that Thread.sleep works in milliseconds, and that you must catch or throw InterruptedException in order to use Thread.sleep().
- A static helper method which sleeps with the necessary try/catch can save some code lines

Submit a single .java file with both classes (do not declare your extended class as public and you can include it in the same file).

Sample output:

       Enter a sentence: Welcome to Wally World!
       Enter a time increment in seconds: 2   <<== user input
       Enter a number of repetitions:  3 <<== user input
       Welcome
       Wally
       World!
       to
       Wally
       to
       Welcome
       World!
       Wally
       World!
       to
       Welcome
       to thread is exiting!
       World! thread is exiting!
       Welcome thread is exiting!
       Wally thread is exiting!
       thread[0] joined
       thread[1] joined
       thread[2] joined
       thread[3] joined
       main thread is exiting!
