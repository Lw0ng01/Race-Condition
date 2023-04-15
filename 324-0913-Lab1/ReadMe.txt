Process Communication Issue

1. The program is returning incorrect values due to the fact that the program would not register the child process total, and only return the parent total.

2. The issue was fixed as before the program was running on 2 different processes, one for the child and one for the parent. During the process, it would compute the child but not register it, only returning the parent total. With the fixed program, upon exit it now totals both the child and the parents processes to output and accurate result.

3. The program starts to return faulty values at n = 26. This is because the exit function returns only one-byte integers, so for n >= 26 function B(x) would produce results greater than 255 which is the maximum size of a one-byte integer.

4. After swapping the parent and child function, the program now goes until n = 45. This is a similar case for Q3, as it computes until 253, the next step for n = 46 would return a value greater than 255 forcing the program to exit.


Race-Condition Issue

1. The reason that the value stored in the file is never over 15000 is because all 3 child processes are trying to modify the value in the file at once, and when the program is unable to do so it defaults to its orignal process.

2. The lower bound value n would be 5000. This is because the worst case execution scenario is that only 1 child or none of the children process goes through, leaving the parent process to default to the original value of 5000.

3. Used wait function to create breaks inbetween child processes in order to return 15000 in eXer_2.c

