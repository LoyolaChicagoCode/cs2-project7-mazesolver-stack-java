# Loyola COMP 271 Project 7: stack-based maze solver

## Group activity

In this activity, we'll implement a stack-based solver for mazes represented as two-dimensional arrays!

# Objectives

An understanding of the following concepts and techniques:

- two-dimensional arrays
- using stacks for depth-first search
- parametric thinking
- object-oriented design

# Description

In this lab, you will have the opportunity to develop a maze solver using stack-based backtracking.
The maze solver behaves as follows:

1. It first reads from the standard input the row and column of the starting point within the maze.
   *(The maze does not need to be square, but all of its rows must have the same width.)*  
1. It then reads from the standard input the maze data in the form of same-length strings representing rows in the maze.
   - \* represents a wall
   - \. represents an empty space we can visit
1. It then attempts to find a way out of the maze from the starting point.
1. Finally, it prints the maze showing 
   - the starting point as a 0 (zero)
   - unvisited cells as \. (dot)
   - visited cells (including those leading out) as + (plus)
   
## Example 1

Input followed by output: 
```
4 4
**********
*.....****
*.***...**
*.***.****
*.**....**
*.**.**.**
*....**...
***.******
*........*
**********

**********
*+++++****
*+***+..**
*+***+****
*+**0+++**
*+**+**+**
*++++**+++
***.******
*........*
**********

We're so out of here!
```

## Example 2

Input followed by output:
```
4 4
**********
*.....****
*.***...**
*.***.****
*.**....**
*.**.**.**
*....**..*
***.******
*........*
**********

**********
*+++++****
*+***+++**
*+***+****
*+**0+++**
*+**+**+**
*++++**++*
***+******
*++++++++*
**********

Bummer, we're stuck...
```

## Instructions

1. Complete the TODO items in the various sources until the program behaves as required. Recommended order:
    - constructor
    - print
    - read (in Main)
    - solve
    - tests

   *This is a short but complex project. You are encouraged to get started early and use the available supports.*   
1. Create at least one additional, *non-square* maze of size 10x10 or larger and with at least two exits.
1. As in the past, run the tests by pressing the green Run button or running `mvn test` in a console or shell window.
1. Also as before, to run the main program in a console or shell window:

       cd <your project's root directory>
       mvn compile
       mvn exec:java < maze1.txt
       ...

1. Answer the following questions in Answers.md:

    1. Why are the methods in the `Maze` class instance methods as opposed to static methods?
    1. Why is it generally advantageous to parameterize the `Maze.print` method with the output destination?
    1. What is the purpose of the `Maze.get` method, given that it is not used in `Main` or `Maze`?

# Submission

-    Make sure you have created a separate project for this activity.
-    Include a project-specific Answers.md file including your reflection and any other thoughts or design decisions.
-    In IDEA, export your project as a zip file and submit as an attachment.

# Grading (total 10 points)

- 5.5 completion of items marked TODO in `src/main` and correct behavior
- 0.5 additional non-square maze
- 2 tests for maze1 and your additional maze
- 2 written part
  - 1.5 responses to the questions above
  - 0.5 grammar, style, formatting

# Extra credit

- 2 Distinguish between the way out and dead-end attempts at the end.
In particular, represent visited cells leading to a dead end as - (minus).
- 1 Try with both a stack (LIFO) and an ordinary queue (FIFO) and briefly discuss your findings. 
- 1 Total for up to two additional non-square mazes of size greater than 10x10.
