# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```#include <stdio.h>

int main() {
    int num = 44;  
    int shifts = 3;  

   
    int result = num << shifts;

   
    printf("The number %d left shifted by %d positions is: %d\n", num, shifts, result);

    return 0;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/ac64721b-eb99-4e98-acca-078391f1ec21)










## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```#include <stdio.h>

int main() {
    int num1, num2;

    
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    
    if (num1 == num2) {
        printf("The numbers are equal.\n");
    } else {
        printf("The numbers are not equal.\n");
    }

    return 0;
}
```


## OUTPUT

![image](https://github.com/user-attachments/assets/214c22b6-a063-4cd1-bc33-53625396e067)

           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```#include<stdio.h>
#include<ctype.h>
int main()
{
    char str[100];
    scanf("%s",str);
    for(int i= 0;str[i];i++)
    {
        str[i]=tolower(str[i]);
    
    
    
    }
        printf("Lower case String is:%s",str);
    
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/3bdf038b-ab07-4eab-a4bf-0c3d460ee405)



## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```#include <stdio.h>
#include <ctype.h>

int main() {
    char str[100];
    int count = 0, i = 0;

   
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

   
    do {
        
        while (str[i] == ' ' || str[i] == '\t' || str[i] == '\n') {
            i++;
        }

       
        if (str[i] != '\0' && str[i] != ' ' && str[i] != '\t' && str[i] != '\n') {
            count++;

           
            while (str[i] != ' ' && str[i] != '\t' && str[i] != '\n' && str[i] != '\0') {
                i++;
            }
        }
    } while (str[i] != '\0');

    
    printf("Total number of words: %d\n", count);

    return 0;
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/7fd85dc3-74d1-41ad-92c7-cb19d7a91aa2)




## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```#include<stdio.h>
#include<ctype.h>
#include<string.h>
int main()
{
    char str1[100],str2[100],mergedstr[200];
    int i,j;
    fgets(str1,sizeof(str1),stdin);
    fgets(str2,sizeof(str2),stdin);
    if(str1[strlen(str1)-1]=='\n') str1[strlen(str1)-1]='\0';
    if(str1[strlen(str2)-1]=='\n') str2[strlen(str2)-1]='\0';
    for( i=0;str1[i]!='\0';i++)
    {
        mergedstr[i]=str1[i];
    }
    for( j=0;str2[j]!='\0';j++)
    {
        mergedstr[i+j]=str2[j];
    }
    mergedstr[i+j]='\0';
    int totalwords=0;
    int inword=0;
    for(i=0;mergedstr[i]!='\0';i++)
    {
        if(isspace(mergedstr[i]))
        {
            inword=0;
        }
        else if(!isspace(mergedstr[i]) && inword==0)
        {
            totalwords++;
            inword=1;
        }
    }
    printf("%s",mergedstr);
    printf("%d",(i++)-1);
}
```

## OUTPUT

 ![image](https://github.com/user-attachments/assets/76ae2ad0-1e5a-42da-b347-4d36a3fcb79a)


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

