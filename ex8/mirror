#include <stdio.h>
#include <omp.h>

int main() {
    int n, m, i, j;
    printf("\n****MIRROR OF THE MATRIX****\n");
    printf("Enter the rows and columns: ");
    scanf("%d %d", &n, &m);
    int a[n][m];
    for (i = 0; i < n; i++)
        for (j = 0; j < m; j++)
            scanf("%d", &a[i][j]);

    #pragma omp parallel for
    for (i = 0; i < n; i++) {
        for (j = 0; j < m / 2; j++) {
            int temp = a[i][j];
            a[i][j] = a[i][m - j - 1];
            a[i][m - j - 1] = temp;
        }
    }

    printf("Mirror Matrix:\n");
    for (i = 0; i < n; i++) {
        for (j = 0; j < m; j++)
            printf("%d ", a[i][j]);
        printf("\n");
    }
    printf("\n");
    return 0;
}
