---
layout: post
title: C语言基础算法案例
---

1、C语言打印一条语句

源代码：

/* C Program to print a sentence. */

#include <stdio.h>

int main()

{
  
  printf("C Programming"); /* printf() prints the content inside quotation */
  
  return 0;
  
}

输出：

C Programming

2、C语言打印用户输入的一个整数

源代码：

#include <stdio.h>
int main()
{
    int num;
    printf("Enter a integer: ");  
    scanf("%d",&num);  /* Storing a integer entered by user in variable num */
    printf("You entered: %d",num);
    return 0;
}
输出：

Enter a integer: 25
You entered: 25
3、C语言实现两个整数相加

源代码：

/*C programming source code to add and display the sum of two integers entered by user */

#include <stdio.h>
int main( )
{
    int num1, num2, sum;
    printf("Enter two integers: ");
    scanf("%d %d",&num1,&num2); /* Stores the two integer entered by user in variable num1 and num2 */

    sum=num1+num2;      /* Performs addition and stores it in variable sum */
    printf("Sum: %d",sum);  /* Displays sum */
    return 0;
}
输出：

Enter two integers: 12
11
Sum: 23
4、C语言实现两个小数相乘

源代码：

/*C program to multiply and display the product of two floating point numbers entered by user. */

#include <stdio.h>
int main( )
{
    float num1, num2, product;
    printf("Enter two numbers: ");
    scanf("%f %f",&num1,&num2);        /* Stores the two floating point numbers entered by user in variable num1 and num2 respectively */
    product = num1*num2;  /* Performs multiplication and stores it */
    printf("Product: %f",product);
    return 0;
}
输出：

Enter two numbers: 2.4
1.1
Product: 2.640000
5、C语言查找字符的ASCII值

源代码：

/* Source code to find ASCII value of a character entered by user */

#include <stdio.h>
int main(){
    char c;
    printf("Enter a character: ");
    scanf("%c",&c);        /* Takes a character from user */
    printf("ASCII value of %c = %d",c,c);
    return 0;
}
输出：

Enter a character: G
ASCII value of G = 71
6、C语言根据用户输入的整数做商和余数

源代码：

/* C Program to compute remainder and quotient  */

#include <stdio.h>
int main(){
    int dividend, divisor, quotient, remainder;
    printf("Enter dividend: ");
    scanf("%d",&dividend);
    printf("Enter divisor: ");
    scanf("%d",&divisor);
    quotient=dividend/divisor;           /*  Computes quotient */
    remainder=dividend%divisor;          /* Computes remainder */
    printf("Quotient = %d\n",quotient);
    printf("Remainder = %d",remainder);
    return 0;
}
输出：

Enter dividend: 25
Enter divisor: 4
Quotient = 6
Remainder = 1
7、C语言获取整型、单精度浮点型、双精度浮点型和字符型的长度

基本语法是：

temp = sizeof(operand);
/* Here, temp is a variable of type integer,i.e, sizeof() operator 
   returns integer value. */
源代码：

/* This program computes the size of variable using sizeof operator.*/

#include <stdio.h>
int main(){
    int a;
    float b;
    double c;
    char d;
    printf("Size of int: %d bytes\n",sizeof(a));
    printf("Size of float: %d bytes\n",sizeof(b));
    printf("Size of double: %d bytes\n",sizeof(c));
    printf("Size of char: %d byte\n",sizeof(d));
    return 0;
}
输出：

Size of int: 4 bytes
Size of float: 4 bytes
Size of double: 8 bytes
Size of char: 1 byte
注：可能会由于系统的不同出来的结果也不尽相同。

8、C语言获取关键字long的长度范围

源代码：

#include <stdio.h>
int main(){
    int a;
    long int b;                /* int is optional. */
    long long int c;            /* int is optional. */
    printf("Size of int = %d bytes\n",sizeof(a));
    printf("Size of long int = %ld bytes\n",sizeof(b));
    printf("Size of long long int = %ld bytes",sizeof(c));
    return 0;
}
输出：

Size of int = 4 bytes
Size of long int = 4 bytes
Size of long long int = 8 bytes
9、C语言交换数值

源代码：

#include <stdio.h>
int main(){
      float a, b, temp;
      printf("Enter value of a: ");
      scanf("%f",&a);
      printf("Enter value of b: ");
      scanf("%f",&b);
      temp = a;    /* Value of a is stored in variable temp */
      a = b;       /* Value of b is stored in variable a */
      b = temp;    /* Value of temp(which contains initial value of a) is stored in variable b*/
      printf("\nAfter swapping, value of a = %.2f\n", a);
      printf("After swapping, value of b = %.2f", b);
      return 0;
}
输出：

Enter value of a: 1.20
Enter value of b: 2.45

After swapping, value of a = 2.45
After swapping, value of b = 1.2
10、C语言检查数值是奇数还是偶数

