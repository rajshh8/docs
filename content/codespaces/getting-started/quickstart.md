#Next Greater Element
#Given an array, print the Next Greater Element (NGE) for every element. The Next greater Element for an element x is the first greater element on the right side of #x in the array. Elements for which no greater element exist, consider the next greater element as -1. 

def solve(A):
    n=len(A)
    maxElement=A[n-1]
    for i in range(n-1,-1,-1):
        if A[i]<maxElement:
            print(f'{A[i]} :: {maxElement}')
            if A[i]>A[i-1]:
                maxElement=A[i]
                
        else:
            print(f'{A[i]} :: {-1}')
            maxElement=A[i]
A=[4,8,7,10,1,0,8]            
solve(A)

#Time Complexity=O(n)
#Space Complexity=O(1)
