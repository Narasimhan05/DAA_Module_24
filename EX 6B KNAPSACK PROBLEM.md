# EX 6B KNAPSACK PROBLEM
## DATE:
## AIM:
To Create a python program for 0/1 knapsack problem using naive recursion method

## Algorithm
1. Base Case: If no items or no capacity, return 0 value.
2. Exclusion: If the current item's weight exceeds capacity, exclude it and consider the remaining items.
3. Inclusion: Recursively calculate value by including the current item (subtract its weight, add its value).
4. Exclusion (Alternative): Recursively calculate value by excluding the current item.
5. Return Max: Choose the maximum value obtained from either including or excluding the current item.   

## Program:
### Developed by: NARASIMHAN S  
### Register Number: 212223230133 

```python
def knapSack(W, wt, val, n):
     if n==0 or W==0:
         return 0
     if wt[n-1]>W:
         return knapSack(W, wt, val, n-1)
     return max(val[n-1]+knapSack(W-wt[n-1], wt, val, n-1),knapSack(W, wt, val, n-1))

x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))
n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
```

## Output:

![image](https://github.com/user-attachments/assets/32fd545c-f162-4a37-a3cc-c2104c0b6701)

## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
