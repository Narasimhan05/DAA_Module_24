# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE:
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)

## Algorithm
1. Generate all possible permutations of visiting cities, excluding the starting city.
2. For each permutation, calculate the total distance of the tour, starting and ending at the designated city.
3. Keep track of the minimum tour distance found so far.
4. Update the minimum distance if a shorter tour is discovered.
5. Return the overall minimum tour distance after checking all permutations.  

## Program:
### Developed by: NARASIMHAN S 
### Register Number: 212223230133 

```python
from sys import maxsize
from itertools import permutations
V = 4
 
def travellingSalesmanProblem(graph, s):
    v=[]
    for i in range(V):
        if i!=s:
            v.append(i)
    np=permutations(v)
    mp=maxsize
    for i in np:
        k=s
        cp=0
        for j in i:
            cp+=graph[k][j]
            k=j
        cp+=graph[k][s]
        mp=min(mp,cp)
    return mp

if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))
```
## Output:

![image](https://github.com/user-attachments/assets/e367d255-bd26-4e54-b8df-6d2ec4f05e16)

## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
