# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
 #include <stdio.h>
 int main() {
 float length, width, area;
 float *ptrLength = &length, *ptrWidth = &width; 
printf("Enter the length of the rectangle: ");
 scanf("%f", ptrLength);
 printf("Enter the width of the rectangle: ");
 scanf("%f", ptrWidth);
 area = (*ptrLength) * (*ptrWidth);
 printf("The area of the rectangle is: %.2f\n", area);
 return 0;
 }
 ```
## OUTPUT
		       	
![image](https://github.com/user-attachments/assets/60a8a5e3-e0fa-4936-832f-0727ced1f63e)


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
 #include <stdio.h>
 #include <stdlib.h>
 int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char)); 
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }
     snprintf(str, 8, "WELCOME");
 printf("%s\n", str);
 free(str);
 return 0;
 }
 ```
## OUTPUT

![image](https://github.com/user-attachments/assets/819a2e95-4987-4e9d-8660-3f33ed028312)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
 #include <stdio.h>
 struct Student {
 char name[50];
 int rollNumber;
 float marks;
 };
 int main() {
 struct Student student; 
  printf("Enter student name: ");
 scanf(" %[^\n]", student.name); 
printf("Enter roll number: ");
 scanf("%d", &student.rollNumber);
 printf("Enter marks: ");
 scanf("%f", &student.marks);
 printf("\nStudent Information:\n");
 printf("Name: %s\n", student.name);
 printf("Roll Number: %d\n", student.rollNumber);
 printf("Marks: %.2f\n", student.marks);
 return 0;
 }
 ```
## OUTPUT

![image](https://github.com/user-attachments/assets/02a974d2-a37c-4df9-adf0-ae12da3438d6)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
 #include <stdio.h>
 int main() {
 int a = 44;  
int b = 3;   
int result = a << b;
 printf("The result of %d << %d is: %d\n", a, b, result);
 return 0;
 }
 ```
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/940fff20-7a54-4100-8059-d9d9bddfb0e6)


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
 #include <stdio.h>
 struct Student {
 char name[10];
 int rollNo;
 int subject[5]; 
int total;
 float average;
 };
 int main() {
 struct Student s[2];
 int i, j;
  for (i = 0; i < 2; i++) {
        printf("Enter details for student %d:\n", i + 1);
        printf("Enter name: ");
        scanf(" %s", s[i].name);
        printf("Enter roll number: ");
        scanf("%d", &s[i].rollNo);
        printf("Enter marks of 5 subjects:\n");
        s[i].total = 0; 
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    printf("\nStudent Details:\n");
    for (i = 0; i < 2; i++) {
        printf("Name: %s\n", s[i].name);
        printf("Roll Number: %d\n", s[i].rollNo);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", s[i].average);
        printf("\n");
    }
    return 0;
 }
 ```
## OUTPUT

 ![image](https://github.com/user-attachments/assets/f0d54833-a3ad-4737-82a3-106f1dac5fab)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


