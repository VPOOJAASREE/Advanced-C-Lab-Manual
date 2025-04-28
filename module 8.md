# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
## Aim:
To write a C program print the lowercase English word corresponding to the number

## Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
## Program:

```

#include <stdio.h>

int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n) {
        case 5:
            printf("seventy one\n");
            break;
        case 6:
            printf("seventy two\n");
            break;
        case 13:
            printf("seventy three\n");
            break;
        default:
            printf("Greater than 13\n");
            break;
    }
    return 0;
}

```


## Output:

![6](https://github.com/user-attachments/assets/75782c67-f6cb-4ab8-8862-43dd8268724a)


Result:
Thus, the program is verified successfully.




 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

## Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
## Program:

```
#include <stdio.h>

int main() {
    char a[50];
    int count[4] = {0}; 

    printf("Enter a string of digits: ");
    scanf("%s", a);

    for (int i = 0; a[i] != '\0'; i++) {
        if (a[i] >= '0' && a[i] <= '3') {
            count[a[i] - '0']++;
        }
    }

    for (int i = 0; i <= 3; i++) {
        printf("%d ", count[i]);
    }
    printf("\n");

    return 0;
}

```


## Output:

![7](https://github.com/user-attachments/assets/ee11c754-bff3-4144-8c69-b95029c98168)


## Result:
Thus, the program is verified successfully.





# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

## Aim:
To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)
3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
## Program:

```

#include <stdio.h>
#include <string.h>
#include <stdlib.h>

void swap(char *x, char *y) {
    char temp = *x;
    *x = *y;
    *y = temp;
}

void sortString(char *str) {
    int len = strlen(str);
    for (int i = 0; i < len-1; i++) {
        for (int j = i+1; j < len; j++) {
            if (str[i] > str[j]) {
                swap(&str[i], &str[j]);
            }
        }
    }
}

int nextPermutation(char *str, int len) {
    int i = len - 2;
    while (i >= 0 && str[i] >= str[i+1]) i--;
    if (i < 0) return 0;

    int j = len - 1;
    while (str[j] <= str[i]) j--;

    swap(&str[i], &str[j]);

    for (int l = i+1, r = len-1; l < r; l++, r--) {
        swap(&str[l], &str[r]);
    }

    return 1;
}

int main() {
    char s[100];
    printf("Enter a string: ");
    scanf("%s", s);

    int len = strlen(s);
    sortString(s);
    do {
        printf("%s\n", s);
    } while (nextPermutation(s, len));

    return 0;
}

```


## Output:

![8](https://github.com/user-attachments/assets/34f70d23-81ef-45f1-b2f7-b633f6c8d12a)


## Result:
Thus, the program is verified successfully.





 
# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.

## Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.

## Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
## Program:

```

#include <stdio.h>

int min(int a, int b) {
    return (a < b) ? a : b;
}

int main() {
    int n;
    printf("Enter value of n: ");
    scanf("%d", &n);

    int len = n * 2 - 1;

    for (int i = 0; i < len; i++) {
        for (int j = 0; j < len; j++) {
            int min1 = min(i, j);
            int min2 = min(len - 1 - i, len - 1 - j);
            int minValue = min(min1, min2);
            printf("%d ", n - minValue);
        }
        printf("\n");
    }

    return 0;
}


```

## Output:

![9](https://github.com/user-attachments/assets/5d14f049-2031-46b0-be35-2e442e956583)



## Result:
Thus, the program is verified successfully.





# EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

## Program:

```

#include <stdio.h>

int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result;
    result = square();
    printf("Square of the number is: %d\n", result);
    return 0;
}

```


## Output:

![10](https://github.com/user-attachments/assets/958d87c3-5af7-47d5-9fe8-c135037d2d6c)



## Result:
Thus, the program is verified successfully.



























