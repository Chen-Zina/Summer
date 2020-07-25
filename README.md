2.筛法求素数.
#include<stdio.h>
int main()
{
    int n;      //求从2到n的素数
    scanf("%d",&n);
    int a[n+1];
    int i,j;
    for(i=0;i<=n;i++)
    a[i]=1;    //1代表a[i]都是素数
    for(i=2;i<=n;i++)
    {
       for(j=2;i*j<=n;j++)
       {
          a[i*j]=0; //0去掉不是素数的数
        
       }
       if(a[i]==1) printf("%d ",i);
    }
    return 0;
}
