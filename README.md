# Pass-by-val-ref
#include <stdio.h>
#include <conio.h>

void swapref(int *, int *); 
void swapval(int, int)

int main()
{
    int a, b; 
    clrscr();   // Clears the screen (works only in Turbo C, not in modern compilers)

    printf("Enter value for A: ");
    scanf("%d", &a);

    printf("Enter value for B: ");
    scanf("%d", &b);

    // Pass by Reference
    swapref(&a, &b);
    printf("\nValues after Pass by Reference \n"); 
    printf("Value of A : %d \n", a);
    printf("Value of B : %d\n", b);

    // Pass by Value
    swapval(a, b);
    printf("\nValues after Pass by Value \n");
    printf("Value of A : %d \n", a); 
    printf("Value of B : %d\n", b);

    getch();
    return 0;
}

/* Pass by Value */
void swapval(int p, int q)
{
    int t; 
    t = p; 
    p = q; 
    q = t;   // fixed mistake (was using 'r' which is undefined)
}

/* Pass by Reference */
void swapref(int *x, int *y)
{
    int t; 
    t = *x;
    *x = *y;
    *y = t;
}
