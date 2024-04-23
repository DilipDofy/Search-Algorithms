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
```python
''' program to search the item in a list one by one from start to end to find the match
Developed by: DILIP MP
RegisterNumber: 212223230048
'''

def search(array,key,n):
    for i in range(0,n):
        if key==array[i]:
            return i
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
'''program to find the element in a list using Binary Search (Iterative Method).
Developed by: DILIP MP
RegisterNumber: 212223230048
'''

def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low= mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)


```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
'''program to find the element in a list using Binary Search (recursive Method).
Developed by: DILIP MP
RegisterNumber: 212223230048
'''

def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
## Sample Input and Output
### Use a linear search method to match the item in a list.
![Screenshot 2024-04-23 111138](https://github.com/DilipDofy/Search-Algorithms/assets/147223497/1a2c338e-d045-494d-8485-40e0a8c2310e)

### Find the element in a list using Binary Search(Iterative Method).
![Screenshot 2024-04-23 111228](https://github.com/DilipDofy/Search-Algorithms/assets/147223497/8609a399-d373-4944-9935-eb35d657bf79)

### Find the element in a list using Binary Search (recursive Method).
![Screenshot 2024-04-23 111311](https://github.com/DilipDofy/Search-Algorithms/assets/147223497/b6dbe79a-5f84-4848-93fb-f31db7f4701f)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
