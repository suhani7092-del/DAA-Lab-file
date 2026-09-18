# Experiment 3: Find the Sum of Elements of an Array Using Two Pointers

## Aim

To find the sum of all elements of an array using the two-pointer technique.

## Algorithm

1. Start.
2. Read the size `n` of the array.
3. Read the elements of the array.
4. Initialize two pointers:
   - `left = 0`
   - `right = n - 1`
5. Initialize `sum = 0`.
6. While `left <= right`:
   - Add `arr[left]` to `sum`.
   - If `left != right`, add `arr[right]` to `sum`.
   - Increment `left`.
   - Decrement `right`.
7. Display the sum.
8. Stop.

## Program

```c
#include <stdio.h>

int main() {
    int n, i;
    int left, right, sum = 0;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter the elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    left = 0;
    right = n - 1;

    while (left <= right) {
        sum += arr[left];

        if (left != right) {
            sum += arr[right];
        }

        left++;
        right--;
    }

    printf("The sum of elements is: %d\n", sum);
    return 0;
}
Sample Input
Enter the number of elements: 6
Enter the elements:
10 20 30 40 50 60
Sample output
The sum of elements is: 210
Time Complexity

O(n)

Each element of the array is visited once.

Space Complexity

O(n)

The array requires space for n elements.

Result

The sum of all elements of the array was successfully calculated using the two-pointer technique
