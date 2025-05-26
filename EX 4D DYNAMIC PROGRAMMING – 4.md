# EX 4D DYNAMIC PROGRAMMING – 4
## DATE: 27/03/2025
## AIM:
To find the minimum number of operations to convert str1 to str2 using Naive recursive method.

## Algorithm
1. If one string is empty, return the length of the other string.
2. If the last characters of both strings match, the cost is 0; else, cost is 1.
3. Recursively calculate three options: insert, delete, or replace a character.
4. Take the minimum of the three operations plus the current cost.
5. Final result is the minimum number of edits needed to convert one string into another.    

## Program:

### Program to implement to find the minimum number of operations to convert str1 to str2 using Naive recursive method
### Developed by: GOKULA PRIYA P  
### Register Number: 212222040044
```
def LD(s, t):
    if s=="":
        return len(t)
    if t=="":
        return len(s)
    if s[-1]==t[-1]:
        cost=0
    else:
        cost=1
    res=min([LD(s[:-1],t)+1,
            LD(s,t[:-1])+1, 
            LD(s[:-1],t[:-1])+cost])
    return res
    ######### Add your code here ###########
    
str1=input()
str2=input()
print('Edit Distance',LD(str1,str2))
```
## Output:
![Screenshot 2025-05-24 185957](https://github.com/user-attachments/assets/b182d486-4741-42a0-979e-92a29a63f0d6)

## Result:
Thus the program was executed successfully for finding edit distance between two strings.
