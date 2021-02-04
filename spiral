//
//  main.c
//  spiral
//
//  Created by wewe on 2021/2/1.
//

#include <stdio.h>
char ans[5005][5005];
int main()
{
    int t=0;
    scanf("%d",&t);
    while(t--)
    {
        int n=0;
        scanf("%d",&n);
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                ans[i][j]=' ';
            }
        }
        
        int left=0;int right=0;
        for(int count=0;count<n;count++)
        {
            if(count%4==2)
            {
                for(int i=right;i>=right-(n-count);i--)
                {
                    ans[left][i]='#';
                    
                }
                right=right-(n-count);
            }
            if(count%4==3)
            {
                for(int i=left;i>=left-(n-count);i--)
                {
                    ans[i][right]='#';
                    
                }
                left=left-(n-count);
            }
            if(count%4==0)
            {
                if(count==0)
                {
                   for(int i=right;i<right+(n-count);i++)

                    {
                        ans[left][i]='#';
                    }
                    right=right+(n-count)-1;
                    
                }
                else
                {
                    for(int i=right+1;i<=right+(n-count);i++)
                       ans[left][i]='#';
                    right=right+(n-count);
                }
            }
            if(count%4==1)
            {
               
                for(int i=left+1;i<=left+(n-count);i++)
                {
                    
                    ans[i][right]='#';
                }
                left=left+(n-count);
            }
        }
        
        
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                printf("%c",ans[i][j]);
            
            }
           
            printf("\n");
        }
    }

    
    
    return 0;
}
