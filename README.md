# interview-questions

The purpose of this repository is twofold:

  1. To document questions I am asked and to provide for my own erudition a
      more complete solution than I am able to provide under the time constraints of
      an interview.
  2. To provide a bank of questions that I have to ask potential candidates when I
      am on the other end of the interview.

For both cases, a fully worked through set of solutions is more valuable for my
understanding and for my ability to parse a candidate's approach.

## The questions.

I'll list here the top level description of the questions, and link to the
relevant code samples appropriately.


### Lowest Common Ancestor

This problem is a pretty good data structures and algorithms question, touching
on binary search trees at the least and probably stacks for most candidates. It
also is a great algorithm question because there are a few pieces of iteration
that we can go through on how to improve the algorithm.

#### Problem statement

Given a binary search tree of size `n` and a list of `k` targets, find their
lowest common ancestor. For example, in the binary search tree

```
      4
     / \
    2   5
   / \
  1   3
```

with the targets `[1, 3]`, the lowest common ancestor is 2.

#### Key components:
- Understanding how a binary search tree works, implementing a node class
- Understanding the stack based approach
- Using min/max instead of the whole list of targets
- Using top down recursion instead of a stack
- Understanding order notation of the algorithm, however they implement it.
- If they use min/max or top-down recursion, calling out the possibility of the
  target not existing in the tree, and the runtime complexity implications of
  validating its existence.

### Disjoint Ranges:

This problem doesn't touch much on data structures, but it is a pretty good
algorithms question. At best, it requires an understanding of binary search, as
well as forcing the candidate to think about the conditions for search.

#### Problem statement:

Given a list of sorted, increasing, disjoint ranges, and a new range, add the new
range of integers into the list, merging any to maintain the properties of
sorted, increasing, and disjoint.

For example, given the list of ranges
```
     [(-3, 5), (7, 8), (200, 500), (1000, 1001)]
```

and the new range `(4, 7)`, the output should be
```
    [(-3, 8), (200, 500), (1000, 1001)]
```

#### Key Components:

- Determining where to place the node using comparisons of the ranges
- using binary search to do so.
- correctly removing the indices to be merged as well as not removing indices
  that are out of scope.
