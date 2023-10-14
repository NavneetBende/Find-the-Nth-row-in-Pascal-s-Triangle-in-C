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
