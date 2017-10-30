# Numerical-statistics

Numerical statistics

Problem Description

统计给定的n个数中，负数、零和正数的个数。 


Input

输入数据有多组，每组占一行，每行的第一个数是整数n（n<100），表示需要统计的数值的个数，然后是n个实数；如果n=0，则表示输入结束，该行不做处理。

 
Output

对于每组输入数据，输出一行a,b和c，分别表示给定的数据中负数、零和正数的个数。

 
Sample Input

6 0 1 2 3 -1 0

5 1 2 3 4 0.5

0  


Sample Output

1 2 3

0 0 5 

解答：

#include<stdio.h>


int main()

{

    int n,i,b1,b2,b3;
    
    double a[101];
    
    while(scanf("%d",&n)!=EOF && n!=0)
    
    {
    
        for(i=0;i<n;i++) scanf("%lf",&a[i]);
        
        b1=b2=b3=0;
        
        for(i=0;i<n;i++)
        
        {
        
            if(a[i]<0) b1++;
            
            else if(a[i]==0) b2++;
            
            else b3++;
            
        }
        
        printf("%d %d %d\n",b1,b2,b3);
        
    }
    
}

