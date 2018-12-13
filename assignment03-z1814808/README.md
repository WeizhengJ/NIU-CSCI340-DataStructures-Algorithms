	CSCI 340						Computer Assignment 03	             Spring 2017

<h2>Sieve of Eratosthenes (15 points)</h2> 

For this computer assignment, you are to write and implement a C++ program to find and print all prime numbers within a range `[lower upper]` using the algorithm known as the *Sieve of Eratosthenes*. The program will have basic interactive user interface to take input values of `lower` and `upper` and allow the user to continue or quit the game.

Starter code for `assignment03.cc` is provided to you as part of this repository.

* `void sieve(set<int>& s, const int lower, const int upper)` This routine can be used to apply the *Sieve of Eratosthenes* algorithm to remove all nonprime numbers from the integer `set s = {lower, …, upper}`.

* `void print_primes(const set < int >& s, const int lower, const int upper)` This routine can be used to print the elements in the integer `set s` (`NO_ITEMS = 8` primes per line and `ITEM_W = 6` spaces allocated for each prime).

* `void run_game(set<int>& s)` This routine maintains a loop to take inputs from a user. The user will be asked for the range of the prime numbers. If the range is not valid, e.g. `lower` is greater than `upper`, the user will be asked to input again. The routine will invoke `sieve()` and `print_primes()`. Once the results are displayed, the user will be asked whether to continue or quit the game. In case of continuing the game, the user will be asked for values of the range again. The game continues until the user requests to stop. 

**Programming Notes:**

When your program is ready for grading, ***commit*** and ***push*** your local repository to remote git classroom repository and follow _**Assignment Submission Instructions**_. 