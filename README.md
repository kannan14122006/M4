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
```
#include <stdio.h>

int main() {
    int num = 44;
    int shifts = 3;
    int result;

    // Perform left shift
    result = num << shifts;

    // Output
    printf("Original number: %d\n", num);
    printf("After left shifting by %d positions: %d\n", shifts, result);

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/f4163afb-e4fe-4557-92a1-681ef8a1b03d)









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
```
#include <stdio.h>

int main() {
    int num1, num2;

    // Input two numbers
    printf("Enter first number: ");
    scanf("%d", &num1);

    printf("Enter second number: ");
    scanf("%d", &num2);

    // Check equality using simple if
    if (num1 == num2) {
        printf("The numbers are equal.\n");
    }

    if (num1 != num2) {
        printf("The numbers are not equal.\n");
    }

    return 0;
}

```

## OUTPUT
     ![image](https://github.com/user-attachments/assets/5c796556-54bb-445d-a4e0-f22625c666e1)
      
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
```
#include <stdio.h>
#include <ctype.h>  // For tolower()

int main() {
    char str[100];

    // Input string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Read string including spaces

    // Convert to lowercase
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]);
    }

    // Output result
    printf("Lowercase string: %s", str);

    return 0;
}
```
## OUTPUT


![image](https://github.com/user-attachments/assets/dd7047aa-fa15-45e6-aa07-0c0e03e0e209)


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
```
#include <stdio.h>

int main() {
    char str[200];
    int i = 0, wordCount = 0;

    // Input string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Read line including spaces

    // Count words using do...while loop
    do {
        // Check for word boundary
        if ((str[i] != ' ' && str[i] != '\n' && str[i] != '\0') &&
            (str[i + 1] == ' ' || str[i + 1] == '\n' || str[i + 1] == '\0')) {
            wordCount++;
        }
        i++;
    } while (str[i] != '\0');

    // Output result
    printf("Total number of words: %d\n", wordCount);

    return 0;
}
```
## OUTPUT


![image](https://github.com/user-attachments/assets/92086871-38df-4215-aecd-c1391496c338)



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
```
#include <stdio.h>

int main() {
    char str1[100], str2[100];
    int i = 0, flag = 0;

    // Input strings
    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);

    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);

    // Compare character by character
    while (str1[i] != '\0' && str2[i] != '\0') {
        if (str1[i] != str2[i]) {
            flag = 1;
            break;
        }
        i++;
    }

    // Also check for different lengths
    if (str1[i] != str2[i]) {
        flag = 1;
    }

    // Output result
    if (flag == 0) {
        printf("Strings are equal.\n");
    } else {
        printf("Strings are not equal.\n");
    }

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/45fe70d1-3dc4-44af-9e83-f1273ac8fc70)

 

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

