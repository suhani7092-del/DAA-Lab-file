# Experiment 4: Write a Program to Reverse an Array

## Aim

To write a program to reverse the elements of a given array.

## Algorithm

1. Start.
2. Read the size `n` of the array.
3. Read the elements of the array.
4. Initialize two pointers:
   - `left = 0`
   - `right = n - 1`
5. While `left < right`:
   - Swap `arr[left]` and `arr[right]`.
   - Increment `left`.
   - Decrement `right`.
6. Display the reversed array.
7. Stop.

## Program

```c
#include <stdio.h>

int main() {
    int n, i, temp;
    int left, right;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter the elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    left = 0;
    right = n - 1;

    while (left < right) {
        temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;

        left++;
        right--;
    }

    printf("Reversed array:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
Sample Input
Enter the number of elements: 5
Enter the elements:
10 20 30 40 50
Sample Output
Reversed array:
50 40 30 20 10
Time Complexity

O(n)

Each element is processed at most once during the reversal.

Space Complexity

O(n)

The array requires space for n elements.

Result

The given array was successfully reversed.
