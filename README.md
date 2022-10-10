# python-queues
python queues



## Using a list

````
customers = []
customers.append((2, "Harry")) #no sort needed here because 1 item. 
customers.append((3, "Charles"))
customers.sort(reverse=True) 
#Need to sort to maintain order
customers.append((1, "Riya"))
customers.sort(reverse=True) 
#Need to sort to maintain order
customers.append((4, "Stacy"))
customers.sort(reverse=True)
while customers:
     print(customers.pop(0))
     
#Will print names in the order: Stacy, Charles, Harry, Riya. 
````


## Using heapq
````
import heapq
customers = []
heapq.heappush(customers, (2, "Harry"))
heapq.heappush(customers, (3, "Charles"))
heapq.heappush(customers, (1, "Riya"))
heapq.heappush(customers, (4, "Stacy"))
while customers:
     print(heapq.heappop(q))
     
#Will print names in the order: Riya, Harry, Charles, Stacy.
````

## Using queue.PriorityQueue

````
from queue import PriorityQueue
customers = PriorityQueue() #we initialise the PQ class instead of using a function to operate upon a list. 
customers.put((2, "Harry"))
customers.put((3, "Charles"))
customers.put((1, "Riya"))
customers.put((4, "Stacy"))
while customers:
     print(customers.get())
     
#Will print names in the order: Riya, Harry, Charles, Stacy.
````




