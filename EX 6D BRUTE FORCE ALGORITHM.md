# EX 6D BRUTE FORCE ALGORITHM
## DATE:
## AIM:
To create a python program to find the maximum value in linear search.

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
def find_maximum(lst):
    maxi=lst[0]
    for i in lst:
        if i>maxi:
            maxi=i
    return maxi

test_scores = []
n=int(input())
for i in range(n):
    test_scores.append(int(input()))
print("Maximum value is ",find_maximum(test_scores))
```
## Output:

![image](https://github.com/user-attachments/assets/3bc3c988-1037-4103-98b2-ea35fbd82a4d)

## Result:
Thus the above program was executed successfully to find the maximum value in linear search.
