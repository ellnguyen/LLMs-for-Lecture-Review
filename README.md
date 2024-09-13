# CPSC_354
Programming Languages

# IDENTIFICATION
- NAME: Ellie Nguyen
- ASSIGNMENT: Using LLMs for Literature Review
- DATE: September 15, 2024

# Assignment Description
This file documents my usage of an LLM to explore a question I have related to Programming Languages.

# LLM Literature Review

In Towers of Hanoi, I saw an example of how recursion can simplify a complex problem into concise, repeatable code. An important motive of the game is to minimize the number of moves taken to complete the level. This led me to think of other performance problems, and how different languages or algorithms might handle certain constraints to efficiently solve these problems.

Particularly, the optimization problem in Hanoi reminded me of shortest path algorithms because they both involve finding an optimal path or sequence of moves to achieve a goal. In Towers of Hanoi, as more disks are added, the complexity (or number of minimum moves) increases. Similarly, as the distance between a starting point and ending point increases, so does the complexity of finding the shortest path between them. 

This connection between Towers of Hanoi and shortest path algorithms led to my first question: 

## What are some important concepts in the intersection between towers of hanoi and shortest path algorithms?

A few points from its response are listed below: 

>1. State Space Representation: Both problems can be represented as state spaces where each state represents a configuration of the problem (e.g., the arrangement of disks in Towers of Hanoi or nodes in a graph).
>
>2. Complexity Analysis: Both problems are analyzed in terms of computational complexity. Towers of Hanoi has an exponential time complexity, while shortest path algorithms (like Dijkstra's) can have polynomial time complexity, depending on the graph structure.
>
>3. Graph Theory: The Towers of Hanoi problem can be modeled as a graph where nodes represent states and edges represent valid moves. Shortest path algorithms can then be applied to this graph representation.
>
>4. Recursive Algorithms: The Towers of Hanoi is naturally recursive, and recursive strategies can also be used in shortest path algorithms (e.g., dynamic programming approaches).


To summarize, ChatGPT brings up some interesting ways of representing the two problems. For instance, both problems can be represented as state spaces where each state is a configuration of the problem. That is, the state may be
1. the arrangement of disks in Towers of Hanoi
2. or nodes in a graph

and the state transitions occur when 
1. moving disks 
2. or when moving from one node to another

ChatGPT also mentioned that, similar to how a shortest path problem is represented, the Towers of Hanoi problem can be modeled as a graph. This can be done by denoting the states as nodes and the edges as valid moves from one state to another. Then, shortest path algorithms, like breadth-first search (BFS), can be applied in this graph representation to determine the shortest sequence of moves. 

I found it interesting that we can represent Towers of Hanoi as a graph, and I wanted to know if doing this will provide a more efficient solution. To follow up, I asked

## If a shortest path algorithm is applied to towers of hanoi, how does this solution compare to the recursive one? How does the complexity change?

It came up with this response:

>Recursive Solution: Uses a divide-and-conquer approach with a time complexity of $O(2^n)$, where $n$ is the number of disks. The recursive solution is more intuitive but less efficient in terms of state exploration.
>
>Shortest Path Algorithm: When using BFS on the graph representation of Towers of Hanoi, the time complexity remains $O(2^n)$ due to the exponential growth of the state space. BFS might be more systematic in exploring states, but it doesn’t reduce the complexity compared to the recursive approach.
>
>In summary, while the shortest path algorithm provides a systematic way to find the solution, it doesn't offer a significant improvement in complexity over the recursive method for Towers of Hanoi. Both methods have exponential time complexity.

I was a bit suprised that rearranging the problem in a very different way can still lead to about the same time complexity.

To put things in a more broad perspective, I see this as an example of how there could be multiple different ways to solve the same problem. And, even though their complexities are about the same, each comes with its own costs and benefits. For instance, while the recursive approach is more intuitive, the shortest path algorithm is more systematic in state exploration. 

## What relevant subfields of programming languages contributed to towers of hanoi and graph theory?

>1. Recursive Programming: Essential for implementing the solution to the problem.
>2. Algorithm Design: Focuses on understanding and analyzing recursive algorithms.
>3. Educational Programming Languages: Used to teach recursion and problem-solving.
>Graph Theory
>1. Graph Algorithms: Includes shortest path algorithms and other methods for graph traversal.
>2. Data Structures: Adjacency lists and matrices for graph representation.
>3. Computational Complexity: Analyzes the efficiency of graph algorithms.

## What references can I read more about this?

These are some papers it gave me about the Towers of Hanoi problem and its connection with graph theory and shortest path algorithms. The resources are linked below.

1. [Variations on the Four-Post Tower of Hanoi Puzzle](https://www.cs.wm.edu/~pkstoc/boca.pdf)
2. [Hanoi graph](https://en.wikipedia.org/wiki/Hanoi_graph#:~:text=In%20graph%20theory%20and%20recreational,moves%20between%20pairs%20of%20states.)

The image below is taken from source 2. It shows the Hanoi graph for a puzzle with 3 disks on 3 towers. 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2c/Tower_of_hanoi_graph.svg/langcy-450px-Tower_of_hanoi_graph.svg.png)

3. [Computing the Shortest Path: A* Search Meets Graph Theory](https://faculty.cc.gatech.edu/~thad/6601-gradAI-fall2012/02-search-Goldberg03tr.pdf)

4. [Graphs S(n, k) and a Variant of the Tower of Hanoi Problem](https://link.springer.com/article/10.1023/A:1022444205860)
