  
import numpy as np  
from sklearn.metrics import pairwise\_distances

def capacitated\_kcenter(X, k, capacity):  
   n \= len(X)  
   centers \= \[np.random.choice(n)\]  
   assignments \= \[\-1\]\*n

   for \_ in range(1, k):  
       dists \= pairwise\_distances(X, X\[centers\]).min(axis\=1)  
       next\_center \= np.argmax(dists)  
       centers.append(next\_center)

   remaining\_capacity \= {c: capacity for c in centers}  
   dmatrix \= pairwise\_distances(X, X\[centers\])

   for i in np.argsort(dmatrix.min(axis\=1)):    
       sorted\_centers \= np.argsort(dmatrix\[i\])  
       for c in sorted\_centers:  
           center\_id \= centers\[c\]  
           if remaining\_capacity\[center\_id\] \> 0:  
               assignments\[i\] \= center\_id  
               remaining\_capacity\[center\_id\] \-= 1  
               break  
   return centers, assignments

This week, I worked on the Capacitated K-Center algorithm, which is about how to deal with constraints on how many points each center can service. I looked into obvious, such as employing binary search on the service radius along with flow or matching checks to make sure capacity is possible. The goal was to make the model more realistic by balancing coverage and load.

I was exploring different algorithms approaches.  
