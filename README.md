# assignment-no-2

#include <stdio.h>
int main()
{
  int n;
  double arr[100];
  printf("Enter the number of elements (1 to 100): ");
  scanf("%d", &n);
  for (int i = 0; i < n; ++i) {
  printf("Enter number%d: ", i + 1);
  scanf("%lf", &arr[i]);
  }
  // storing the largest number to arr[0]
  for (int i = 1; i < n; ++i)
  {
  if (arr[0] < arr[i])
  {
    arr[0] = arr[i];
  }
  }
  printf("Largest element = %.2lf", arr[0]);
  return 0;
}

question 2

#include <stdio.h>
int main ()
{
  int n = 0, i = 0, largest1 = 0, largest2 = 0, temp = 0;
  printf ("Enter the size of the array\n");
  scanf ("%d", &n);
  int array[n];
  printf ("Enter the elements\n");
  for (i = 0; i < n; i++)
  {
    scanf ("%d", &array[i]);
  }
   printf ("The array elements are : \n");
   for (i = 0; i < n; i++)
  {
   printf ("%d\t", array[i]);
  }
   printf ("\n");
   largest1 = array[0];
   largest2 = array[1];
   if (largest1 < largest2)
   {
     temp = largest1;
     largest1 = largest2;
     largest2 = temp;
   }
    for (int i = 2; i < n; i++)
   { 
    if (array[i] > largest1)
   {
     largest2 = largest1;
     largest1 = array[i];
    }
      else if (array[i] > largest2 && array[i] != largest1)
    {
      largest2 = array[i];
    }
    }
    printf ("The FIRST LARGEST = %d\n", largest1);
    printf ("THE SECOND LARGEST = %d\n", largest2);
    return 0;
 }
 
 question 3
 
 #include <stdio.h>
void main ()
{
  int number[30];
  int i, j, a, n, counter, average;
  printf("Enter the value of N\n");
  scanf("%d", &n);
  printf("Enter the numbers \n");
  for (i = 0; i < n; ++i)
  scanf("%d", &number[i]);
  for (i = 0; i < n; ++i)
 {
   for (j = i + 1; j < n; ++j)
 {
   if (number[i] < number[j])
 {
    a = number[i];
    number[i] = number[j];
    number[j] = a;
  }
  }
  }
    printf("The numbers arranged in descending order are given below \n");
    for (i = 0; i < n; ++i)
  {
     printf("%d\n", number[i]);
  }
     printf("The 2nd largest number is  = %d\n", number[1]);
     printf("The 2nd smallest number is = %d\n", number[n - 2]);
     average = (number[1] + number[n - 2]) / 2;
     counter = 0;
     for (i = 0; i < n; ++i)
 {
     if (average == number[i])
 {
     ++counter;
 }
 }
    if (counter == 0 )
    printf("The average of %d  and %d is = %d is not in the array \n", number[1], number[n - 2], average);
    else
    printf("The average of %d  and %d in array is %d in numbers \n", number[1], number[n - 2], counter);
 }
 
 question 4
 
 #include <stdio.h>
int maximum_difference(int array[], int arr_size)
{
  int max_diff = array[1] - array[0];
  int i, j;
  for (i = 0; i < arr_size; i++)
 {
   for (j = i + 1; j < arr_size; j++)
 {
   if (array[j] - array[i] > max_diff)
   max_diff = array[j] - array[i];
 }
 }
   return max_diff;
}
int main()
{
  int array[] = {10, 15, 90, 200, 110};
  printf("Maximum difference is %d",  maximum_difference(array, 5));
  getch();
  return 0;
}

question 5

#include <stdio.h>
#include <conio.h>
int main ()
{
  // declare local variables
  int arr[20], i, j, k, size;
  printf (" Define the number of elements in an array: ");
  scanf (" %d", &size);
  printf (" \n Enter %d elements of an array: \n ", size);
  // use for loop to enter the elements one by one in an array
  for ( i = 0; i < size; i++)
{
  scanf (" %d", &arr[i]);
}
  for ( i = 0; i < size; i ++)
{
  for ( j = i + 1; j < size; j++)
{
   if ( arr[i] == arr[j])
{
   for ( k = j; k < size - 1; k++)
{
   arr[k] = arr [k + 1];
 }
    size--;
    j--;
 }
 }
 }
   printf (" \n Array elements after deletion of the duplicate elements: ");
   // for loop to print the array
   for ( i = 0; i < size; i++)
 {
    printf (" %d \t", arr[i]);
 }
   return 0;
}

question 6

