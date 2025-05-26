# EX 4C DYNAMIC PROGRAMMING – 3
## DATE: 26/03/2025
## AIM:
Given a sequence, find the length of the longest palindromic subsequence in it.

## Algorithm
1. Take the input string and reverse it.
2. Compare both strings using dynamic programming to find matching characters.
3. If characters match, increase the length by 1 and move diagonally.
4. If not matching, move in the direction where maximum length is found (left or up). 
5. Final answer is the length of the longest palindromic subsequence.  

## Program:

### Program to implement to find the length of the longest palindromic subsequence in it
### Developed by: GOKULA PRIYA P 
### Register Number: 212222040044
```
def fun(x):
    m=len(x)
    y=x[::-1]
    n=len(y)
    matrix=[[0]*(n+1) for i in range(m+1)]
    for i in range(m+1):
        for j in range(n+1):
            if i==0 or j==0:
                matrix[i][j]=0
            elif x[i-1]==y[j-1]:
                matrix[i][j]=1+matrix[i-1][j-1]
            else:
                matrix[i][j]=max(matrix[i-1][j],matrix[i][j-1])
    return matrix[-1][-1]
x=input()
print("The length of the LPS is",fun(x))
```
## Output:
![Screenshot 2025-05-24 185649](https://github.com/user-attachments/assets/a128df84-8ea4-491f-b415-c060ba7d29b9)

## Result:
Thus the program was executed successfully for finding the length of longest palindromic string.
