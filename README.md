#include<math.h>
#include<iostream>
using namespace std;

int bin(unsigned int);

int main()
{
	int decimaln;
	cout<<"Enter decimal number:"<<endl;
	cin>>decimaln;
	cout<<"The Decimal number "<<decimaln<<" is quivalent to "<<bin(decimaln)<<" in binary"<<endl;
	return 0;
}



int bin(unsigned int decimaln)
{
	int x=0,i=0;
	unsigned int number;
	while(decimaln!=0)
	{
		number=decimaln%10;
		x=x+number*pow(2,i);
		decimaln=decimaln/10;
		i++;
	}
	return x;
}
