# Find-the-Nth-row-in-Pascal-s-Triangle-in-C

Nth row of Pascal’s Triangle in C
Here, in this page we will discuss the program to find Nth row of pascal’s triangle in C Programming language. We are given with a non-negative integer and we need to print the Nth row. We are assuming zero based starting of the rows.

Nth row in Pascal’s Triangle in C
Example
Pascal Triangle :
1
1 1
1 2 1
1 3 3 1
1 4 6 4 1 
For N=2,
Output : 1 2 1
Algorithm :
In this method we will discuss the efficient way to find the Nth row of the triangle.

Nth row = nC 0 nC1 nC2 … nCn
So, by using the above concept to find the nth row.
nCr = (nCr-1 * (n – r + 1))/r
Take a variable say prev=1 (as, nC0=1)and print prev.
Now, Run a loop from [1, N], take a variable say curr, and set curr = (prev * (N – i + 1)) / i;
And, Print Curr.
Code in C
Run
#include <stdio.h>

//Function to print N-th row
void getrow(int N)
{
   int prev = 1;
   printf("%d ", prev);

   for (int i = 1; i <= N; i++) {
     int curr = (prev * (N - i + 1)) / i;
     printf("%d ", curr);
     prev = curr;
   }
}

// Driver Program
int main()
{

  int N = 5;
  getrow(N);
  return 0;
}
Output :
1 5 10 10 5 1
