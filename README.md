# CQ7-CSCI160-01

Recursive definition for Ice Cream Parlor problem:

icecreamParlor(m, A, i, j, result) = 
{ return result                                 if i=n
  
  icecreamParlor(m, A, i+1, i+2, result)        if j >= n

  icecreamParlor(m, A, i, j+1, result+1)        if A[i] + A[j] = m

  icecreamParlor(m, A, i, j+1, result)          otherwise

  }

The base case is if i reaches the end of A, meaning there are no more ice cream flavors left to look through.

j >= n checks if j has reached the end of the ice cream flavors. The recursive call increments i and changes j to the next number after the new i, so we don't count flavor combinations twice.

A[i] + A[j} = m checks if a flavor combination is exactly the target price. The recursive call increments result and j to continue comparing.

The final recursive call increments j to continue comparing as normal.


Running Time of Algorithms runtime and space complexity analysis:

The runtime is O(n^2) where n = the length of arr, since there are two loops which in the worst case scenario run n times.
The space complexity is O(n), since it maintains a list of size n and a integer throughout the algorithm and O(n) is the dominant term.                                      
