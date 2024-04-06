
# GraphLibrary

GraphLibrary is a versatile C++ library designed for graph representation and manipulation. It supports both directed and undirected graphs, with the option for weighted edges. The library offers a range of functionalities including cycle detection, topological sorting, finding strongly connected components, minimum spanning tree construction, and more.

## Features

- Support for both directed and undirected graphs.
- Optional edge weighting.
- Cycle detection.
- Topological sorting (for Directed Acyclic Graphs - DAGs).
- Strongly connected components (Kosaraju's algorithm).
- Minimum Spanning Tree (Kruskal's algorithm).
- Eulerian Path and Cycle detection.
- Maximum flow (Ford-Fulkerson algorithm).
- Shortest path finding using Dijkstra's algorithm.
- Graph serialization and deserialization to/from files.
- Vertex naming for improved readability.


## Installation

To use GraphLibrary, include GraphLibrary.h in your project directory. Ensure your build system can locate this header file, and include it in your source files where graph functionality is required:

```cpp
  #include "GraphLibrary.h"
```
No additional libraries are required for the core functionality.
    
## Deployment

To deploy this project run

```bash
  npm run deploy
```


## Usage/Examples

Creating a Graph

```cpp
// Create a directed, weighted graph with 5 vertices
Graph myGraph(5, true, true);
```
Adding Edges and Vertices
```cpp
// Adding a directed edge with a weight
myGraph.addDirectedEdge(0, 1, 10);

// Adding an undirected edge with default weight
myGraph.addUndirectedEdge(2, 3);

// Naming vertices for better readability
myGraph.addVertexName(0, "A");
myGraph.addVertexName(1, "B");
```
Utility Methods
```cpp
// Check if the graph contains a cycle
bool hasCycle = myGraph.isCyclic();

// Find strongly connected components
auto sccs = myGraph.getStronglyConnectedComponents();

// Print graph
myGraph.printGraph();
```
Serialization and Deserialization
```cpp
// Save graph to file
myGraph.saveToFile("myGraph.txt");

// Load graph from file
Graph loadedGraph(0);
loadedGraph.loadFromFile("myGraph.txt");

```

Finding the Shortest Path
```cpp
// Find shortest paths from vertex 0 using Dijkstra's algorithm
std::vector<int> distances = g.dijkstra(0);

// Print shortest distances
for (size_t i = 0; i < distances.size(); i++) {
    std::cout << "Distance from 0 to " << i << ": " << distances[i] << std::endl;
}

```


## Contributing

Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change.

Please ensure to update tests as appropriate.
## Support

For support, email sahs82341@gmail.com 

