#include<iostream>
using namespace std;
int n;int v[100];int k;
int start; int sfarsit;
int binalysearch( char start, char sfarsit,char k)
{
    int mijloc;
    mijloc=start+(sfarsit-start)/2;
    if (v[mijloc]=k);
        return 1;
    if(v[mijloc]<k)
        return binalysearch(mijloc+1, sfarsit,k);
    else
        return binalysearch(start, mijloc-1, k);
}

int main()
{
     cout << "n=";
     cin >> n;
    for (int i = 0; i < n; i++) {
        cout <<"v[" << i << "]=";
        cin >> v[i];
    }
    cout <<"k=";
    cin >>k;
    cout<<"reponse=";
    cout<<binalysearch(1,n,k);
}
