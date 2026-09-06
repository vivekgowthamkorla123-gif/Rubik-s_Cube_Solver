# Rubik's Cube Solver using Korf's IDA*

A high-performance **Rubik's Cube solver implemented in C++**, exploring classical and heuristic search algorithms for efficient cube-state exploration. The project models the cube using object-oriented programming and focuses on optimizing state representation, hashing, and search performance.

## Overview

The solver implements and compares multiple search strategies before applying **Korf's IDA*** algorithm for more efficient solution search.

The project explores:

* 3D Rubik's Cube modeling using **C++ and OOP**
* Efficient representation of cube states
* **BFS, DFS, and IDDFS** search algorithms
* **IDA*** based on Korf's approach
* Optimized state exploration and hashing
* Compact cube-state representation using **nibble arrays**
* Performance and memory optimization

## Search Algorithms

### BFS

Breadth-First Search explores states level by level and guarantees the shortest solution, but its memory requirements grow rapidly with the search depth.

### DFS

Depth-First Search requires significantly less memory than BFS but does not guarantee an optimal solution and can spend substantial time exploring unproductive branches.

### IDDFS

Iterative Deepening Depth-First Search combines the low memory usage of DFS with the depth-optimal behavior of BFS by repeatedly increasing the depth limit.

### Korf's IDA*

The project uses **Iterative Deepening A*** to improve search efficiency. IDA* combines the memory efficiency of depth-first search with heuristic guidance to avoid exploring unnecessary cube states.

The algorithm repeatedly performs depth-first searches using an `f(n) = g(n) + h(n)` threshold, where the heuristic estimates the remaining distance to the solved state.

## Cube Representation

The Rubik's Cube is modeled as a 3D object using **object-oriented C++ design**. Cube operations are implemented for performing face rotations and generating successor states.

To improve search performance, the project uses:

* Compact cube-state encoding
* Optimized hashing
* Efficient state comparison
* Nibble arrays for reduced memory consumption

These optimizations are particularly important because IDA* may explore a very large number of cube states during deeper searches.

## Performance

The implemented search strategies were evaluated on progressively deeper scrambles.

* **BFS, DFS, and IDDFS** were tested on 8-move scrambles, with optimized exploration solving them in **under 4 seconds**.
* **Korf's IDA*** was applied to deeper scrambles and achieved **sub-10-second solutions for 12-move scrambles**.
* Compact state representation and optimized hashing helped reduce memory requirements and improve search efficiency.

## Technologies

* **C++**
* Object-Oriented Programming
* Graph Search Algorithms
* Heuristic Search
* IDA*
* Hashing
* Memory Optimization
* Data Structures
