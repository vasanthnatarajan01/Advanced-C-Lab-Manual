# Advanced-C-Lab-Manual

EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim: To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:

Declare structure eligible with age (integer) and n (character array)
Declare variable e of type eligible
Input age and name using scanf, store in e
If e.age <= 6
Print "Vaccine Eligibility: No" Else
Print "Vaccine Eligibility: Yes"
Print details (e.age, e.n)
Return 0
Program:

```
#include <stdio.h>
struct Person
{
 char name[50];
 int age;
};
void checkEligibility(struct Person people[], int n)
{
 printf("\n--- Vaccine Eligibility ---\n");
for (int i = 0; i < n; i++)
 {
 printf("Name: %s\n", people[i].name);
 printf("Age: %d\n", people[i].age);
 if (people[i].age >= 6)
 {
 printf("Status: Eligible for vaccine.\n");
 }
 else
 {
 printf("Status: Not eligible for vaccine.\n");
 }
 printf("---------------------------\n");
 }
} 
int main()
{
 struct Person people[100];
 int n;
 printf("Enter number of people: ");
 scanf("%d", &n);
 for (int i = 0; i < n; i++)
 {
 printf("\nEnter details for person %d:\n", i + 1);
 printf("Name: ");
 scanf(" %[^\n]", people[i].name);
 printf("Age: ");
 scanf("%d", &people[i].age);
 }
 checkEligibility(people, n);
 return 0;
}
```


Output:

![image](https://github.com/user-attachments/assets/18fdfc79-2ae0-4233-94c7-f6f053501c3a)

Result: Thus, the program is verified successfully.

EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION Aim: To write a C program for passing structure as function and returning a structure from a function

Algorithm:

Define structure numbers with members a and b.
Declare variable n of type numbers.
Prompt the user to enter values for a and b.
Input values for a and b into n using scanf.
Call the add function with n as an argument.
Print the result returned by the add function.
Return 0
Program:
```
#include<stdio.h>
struct number
{
 int num1;
 int num2;
};
struct result
{
 int add;
};
struct result process(struct number num)
{
 struct result res;
 res.add=num.num1+num.num2;
 return res;
};
int main() 
{
 struct number num;
 scanf("%d %d ",&num.num1,&num.num2);
 struct result result;
 result=process(num);
 printf("%d",result.add);
 return 0;
}
```

Output:

![Screenshot 2025-05-20 203332](https://github.com/user-attachments/assets/6078f9f3-f961-4902-86c6-df4e4d00fb67)




Result: Thus, the program is verified successfully

EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim: To write a C program to read a file name from user

Algorithm:

Include the necessary header file stdio.h.
Begin the main function.
Declare a file pointer p. Declare a character array name to store the file name.
Prompt the user to enter a file name. Use scanf to input the file name into the name array.
Print a message indicating that the file with the specified name has been created successfully.
Use fopen to open a file with the name provided by the user in write mode ("w").
If successful, continue to the next step.
If unsuccessful, print an error message and exit the program with a non-zero status.
Print a message indicating that the file has been opened successfully.
Use fclose to close the file.
Print a message indicating that the file has been closed.
End the main function.
Return 0 to indicate successful program execution.
Program:

```
#include <stdio.h>
int main ()
{
 char str[50];
 scanf("%s",str);
 FILE *ptr;
 ptr=fopen(str,"w");
 printf("%s File Created Successfully\n",str);
 if(ptr!=NULL)
 {
 printf("%s File Opened\n",str);
 }
 fclose(ptr);
 printf("%s File Closed",str);
}
```
Output:

![image](https://github.com/user-attachments/assets/54fc2ee7-5c81-42b9-a5a9-28389f6feb5d)


Result: Thus, the program is verified successfully

EXP NO:4 PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE Aim: To write a C program to read, a file and insert text in that file Algorithm:

Include the necessary header file stdio.h.
Begin the main function.
Declare a file pointer p. Declare character arrays name and text. Declare an integer variable num.
Prompt the user to enter a file name and the number of strings. Use scanf to input the file name into the name array and the number of strings into the num variable.
Use fopen to open a file with the name provided by the user in write mode ("w").
If successful, continue to the next step.
If unsuccessful, print an error message and exit the program with a non-zero status.
Print a message indicating that the file has been opened successfully.
Use a loop to input strings from the user and write them to the file using fputs.
Use fclose to close the file.
Print a message indicating that data has been added successfully.
End the main function.
Return 0 to indicate successful program execution.
Program:

```
#include <stdio.h>
int main ()
{
 char str[50];
 scanf("%s",str);
 FILE *ptr;
 ptr=fopen(str,"w");
 printf("%s Opened\n",str);
 int a;
 float b;
 scanf("%d",&a);
 for(int i=0;i<b;i++)
 {
 scanf("%f",&b);
 }
 printf("Data added Successfully\n");
 fclose(ptr);
}

```

Output:


![image](https://github.com/user-attachments/assets/c15256da-7c5f-41c2-af0e-6f29a2d1354a)


Result: Thus, the program is verified successfully

Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim: The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm: 1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Subject
{
 char name[50];
 int marks;
};
int main()
{
 int n, i;
 struct Subject *s;
 printf("Enter the number of subjects: ");
 scanf("%d", &n);
 s = (struct Subject *)malloc(n * sizeof(struct Subject));
 if (s == NULL)
 {
 printf("Memory allocation failed.\n");
 return 1;
 }
 for (i = 0; i < n; i++)
 {
 printf("\nEnter details for subject %d:\n", i + 1);
 printf("Subject Name: ");
 scanf(" %[^\n]", s[i].name);
 printf("Marks: ");
 scanf("%d", &s[i].marks);
 }
 printf("\n--- Subject Details ---\n");
 for (i = 0; i < n; i++) {
 printf("Subject %d: %s - %d marks\n", i + 1, s[i].name, s[i].marks);
 }
 free(s);
 return 0; 
```
Output:

![image](https://github.com/user-attachments/assets/f3c55a5e-b822-413f-9a30-17a2d69dc1f9)


Result: Thus, the program is verified successfully
