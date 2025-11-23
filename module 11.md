EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

int max_of_four(int a, int b, int c, int d){
    if(a > b && a > c && a > d) return a;
    else if(b > a && b > c && b > d) return b;
    else if(c > a && c > b && c > d) return c;
    else return d;
}

int main(){
    int a, b, c, d;
    scanf("%d\n%d\n%d\n%d", &a, &b, &c, &d);
    int max = max_of_four(a, b, c, d);
    printf("%d", max);
}
```


Output:

<img width="324" height="328" alt="image" src="https://github.com/user-attachments/assets/cb50455a-6b10-4d44-85a5-c53d553edc8b" />




Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>

void calculate_the_maximum(int n, int k){
    int max_and = 0;
    int max_or = 0;
    int max_xor = 0;
    int a = 0, b = 0, c = 0;
    for(int i = 1; i < n; i++){
        for(int j = i + 1; j <= n; j++){
            a = i & j;
            b = i | j;
            c = i ^ j;
            if(a > max_and && a < k) max_and = a;
            if(b > max_or && b < k) max_or = b;
            if(c > max_xor && c < k) max_xor = c;
        }
    }
    printf("%d\n%d\n%d\n", max_and ,max_or, max_xor);
}

int main(){
    int n, k;
    scanf("%d %d", &n, &k);
    
    calculate_the_maximum(n, k);
}
```


Output:

<img width="332" height="369" alt="image" src="https://github.com/user-attachments/assets/b7373c4d-1e78-456a-abcc-5c8a65ae5ea9" />




Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:

```
#include <stdio.h>
#include <string.h>

void series(int n,int a, int b, int c){
    if(n == 4){
        printf("%d", a + b + c);
        return;
    }
    series(n - 1, b, c, a + b + c);
}

int main(){
    int n;
    scanf("%d\n", &n);
    int a, b, c;
    scanf("%d %d %d", &a, &b, &c);
    series(n, a, b, c);
}
```


Output:

<img width="320" height="169" alt="image" src="https://github.com/user-attachments/assets/95cdc681-b10e-409c-bbc4-4277cf1c8404" />



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
#include <string.h>

int main(){
    char str[20];
    scanf("%[^\n]%*c", str);
    for(int i = 0; str[i] != '\0'; i++){
        if('A' <= str[i] && str[i] <= 'Z'){
            str[i] = (str[i] + 32);
        }
    }
    printf("%s", str);
}
```


Output:

<img width="382" height="192" alt="image" src="https://github.com/user-attachments/assets/ae6d0c05-043d-456a-810b-048603bbfc1f" />



Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:

```
#include <stdio.h>
#include <string.h>

void reverse(char *s){
    int n = strlen(s);
    char sr[n];
    printf("Input String: %s\n", s);
    for(int i = 0; i < n; i++){
        sr[i] = s[n - i - 1];
    }
    sr[n] = '\0';
    printf("Reverse String: %s\n", sr);
}

int main(){
    char str[20];
    scanf("%[^\n]%*c", str);
    reverse(str);
}
```


Output:

<img width="560" height="236" alt="image" src="https://github.com/user-attachments/assets/0d2dcd70-81b4-4b3f-85c1-3c85e7808dba" />






Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
