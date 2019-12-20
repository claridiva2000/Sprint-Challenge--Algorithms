# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n         #O(n)

      O(n)
```


```
b)  sum = 0
    for i in range(n): #o(n)
      j = 1
      while j < n:    #O(n)
        j *= 2
        sum += 1   #O(n)

        O(n**3)
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:   #O(1)
        return 0

      return 2 + bunnyEars(bunnies-1) #O(n)
     
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

start in the middle floor and drop the egg. if it breaks then we don't have to test any of the higher floors and can just test the lower half of the floors.
go to the halfway point of the lower floors. if it doesn't break, go the halfway point of the remaining above floors. repeat until we find the second breaking egg.


This is my attempt at an O(logn) solution:


def eggdrop(n):
  starting_floor = n//2
  cur_floor = starting_floor
  broken = False
  eggcount= 0
  
    drop_egg()
    eggcount +=1
    if broken = False:
       eggdrop(len(n-cur_floor))
    elif:
      broken == True:
      return cur_floor

but just incase that doesns't work here's linear O(n) assuming an egg dropped from the roof is guaranteed to break we go down one floor until the eggs no longer break when dropped:

def eggdrop(n)
starting floor = n
cur_floor = starting floor-1
eggcount = 1
broken = true

While (broken == false AND eggcount <=n):
    drop egg from cur_floor
    if egg breaks:
        eggcount+=1
        cur_floor -= 1
    elif broken == False:
        return f' the egg is safe at {cur_floor} and below. {eggcount} eggs have been sacrificed in the pursuit of knowlege'
        

