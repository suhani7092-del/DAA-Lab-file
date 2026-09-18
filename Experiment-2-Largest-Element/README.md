# Experiment 2: Find the Largest Element in an Array

## Aim

To find the largest element present in a given array.

## Algorithm

1. Start.
2. Read the size `n` of the array.
3. Read all `n` elements.
4. Assume the first element is the largest.
5. Compare each remaining element with the current largest element.
6. If an element is greater, update the largest element.
7. Display the largest element.
8. Stop.

## Program

The following C program finds the largest element in an array.

```c
#include <stdio.h>

int main() {
    int n, i, largest;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter the elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    largest = arr[0];

    for (i = 1; i < n; i++) {
        if (arr[i] > largest) {
            largest = arr[i];
        }
    }

    printf("The largest element is: %d\n", largest);
## Sample Input

```text
Enter the number of elements: 5
Enter the elements:
12 45 7 89 23
The largest element is: 89


    return 0;
}
Time Complexity

O(n)

The program compares each element of the array once.

Space Complexity

O(n)

The array requires space to store n elements.

Result

The largest element in the given array was successfully found and displayed.
