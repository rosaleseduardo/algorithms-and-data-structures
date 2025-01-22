<div align = "center">
  <img
    src = "./assets/logo.png"
    width = "80%"
    alt = "repo-logo" />
</div>

<hr>

## Table of Contents

- [What is the Big O?](#what-is-the-big-o)
- [Techniques](#techniques)

Extra Important Official References

- [What is Big O Notation Explained: Space and Time Complexity](https://www.freecodecamp.org/news/big-o-notation-why-it-matters-and-why-it-doesnt-1674cfa8a23c/)
- [Learn Big O Notation In 12 Minutes](https://drive.google.com/file/d/1oad1yMHhsvL0hrxSY5hr5hl2YUqmn6o1/view?usp=drive_link)

# What is the Big O?

Metric used in Software Engineering to measure the efficiency of our algorithms.
It is essential for determining how our algorithms will perform under a high
workload.

Time is not the only important factor when analyzing an algorithm. The amount of
memory used can also be highly relevant. Typically, trade-offs are made between
time complexity and space complexity, as improving one often leads to worsening
the other.

Therefore, the goal is to find a good balance between the two complexities and
choose the one that best suits our needs, given our specific conditions.

# Techniques

## Two Pointers

Get an undertanding of the technique by taking a look at these resources:

- [AlgoMaster Newsletter - Two Pointers](https://blog.algomaster.io/p/69025a2e-b0d5-4705-8507-bba16c2691f1)
- [YouTube - How to Use the Two Pointer Technique](https://www.youtube.com/watch?v=-gjxg6Pln50)

### General Indicators to use it:

- **Linearity:** The problem involves linear traversal or optimization. It means
  that the problem can be solved by examining or processing the elements of a
  sequence (such as an array, string, or linked list) in a linear fashion (i.e.,
  one element at a time, from start to finish, or by controlled movement of
  pointers).
- **Two Ends:** Conditions are best evaluated from both ends of a structure.
- **Adjustable Window:** The solution can be found by expanding or shrinking a
  range.
- **Sorting Advantage:** Sorted data simplifies the logic for satisfying
  conditions.

Here are the primary contexts where the Two Pointers technique shines:

1. **Finding Pairs or Triplets**

   When searching for pairs or groups of elements that satisfy a condition.

   Examples:

   - Find two numbers in a sorted array that sum to a target (Two Sum
     problem).
   - Find all unique triplets in an array that sum to zero (3Sum
     problem).

   Why Useful?
   Reduces complexity from O(n2)O(n2) or O(n3)O(n3) to O(n)O(n) or
   O(n2)O(n2).

2. **Searching in Sorted Arrays**

   When working with sorted data, the Two Pointers technique can efficiently
   explore the range of elements.

   Examples:

   - Checking for duplicates.
   - Identifying elements within a specific range.

   Why Useful?
   Sorted data allows the pointers to adjust dynamically without re-evaluating
   all elements.

3. **Sliding Window Problems**

   When dealing with subarray or substring problems, where a window of elements
   is expanded and contracted.

   Examples:

   - Longest substring without repeating characters.
   - Maximum or minimum subarray sum.
   - Smallest subarray with a given sum.

   Why Useful?
   Avoids recalculating values repeatedly by maintaining a running
   total or condition.

4. **Palindromes and Mirror-like Problems**

   When comparing elements from both ends toward the center.

   Examples:

   - Checking if a string is a palindrome.
   - Finding the longest palindromic substring.

   Why Useful?
   Eliminates the need for redundant checks or nested loops.

5. **Partitioning Problems**

   When splitting data into two or more parts based on specific criteria.

   Examples:

   - Dutch National Flag problem (partitioning into three groups).
   - Rearranging elements (e.g., all negatives before positives).

   Why Useful?
   Processes elements in-place with minimal extra space.

6. **Cycle Detection**

   In problems involving cyclic structures, like linked lists or graphs.

   Examples:

   - Detecting a cycle in a linked list (Floyd’s Cycle Detection).
   - Finding the starting point of a cycle.

   Why Useful?
   Uses two pointers (slow and fast) to detect cycles efficiently.

7. **Merging Intervals or Arrays**

   When working with sorted intervals or arrays that need to be combined or
   processed together.

   Examples:

   - Merging two sorted arrays.
   - Merging overlapping intervals.

   Why Useful?
   Maintains order and processes elements with O(n)O(n) complexity.

8. **Optimizing Space or Time Complexity**

   When aiming to solve problems that can be brute-forced in O(n2)O(n2) or
   O(n3)O(n3) but want to optimize to O(n)O(n) or O(nlog⁡n)O(nlogn).

   Examples:

   - Maximize/minimize distances, sums, or other metrics between elements.

## Sliding Window Pattern

- https://blog.algomaster.io/p/f4412a17-7a3a-4d0b-8e39-9ea8f429bf7c
- https://drive.google.com/file/d/1CTRJ3O99iUn8okB3waIQ_2ejOwskskcC/view?usp=drive_link

## Prefix Sum Pattern

- https://www.youtube.com/watch?v=yuws7YK0Yng
- https://drive.google.com/file/d/1GKyMyo6JjgeWvZIem8eKn8WEPCrTyxE8/view?usp=drive_link

1. Understand the Problem

   What is the problem asking for?
   Identify the input, output, and constraints clearly.
   What type of problem is this?
   Common types include searching, sorting, optimization, combinatorics, or
   dynamic programming.
   What edge cases or special conditions should I handle?
   Think about edge cases like empty inputs, large numbers, or invalid data.

2. Analyze the Input and Output

   What is the structure of the input data?
   Is it a string, array, matrix, tree, or graph? This can hint at applicable patterns.
   What size can the input grow to?
   If the input is large, you may need an efficient pattern, like sliding window or divide and conquer.
   Is the output a single value, a subset of input, or something else?

3. Explore Constraints and Optimization

   What are the performance constraints?
   E.g., can a brute-force solution work within the limits, or is an optimized pattern necessary?
   Is there a time-space tradeoff to consider?
   Can you reduce time complexity by using more space, or vice versa?
   Are the constraints restrictive enough to enable specific optimizations?
   E.g., "the array is sorted" might point toward binary search.

4. Test the Problem for Feasibility

   Can I break the problem into smaller subproblems?
   If yes, consider divide and conquer or recursion.
   Can the problem be solved incrementally?
   Patterns like sliding window or greedy algorithms may work.
   Can I precompute results for efficiency?
   If yes, try preprocessing or caching techniques.

5. Evaluate Patterns for Fit

   Which known patterns align with the problem?
   Examples of patterns:
   Two pointers/sliding window for subarray problems.
   Greedy for optimization problems with local decisions.
   Backtracking for combinations and permutations.
   BFS/DFS for tree/graph traversal.
   Dynamic programming for overlapping subproblems.
   How does the pattern reduce complexity or improve clarity?
   Ensure the chosen pattern simplifies implementation.

6. Validate and Refine

   Can I explain the logic of my chosen pattern?
   If not, revisit and reassess.
   How will I test my solution against edge cases?
   Plan tests to validate the robustness of the pattern.
   Is my implementation scalable?
   Will it handle the largest possible inputs efficiently?
