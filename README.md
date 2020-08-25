# AND-OR-NOT-Gates
C Program to Display the Boolean Truth Table for AND,OR,NOT.


 Logic gates
Digital systems are said to be constructed by using logic gates. These gates are the AND, OR, NOT, NAND, NOR, EXOR and EXNOR gates. The basic operations are described below with the aid of truth tables.

AND gate

 		
The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high.  A dot (.) is used to show the AND operation i.e. A.B.  Bear in mind that this dot is sometimes omitted i.e. AB
 
OR gate
 		
The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high.  A plus (+) is used to show the OR operation.
 
NOT gate

		
The NOT gate is an electronic circuit that produces an inverted version of the input at its output.  It is also known as an inverter.  If the input variable is A, the inverted output is known as NOT A.  This is also shown as A', or A with a bar over the top, as shown at the outputs. The diagrams below show two ways that the NAND logic gate can be configured to produce a NOT gate. It can also be done using NOR logic gates in the same way.


Following table shows all the logical operators supported by C language. Assume variable A holds 1 and variable B holds 0, then −

In c we use them as -

&&	Called Logical AND operator. If both the operands are non-zero, then the condition becomes true.	(A && B) is false.

||	Called Logical OR Operator. If any of the two operands is non-zero, then the condition becomes true.	(A || B) is true.

!	Called Logical NOT Operator. It is used to reverse the logical state of its operand. If a condition is true, then Logical NOT operator will make it false.

#include<stdio.h>

void main()
{
 int a[2][2],b[2][2],c[2];
 int i,j;
 for(i=0;i<=1;i++)
 {
 for(j=0;j<=1;j++)
  {
   a[i][j]=(i&&j);
   b[i][j]=(i||j);
  }
 }

 for(i=0;i<=1;i++)
 {
 c[i]=(!i);
 }

 printf("\nThe Truth Table for AND Gate( && ) is..\n");
 printf("   A    B     :    C=A&&B\n");
for(i=0;i<=1;i++)
 {
  for(j=0;j<=1;j++)
   {
    printf("   %d    %d     :    %d\n",i,j,a[i][j]);
   }
 }
 printf("\nThe Truth Table for OR Gate( || ) is..\n");
 printf("   A    B     :    C=A||B\n");
 for(i=0;i<=1;i++)
 {
  for(j=0;j<=1;j++)
   {
    printf("   %d    %d     :    %d\n",i,j,b[i][j]);
   }
 }
 printf("\nThe Truth Table for NOT Gate (!) is..\n");
 printf("   A   :  B = !A\n");
 for(i=0;i<=1;i++)
 {
   printf("   %d   :  %d\n",i,c[i]);
 }
}
