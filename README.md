# Prim's Algorithm (Minimum Spanning Tree): Implementation & Time Analysis

A Jupyter notebook implementing and analyzing **Prim's algorithm** in Python to find the **Minimum Spanning Tree (MST)** of a connected, undirected, weighted graph.

## Features
- Weighted graph class using an adjacency list
- Prim's algorithm with a **min-heap (priority queue)** — `O(E log V)`
- Prim's algorithm with a simple **array scan** — `O(V²)`
- Interactive user input for custom weighted edges and a starting vertex
- Real runtime measurement using Python's `time` module
- Time and space complexity analysis for both implementations
- Graph visualization with the MST highlighted (via `networkx` / `matplotlib`)
- Verification of results against `networkx`'s built-in MST
- Runtime comparison of heap vs array versions on **sparse** and **dense** random graphs, with charts

## Getting Started
1. Clone the repo
2. Install dependencies: `pip install jupyter matplotlib networkx`
3. Open `prims_algorithm_analysis.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab
4. Run the cells top to bottom — demo cells use a sample graph by default; swap in `get_user_edges()` / `get_user_start_node(nodes)` (no arguments) to enter your own graph

## Complexity Summary

| Implementation        | Time Complexity | Space Complexity | Best For       |
|-------------------------|-------------------|---------------------|------------------|
| Prim's with min-heap    | O(E log V)         | O(V + E)             | Sparse graphs    |
| Prim's with array scan  | O(V²)              | O(V)                 | Dense graphs     |

Where `V` = number of vertices, `E` = number of edges.

Prim's is a **greedy** algorithm: it repeatedly adds the cheapest edge crossing the cut between the growing tree and the remaining vertices, which is provably optimal by the cut property. An MST of a connected graph with `V` vertices always has exactly `V − 1` edges.

## License
MIT
