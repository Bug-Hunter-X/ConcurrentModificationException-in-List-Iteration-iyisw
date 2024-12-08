# ConcurrentModificationException in Java List Iteration

This repository demonstrates a common error in Java involving the `ConcurrentModificationException` when modifying a list while iterating using a standard `for` loop.  The example shows how to reproduce the error and the proper way to fix it using an `Iterator`.

## Problem

The provided `ConcurrentModificationExceptionExample.java` demonstrates a program that attempts to remove even numbers from a list. However, it does so in a way that triggers a `ConcurrentModificationException` because it directly modifies the list's structure while iterating using the index-based for loop.

## Solution

The solution, `ConcurrentModificationExceptionExampleSolution.java`, utilizes an `Iterator` to safely remove elements. This ensures that the list's internal structure is modified in a way that the `Iterator` is aware of. 