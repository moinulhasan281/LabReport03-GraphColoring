# Graph Coloring Using Backtracking

### Problem Overview
This Python program solves the **Graph Coloring Problem** using the **Backtracking** technique. Given an undirected graph with `N` vertices and `M` edges, the task is to determine if the graph can be colored using `K` colors such that no two adjacent vertices share the same color. The program reads the input from a file, processes the graph, and outputs whether a valid coloring exists or not.


### Problem Description
The program reads the following input format:

1. **Three integers**: `N` (number of vertices), `M` (number of edges), and `K` (number of available colors).
2. Followed by `M` lines, each containing two integers `u` and `v`, representing an undirected edge between vertices `u` and `v`.

#### Input Format:

- **First line**: Three integers `N`, `M`, and `K`.
- **Next M lines**: Each line contains two integers `u` and `v`, representing an undirected edge between vertices `u` and `v`.

Example input:

4 5 3
0 1
0 2
1 2
1 3
2 3




### Output Format
- If the graph can be colored using `K` colors, the output should indicate that coloring is possible and display the color assignments for the vertices.
- If the graph cannot be colored using `K` colors, the output should indicate that coloring is not possible.

#### Example Output:
**Case 1:**

Coloring Possible with 3 Colors
Color Assignment: [1, 2, 3, 1]


**Case 2:**

Coloring Not Possible with 2 Colors

### Algorithm and Approach

#### Backtracking:
The algorithm works by attempting to assign colors to each vertex, starting from vertex 0. For each vertex, it tries to assign a color from `1` to `K`, ensuring that no two adjacent vertices share the same color. If a valid coloring is found, it returns the coloring assignment. If not, it backtracks and tries a different color.

#### Graph Representation:
The graph is represented as an **adjacency list** where each vertex is mapped to a list of its adjacent vertices.

#### Coloring Check:
A helper function checks if it is safe to assign a color to a vertex, ensuring that no adjacent vertex has the same color.



### Requirements
- Python 3.x
- No external libraries are required.



### How to Run

1. **Clone the repository** (if applicable):

bash
    git clone https://github.com/yourusername/graph-coloring-backtracking.git


2. **Navigate to the project directory**:

bash
    cd graph-coloring-backtracking
  

3. **Prepare the input file**:
   Create a file (e.g., `input_file.txt`) containing the graph description, where the first line contains the number of vertices, edges, and available colors, and the subsequent lines represent the edges of the graph.

4. **Run the Python script with the input file**:

bash
    python graph_coloring.py input_file.txt
  

   Replace `input_file.txt` with the actual file path containing your input.



### Code Explanation

- **Input Parsing**: The program reads input from a file where the first line contains the number of vertices, edges, and available colors. The following lines represent the edges of the graph.
- **Backtracking Function**: The `is_safe()` function checks if a color can be assigned to a vertex. The `graph_coloring()` function attempts to assign colors using backtracking.
- **Graph Representation**: The graph is represented using an adjacency list, which is efficient for storing and accessing the edges.
- **Output**: The result is printed, indicating whether a valid coloring is possible or not.



### Example Run

**For Case 1:**

**Input:**

4 5 3
0 1
0 2
1 2
1 3
2 3


**Output:**

Coloring Possible with 3 Colors
Color Assignment: [1, 2, 3, 1]


**For Case 2:**

**Input:**

4 5 2
0 1
0 2
1 2
1 3
2 3


**Output:**

Coloring Not Possible with 2 Colors


This readme gives a clear, structured overview of the program and how to use it. It explains the problem, input/output format, and provides examples along with the algorithm’s approach.
