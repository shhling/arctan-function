//# arctan-function
//C++ code for arctan function 
#include "stdafx.h"
#include <iostream>
using namespace std;

double power(double y,int n)
{
	double val=1.0;
	while(n--) val=val*y;
	return val;
}
double arctan(double x)
{
   double sum=0.0,j=0.0;
   for(int k=1;j>1e-15;k++)
	  {
		  j=1/(2*k-1)*power(x,2*k-1);
       sum=sum-j*power(-1,k);
       }
	   return sum;
}
int main()
{
	double pi;
    pi=16.0*arctan(1/5.0)-4.0*arctan(1/239.0);
	cout<<pi;
    return 0;
}
