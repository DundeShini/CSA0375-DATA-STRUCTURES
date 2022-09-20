# CSA0375-DATA STRUCTURES

*programs*
1. program for matrix multiplication

#include<stdio.h>
int main()
{
	int a[2][2],b[2][2],c[2][2];
	int i,j,k,sum;
	printf("Enter A Matrix\n");
	for(i=0;i<2;i++)
	{
	  for(j=0;j<2;j++)
	  {
	   scanf("%d",&a[i][j]);
      } 
	}
	
	printf("Enter B Matrix\n");
	for(i=0;i<2;i++)
	{
	  for(j=0;j<2;j++)
	  {
	   scanf("%d",&b[i][j]);
}
}
	for(i=0;i<2;i++)
	{
	  for(j=0;j<2;j++)
    {
	   c[i][j]= 0;
	   for(k=0;k<2;k++)
	{
		c[i][j]+= a[i][k]*b[k][j];
		
	}
    } 
   }
   
   printf("\nthe multiplication of two matrices \n");
   	for(i=0;i<2;i++)
   	{
	   
   	 for(j=0;j<2;j++)
   {
   	
   	printf("%d  ",c[i][j]);
	   	   }   	
	   	   printf("\n");
	   }
}
![matrix multiplication output](https://user-images.githubusercontent.com/112486766/191181151-6a635022-e526-4047-bee5-6c2ef6a0b494.png)
 2. program for Odd or Even number 
    #include <stdio.h>
    int main() {
    int num;
    printf("Enter an integer: ");
    scanf("%d", &num);

    // true if num is perfectly divisible by 2
    if(num % 2 == 0)
        printf("%d is even.", num);
    else
        printf("%d is odd.", num);
    
    return 0;
    }
![even or odd output](https://user-images.githubusercontent.com/112486766/191181664-69163918-cff3-497c-b1fd-5316fddf1e09.png)
3. program  for Factorial of a given number without using Recursion
  #include<stdio.h>    
  int main()    
 {    
 int n1=1,n2=1,n3,i,number;    
 printf("Enter the number of elements:");    
 scanf("%d",&number);    
 printf("\n%d %d",n1,n2);  
 for(i=2;i<number;++i)  
 {    
  n3=n1+n2;    
  printf(" %d",n3);    
  n1=n2;    
  n2=n3;    
 }  
  return 0;  
 }
 ![fibonacci series without recursion output](https://user-images.githubusercontent.com/112486766/191181998-01153e98-07c8-4495-9fa7-73b429c81183.png)
