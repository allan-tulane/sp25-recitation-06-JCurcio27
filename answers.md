# CMPS 2200 Recitation 06
## Answers

**Name:** Jaedan Curcio


Place all written answers from `recitation-07.md` here for easier grading.



- **2)** A recurrence for the work of this algorithm is W(n) = W(n-1) + W(n-2) + O(1). Expanding this, 
you get W(n) = W(n-1) + W(n-2) = W(n-2) + W(n-3) + W(n-3) + W(n-4), and so forth. This means that the total number
of problems at each level grows exponentially, and since the recurrence is leaf dominant since the work done
at each level is O(1), the total work is O(2^n).


- **3)** Since the second recursive call is dependent on the first, the recurrence above can be simplified to
S(n) = S(n-1) + O(1) for the span of the algorithm. S(n-1) = S(n-2) + 1, so S(n) = S(n-2) + 2. This gets the pattern
S(n) = S(n-k) + k, where K is the depth of the tree. At S(0) (base case), k = n, so you get S(n) = S(0) + n. Assuming
S(0) is O(1), this means that the total span is O(n).


- **4)** The pattern that appears when observing counts is that the number of times each fibonacci number is
calculated is the inverse of the fibonacci sequence (with the exception of the first number).


- **6)** For fib_top_down, the maximum amount of times any number will be called is 1, as if the number has already been 
calculated, it simply returns the stored value. This tells you that the work and span are both O(n), since
the total amount of work done is equal to the size of the list, and each calculation is dependent on the one before it.


- **8)** The maximum amount of times any number will be read is two. The work of the algorithm is O(n), as 
it is simply iterating through the list, and the total work depends on the size of the list. Since each calculation
of the fibonacci number is dependent on the one before it, the span is also O(n).
