---
author: Nikola
title: Visualizing different sorting algorithms
date: 2024-02-18
description: visualization of diffrent sorting algorithms
toc: true
---

## Introduction
In this Blog I will showing a few sorting algorithms explaining them and sample code from GeeksForGeeks.I will be also visualizing them by making a Rust Program using OpenGL where you can see a 2d versions of how the diffrent algorithms sort stuff.


## Bubble Sort
Bubble Sort is one of the simplest sorting algorithms. It sorts arrays by starting from the left-hand side and comparing each element with the next one. If the second element is bigger than the first one, it switches them otherwise, it leaves them and does not change them. This process continues until the array is sorted.

![image](/media/bubblesort.png)



### Code Example In Python(Source:Geeksforgeeks.org)
```python
# Optimized Python program for implementation of Bubble Sort
def bubbleSort(arr):
    n = len(arr)
    # Traverse through all array elements
    for i in range(n):
        swapped = False
 
        # Last i elements are already in place
        for j in range(0, n-i-1):
 
            # Traverse the array from 0 to n-i-1
            # Swap if the element found is greater
            # than the next element
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if (swapped == False):
            break
# Driver code to test above
if __name__ == "__main__":
    arr = [64, 34, 25, 12, 22, 11, 90]
 
    bubbleSort(arr)
 
    print("Sorted array:")
    for i in range(len(arr)):
        print("%d" % arr[i], end=" ")
 
# This code is modified by Suraj krushna Yadav
```

## Selection Sort
Selection Sort is an algorithm that takes the smallest element in an unsorted array and brings in to the front.It goes through every single on untill its sorted.


![image](/media/selectionsort.png)




### Code Example In Python(Source:Geeksforgeeks.org)
```python
# Python program for implementation of Selection 
# Sort 
import sys 
A = [64, 25, 12, 22, 11] 
  
# Traverse through all array elements 
for i in range(len(A)): 
      
    # Find the minimum element in remaining  
    # unsorted array 
    min_idx = i 
    for j in range(i+1, len(A)): 
        if A[min_idx] > A[j]: 
            min_idx = j 
              
    # Swap the found minimum element with  
    # the first element         
    A[i], A[min_idx] = A[min_idx], A[i] 
  
# Driver code to test above 
print ("Sorted array") 
for i in range(len(A)): 
    print("%d" %A[i],end=" , ")  
```


## Insertion Sort



### Code Example In Python(Source:Geeksforgeeks.org)
```python

# Python program for implementation of Insertion Sort
 
# Function to do insertion sort
def insertionSort(arr):
 
    # Traverse through 1 to len(arr)
    for i in range(1, len(arr)):
 
        key = arr[i]
 
        # Move elements of arr[0..i-1], that are
        # greater than key, to one position ahead
        # of their current position
        j = i-1
        while j >= 0 and key < arr[j] :
                arr[j + 1] = arr[j]
                j -= 1
        arr[j + 1] = key
 
 
# Driver code to test above
arr = [12, 11, 13, 5, 6]
insertionSort(arr)
for i in range(len(arr)):
    print ("% d" % arr[i])
 
# This code is contributed by Mohit Kumra
```

## Quick Sort


### Code Example In Python(Source:Geeksforgeeks.org)
```python
# Python3 implementation of QuickSort
 
 
# Function to find the partition position
def partition(array, low, high):
 
    # Choose the rightmost element as pivot
    pivot = array[high]
 
    # Pointer for greater element
    i = low - 1
 
    # Traverse through all elements
    # compare each element with pivot
    for j in range(low, high):
        if array[j] <= pivot:
 
            # If element smaller than pivot is found
            # swap it with the greater element pointed by i
            i = i + 1
 
            # Swapping element at i with element at j
            (array[i], array[j]) = (array[j], array[i])
 
    # Swap the pivot element with
    # the greater element specified by i
    (array[i + 1], array[high]) = (array[high], array[i + 1])
 
    # Return the position from where partition is done
    return i + 1
 
 
# Function to perform quicksort
def quicksort(array, low, high):
    if low < high:
 
        # Find pivot element such that
        # element smaller than pivot are on the left
        # element greater than pivot are on the right
        pi = partition(array, low, high)
 
        # Recursive call on the left of pivot
        quicksort(array, low, pi - 1)
 
        # Recursive call on the right of pivot
        quicksort(array, pi + 1, high)
 
 
# Driver code
if __name__ == '__main__':
    array = [10, 7, 8, 9, 1, 5]
    N = len(array)
 
    # Function call
    quicksort(array, 0, N - 1)
    print('Sorted array:')
    for x in array:
        print(x, end=" ")
 
# This code is contributed by Adnan Aliakbar
```

## Bogosort (Theoretically the Fastest One)
Bogosort is a very inefficient algorithm where it tries to sort an array by randomly shufflying the elements.


### Code Example In Python(Source:Geeksforgeeks.org)
```python

import random
  
# Sorts array a[0..n-1] using Bogo sort
def bogoSort(a):
    n = len(a)
    while not sorted(a) == a:
        random.shuffle(a)
  
# Driver code to test above
a = [3, 2, 4, 1, 0, 5]
bogoSort(a)
print("Sorted array:")
for i in range(len(a)):
    print ("%d" %a[i]),
```


## Visualization



## Side by Side Comparasion


