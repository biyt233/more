```
//
// Created by lc on 2023/11/24.
#include <bits/stdc++.h>
using namespace std;
int mao(int x){
    return x>=500?x-x/10:x;
}
int dong(int x){
    return x>=1000?x-150:x;
}
int yin(int x){
    if(x==1111) return 0;
    return x-x/20;
}
int main() {
    int a;
    cin>>a;
    long  long money=0;
    for (int i=1; i<=a;i++) {
       int x;
       cin>>x;
        money=money+min({mao(x), dong(x), yin(x)});
    }
    cout << money;
}
```