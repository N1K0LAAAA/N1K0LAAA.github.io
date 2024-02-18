---
author: Nikola
title: Visualizing different sorting algorithms
date: 2024-02-18
description: visualization of diffrent sorting algorithms
toc: true
---

## Introduction
In this Blog I will be writing a few sorting algorithms, visualizing them, and showing the mathematics behind each algorithm.


## Bubble Sort
Bubble Sort is one of the simplest sorting algorithms. It sorts arrays by starting from the left-hand side and comparing each element with the next one. If the second element is bigger than the first one, it switches them otherwise, it leaves them and does not change them. This process continues until the array is sorted.

![image](/media/bubblesort.png)



### Code Example In Rust
```rs
fn main() {
    let  mut sort_array:[i32; 5] = [4, 6, 7, 5, 3];
    for i in 0..sort_array.len() {
        for j in 0 .. sort_array.len()-i-1{
            if sort_array[j] > sort_array[j+1]{
                sort_array.swap(j, j + 1);
            }
        }

        
    }
    print!("{:?}" ,sort_array);
}
```

## Selection Sort
Selection Sort is an algorithm that takes the smallest element in an unsorted array and brings in to the front.It goes through every single on untill its sorted.


![image](/media/selectionsort.png)




### Code Example In Rust
```rs
fn main() {
    let mut sort_array: [i32; 5] = [4, 6, 7, 5, 3];
    
    for i in 0..sort_array.len() {
        let mut min_index = i;
        
        for j in (i+1)..sort_array.len() {
            if sort_array[j] < sort_array[min_index] {
                min_index = j;
            }
        }
        
        if min_index != i {
            sort_array.swap(i, min_index);
        }
    }
    
    println!("{:?}", sort_array);
}
```


## Insertion Sort
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

## Quick Sort
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.


## Randomsort (Theoretically the Fastest One)
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

## Visualization
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

## Side by Side Comparasion
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.