#include <stdio.h>
void main()
 {
   long int ARR[10], ODD[10], EVEN[10];
   int i, j = 0, k = 0, n;
   printf("Enter the size of array  ");
   scanf("%d", &n);
   printf("Enter the elements of the array ");
   for (i = 0; i < n; i++)
 {
   scanf("%ld", &ARR[i]);
   fflush(stdin);
 }
   for (i = 0; i < n; i++)
{
   if (ARR[i] % 2 == 0)
{
   EVEN[j] = ARR[i]
   j++;
}
   else
{
   ODD[k] = ARR[i];
    k++;
 }
 }
   printf("The elements of ODD are");
   for (i = 0; i < k; i++)
 {
   printf("%d\n", ODD[i]);
 }
   printf("The elements of EVEN are ");
   for (i = 0; i < j; i++)
 {
   printf("%d\n", EVEN[i]);
}
}
  
question 7

#include <stdio.h>
#define N 1000
int main() 
{
  int arr[N];
  int n;
  printf("Enter the size of the array: ");
  scanf("%d", &n);
  printf("Enter an array: ");
  for (int i = 0; i< n; i++)
{
  scanf("%d", &arr[i]);
}
  printf("Reversed array: ");
  for (int i = n-1; i>=0; i--)
{
  printf("%d ", arr[i]);
}
  return 0;
}
  
 question 8
 
 #include <stdio.h>
int main()
{
 int arr[100], freq[100];
 int size, i, j, count;
 /* Input size of array */
 printf("Enter size of array: ");
 scanf("%d", &size);
 /* Input elements in array */
 printf("Enter elements in array: ");
 for(i=0; i<size; i++)
{
  scanf("%d", &arr[i]);
  freq[i] = -1;
}
  for(i=0; i<size; i++)
{       
  count = 1;
  for(j=i+1; j<size; j++)
{
  if(arr[i]==arr[j])
{
  count++;
  freq[j] = 0;
 }
 }
   if(freq[i] != 0)
 {
   freq[i] = count;
 }
 }
   printf("\nFrequency of all elements of array : \n");
   for(i=0; i<size; i++)
{
   if(freq[i] != 0)
{
   printf("%d occurs %d times\n", arr[i], freq[i]);
}
}
   return 0;
}


question 9

#include <stdio.h>
 void main ()
 {
  int number[30];
  int i, j, a, n, counter, average;
  printf("Enter the value of N\n");
  scanf("%d", &n);
  printf("Enter the numbers \n");
  for (i = 0; i < n; ++i)
  scanf("%d", &number[i]);
  for (i = 0; i < n; ++i)
  {
    for (j = i + 1; j < n; ++j)
  {
    if (number[i] < number[j])
  {
     a = number[i];
     number[i] = number[j];
     number[j] = a;
   }
   }
   }
     printf("The numbers arranged in descending order are given below \n");
     for (i = 0; i < n; ++i)
   {
     printf("%d\n", number[i]);
   }
     printf("The 2nd largest number is  = %d\n", number[1]);
     printf("The 2nd smallest number is = %d\n", number[n - 2]);
     average = (number[1] + number[n - 2]) / 2;
     counter = 0;
     for (i = 0; i < n; ++i)
   {
     if (average == number[i])
   {
     ++counter;
   }
   }
     if (counter == 0 )
     printf("The average of %d  and %d is = %d is not in the array \n",
     number[1], number[n - 2], average);
     else
     printf("The average of %d  and %d in array is %d in numbers \n",
     number[1], number[n - 2], counter);
   }
   
   question 10
   
   #include <limits.h>
#include <stdio.h>
int min(int x, int y) { return (x < y) ? x : y; }
// Returns minimum number of
// jumps to reach arr[n-1] from arr[0]
int minJumps(int arr[], int n)
{
	// jumps[n-1] will hold the result
	int jumps[n];
	int i, j;
	if (n == 0 || arr[0] == 0)
	return INT_MAX;
	jumps[0] = 0;
	// Find the minimum number of
	// jumps to reach arr[i]
	// from arr[0], and assign this
	// value to jumps[i]
	for (i = 1; i < n; i++)
{
	jumps[i] = INT_MAX;
	for (j = 0; j < i; j++)
{
	if (i <= j + arr[j] && jumps[j] != INT_MAX)
{
	jumps[i] = min(jumps[i], jumps[j] + 1);
	break;
}
}
}
 return jumps[n - 1];
}
// Driver program to test above function
int main()
{
	int arr[] = { 1, 3, 5, 8, 9, 2, 6, 7, 6, 8, 9 };
	int size = sizeof(arr) / sizeof(int);
	printf("Minimum number of jumps to reach end is %d ",
	minJumps(arr, size));
	return 0;
}
  
