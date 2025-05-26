# EX 4B DYNAMIC PROGRAMMING – 2
## DATE: 26/03/2025
## AIM:
To find the longest string (or strings) that is a substring (or are substrings) of two strings..

## Algorithm
1. Create a table lookup to store lengths of matching characters.
2. Compare each character of X with each character of Y.
3. If characters match, update the lookup value and track the maximum length and ending position.
4. After filling the table, the longest common substring is found at the tracked position. 
5. Extract and print the substring from X using the recorded indices.  

## Program:

### Program to implement the longest common substring problem
### Developed by: GOKULA PRIYA P 
### Register Number: 212222040044

```
def fun(x,y,m,n):
    lcs=[[0]*(n+1) for i in range(m+1)]
    result=0
    endresult=0
    for i in range(1,m+1):
        for j in range(1,n+1):
            if x[i-1]==y[j-1]:
                lcs[i][j]=1+lcs[i-1][j-1]
                if(lcs[i][j]>result):
                    result=lcs[i][j]
                    endresult=i
            
    return x[endresult-result:endresult]
x=input()
y=input()
m=len(x)
n=len(y)
print("The longest common substring is",fun(x, y, len(x), len(y)))
```
## Output:
![Screenshot 2025-05-24 185118](https://github.com/user-attachments/assets/7e8f9202-778a-4a37-a983-7a96e9054bfe)

## Result:
Thus the program was executed successfully for finding the longest common substring .
