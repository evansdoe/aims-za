---
layout: page
permalink: /ems/2024-25/homework/
title: Homework
---


* (The list will be replaced with the table of contents.)
{:toc}

***
This page is where your handed-in, graded homework assignments will be posted along with their due dates and other information.

### WARNING

_Do not only do these assignments! Each lecture has assignments to help you revise what we did in class and possibly for the next lecture as well. Many of those lectures will show up as homework but not all. Please try as much as possible to do all assigned work, to get the very most out of class._

### Instructions for all homework assignments

- You must write, type, use Jupyter notebook, or use LaTeX to submit homework. ALL CODE MUST BE EXPLAINED. That means you should have at least one English sentence to explain each line of code that you write. This may be in a form of a comments or in a paragraph after each computation in your upyter notebook. 

- Similarly, do not simply write your explorations as lists of numbers, but write explanations of what you tried, and what didn't work.  

- Do **NOT** use internet resources for the exploration; for help with SageMath you may search the internet, of course. You are also welcome to ask me or any of the tutors.

- Starred (*) exercises are more important; you should be working on them early and often. To pass the course you should try to do all the starred exercises.

### First Assignment (Saturday, 9th November 2024, at 21:00)
_Please do not forget to read the general instruction for all homework assignments._

- Plot the $\sin(x)$ sine-function of x ranging from $0$ to $\pi$ along with its third derivative on the same set of axes, in a different color. Make the vertical axes range from -3 to +3.
- Create a nontrivial $7 \times 7$ diagonal matrix in Sage using a special command for it, and verify that the diagonal entries are the same as the eigenvalues of the matrix. Confirm that the eigenvectors are just the elementary basis vectors.
- For each of the numbers $n=10, 100, 1000, 10000, 100000, 1000000, 10000000$ and $100000000$ compare the number of primes less than $n$ to the value of $\frac{n}{\log(n)}$. You just need to make a table or write some sentences or something.  (Here, $\log$ is the natural logarithm.)
- Solve any differential equation using Sage.  It can be a really easy one.
- (*) Compute the conductor and Frobenius number of the following pairs: $\{4,7\}$, $\{4,6\}, and $\{7,9\}$, if they exist.  How many numbers are not writable in each case?
- (*) Prove that your computation of the conductor for $\{4, 7\}$ is correct.  Use your own words!
- (*) Write a Python function (a function using **"def"**) in SageMath to list enough numbers for a general pair $\{a, b\}$ where a and b are natural numbers to guess the conductor of $a$ and $b$. (And explain it!)
- (*) Make a conjecture for a formula for the conductor and the Frobenius number, given the pair $\{a, b\}$.  Also conjecture how many are not writable for the pair $\{a, b\}$ in general.  Be sure to write down whatever evidence you have for these conjectures (no code needed). Just stating a possible formula will not receive full credit, you must actually write about or show your experiments.  You do **NOT** need a proof.
- (*) Write a formal proof as I illustrated in class for the following statements:
  - Suppose $A \subseteq C$, and $B$ and $C$ are disjoint. Prove that if $x \in A$ then $x \notin B$.
  - Suppose that $A \setminus B$ is disjoint from $C$ and $x \in A$. Prove that if $x \in C$ then $x \in B$.
  - Use the method of proof by contradiction to prove the following statements:
    - Suppose $A \cap C \subseteq B$ and $a \in C$. Prove that $a \notin A \setminus B$.
    - Suppose that $A \subseteq B$, $a\in A$, and $a \notin B \setminus C$. Prove that $a \in C$.
  - Suppose that $y + x = 2\,y - x$, and $x$ and $y$ are not both zero. Prove that $y \neq 0$.
  - Prove that for every natural number $n\in\mathbb{N}$, $3$ divides $(-n + n^3)$.