源代码：

/*C program to check whether a number entered by user is even or odd. */

#include <stdio.h>
int main(){
      int num;
      printf("Enter an integer you want to check: ");
      scanf("%d",&num);
      if((num%2)==0)      /* Checking whether remainder is 0 or not. */
           printf("%d is even.",num);
      else
           printf("%d is odd.",num);
      return 0;
}
输出1：

Enter an integer you want to check: 25
25 is odd.
输出2：

Enter an integer you want to check: 12
12 is even.
也可以用条件运算符解决：

/* C program to check whether an integer is odd or even using conditional operator */

#include <stdio.h>
int main(){
    int num;
    printf("Enter an integer you want to check: ");
    scanf("%d",&num);
    ((num%2)==0) ? printf("%d is even.",num) : printf("%d is odd.",num);
    return 0;
}
11、C语言检查是元音还是辅音

源代码：

#include <stdio.h>
int main(){
  char c;
  printf("Enter an alphabet: ");
  scanf("%c",&c);
  if(c=='a'||c=='A'||c=='e'||c=='E'||c=='i'||c=='I'||c=='o'||c=='O'||c=='u'||c=='U')
       printf("%c is a vowel.",c);
  else
       printf("%c is a consonant.",c);
  return 0;
}
输出1：

Enter an alphabet: i
i is a vowel.
输出2：

Enter an alphabet: G
G is a consonant.
也可以用条件运算符解决

/* C program to check whether a character is vowel or consonant using conditional operator */

#include <stdio.h>
int main(){
 char c;
 printf("Enter an alphabet: ");
 scanf("%c",&c);
 (c=='a'||c=='A'||c=='e'||c=='E'||c=='i'||c=='I'||c=='o'||c=='O'||c=='u'||c=='U') ? printf("%c is a vowel.",c) : printf("%c is a consonant.",c);
  return 0;
}
输出结果和上面的程序相同。

12、C语言实现从三个数值中查找最大值

实现1：

/* C program to find largest number using if statement only */

#include <stdio.h>
int main(){
      float a, b, c;
      printf("Enter three numbers: ");
      scanf("%f %f %f", &a, &b, &c);
      if(a>=b && a>=c)
         printf("Largest number = %.2f", a);
      if(b>=a && b>=c)
         printf("Largest number = %.2f", b);
      if(c>=a && c>=b)
         printf("Largest number = %.2f", c);
      return 0;
}
实现2：

/* C program to find largest number using if...else statement */

#include <stdio.h>
int main(){
      float a, b, c;
      printf("Enter three numbers: ");
      scanf("%f %f %f", &a, &b, &c);
      if (a>=b)
      {
          if(a>=c)
            printf("Largest number = %.2f",a);
          else
            printf("Largest number = %.2f",c);
      }
      else
      {
          if(b>=c)
            printf("Largest number = %.2f",b);
          else
            printf("Largest number = %.2f",c);
      }
      return 0;
}
实现3：

/* C Program to find largest number using nested if...else statement */

#include <stdio.h>
int main(){
      float a, b, c;
      printf("Enter three numbers: ");
      scanf("%f %f %f", &a, &b, &c);
      if(a>=b && a>=c)
         printf("Largest number = %.2f", a);
      else if(b>=a && b>=c)
         printf("Largest number = %.2f", b);
      else
         printf("Largest number = %.2f", c);
      return 0;
}
输出结果相同：

Enter three numbers: 12.2
13.452
10.193
Largest number = 13.45
13、C语言解一元二次方程

源代码：

/* Program to find roots of a quadratic equation when coefficients are entered by user. */
/* Library function sqrt() computes the square root. */

#include <stdio.h>
#include <math.h> /* This is needed to use sqrt() function.*/
int main()
{
  float a, b, c, determinant, r1,r2, real, imag;
  printf("Enter coefficients a, b and c: ");
  scanf("%f%f%f",&a,&b,&c);
  determinant=b*b-4*a*c;
  if (determinant>0)
  {
      r1= (-b+sqrt(determinant))/(2*a);
      r2= (-b-sqrt(determinant))/(2*a);
      printf("Roots are: %.2f and %.2f",r1 , r2);
  }
  else if (determinant==0)
  {
    r1 = r2 = -b/(2*a);
    printf("Roots are: %.2f and %.2f", r1, r2);
  }
  else
  {
    real= -b/(2*a);
    imag = sqrt(-determinant)/(2*a);
    printf("Roots are: %.2f+%.2fi and %.2f-%.2fi", real, imag, real, imag);
  }
  return 0;
}
输出1：

Enter coefficients a, b and c: 2.3
4
5.6
Roots are: -0.87+1.30i and -0.87-1.30i
输出2：

Enter coefficients a, b and c: 4
1
0
Roots are: 0.00 and -0.25
14、C语言检查是否是闰年

