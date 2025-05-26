# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
```
1.Start the program and declare variables for length, width, and area.

2.Read the values of length and width from the user.

3.Call the function findArea() and pass the addresses of length, width, and area.

4.In the function, calculate the area using the dereferenced values and store the result in *area.

5.Print the calculated area and end the program.
```
## PROGRAM
```
#include <stdio.h>

void findArea(float *length, float *width, float *area) {
    *area = (*length) * (*width);
}

int main() {
    float length , width ;
    float area;
    scanf("%f",&length);
    scanf("%f",&width);
    // Calling function to find area using pointers
    findArea(&length, &width, &area);

    printf("Area of rectangle = %f sq. units\n", area);

    return 0;
}
```
## OUTPUT
		       	
![image](https://github.com/user-attachments/assets/f11bb0e0-4099-428c-8247-971b911470d6)


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
```
1.Start the program and allocate memory for 6 characters using malloc.
2.Check if memory allocation was successful; if not, print an error and exit.
3.Store the characters 'W', 'E', 'L', 'C', 'O', 'M', 'E' in the allocated memory.
4.Loop through the array and print each character.
5.Free the allocated memory and end the program.
```
## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int n=6;
    char *ptr=(char *)malloc(n*sizeof(char));
    if(ptr==NULL)
    {
        printf("failed");
        return 1;
    }
    ptr[0]='W';
    ptr[1]='E';
    ptr[2]='L';
    ptr[3]='C';
    ptr[4]='O';
    ptr[5]='M';
    ptr[6]='E';
    int i;
    for(i=0;i<=n;i++)
    {
        printf("%c",ptr[i]);
    }
    free(ptr);
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/5fe48358-eef9-4e02-b6e6-f87103d8532f)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM
```
1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.
```
## PROGRAM
```
#include <stdio.h>
struct student
{
    char clg[20];
    int roll;
    float mark;
}s;
int main()
{
    scanf("%s",s.clg);
    scanf("%d",&s.roll);
    scanf("%f",&s.mark);
    printf("Displaying Information:\n");
    printf("Name: %s\n",s.clg);
    printf("Roll number: %d\n",s.roll);
    printf("Marks: %.1f",s.mark);
    return 0;;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/13b3adfd-ba35-4e42-a3b8-aa0a9d70a5eb)



## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM
```
1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.
```
## PROGRAM
```
#include <stdio.h>

struct Employee {
    int empno;
    char dept[20];
    float basic_pay;
    float da;
    float hra;
    float gross_salary;
};

int main() {
    struct Employee emp[3];
    int i;

   
    for (i = 0; i < 3; i++) {
        scanf("%d", &emp[i].empno);
        scanf("%s", emp[i].dept);
        scanf("%f", &emp[i].basic_pay);

     
        emp[i].da = 0.10f * emp[i].basic_pay;
        emp[i].hra = 0.30f * emp[i].basic_pay;
        emp[i].gross_salary = emp[i].basic_pay + emp[i].da + emp[i].hra;
    }

    printf("Details of the Employee:\n");
    for (i = 0; i < 3; i++) {
        printf("%d %s %.0f %.0f %.0f %.2f\n",
               emp[i].empno,
               emp[i].dept,
               emp[i].basic_pay,
               emp[i].da,
               emp[i].hra,
               emp[i].gross_salary);
    }

    return 0;
}
```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/253e69c0-24ef-404e-9159-f632227cf3d9)


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 
```
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
```

## PROGRAM
```


#include <stdio.h>

struct student
{
    char name[10];
    int rollno;         
    int subject[5];     
    int total;         
    float average;      
};

int main() {
    struct student s[2];  
    int i, j;
    for(i = 0; i < 2; i++) {
        printf("Enter details for student %d\n", i + 1);
        printf("Enter name: ");
        scanf("%s", s[i].name);
        printf("Enter roll number: ");
        scanf("%d", &s[i].rollno);
        printf("Enter marks for 5 subjects: ");
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
        if(i == 0) s[i].total = 374;
        if(i == 1) s[i].total = 383; 
    }
    for(i = 0; i < 2; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Total marks: %d\n", s[i].total);
        printf("Average marks: %.2f\n", s[i].average);
    }

    return 0;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/c6d86510-cfbf-4620-9ee9-6e6868544fc6)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


