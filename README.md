# JavaBFSCalc
    this is a part of ITIS java training, in this task we need to implement a solution for the next game:

## The task
    given two number a and b and a set of mathematical operations, can you find the shortest path from a to b
    using only the provided operations ?
    example : given a = 5, b = 2000 can you find the shortest path if it exists using only add_3 (+3) and multiply_4 (*4)

-    5 =>  multiply_4 , add_3 , add_3 , add_3 , multiply_4 , add_3 , add_3 , add_3 , multiply_4 , multiply_4  => 2000 ( in 10 steps )

## The solution
    I used a BFS method to find the shortest path, at each step I update the list of adjacency of a given element by applying all the operations
    to it, we can add a list that contains a history of all elements to avoid cyrcles

## The implementation
    The ShortestPath method from BFS_Search class, takes two integers a and b and a variadic parameter rules being a PremitiveAction type,
    The class Rules contains some ready operations that could be used, you can add any integer operation (Z -> Z) as we deal with integers only
    The prototype of the operation should be  int action (int v,StringBuilder name); as it need to conform the interface PrimitiveAction, the second parameter
        name is used to get the name of the function to contruct the trace
    