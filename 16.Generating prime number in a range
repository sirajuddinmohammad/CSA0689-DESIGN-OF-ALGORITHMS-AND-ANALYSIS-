#include<stdio.h>
int main()
{
	int i,j,n,count,s;
	printf("enter starting value=");
	scanf("%d",&s);
	printf("enter ending value=");
	scanf("%d",&n);
	printf("prime numbers in between %d and %d are =",s,n);
	if(n==1)
	{
		printf("enter a valid number");
	}
	else
	{
	for(i=s;i<=n;i++)
	{
		count=0;
		for(j=2;j<=i/2;j++)
		{
			if(i%j==0)
			{
				count++;
				break;
			}
		}
		if(count==0)
		{
			printf("\n %d ",i);
		}
	}
    }
	return 0;
} 
