#include <stdio.h>

int main() {
    int A[3][3], B[3][3];
    int sum[3][3], mul[3][3];
    int i, j, k;

    // Input Matrix A
    printf("Enter elements of Matrix A (3x3):\n");
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            scanf("%d", &A[i][j]);
        }
    }

    // Input Matrix B
    printf("Enter elements of Matrix B (3x3):\n");
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            scanf("%d", &B[i][j]);
        }
    }

    // Matrix Addition
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            sum[i][j] = A[i][j] + B[i][j];
        }
    }

    // Matrix Multiplication
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            mul[i][j] = 0;
            for(k = 0; k < 3; k++) {
                mul[i][j] += A[i][k] * B[k][j];
            }
        }
    }

    // Print Addition Result
    printf("\nMatrix Addition Result:\n");
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            printf("%d ", sum[i][j]);
        }
        printf("\n");
    }

    // Print Multiplication Result
    printf("\nMatrix Multiplication Result:\n");
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            printf("%d ", mul[i][j]);
        }
        printf("\n");
    }

    return 0;
}
