```
NAME: V. POOJAA SREE
REG.: 212223040147

```

## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

### Aim:
To write a C program to create a function to find the greatest number

### Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
### Program:

```
#include <stdio.h>

int max(int x, int y) {
    return (x > y) ? x : y;
}

int max_of_four(int a, int b, int c, int d) {
    return max(max(a, b), max(c, d));
}

int main() {
    int a, b, c, d;
    
    scanf("%d%d%d%d", &a,&b,&c,&d);
    printf("%d\n", max_of_four(a, b, c, d));
    
    return 0;
}

```

### Output:

![21](https://github.com/user-attachments/assets/60663e13-2cad-4e78-9a84-80d0b131afb0)


### Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

### Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

### Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
### Program:

```
#include<stdio.h>

void calculate_the_maximum(int n,int k){
    int max_and = 0, max_or = 0 , max_xor=0;
    
    for(int a=1; a<=n; a++){
        for(int b=a+1; b<=n; b++){
            int c_and = a&b;
            int c_or = a|b;
            int c_xor = a^b;
            
            if(c_and < k && c_and > max_and){
                max_and = c_and;
            }
            if(c_or < k && c_or > max_or){
                max_or = c_or;
            }
            if(c_xor < k && c_xor > max_xor){
                max_xor = c_xor;
            }
         }
    }
    printf("%d\n%d\n%d",max_and,max_or,max_xor);
}
int main(){
    int n,k;
    scanf("%d%d",&n,&k);
    calculate_the_maximum(n,k);
    
    return 0;
}

```

### Output:

![22](https://github.com/user-attachments/assets/40709ad0-657f-42b7-ad66-ae6c84c84c50)


### Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

### Aim:
To write a C program to write the logic for the requests

### Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

typedef struct {
    int *books;
    int size;
} Shelf;

void insertBook(Shelf *shelves, int shelfIndex, int pages) {
    shelves[shelfIndex].books = realloc(shelves[shelfIndex].books, (shelves[shelfIndex].size + 1) * sizeof(int));
    shelves[shelfIndex].books[shelves[shelfIndex].size++] = pages;
}

int main() {
    int numShelves, numRequests;
    scanf("%d", &numShelves);
    scanf("%d", &numRequests);

    Shelf *shelves = (Shelf *)malloc(numShelves * sizeof(Shelf));
    for (int i = 0; i < numShelves; i++) {
        shelves[i].books = NULL;
        shelves[i].size = 0;
    }

    for (int i = 0; i < numRequests; i++) {
        int query, x, y;
        scanf("%d", &query);
        if (query == 1) {
            scanf("%d %d", &x, &y);
            insertBook(shelves, x, y);
        } else if (query == 2) {
            scanf("%d %d", &x, &y);
            printf("%d\n", shelves[x].books[y]);
        } else if (query == 3) {
            scanf("%d", &x);
            printf("%d\n", shelves[x].size);
        }
    }

    // Free allocated memory
    for (int i = 0; i < numShelves; i++) {
        free(shelves[i].books);
    }
    free(shelves);

    return 0;
}

```

### Output:

![23](https://github.com/user-attachments/assets/76ea122c-a23c-4b43-9ca2-42478685557c)



### Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

### Aim:
To write a C program print the sum of the integers in the array.

### Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.

### Program:

```
#include<stdio.h>
#include<stdlib.h>

int main() {
    int n,i,sum=0;
    scanf("%d",&n);
    int *arr = (int *)malloc(n * sizeof(int));
    if(arr == NULL) {
        printf("Memory Allocation Failed\n");
        return 1;
    }
    for(i=0;i<n;i++) {
        scanf("%d",&arr[i]);
        sum += arr[i];
    }
    printf("%d",sum);
    free(arr);
    return 0;
}

```

### Output:

![24](https://github.com/user-attachments/assets/0106c01a-c893-48bf-ac47-614548369ccc)


### Result:
Thus, the program prints the sum of the integers in the array is verified successfully.



 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A  SENTENCE

### Aim:
To write a C program that counts the number of words in a given sentence.

### Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.

### Program:

```
#include <stdio.h>
#include <string.h>

int main() {
    char sentence[1000];
    int i, count = 0;
    int inWord = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin); 

    for (i = 0; sentence[i] != '\0'; i++) {
        
        if (sentence[i] != ' ' && sentence[i] != '\n' && sentence[i] != '\t') {
            if (inWord == 0) {
                inWord = 1;  
                count++;
            }
        } else {
            inWord = 0;  
        }
    }

    printf("Number of words in the sentence: %d\n", count);

    return 0;
}

```

### Output:

![25](https://github.com/user-attachments/assets/879215e4-78e8-4525-a2fc-80047f6e76e5)


### Result:
Thus, the program that counts the number of words in a given sentence is verified 
successfully.
