def binary_search(arr,x):
    low=0
    high=len(arr)-1
    while low<=high:
        mid=(low+high)//2
        if arr[mid]==x:
            return mid
        elif arr[mid]<x:
            low=mid+1
        else:
            high=mid-1
    return -1

numbers=list(map(int,input("Enter sorted numbers: ").split()))
x=int(input("Enter element to search: "))
result=binary_search(numbers,x)
if result!=-1:
    print("Found at position",result)
else:
    print("Not Found")
Output
Enter sorted numbers: 1 3 5 7 9
Enter element to search: 7
Found at position 3
