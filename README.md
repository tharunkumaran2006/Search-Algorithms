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
### i) Use a linear search method to match the item in a list.
```
lst=eval(input())
n=int(input())
lst.sort()
print(lst)
for i in range(len(lst)):
    if(lst[i]==n):
        print("Element found at index: ",i)
        break
else:
    print("Element not found")
//Developed By: Tharun V K
//Register Number: 212223230231

```
### ii) Find the element in a list using Binary Search(Iterative Method).
```
def binary(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    else:
        return -1
array = eval(input())
array.sort()
k = eval(input()) 
print(array)
res=binary(array,k,0,len(array)-1)
if res==-1:
    print("Element not found")
else:
    print("Element found at index: ",res)
//Developed By: Tharun V K
//Register Number: 212223230231
```
### iii) Find the element in a list using Binary Search (recursive Method).
```
def binary(array, k, low, high):
    if low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
            return binary(array, k, low, high)
        else:
            high=mid-1
            return binary(array, k, low, high)
    else:
        return -1
array = eval(input())
array.sort()
k = eval(input()) 
print(array)
res=binary(array,k,0,len(array)-1)
if res==-1:
    print("Element not found")
else:
    print("Element found at index: ",res)
//Developed By: Tharun V K
//Register Number: 212223230231
```
## Sample Input and Output
### i) Use a linear search method to match the item in a list.
![alt text](<Screenshot 2024-04-13 214459.png>)
### ii) Find the element in a list using Binary Search(Iterative Method).
![alt text](<Screenshot 2024-04-13 214516.png>)
### iii) Find the element in a list using Binary Search (recursive Method).
![alt text](<Screenshot 2024-04-13 214532.png>)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
