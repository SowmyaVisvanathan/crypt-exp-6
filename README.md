#### Name : Sowmya V
#### Reg no : 212222110045
#### Date : 

## EX - 6 : Pseudorandom-Number-Generation

### Aim:
Implementation of Pseudorandom Number Generation Using Standard library

### Algorithm
```
1. Start.
2. Declare variables count, min, max, and random_number.
3. Prompt the user to input the number of random numbers to generate (count).
    --> If the input is invalid (i.e., not a positive integer), repeat the prompt until a valid input is provided.
4. Prompt the user to input the minimum value (min).
5. Prompt the user to input the maximum value (max).
    -->Ensure that max is greater than min. If not, prompt the user to re-enter the value of max.
6. Seed the random number generator using the current time (srand(time(NULL))).
7. For each number from i = 0 to count - 1 (i.e., generate count random numbers):
    --> Generate a random number using the formula:
           random_number = (rand() % (max - min + 1)) + min.
    --> This formula ensures the random number is within the range [min, max].
    -->Print the random number.
8. End.
```
### Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() 
{
    int count, min, max;
    printf("Enter the number of random numbers to generate: ");
    while (scanf("%d", &count) != 1 || count <= 0) 
    {
        printf("Invalid input. Please enter a positive integer: ");
        while (getchar() != '\n'); 
    }
    printf("Enter the minimum value: ");
    scanf("%d", &min);
    printf("Enter the maximum value: ");
    while (scanf("%d", &max) != 1 || max <= min) 
    {
        printf("Invalid input. Maximum must be greater than minimum. Please enter again: ");
        while (getchar() != '\n');  // Clear the input buffer
    }
    srand(time(NULL));
    printf("\nPseudorandom numbers between %d and %d:\n", min, max);
    for (int i = 0; i < count; i++) 
    {
        int random_number = (rand() % (max - min + 1)) + min;
        printf("%d\n", random_number);
    }
    return 0;
}
```
### Output

![image](https://github.com/user-attachments/assets/a3c54d76-9247-4af6-ae12-d015fbd564f4)

### Result
The Implementation of Pseudorandom Number Generation Using Standard library is successful.
