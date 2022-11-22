# -DFS-Depth-First-Search
Bro Code DFS Tutorial

DFS = a search algorithm for traversing
    a tree or graph data structure

Steps:
    1. Pick a route
    2. Keep going until you reach a dead end,
        or a previously visited node
    3. Backtrack to last node the has unvisited
        adjacent neighbors

* Navigating a Maze:
    1. Travel a path until to reach a dead end
        1a. When you encounter forks, the protocol will dictate the first choose (EX: left first)
    2. Once a deadend is reached, go back to the last fork, and travel the other way
    3. Repeat until you reach the end

    ? Question: Is flooding where to release multiple "rats" to travel all avaiable paths?
        * Theory: Flooding is where all avalible paths are searched for and found
        ** So a 'Flood' in a since just sends data through every path

DFS "Go to I" Example:
    * Note, this uses a Stack interface

    A ------- B ------- C
    |                   |
    |                   |
    D ------- E         F
    |         |         |
    |         |         |
    G ------- H         I

First Path:

    A
    |
    |
    D ------- E
    |         |
    |         |
    G ------- H
Stack on First Path: *Starting at A, last is on top

        D
        E
        H
        G
        D
        A

Stack has a duplicate, 'D', so we will backtrack to the node with unvisited neighbors, 'A'

* To go back to A, pop off elements from the stack until you reach 'A'

* Stack after popping:

        A

2nd Path:

    A ------- B ------- C
                        |
                        |
                        F
                        |
                        |
                        I
* Stack on 2nd Path:

        I
        F
        C
        B
        A
*** 'I' reached!