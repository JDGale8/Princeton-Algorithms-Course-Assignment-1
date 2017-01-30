# Assignment 1 - Percolation
Part of the Princeton Algorithms I course on Coursera.

## Problem

This is an application of the Dynamic connectivity problem.
The course covers the development of an algorithm to find whether two points are connected.
The problem outlined is asking the user to computationally find the time at which a `n x n` grid percolates, meaning there is a path from the top to the bottom.

This is done by creating two virtual notes, above and below the grid, and checking if, at any time, these two are connected.
More information on this problem and percolation can be found [here](http://coursera.cs.princeton.edu/algs4/assignments/percolation.html)

## Algorithm
A number of iterative solutions to the Dynamic connectivity problem are solved, including quick find, and quick union.
Eventually a solution with a time of order `O(lg(n))` is found. This is the `weighted tree quick union` algorithm, and is what is used in this solution.

The course provides a read-only java file for this algorithm, but in the src folder I have provided my own as well. 
The provided files are in the `./libs` folder.

The report in `./report` shows the results for the automatic grading of the test. The solution solves 90% of the required amounts but falls short due to a backwash problem. More info on the backwash problem [here](http://www.sigmainfy.com/blog/avoid-backwash-in-percolation.html).

I tried solving it using bitwise operators to add layered state information for each node and each node's parent. Although it worked in most general cases, it did not solve the backwash problem.



