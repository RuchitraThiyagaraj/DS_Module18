# Ex29 Travelling Salesman Problem
## DATE:
## AIM:
To write a C Program to implement Travelling Salesman Problem for finding shortest path.
## Algorithm
1. Start from the first city and mark it as visited.
2. At each step, choose the nearest unvisited city.
3. Mark the selected city as visited and add its cost to total.
4. Repeat until all cities are visited.
5. Return to the starting city and add the return cost.
## Program:
```
/*
Program to implement Travelling Salesman Problem for finding shortest path
Developed by: T.RUCHITRA
RegisterNumber: 212223110043
#include<stdio.h>
int a[10][10],visited[10],n,cost=0;

void get()
{
	int i,j;
		scanf("%d",&n);
	for(i=0;i < n;i++)
	{
			for( j=0;j < n;j++)
			scanf("%d",&a[i][j]);
		visited[i]=0;
	}
	}

void mincost(int city)
{
	int ncity;
	int least(int);
	visited[city]=1;	
	printf("%d -->",city+1);
	ncity=least(city);
	if(ncity==999)
	{
		ncity=0;
		printf("%d",ncity+1);
		cost+=a[city][ncity];
		return;
	}
	mincost(ncity);
}

int least(int c)
{
	int i,nc=999;
	int min=999,kmin;
	for(i=0;i < n;i++)
	{
		if((a[c][i]!=0)&&(visited[i]==0))
			if(a[c][i] < min)
			{
				min=a[i][0]+a[c][i];
				kmin=a[c][i];
				nc=i;
			}
	}
	if(min!=999)
		cost+=kmin;
	return nc;
}

void put()
{
	printf("\n\nMinimum cost:%d",cost);
}

int main()
{
	get();
	mincost(0);
	put();
	return 0;
}

*/
```

## Output:
![ts](https://github.com/user-attachments/assets/594820c8-14a4-4176-8923-ab5c0df52bf6)


## Result:
Thus, the C program to implement Travelling Salesman Problem for finding shortest path is implemented successfully.
