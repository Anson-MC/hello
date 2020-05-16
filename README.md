#include<iostream>
#include<ctime>
#include<cstdlib>
using namespace std;
int main()
{
	int i,j,k,a,b,temp;//i控制循环一，j控制循环2，k控制数组数数量，a生成随机数，b输出。 
	cout<<"write a number.\n\n";
	cin>>k; 
	int num[k];
	srand(time(NULL));
	for(a=0;a<=k;a++)
	{
		num[a]=rand()%100+1;
	}
	for(i=0;i<=k;i++)
	{
		for(i=k-1;i>=1;i--)
		{
			for(j=0;j<i;j++)
			{
				if(num[j]<num[j+1])
				{
					temp=num[j];
					num[j]=num[j+1];
					num[j+1]=temp;
					temp=0;
				}
			}
		}
	}
	for(b=0;b<=k+1;b++)
	{
		cout<<num[b]<<"\n\n";
	}
	return 0;
}
