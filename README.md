# Arraysearch
Simple program for searching array
//binary search
#include<iostream.h>
#include<conio.h>

int bsearch(int ar[], int size, int element)
{
int beg, last, mid;
beg=0,last=size-1;
while(beg<=last)
{
mid=(beg+last)/2;
if(element==ar[mid])
return mid;
else if (element > ar[mid])
beg=mid+1;
else
last=mid-1;
}
return -1;	//loop will reach here
		//when item not found
}

void main()
{
int array[10], item, n, index;
clrscr();
cout<<"\n \t enter array size (max 10):";
cin>>n;

for(int i=0;i<n;i++)
{
cout<<"\n \t enter value in ascending order:";
cin>>array[i];
}

cout<<"\n \t enter element to be searched:";
cin>>item;

index=bsearch(array,n,item);

if(index==-1)
cout<<"\n \t given element could not be found";
else
cout<<"\n \t element found at index:"<<index<<" position="<<index+1;

getch();
}

