// Insertion_Sort

#include<stdio.h>
#include<stdlib.h>
#define MAX 50
int main()
{
    void read(int[MAX],int);
    void insertion_sort(int[MAX],int);
    void show(int[MAX],int);
    int a[MAX],n;
    printf("Enter the range");
    scanf("%d",&n);
    if(n<1 || n>MAX)
    {
        printf("%d is out of range",n);
        exit(0);
    }
    printf("Enter %d no. of elements",n);
    read(a,n);
    printf("\n Before sorting, the list is \n");
    show(a,n);
    insertion_sort(a,n);
    printf("\n After sorting, the list is \n");
    show(a,n);
}
void read(int b[MAX],int m)
{
    int i;
    for(i=0;i<m;i++)
       scanf("%d",&b[i]);
}
void show(int c[MAX],int l)
{
    int i;
    for(i=0;i<l;i++)
       printf("%d ",c[i]);
}
void insertion_sort(int d[MAX],int r)
{
    int i,j,k;
    for(i=1;i<r;i++)
    {
        k=d[i];

        for(j=i-1;k<d[j] && j>=0;j--)
        {
            d[j+1]=d[j];
        }
        d[j+1]=k;
    }
}
