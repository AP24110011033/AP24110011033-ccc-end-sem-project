#include <stdio.h>
#include <limits.h>

#define MAX 100
#define INF 99999

// ---------- DIJKSTRA ----------

int minDistance(int dist[], int visited[], int n) {
    int min = INT_MAX, min_index = -1;

    for (int i = 0; i < n; i++) {
        if (!visited[i] && dist[i] <= min) {
            min = dist[i];
            min_index = i;
        }
    }
    return min_index;
}

void dijkstra(int graph[MAX][MAX], int n, int src) {
    int dist[MAX], visited[MAX];

    for (int i = 0; i < n; i++) {
        dist[i] = INT_MAX;
        visited[i] = 0;
    }

    dist[src] = 0;

    for (int count = 0; count < n - 1; count++) {
        int u = minDistance(dist, visited, n);
        if (u == -1) break;

        visited[u] = 1;

        for (int v = 0; v < n; v++) {
            if (!visited[v] && graph[u][v] &&
                dist[u] != INT_MAX &&
                dist[u] + graph[u][v] < dist[v]) {

                dist[v] = dist[u] + graph[u][v];
            }
        }
    }

    printf("\n--- Dijkstra (Greedy) Result ---\n");
    for (int i = 0; i < n; i++) {
        printf("Distance from %d to %d = %d\n", src, i, dist[i]);
    }
}

// ---------- FLOYD WARSHALL ----------

void floydWarshall(int graph[MAX][MAX], int n) {
    int dist[MAX][MAX];

    // Copy graph
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (graph[i][j] == 0 && i != j)
                dist[i][j] = INF;
            else
                dist[i][j] = graph[i][j];
        }
    }

    // DP logic
    for (int k = 0; k < n; k++) {
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if (dist[i][k] + dist[k][j] < dist[i][j]) {
                    dist[i][j] = dist[i][k] + dist[k][j];
                }
            }
        }
    }

    printf("\n--- Floyd Warshall (DP) Result ---\n");
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (dist[i][j] == INF)
                printf("INF ");
            else
                printf("%d ", dist[i][j]);
        }
        printf("\n");
    }
}

// ---------- MAIN ----------

int main() {
    int n, graph[MAX][MAX], choice, src;

    printf("Enter number of vertices: ");
    scanf("%d", &n);

    printf("Enter adjacency matrix (0 if no edge):\n");
    for (int i = 0; i < n; i++)
        for (int j = 0; j < n; j++)
            scanf("%d", &graph[i][j]);

    while (1) {
        printf("\n===== MENU =====\n");
        printf("1. Dijkstra (Greedy)\n");
        printf("2. Floyd Warshall (DP)\n");
        printf("3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter source vertex: ");
                scanf("%d", &src);
                if (src < 0 || src >= n) {
                    printf("Invalid source!\n");
                } else {
                    dijkstra(graph, n, src);
                }
                break;

            case 2:
                floydWarshall(graph, n);
                break;

            case 3:
                printf("Exiting program...\n");
                return 0;

            default:
                printf("Invalid choice!\n");
        }
    }
}
