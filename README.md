# Prim's-Algorithm

**Adjacency Matrix**
vector<vector<pair<int, int>>> adj(n + 1);

*operation*
adj[u].push_back(make_pair(v, w));  ---> both same
adj[u].emplace_back(v, w);  ---> both same
adj[u].size(); ---> get the out - degree of a node

**DFS trversal**
void dfs(int u, vector<bool> &visited) {
    visited[u] = true;
    for (auto [v, w] : adj[u]) {
        if (!visited[v]) dfs(v, visited);
    }
}

**Converting to edge Matrix**
vector<tuple<int, int, int>> edges;
for (int u = 1; u <= n; u++) {
    for (auto [v, w] : adj[u]) {
        edges.push_back({u, v, w});
    }
}







