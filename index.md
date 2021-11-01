## A Collatz Program in Python

This [program](https://github.com/FuzzyBunnys/A-Different-Orbit-Counting-Program/blob/main/Collatz%20Simulation) sorts odd numbers based on how they behave in the Collatz function. In particular it counts how many times a number moves through the 3n+1 step of the Collatz function. In writing this program, I was hoping to find a generalizable rule that would let me attack the problem of proving the conjecture from a different tack. I didn't find a solution, but there are lots of very interesting patterns. 

### One Step
Patterns that collapse after a single step through the 3n+1 portion of the Collatz function are very pleasing. In binary they have the form of alternating ones and zeroes, ie: 10101...
In decimal notation these are numbers like 5, 21, 85..., and are sequence [A002450](http://oeis.org/A002450) in the online encyclopedia of integer sequences. Broadly, they are numbers that turn into a power of 2 after being multiplied by 3 and having 1 added to them.

### Two Step
Patterns that collapse after a second step through the 3n+1 part of the function also have an apparent pattern although it is not as simple as the one step pattern. I have not investigated it as deeply as I would like, but the pattern 111000111.... turns into 1010101... after being multiplied by 3 and adding 1. So the lowest place value of this class of number is of the pattern 10101... and it is concatenated with higher place value digits in the 111000111 pattern. There are some details about how to add these together that preclude certain combinations but overall that is the general idea. 

### Non Adjacent Format
In addition to calculating and grouping based on the number of steps they take through the Collatz function, this program also calculates a representation of the number in question known as the Non-Adjacent Format (NAF), it is sometimes also called the balanced binary representation. The following [blog post](https://phlay.de/post/non-adjacent-form/) by Phillip Lay was a huge help in understanding the number format and implementing the necessary code. I was hoping that given the pattern apparent in numbers that collapse after one step through the Collatz function, I might be able to see more patterns using the NAF. I did not have much luck with that idea. 
