# ROUND1-HASH

```
NAME: VIJAY KUMAR V R                
COLLEGE NAME: SAVEETHA ENGINEERING COLLEGE 
DEPARTMENT: B.E(CSE) 
```
# First Challenge for Hash Agile Internship/Freshers Drive 

# ROUND 1: Problem statement: 

 ```
Find the Majority Element in an Array 

Write a program to find the majority element in an array (an element that appears more than n/2 times). 

For example, in the array [3, 3, 4, 2, 4, 4, 2, 4, 4], the output should be 4. Do not use any 

built-in functions for array manipulation or counting. 

Instructions: Implement a manual count and comparison logic to find the majority element. 
```
## PROGRAM:
C program: 
```
#include <stdio.h>


int findCandidate(int arr[], int size) {
    int candidate = arr[0];
    int count = 1;


    for (int i = 1; i < size; i++) {
        if (arr[i] == candidate) {
            count++;
        } else {
            count--;
        }


        if (count == 0) {
            candidate = arr[i];
            count = 1;
        }
    }
    return candidate;
}


int isMajority(int arr[], int size, int candidate) {
    int count = 0;


    for (int i = 0; i < size; i++) {
        if (arr[i] == candidate) {
            count++;
        }
    }


    return (count > size / 2);
}


void findMajorityElement(int arr[], int size) {
    int candidate = findCandidate(arr, size);

    if (isMajority(arr, size, candidate)) {
        printf("The majority element is: %d\n", candidate);
    } else {
        printf("No majority element found.\n");
    }
}


int main() {
    // Test cases
    int arr1[] = {3, 3, 4, 2, 4, 4, 2, 4, 4};
    int arr2[] = {1, 1, 2, 1, 3, 5, 1};
    int arr3[] = {6, 6, 7, 8, 6, 6, 6};

    int size1 = sizeof(arr1) / sizeof(arr1[0]);
    int size2 = sizeof(arr2) / sizeof(arr2[0]);
    int size3 = sizeof(arr3) / sizeof(arr3[0]);


    printf("For the first array:\n");
    findMajorityElement(arr1, size1);

    printf("\nFor the second array:\n");
    findMajorityElement(arr2, size2);

    printf("\nFor the third array:\n");
    findMajorityElement(arr3, size3);

    return 0;
}

```
 ## OUTPUT:

![HASH](https://github.com/user-attachments/assets/e1fb4742-20eb-40d4-82cc-b91b0f0943c7)


# RESULT :

Thus the program for majority element of array for given inputs was successfully executed. 


