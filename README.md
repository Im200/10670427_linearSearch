# 10670427_linearSearch
#include <iostream>
using namespace std;
int main ()
{
int mn,mx;
const int Numb = 10;
int a[Numb]; //10 elements
cout<<"Enter 10 values:"; //prompts user for 10 values.
for(int i=0;i<10;i++)
{
cout<< "\nEnter value: ";
cin>> a[i]; // puts values in array
}

mn=a[0];
mx=a[0];
for(int i=1;i<10;i++)
	{
		if(mn>a[i])
		{
			mn=a[i];
		}
		else if(mx<a[i])
		{
			mx = a[i];
		}
	}

cout<<"Maximum number is: "<< mx << endl;
cout<<"Minimum number is: "<< mn << endl;

return 0;

}
  Time Complexity
T(n) = T(floor(n/2)) + T(ceil(n/2)) + 2  
  T(2) = 1
  T(1) = 0
If n is a power of 2, then we can write T(n) as:

   T(n) = 2T(n/2) + 2 
After solving above recursion, we get

  T(n)  = 3n/2 -2 
Thus, the approach does 3n/2 -2 comparisons if n is a power of 2. And it does more than 3n/2 -2 comparisons if n is not a power of 2.


