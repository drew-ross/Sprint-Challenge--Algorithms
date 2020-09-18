#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
O(n). For this function, a is changed while less than n^3, but a increases by n^2 each loop. This means that the loop will run for n operations before ending.

b)
O(nlogn). The outer loop has O(n) runtime, and the inner loop has O(logn) runtime because j doubles each loop, causing j to catch up to n at an exponential rate.

c)
O(n) where n = bunnies. This function recursively calls itself with n-1 until n == 0, and the rest of the function is O(1).

## Exercise II

If I wanted to find the exact floor f where an egg wouldn't break if dropped, I would start at the middle floor, n // 2.
If the egg breaks, I would have to go lower, so I would go to the middle of the remaining floors below me, and drop another egg. If the egg didn't break, I would go higher.

This problem works like a binary search algorithm:

building has n floors
start at floor n // 2
while I don't know f:
  drop egg
  if breaks:
    go to the lower middle of remaining floors
  if doesn't break:
    go to the higher middle of remaining floors
  The very last floor I visit will either be f or f-1 depending
  on whether the egg breaks

The runtime will be O(logn)