源代码：

/* C program to check whether a year is leap year or not using if else statement.*/

#include <stdio.h>
int main(){
      int year;
      printf("Enter a year: ");
      scanf("%d",&year);
      if(year%4 == 0)
      {
          if( year%100 == 0) /* Checking for a century year */
          {
              if ( year%400 == 0)
                 printf("%d is a leap year.", year);
              else
                 printf("%d is not a leap year.", year);
          }
          else
             printf("%d is a leap year.", year );
      }
      else
         printf("%d is not a leap year.", year);
      return 0;
}
输出1：

Enter year: 2000
2000 is a leap year.
输出2：

Enter year: 1900
1900 is not a leap year.
输出3：

Enter year: 2012
2012 is a leap year.
15、C语言检查一个数是正数、负数还是零

源代码：

#include <stdio.h>
int main()
{
    float num;
    printf("Enter a number: ");
    scanf("%f",&num);
    if (num<=0)
    {
        if (num==0)
          printf("You entered zero.");
        else
          printf("%.2f is negative.",num);
    }
    else
      printf("%.2f is positive.",num);
    return 0;
}
也可以使用if-else语句

/* C programming code to check whether a number is negative or positive or zero using nested if...else statement. */

#include <stdio.h>
int main()
{
    float num;
    printf("Enter a number: ");
    scanf("%f",&num);
    if (num<0)      /* Checking whether num is less than 0*/
      printf("%.2f is negative.",num);
    else if (num>0)   /* Checking whether num is greater than zero*/
      printf("%.2f is positive.",num);
    else
      printf("You entered zero.");
    return 0;
}
输出1：

Enter a number: 12.3
12.30 is positive.
输出2：

Enter a number: -12.3
-12.30 is negative.
输出3：

Enter a number: 0
You entered zero.
16、C语言检查某字符串是不是字母

源代码：

/* C programming code to check whether a character is alphabet or not.*/

#include <stdio.h>
int main()
{
    char c;
    printf("Enter a character: ");
    scanf("%c",&c);
    if( (c>='a'&& c<='z') || (c>='A' && c<='Z'))
       printf("%c is an alphabet.",c);
    else
       printf("%c is not an alphabet.",c);
    return 0;
}
输出1：

Enter a character: *
* is not an alphabet
输出2：

Enter a character: K
K is an alphabet
17、C语言计算自然数的和

源代码：

/* This program is solved using while loop. */

#include <stdio.h>
int main()
{
    int n, count, sum=0;
    printf("Enter an integer: ");
    scanf("%d",&n);
    count=1;
    while(count<=n)       /* while loop terminates if count>n */
    {
        sum+=count;       /* sum=sum+count */
        ++count;
    }
    printf("Sum = %d",sum);
    return 0;
}
也可以使用for循环语句

/* This program is solve using for loop. */

#include <stdio.h>
int main()
{
    int n, count, sum=0;
    printf("Enter an integer: ");
    scanf("%d",&n);
    for(count=1;count<=n;++count)  /* for loop terminates if count>n */
    {
        sum+=count;                /* sum=sum+count */
    }
    printf("Sum = %d",sum);
    return 0;
}
输出：

Enter an integer: 100
Sum = 5050
也可以通过if-else语句

/* This program displays error message when user enters negative number or 0 and displays the sum of natural numbers if user enters positive number. */

#include <stdio.h>
int main()
{
    int n, count, sum=0;
    printf("Enter an integer: ");
    scanf("%d",&n);
    if ( n<= 0)
        printf("Error!!!!");
    else
    {
       for(count=1;count<=n;++count)  /* for loop terminates if count>n */
       { 
          sum+=count;                    /* sum=sum+count */
       }
       printf("Sum = %d",sum);
    }
    return 0;
}
18、C语言计算阶乘

对于任意正数n，阶乘指的是：

factorial = 1*2*3*4....n
如果数值是负数，那么阶乘就不存在。并且我们规定，0的阶乘就是1。

源代码：

/* C program to display factorial of an integer if user enters non-negative integer. */

#include <stdio.h>
int main()
{
    int n, count;
    unsigned long long int factorial=1;         
    printf("Enter an integer: ");
    scanf("%d",&n);
    if ( n< 0)
        printf("Error!!! Factorial of negative number doesn't exist.");
    else
    {
       for(count=1;count<=n;++count)    /* for loop terminates if count>n */
       {
          factorial*=count;              /* factorial=factorial*count */
       }
    printf("Factorial = %lu",factorial);
    }
    return 0;
}
输出1：

Enter an integer: -5
Error!!! Factorial of negative number doesn't exist.
输出2：

Enter an integer: 10
Factorial = 3628800
先介绍到这里，下一篇将分享更多的C语言基础算法，敬请期待。
