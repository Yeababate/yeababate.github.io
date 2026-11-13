{
  "title": "Stations Pathfinder",
  "description": "A Go train-routing simulation. I was responsible for the pathfinding algorithm, using BFS and Edmonds–Karp maximum flow to find routes through a capacity-constrained railway network.",
  "summary": "A Go train-routing simulation with capacity-aware pathfinding. My responsibility was the algorithm.",
  "weight": 5,
  "technologies": [
    "Go"
  ],
  "source": "https://github.com/Yeababate/pathfinder",
  "category": "05 / ALGORITHMS · TEAM PROJECT",
  "tags": [
    "Go",
    "Algorithms"
  ]
}

A command-line train dispatching simulation that reads a railway network and produces turn-by-turn movement instructions for multiple trains.

## My contribution

I was responsible for the pathfinding algorithm. The implementation models the railway as a capacity-aware flow network, uses breadth-first search to find augmenting paths, and applies the Edmonds–Karp maximum-flow algorithm to discover routes.

## The algorithmic challenge

Finding a single short route is not enough when several trains share the network. Intermediate stations have limited capacity, so routes must account for those constraints.

The implementation splits intermediate stations into inbound and outbound nodes connected by a capacity-one edge. A residual network supports flow updates, and the resulting flow is used to extract routes for the train scheduler.

## What the project does

- Parses and validates station maps and connections.
- Finds routes between the start and destination stations.
- Distributes trains across available routes.
- Outputs movements one turn at a time.

[View source on GitHub](https://github.com/Yeababate/pathfinder)
