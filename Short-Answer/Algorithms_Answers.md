#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)  O(n)


b)O(n**3)


c)O(n)

## Exercise II

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
broken = True

While (broken == false AND eggcount <=n):
    drop egg from cur_floor
    if egg breaks:
        eggcount+=1
        cur_floor -= 1
    elif broken == False:
        return f' the egg is safe at {cur_floor} and below. {eggcount} eggs have been sacrificed in the pursuit of knowlege'
        


