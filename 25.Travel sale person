#include <stdio.h>
#include <limits.h>
#define N 4 
int min(int a, int b) {
    return (a < b) ? a : b;
}
int tsp(int graph[][N], int mask, int pos, int n, int dp[][N]) {
    if (mask == (1 << n) - 1) {
        return graph[pos][0]; 
    }
    if (dp[mask][pos] != -1) {
        return dp[mask][pos];
    }
    int ans = INT_MAX;
    for (int city = 0; city < n; city++) {
        if (!(mask & (1 << city))) {
            int newAns = graph[pos][city] + tsp(graph, mask | (1 << city), city, n, dp);
            ans = min(ans, newAns);
        }
    }
    return dp[mask][pos] = ans;
}
int main() {
    int graph[N][N] = {{0, 10, 15, 20},
                      {10, 0, 35, 25},
                      {15, 35, 0, 30},
                      {20, 25, 30, 0}};

    int dp[1 << N][N]; 
    for (int i = 0; i < (1 << N); i++) {
        for (int j = 0; j < N; j++) {
            dp[i][j] = -1;
        }
    }

    int minCost = tsp(graph, 1, 0, N, dp);
    printf("Minimum cost for Travel Sales Person: %d\n", minCost);

    return 0;
}
