# Ex 1d Evaluation of prefix expression
## DATE: 26/02/2025
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1. Start
2. Initialize an empty stack s with a variable top for tracking the stack index.
3. Define a push() function to add an element to the stack.
4. Define a pop() function to remove and return the top element from the stack.
5. In evalprefix(), loop through the given prefix expression from right to left.
6. For each character, if it’s an operator (+, *), pop two operands from the stack, perform the
operation, and push the result.
7. If it's a digit, convert it to an integer and push it onto the stack; finally, print the result after
the loop ends.
8. End
## Program:

/*
Program to evaluate the given prefix expression
Developed by: Varshini D
RegisterNumber: 212223230234
*/
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int s[50];
int top=0;
void push(int ch)
{
top++;
s[top]=ch;
}
int pop()
{
int ch;
ch=s[top];
top=top-1;
return(ch);
}
void evalprefix(char p[50])
{
int a,b,c,i;
for(i=strlen(p)-1;i>=0;i--)
{
if(p[i]=='+')
{
a=pop();
b=pop();
c=a+b;
push(c);
}
else if(p[i]=='*')
{
a=pop();
b=pop();
c=a*b;
push(c);
}
else
{
push(p[i]-48);
}
}
printf("%d",pop());
}



## Output:
![image](https://github.com/user-attachments/assets/26c180b4-5fd8-4867-812f-53d795d0d9c5)



## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
