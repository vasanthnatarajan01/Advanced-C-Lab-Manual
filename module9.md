## EXP NO 3A : C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim:
To write a C program to display stack elements using an array.

## Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
## Program:
~~~
int stack[40],top,i;
 void display()
{
    for(i=top;i>=0;i--)
       {
           printf("%d\n",stack[i]);
       }
}
~~~
## Output:
![437944090-301f186a-1daf-4c79-9b3e-c832544d5598](https://github.com/user-attachments/assets/e3fddc1a-7911-4b6d-982b-157feaaa7085)

## Result:
Thus, the program to display stack elements using an array is verified successfully.
 


## EXP NO 3B : PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

## Aim:
To create a C program to push the given element in to a stack using array.

## Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
## Program:
~~~
int size=3,top=1;
float stack[40];
void push (float data)
{
    if (top==size-1 )
    {
        printf("stack is full\n");      
    }
    else
    {
        top ++;
        stack[top] = data;
    }
}
~~~
## Output:
![437944304-d5971ab1-21bb-4d67-ace8-ae047a4191f3](https://github.com/user-attachments/assets/1570266c-f032-4483-ad01-67cf36783750)

## Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO 3C : C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

## Aim:
To write a C program to display queue elements using array

## Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
## Program:
~~~
int queue[50], rear, front,i;
void display()
{
    if(front==-1)
    {
        printf("No elements to display");     
    }
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%d ",queue[i]);    
        }  
    }
}
~~~
## Output:
![437944365-aec17816-2ed5-4428-b9cc-1c959c7724c8](https://github.com/user-attachments/assets/1b7cd718-197e-4200-b9a2-3bda62e0facb)

## Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO 3D : C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

## Aim:
To write a C program to insert elements in queue using array.

## Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

## Program:
~~~
int size=4, rear=-1, front=-1; 
float queue[50];
void enqueue(float data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
        
    }
}
~~~

## Output:
![437944452-f139757a-0191-44c7-982a-90b6fdc632a5](https://github.com/user-attachments/assets/a22ed28b-7c32-4a5f-a00b-fcf104a7e8eb)

## Result:
Thus, the program to insert elements in queue using array is verified successfully.



 ## EXP NO 3E : C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

## Aim:
To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:
1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.

## Program:
~~~
int front, rear;
void dequeue()
{
    if(front==-1&&rear==-1)
    printf("Queue Underflow.");
    else if(front==rear)
    front=rear=-1;
    else{
        front=front+1;
    }
}
~~~

## Output:
![437944794-8f33d7b6-b48f-4ac8-a07e-beb41b2575dc](https://github.com/user-attachments/assets/5b6b14a9-55d7-49c0-81e9-ca4008bdfe77)

## Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
