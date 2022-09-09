# reversing-of-array
This is a program for reversing complete array using functions and swapping in C programming.


#include <stdio.h>
void arrayprint(int a[]);
void arrarev(int a);

int main()
{
    int a[] = {1, 2, 3, 4, 5, 6, 89};
    printf("\nBefore reversing:");
    arrayprint(a);
    arrayrev(a);
    printf("\nAfter reversing:");
    arrayprint(a);
    return 0;
}

void arrayprint(int a[])
{
    for (int i = 0; i < 7; i++)
    {
        printf("The value of element %d is %d\n", i, a[i]);
    }
}

void arrayrev(int a[])
{
    int t;
    for (int i = 0; i < 7 / 2; i++)
    {
        t = a[i];
        a[i] = a[6 - i];
        a[6 - i] = t;
    }
}

Output:
Before reversing:
The value of element 0 is 1
The value of element 1 is 2
The value of element 2 is 3
The value of element 3 is 4
The value of element 4 is 5
The value of element 5 is 6
The value of element 6 is 89

After reversing:
The value of element 0 is 89
The value of element 1 is 6
The value of element 2 is 5
The value of element 3 is 4
The value of element 4 is 3
The value of element 5 is 2
The value of element 6 is 1
