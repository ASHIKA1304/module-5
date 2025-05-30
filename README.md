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
    float *ptrLength = &length, *ptrWidth = &width, *ptrArea = &area;

    printf("Enter length of rectangle: ");
    scanf("%f", ptrLength);

    printf("Enter width of rectangle: ");
    scanf("%f", ptrWidth);

    *ptrArea = (*ptrLength) * (*ptrWidth);

    printf("Area of rectangle: %.2f\n", *ptrArea);

    return 0;
}
```
## OUTPUT
		       	

![438200097-d57acebc-a509-4b8d-9aed-88898bf5b657](https://github.com/user-attachments/assets/e57c1f9d-2279-4723-a6cf-c6ca2f6cdf5f)

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
#include <strings.h>

int main() {
    char *str;
    str = (char*) malloc(8 * sizeof(char));

    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }
    strcpy(str,"WELCOME");
    printf("%s\n", str);
    return 0;
}
```
## OUTPUT

![438200402-b3c49aa7-8486-48f4-9f0b-5379bcfcc9f0](https://github.com/user-attachments/assets/6c3bb68a-1c8b-4699-922d-1acf3ed62cea)



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



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

struct Employee 
{
    int id;
    char name[50];
    float age;
};

int main() 
{
    struct Employee employees;
    scanf("%d", &employees.id);
    scanf(" %s", employees.name);
    scanf("%f", &employees.age);
    printf("Rollno is: %d\nName is: %s\nPercentage is: %.2f\n", employees.id, employees.name, employees.age);
  

    return 0;
}
```

## OUTPUT

![438200725-c3d1db83-f99e-4dbc-a476-ffae39c1049e](https://github.com/user-attachments/assets/7e06f61b-b47b-45a7-902f-39797bf8794e)

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

struct Employee {
    char name[50];
    float basicSalary;
    float hra;
    float da;
    float grossSalary;
};

int main() {
    struct Employee emp[3];

    for (int i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        
        printf("Enter Name: ");
        scanf("%s", emp[i].name);
        
        printf("Enter Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);
        
        printf("Enter HRA: ");
        scanf("%f", &emp[i].hra);
        
        printf("Enter DA: ");
        scanf("%f", &emp[i].da);

        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
        printf("\n");
    }

    printf("Employee Details and Gross Salary:\n");
    for (int i = 0; i < 3; i++) {
        printf("Employee %d\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("Basic Salary: %.2f\n", emp[i].basicSalary);
        printf("HRA: %.2f\n", emp[i].hra);
        printf("DA: %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].grossSalary);
        printf("\n");
    }

    return 0;
}
```

 ## OUTPUT
 


 ![438200952-68fad761-c57b-4daf-b2bc-ea83e5a9389b](https://github.com/user-attachments/assets/c3bafe73-b787-4f35-982a-85bdc1764d9e)


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
    char name[50];
    int marks[5];
    float total;
    float average;
};

int main() {
    struct Student student;
    int sum = 0;

    printf("Enter student's name: ");
    scanf("%s", student.name);

    printf("Enter marks for 5 subjects:\n");
    for (int i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%d", &student.marks[i]);
        sum += student.marks[i];
    }

    student.total = sum;
    student.average = sum / 5.0;

    printf("\nStudent Name: %s\n", student.name);
    printf("Total Marks: %.2f\n", student.total);
    printf("Average Marks: %.2f\n", student.average);

    return 0;
}
```

## OUTPUT


![WhatsApp Image 2025-05-30 at 22 49 09_5069afa2](https://github.com/user-attachments/assets/6ce1f71c-471c-43d7-b7bd-473e1f2dccb1)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


