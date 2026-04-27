#include <stdio.h>
#include <omp.h>

int main() {
    int n, i;

    printf("\n****RUNNING MINIMUM OF ARRAY****\n");
    printf("Enter the size: ");
    scanf("%d", &n);

    int a[n], prefix[n];

    printf("Enter the elements: ");
    for (i = 0; i < n; i++)
        scanf("%d", &a[i]);

    prefix[0] = a[0];
    for (i = 1; i < n; i++)
        prefix[i] = (prefix[i - 1] < a[i]) ? prefix[i - 1] : a[i];

    printf("Prefix minimum array: ");
    for (i = 0; i < n; i++)
        printf("%d ", prefix[i]);

    printf("\n\n");
    return 0;
}
