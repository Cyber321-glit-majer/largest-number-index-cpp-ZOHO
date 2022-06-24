# largest-number-index-cpp-ZOHOput:

**PROBLEM STATEMENT**
You are an integer array nums where the largest integer is unique.
Determine whether the largest element in the array is at least twice as much as the other number in the array.
if it is,return the index of the largest element ,or return -1 otherwise.

**NOTE:**
1): Do not sort the array
2):Do not use new array

Example:
Input1: a[]={1,3,6,2}
output:2

Input2: a[]={1,4,2,5}
Output: -1


**CODE**

```

#include<bits/stdc++.h>
using namespace std;
int solve(int a[],int n)
{
    int mx=a[0];
    int mdi=0;
    for(int i=0;i<n;i++)
    {
        if(mx<a[i])
        {
            mx=a[i];
            mdi=i;
        }
        
    }
    bool flag=true;
    for(int i=0;i<n;i++)
    {
        if(a[i]!=mx)
        {
            if(2*a[i]<mx)
            {
                flag=true;
            }
        }
    }
    return flag?mdi:-1;
}
int main()
{
    
    int a[]={1,3,6,2};
    int n=sizeof(a)/sizeof(a[0]);
    cout<<solve(a,n);
    return 0;
}


