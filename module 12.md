```
NAME: V.POOJAA SREE
REG.NO.: 212223040147

```

## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

### Aim:
To write a C program to display stack elements using linked list.

### Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
### Program:

```
struct Node   
{  
char data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp = head;
    if(head==NULL)
    {
        printf("stack is empty\n");
        return;
    }
    while(temp!=NULL)
    {
        printf("%c\n",temp->data);
        temp=temp->next;
    }
    printf("\n");
    
}

```

### Output:

![26](https://github.com/user-attachments/assets/a0ea682e-916b-4a82-bc6d-9d5cfa747bdf)


### Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.

### Aim:
To write a C program to pop an element from the given stack using liked list.

### Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
### Program:

```
struct Node   
{  
char data[100];  
struct Node *next;  
}*head;  
void pop()  
{  
    struct Node *temp=head;
    if(head==NULL)
    {
        printf("stack is empty\n");
        return;
    }
    head=temp->next;
    free(temp);
}

```

### Output:

![27](https://github.com/user-attachments/assets/808ac346-0f58-4fe9-9304-e6eaf3a79711)


### Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.



## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

### Aim:
To write a C program to display queue elements using linked list.

### Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
### Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp = front;
    if(front==NULL)
    {
        printf("queue is empty\n");
        return;
    }
    printf("Queue elements:\n");
    while(temp!=NULL)
    {
        printf("%.3f\n",temp->data);
        temp=temp->next;
    }       
}

```

### Output:

![28](https://github.com/user-attachments/assets/1849d097-fa0b-4f75-a1ff-84ae2200c0df)


### Result:
Thus, the program to display queue elements using linked list is verified successfully.



 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

### Aim:
To write a C program to insert elements in queue using linked list

### Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
### Program:

```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *temp = (struct Node *)malloc(sizeof(struct Node));
    temp->data=data;
    temp->next=NULL;
    if(front==NULL)
    {
       front=temp;
       rear=temp;
       return;
    }
    rear->next=temp;
    rear=temp;
}

```

### Output:

![29](https://github.com/user-attachments/assets/0373d90f-430a-4e2a-81dd-8133e3d37d3d)


### Result:
Thus, the program to insert elements in queue using linked list is verified successfully.




## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

### Aim:
The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

### Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

### Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    if(front==NULL)
    {
        printf("queue is empty\n");
        return;
    }
     printf("%.2f",front->data);
}

```

### Output:

![30](https://github.com/user-attachments/assets/c6aa53ad-f325-4815-ad9e-615fa0f3a58d)


### Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


