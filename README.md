# student-details-project
                         /*Simple Student Report Card System

Features (using your syllabus concepts):

1. Input & Output → Take student details (name, roll number, marks in subjects).

2. Operators & Expressions → Calculate total marks and percentage.

3. If-Else → Decide whether the student passed or failed.

4. Switch-Case → Display grade based on percentage.

5. Loops → Allow entering details for multiple students.

---
Example Flow:

Enter Student Name: John
Enter Roll Number: 101
Enter marks in 3 subjects: 80 70 90

Total = 240
Percentage = 80.00

Grade = A
Result = PASS*/

// Main program 

#include<stdio.h>
int main()
{
    int n; //number of students
    printf("Enter number of students: ");
    scanf("%d",&n);


// 1. Input & Output → Take student details (name, roll number, marks in subjects).
    for (int i = 1; i <= n; i++)
    {
        char name[70];
    int rollno;
    float marks,hindi,science,english,kannada,socialscience,maths;
    float total;
    float percentage;
    char grades;

    printf("\n--------------------------------------\n");
    printf("Enter the student details : \n");
    printf("--------------------------------------\n");

    printf("Student Name : ");
    scanf("%s",name);

    printf("RollNo : ");
    scanf("%d",&rollno);

    printf("Enter your Marks in below mentioned subjects : \n");
    printf("hindi : ");
    scanf("%f", &hindi);

    printf("English : ");
    scanf("%f", &english);

    printf("Kannada : ");
    scanf("%f", &kannada);

    printf("Science : ");
    scanf("%f", &science);

    printf("SocialScience: ");
    scanf("%f", &socialscience);

    printf("Maths : ");
    scanf("%f", &maths);

    //2. Operators & Expressions → Calculate total marks and percentage.

    total = hindi + english + kannada + science + socialscience + maths;
    percentage = total / 625 * 100;

    printf("--------------------------------------");
    printf("\nStudent Details are mentioned below :\n");
    printf("--------------------------------------");
    printf("\nStudent Name : %s\nRollNo : %d\nhindi : %f\nscience : %f\nEnglish : %f\nKannada : %f\nsocialscience : %f\nMaths : %f\n\n" , name,rollno,hindi,science,english,kannada,socialscience,maths);

    printf ("Total Marks : %f\n" , total);
    printf ("Percentage : %f\n" , percentage);

// 3. If-Else → Decide whether the student passed or failed.

    if (percentage>=75)
    {
        printf("\nResult : DISTINCTION\n");
    }
    else if(percentage>=60){
        printf("\nResult : FIRST CLASS\n");
    }
    else if(percentage>=50){
        printf("\nResult : SECOND CLASS\n");
    }
    else{
        printf("\nResult : FAILED !! ");
    }

// 4. Switch-Case → Display grade based on percentage.

    printf("Enter your percentage to check Grades: ");
    scanf("%f",&percentage);

    // Assign grade based on percentage
    if (percentage>=75)
    {
        grades='A';
    }
    else if (percentage>=60)
    {
        grades='B';
    }
    else if (percentage>=50)
    {
        grades='C';
    }
    else{
        grades='B';
    }

    printf("\nYour Grades are displayed below:\n");

    switch (grades)
    {
    case 'A':
        printf("Your percentage is: %.2f\nGrade: %c",percentage,grades);
        break;
    case 'B':
        printf("Your percentage is: %.2f\nGrade: %c",percentage,grades);
        break;
    case 'C':
        printf("Your percentage is: %.2f\nGrade: %c",percentage,grades);
        break;
    case 'D':
        printf("Your percentage is: %.2f\nGrade: %c",percentage,grades);
        break; 
    default:
        printf("\nInvalid data!!!");
        break;
    }


    }
    
        return 0;
}
