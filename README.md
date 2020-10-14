# CSE-Assignment-




Assignment_01

#include<stdio.h>

main(){

int row,col;
for(row=5;row>=1;row--){
    
    for(col=1;col<=row;col++)
    printf("*");
    printf("\n");
} 
}

Assignment_02

#include<stdio.h>

main(){

int row,col,count=1;
for(row=1;row<=5;row++){
    
    for(col=1;col<=row;col++)
    printf("%d ", count++);
    printf("\n");
} 
}



#MATRIX_ADDITION-

#include<stdio.h>

int main(){

int i,j,numberOfRows,numberOfCols;

int A[10][10],B[10][10],C[10][10];

printf("Enter the number of Rows and Cols: ");

scanf("%d %d", &numberOfRows,&numberOfCols);

//scanning matrix A

printf("Enter elements for matrix A.\n");

for(i=0;i<numberOfRows;i++)

{  
   for(j=0;j<numberOfCols;j++)
    
 { 
   printf("A[%d][%d] = ",i,j);
    scanf("%d",&A[i][j]);
} 

printf("\n");

}
//scanning matrix B

printf("\n\nEnter elements for matrix B.\n");

for(i=0;i<numberOfRows;i++)

{ 
  for(j=0;j<numberOfCols;j++)

   { printf("B[%d][%d]= ",i,j);
    scanf("%d",&B[i][j]);
} 

printf("\n");

}


//printing matrix A.

printf("A= ");

for(i=0;i<numberOfRows;i++)
{
    printf("\t");
        for(j=0;j<numberOfCols;j++)
    
  {  
     printf("%d  ", A[i][j]);
   
} 
    
printf("\n");
    
}



 
//printing matrix B.

printf("\n\nB= ");

for(i=0;i<numberOfRows;i++)
{
   printf("\t");
        for(j=0;j<numberOfCols;j++)

   {
       printf("%d  ", B[i][j]);
   
} 
    
printf("\n");
    
}

//ADDITION OF A & B

for(i=0;i<numberOfRows;i++)
{
    for(j=0;j<numberOfCols;j++)

    {
        
       C[i][j]=A[i][j] + B[i][j];
        
    }
    
}


//printing C MATRIX.

printf("\nA+B= ");

for(i=0;i<numberOfCols;i++)

{
    printf("\n");
    
    printf("\t");
    
    for(j=0;j<numberOfCols;j++)

    {
        printf("%d  ",C[i][j]);
    }
    
    printf("\n");
     
}





} 
#MATRIX_SUBTRACTION-

#include<stdio.h>

int main() { int i,j,numberOfRows,numberOfCols; int A[10][10],B[10][10],C[10][10];

printf("Enter the number of Rows and Cols: ");
scanf("%d %d", &numberOfRows,&numberOfCols);

//scanning matrix A

printf("Enter elements for matrix A.\n");
for(i=0;i<numberOfRows;i++)
{  for(j=0;j<numberOfCols;j++)
    
 { printf("A[%d][%d] = ",i,j);
    scanf("%d",&A[i][j]);
} 
printf("\n");
}
//scanning matrix B

printf("\n\nEnter elements for matrix B.\n");
for(i=0;i<numberOfRows;i++)
{ for(j=0;j<numberOfCols;j++)
   { printf("B[%d][%d]= ",i,j);
    scanf("%d",&B[i][j]);
} 
printf("\n");

}


//printing matrix A

printf("A= ");

for(i=0;i<numberOfRows;i++)
{
    printf("\t");
        for(j=0;j<numberOfCols;j++)
    
  {  printf("%d  ", A[i][j]);
   
} 
    
printf("\n");
    
}



 
//printing matrix B

printf("\n\nB= ");

for(i=0;i<numberOfRows;i++)
{
{    printf("\t");
        for(j=0;j<numberOfCols;j++)
     printf("%d  ", B[i][j]);
   
} 
    
printf("\n");
    
}

//SUBTRACTION (A-B)

for(i=0;i<numberOfRows;i++)
{
    for(j=0;j<numberOfCols;j++)
    {
        
       C[i][j]=A[i][j]-B[i][j];
        
    }
    
}


//printing C MATRIX

printf("\nA-B= ");
for(i=0;i<numberOfCols;i++)
{
    printf("\n");
    
    printf("\t");
    
    for(j=0;j<numberOfCols;j++)
    {
        printf("%d  ",C[i][j]);
    }
    
    printf("\n");
    
   
}




}
#MATRIX-MULTIPLICATION_

#include<stdio.h>

int main(){

int A[10][10],B[10][10],C[10][10];
int R1,R2,C1,C2,i,j,k,sum=0;
printf("Enter rows and columns for Matrix A: "); scanf("%d %d", &R1,&C1);

printf("Enter rows and columns for Matrix B: ");
scanf("%d %d", &R2,&C2);


while(C1!=R2)
{
printf("Error !!! Column of A Matrix is not equal to the row of B Matrix.");

    printf("Enter rows and columns for Matrix A: ");
scanf("%d %d", &R1,&C1);


printf("Enter rows and columns for Matrix B: ");
scanf("%d %d", &R2,&C2);   
    
}
//taking input for Matrix A.

printf("\nEnter elements for Matrix A.\n");

for(i=0;i<R1;i++)
{
    for(j=0;j<C1;j++)
    
   {
        printf("A[%d][%d]= ",i,j);
        scanf("%d",&A[i][j]);
    } 
    printf("\n");
    
}

//taking input for Matrix B.


printf("\nEnter elements for Matrix B.\n");

for(i=0;i<R2;i++)
{
    for(j=0;j<C2;j++)
    
   {
        printf("B[%d][%d]= ",i,j);
        scanf("%d",&B[i][j]);
    }
     printf("\n");
    
}

// printing Matrix A . 

printf("\nA Matrix=\n");

for(i=0;i<R1;i++)
{
    printf("\t");
    
    for(j=0;j<C1;j++)
    
    {
        printf("%d  ", A[i][j]);
        
        
    } 
     printf("\n");
    
    
}

 // printing Matrix B. 

printf("\nB Matrix=\n");

for(i=0;i<R2;i++)
{
   printf("\t");
    
    for(j=0;j<C2;j++)
    
    {
        printf("%d  ", B[i][j]);
        
    } 
      printf("\n");
    
    
}


// Multiplying A & B Matrix.

for(i=0;i<R1;i++)

{
    for(j=0;j<C2;j++)
    
    
    {
       for(k=0;k<C1;k++) 
        
       sum=sum+A[i][k]*B[k][j];
        
        
        C[i][j]=sum;
        
        sum=0;
    }
    
}
// printing C Matrix.

printf("\nA*B= ");

for(i=0;i<R1;i++)

{
    
   printf("\n");
    printf("\t");
    
    for(j=0;j<C1;j++)
    
    {
        printf("%d  ", C[i][j]);
    }
    
    printf("\n");
    
  }  
}

