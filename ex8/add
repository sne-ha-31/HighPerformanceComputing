#include <stdio.h>
#include <stdlib.h>
#include <omp.h>

int main()
{
    int *A;
    int SIZE, i, constant;

    printf("\n****ADDITION OF CONSTANT WITH ARRAYS****\n");
    printf("\nEnter size of array: ");
    scanf("%d", &SIZE);

    printf("Enter constant value to add: ");
    scanf("%d", &constant);

    A = (int*) malloc(SIZE * sizeof(int));

    for(i = 0; i < SIZE; i++)
    {
        A[i] = i;
    }

    #pragma omp parallel for num_threads(4)
    for(i = 0; i < SIZE; i++)
    {
        A[i] = A[i] + constant;
    }

    printf("First 50 elements after adding constant:\n");
    for(i = 0; i < SIZE && i < 50; i++)
    {
        printf("%d ", A[i]);
    }
    printf("\n\n");

    free(A);
    return 0;
}
