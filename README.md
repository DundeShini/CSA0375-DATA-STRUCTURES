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

![factorial without recursion](https://user-images.githubusercontent.com/112486766/191202736-81f7381f-c835-4f0b-bc89-e0b5c532ca88.png)
 
 4. program for fibonacci series without recursion

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
 
 ![fibonacci series without recursion output](https://user-images.githubusercontent.com/112486766/191202997-e43323a4-0bd6-4f25-a18b-f81704f3bcbe.png)
 
5. program for factorial with recursion

#include<stdio.h>
int factorial(int num);
int main()
{
	int number,result;
	printf("enter a positive number \n");
	scanf("%d",&number);
	result=factorial(number);
	printf("factorial=%d",result);
}
int factorial(int num)
{
	if(num!=1)
	{
		return num*factorial(num-1);
	}
	else
	{
		return num;
	}
}

![factorial with recursion output](https://user-images.githubusercontent.com/112486766/191203605-215ba081-dbb2-4e4e-acf0-399bba9b049c.png)


 6..program for fibonacci series with recursion
 
 #include<stdio.h>    
void printFibonacci(int n){    
    static int n1=1,n2=1,n3;    
    if(n>0){    
         n3 = n1 + n2;    
         n1 = n2;    
         n2 = n3;    
         printf("%d ",n3);    
         printFibonacci(n-1);    
    }    
}    
int main(){    
    int n;    
    printf("Enter the number of elements: ");    
    scanf("%d",&n);    
    printf("Fibonacci Series: ");    
    printf("%d %d ",0,1);    
    printFibonacci(n-2);//n-2 because 2 numbers are already printed    
  return 0;  
 } 
 
 ![fibonacci series with recursion output](https://user-images.githubusercontent.com/112486766/191200336-444b9d9f-d2f6-49b6-8a59-558153660391.png)
 
 7. program for  Array operations such as Insert, Delete and Display
 
 #include <stdio.h>
int main()
{
int i,n,pos,ele,c,position,arr[100];
printf("Enter array size:");
scanf("%d",&n);
printf("Enter elements:");
for(i = 0; i < n; i++)
{
scanf("%d",&arr[i]);
}
printf("Enter the position to be inserted:");
scanf("%d",&pos);
printf("Enter the element to be inserted:");
scanf("%d",&ele);
if(pos > n)
printf("Invalid Input");
else
for(i=n-1;i>=pos-1;i--)
arr[i+1] = arr[i];
arr[pos-1] = ele;
printf("Array after insertion is:\n");
for (i = 0; i <= n; i++)
printf("%d\n", arr[i]);
printf("Enter the position to be deleted:");
scanf("%d",&position);
if (position > n+1)
printf("\nDeletion not possible.\n");
else
for(c=position-1;c<n-1;c++)
arr[c] = arr[c+1];
printf("\nArray after deletion :\n");
for(c=0;c<n-1;c++)
printf("%d\n", arr[c]);
printf("\nEnter element :");
scanf("%d", &ele);
for(c = 0; c < n ; c++)
{
if(arr[c] == ele)
{
printf("\nElement found\n");
}
}
return 0;
}

![insert delete search output](https://user-images.githubusercontent.com/112486766/191207471-a38c79c3-2df0-47eb-b04b-6483a8714ffd.png)

8. program for search a number using Linear Search method

#include <stdio.h>
int main()
{
 int array[100], search, c, n;
 printf("Enter number of elements in array\n");
 scanf("%d", &n);
 printf("Enter %d integer(s)\n", n);
 for (c = 0; c < n; c++)
 scanf("%d", &array[c]);
 printf("Enter a number to search\n");
 scanf("%d", &search);
 for (c = 0; c < n; c++)
 {
 if (array[c] == search) 
 {
 printf("%d is present at location %d.\n", search, c+1);
 break;
 }
 }
 if (c == n)
 printf("%d isn't present in the array.\n", search);
 return 0;
}

![linear search output](https://user-images.githubusercontent.com/112486766/191208412-79866db4-d827-4a61-a110-841752e0c7e6.png)











 
