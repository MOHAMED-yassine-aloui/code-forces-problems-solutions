#include<bits/stdc++.h>
using namespace std;
int main()
{

    string a,b;
    cin>>a>>b;
    long long i=0,j=0,x=0,ans=0,diff=b.size()-a.size()+1;
    for(int i=0;i<diff;i++)
    {
        x+=b[i]-'0';
    }
    for(int i=0;i<a.size();i++)
    {
       ans+=(a[i]=='0')?x:diff-x;
       x+=b[diff+i]-b[i];
    }
cout<<ans;
}
