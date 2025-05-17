# Ex 1 e Stack Operations
## DATE: 28/02/2025
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1. Initialize top as -1 and declare stack as a character array.
2. To push, increment top and assign the character to stack[top].
3. To pop, check if top is -1 and return -1 if true.
4. If not, return stack[top] and decrement top.

## Program:

```
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Varshini D
RegisterNumber: 212223230234
```
char stack[100];
int top = -1;
void push(char x)
{
 stack[++top] = x;
}
char pop()
{
 if(top == -1)
 return -1;
 else
 return stack[top--];
}


## Output:

![image](https://github.com/user-attachments/assets/59341887-7ef7-424d-a6a0-f5ba67277f5d)


## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
