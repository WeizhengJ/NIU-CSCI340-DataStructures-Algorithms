	CSCI 340						Computer Assignment 02	             Spring 2017

Similar to **assignment01**, you are to implement two search algorithms (*linear search* and *binary search*) in C++ on randomly generated integers stored in vectors. In this assignment, you will use routines from STL <algorithm> to implement these algorithms.

The program is partially implemented. The source file `assignment02.cc` is included within this Git repository.

In this file, the main function is already implemented. You are required to implement the following functions:

* `int linearSearch(const vector <int>& inputVec, int x)` A linear search algorithm, where `x` is the searched item in vector `inputVec`. It simply starts searching for `x` from the beginning of vector `v` to the end, but it stops searching when there is a match. If the search is successful, it returns the position (starting at 0) of found item; otherwise, it returns `-1`. To implement this routine, simply call the `find()` function from the STL \<algorithm>.

* `int binarySearch (const vector <int>& inputVec, int x)` A binary search algorithm, where `x` is the searched item in vector `inputVec`. If the search is successful, it returns the position (starting at `0`) of found item; otherwise, it returns `-1`. To implement this routine, simply call the `equal_range()` function from the STL \<algorithm>.

* `int search(const vector<int>& inputVec,const vector<int>& searchVec,int(*p)(const vector<int>&,int))` A generic search algorithm – takes a pointer to the search routine `p()`, and then it calls `p()` for each element of vector `searchVec` in vector `inputVec`. It computes the total number of successful searches and returns that value to the `main()` routine as an input argument to the print routine `printStat()`, which is used to print out the final statistics for a search algorithm.

* `void sortVector(vector <int>& inputVec)` A sort algorithm to sort the elements of vector `inputVec` in ascending order. To implement this routine, simply call the `sort()` function from the STL.

* `void printStat(int totalSucCnt, int vec_size)` Prints the percent of successful searches as floating-point numbers on `stdout`, where `totalSucCnt` is the total number of successful comparisons and `vec_size` is the size of the test vector. 

* `void print_vec(const vector <int>& vec)` This routine displays the contents of vector `vec` on standard output, printing exactly `NO_ITEMS = 12` numbers on a single line, except perhaps the last line. The sorted numbers need to be properly aligned on the output. For each printed number, allocate `ITEM_W = 5` spaces on standard output. You can re-use the implementation of this routine from Assignment01, but remember to change the values of related constants.

**Programming Notes:**

* Execute the `srand()` function only once before generating the first random integer with the given seed value `SEED`. The `rand()` function generates a random integer in the range `[0, RAND_MAX]`, where the constant value `RAND_MAX` is the largest random integer returned by the `rand()` function and its value is system dependent. To normalize the return value to a value in the range `[LOW, HIGH]`: 


When your program is ready for grading, ***commit*** and ***push*** your local repository to remote git classroom repository and follow _**Assignment Submission Instructions**_. 