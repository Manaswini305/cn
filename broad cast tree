
Aim: Write a C program to obtain Board cast Tree for a subnet of hosts. 

Program:

#include <stdio.h>
void adj(int a[20][20], int n, int k);
int main() {
    int i, j, n, root, a[20][20];
    printf("Enter number of nodes: ");
    scanf("%d", &n);
    printf("Enter adjacency matrix:\n");
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n; j++) {
            scanf("%d", &a[i][j]);
        }
    }
    printf("Enter root node: ");
    scanf("%d", &root);
    adj(a, n, root);
    return 0;
}
void adj(int a[20][20], int n, int k) {
    int i, j, visited[20] = {0};  
    for (j = 1; j <= n; j++) {
        if (a[k][j] == 1 || a[j][k] == 1) {
            visited[j] = 1;
            printf("%d -> %d\n", k, j);
        }
    }
    printf("\n");
    for (i = 1; i <= n; i++) {
        if ((a[i][k] == 0) && (i != k)) {
            for (j = 1; j <= n; j++) {
                if (a[i][j] != 0 && visited[i] != 1) {
                    visited[i] = 1;
                    printf("%d -> %d\n", j, i);
                }
            }
        }
    }
}





Output:
Enter number of nodes: 4
Enter adjacency matrix:0 1 1 0
1001
1001
0110
Enter root node: 2
2->1
2->4

1->3
