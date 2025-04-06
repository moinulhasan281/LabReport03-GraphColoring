Graph Coloring using Backtracking
Problem Overview
This program solves the Graph Coloring Problem using the Backtracking technique. Given an undirected graph with N vertices and M edges, the task is to determine if the graph can be colored using K colors such that no two adjacent vertices share the same color. The program reads input from a file and outputs the result based on the possibility of a valid coloring.

Problem Description
The program reads the following input format:

Three integers: N (number of vertices), M (number of edges), and K (number of available colors).

M lines follow, each containing two integers u and v, representing an undirected edge between vertices u and v.

Input Format:
First Line: Three integers: N (number of vertices), M (number of edges), and K (number of available colors).

Following M lines: Each contains two integers u and v, representing an undirected edge between vertices u and v.

Example Input:
Case 1:
Copy
Edit
4 5 3
0 1
0 2
1 2
1 3
2 3
Case 2:
Copy
Edit
4 5 2
0 1
0 2
1 2
1 3
2 3
Output Format:
If the graph can be colored using K colors, the output should indicate that coloring is possible and display the color assignments for the vertices.

If the graph cannot be colored using K colors, the output should indicate that coloring is not possible.

Example Output:
Case 1:
csharp
Copy
Edit
Coloring Possible with 3 Colors
Color Assignment: [1, 2, 3, 1]
Case 2:
csharp
Copy
Edit
Coloring Not Possible with 2 Colors
Algorithm and Approach
Backtracking: The algorithm attempts to assign colors to each vertex starting from vertex 0. For each vertex, it tries to assign a color from 1 to K, ensuring that no two adjacent vertices share the same color. If it finds a valid coloring, it returns the coloring assignment; otherwise, it backtracks and tries a different color.

Graph Representation: The graph is represented as an adjacency list where each vertex is mapped to a list of its adjacent vertices.

Coloring Check: A helper function checks if it is safe to assign a color to a vertex, ensuring that no adjacent vertex has the same color.

Requirements
Python 3.x

No external libraries are required.

How to Run
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/graph-coloring-backtracking.git
Navigate to the project directory:

bash
Copy
Edit
cd graph-coloring-backtracking
Run the Python script with the input file:

nginx
Copy
Edit
python graph_coloring.py input_file.txt
Make sure to replace input_file.txt with the actual file containing your input.

Code Explanation
Input Parsing: The input is read from a file, where the first line contains the number of vertices, edges, and available colors. The subsequent lines represent the edges of the graph.

Backtracking Function: The function is_safe() checks if a color can be assigned to a vertex. The graph_coloring() function tries to assign colors using backtracking.

Graph Representation: The graph is stored as an adjacency list for efficient traversal.

Output: The result is printed to indicate whether a valid coloring is possible or not.

Example Run
For Case 1:

vbnet
Copy
Edit
Input:
4 5 3
0 1
0 2
1 2
1 3
2 3

Output:
Coloring Possible with 3 Colors
Color Assignment: [1, 2, 3, 1]
For Case 2:

vbnet
Copy
Edit
Input:
4 5 2
0 1
0 2
1 2
1 3
2 3

Output:Coloring Not Possible with 2 Colors
