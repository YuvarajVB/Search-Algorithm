# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Yuvaraj.V
RegisterNumber: 23013769
'''
def linearsearch(array,n,k):
    ans =-1
    for i in range(0,n):
        if(array[i]==k):
            ans =  i
            break
    return ans
array=eval(input())
k=eval(input())
n=len(array)
array.sort()
result=linearsearch(array,n,k)
if(result==-1):
    print(array,"\nElement not found")
else:
    print(array,"\nElement found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Yuvaraj.V
RegisterNumber: 23013769
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
           return mid
        elif array[mid]<k:
           low=mid+1
        else:
           high=mid-1
    return -1
    
array = eval(input())
# sort the array
k = eval(input()) #k-item to be searched
array.sort()
low=0
high=len(array)-1
# use the binary search function to find the item in the list
result=binarySearchIter(array,k,low,high)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", resul
if result==-1:
    print(array,"\nElement not found")
else:
    print(array,"\nElement found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: your name: Yuvaraj.V
RegisterNumber: 23013769
'''
def BinarySearch(arr, k, low, high):
    
    if(low<=high):
        mid = (low + high)//2
        
        if(arr[mid]==k):
            return mid
        elif(arr[mid]<k):
            return BinarySearch(arr, k, mid+1, high)
        else:
            return BinarySearch(arr, k, low, mid-1)
            
    else:
        return -1

    
arr = eval(input())
arr.sort()
print(arr)
k = eval(input()) 

ans = BinarySearch(arr, k, 0, len(arr)-1)

if(ans!=-1):
    print("Element found at index: ",ans)
else:
    print("Element not found")
```
## Sample Input and Output
i)Use a linear search method to match the item in a list.
![Screenshot 2023-12-24 144713](https://github.com/YuvarajVB/Search-Algorithm/assets/151488375/da936157-8246-406d-9a6c-03109cbb97b8)
ii)Find the element in a list using Binary Search(Iterative Method)
![Screenshot 2023-12-24 144814](https://github.com/YuvarajVB/Search-Algorithm/assets/151488375/836e5459-34c9-42d7-b86c-5edab8ab5136)
iii)Find the element in a list using Binary Search (recursive Method).
![Screenshot 2023-12-24 144903](https://github.com/YuvarajVB/Search-Algorithm/assets/151488375/3901bc7a-cd86-42fb-9116-4bf2a92d6c8d)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
