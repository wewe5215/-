//
//  main.c
//  12519 the secrecy
//
//  Created by wewe on 2020/12/12.
//

#include <stdio.h>
#include <string.h>
int n=0;
char p[5005];
char s[5005];
char alp[26];
int count=0;
char ans[5005][5005];
int f[5005];int flag=0;
int calculator(char* p,char* s);
int main()
{
    scanf("%d %s",&n,p);
    while(n--)//判斷有沒有重複的並加上次數
    {
        scanf("%s",s);
        if(calculator(p,s)==0)continue;
        flag=0;
        int i=0;
        for(i=0;i<count;i++)
        {
            if(strcmp(ans[i],s)==0)
            {
                flag=1;
                break;
            }
        }
            if(flag==1)f[i]++;
            else
            {
            strcpy(ans[count],s);
            f[count]=1;
            count++;
            }
    }
    printf("%d\n",count);
    for(int i=0;i<count;i++)//arrange the answer
    {
        for(int j=0;j<count-1-i;j++)
        {
            flag=0;
            if(f[j]<f[j+1])flag=1;
            else if(f[j]>f[j+1])flag=0;
            else//only when the frequency is equal,then we consider this condition
            {
            if(strcmp(ans[j],ans[j+1])>0)flag=1;
            }
            char change[5010];int change_int=0;
            if(flag)
           {
               strcpy(change,ans[j]);strcpy(ans[j],ans[j+1]);strcpy(ans[j+1],change);
               change_int=f[j];f[j]=f[j+1];f[j+1]=change_int;
           }
        }
    }
    for(int i=0;i<count;i++)printf("%s %d\n",ans[i],f[i]);
    
    
    return 0;
}
int calculator(char* p,char* s)
{
    char alp1[26]={'\0'};//initialize
    char alp2[26]={'\0'};
    if(strlen(p)!=strlen(s))return 0;
    else
    {
        for(int i=0;i<strlen(s);i++)
        {
            
//e.g. abcccd abbbbd,p to s is correct but on the opposite,it's false
            alp1[s[i]-'a']=p[i];
            alp2[p[i]-'a']=s[i];
        }
        
        for(int i=0;i<strlen(s);i++)
        {
            if(alp1[s[i]-'a']!=p[i]||alp2[p[i]-'a']!=s[i])return 0;
           
        }
    }
   return 1;
    
}
