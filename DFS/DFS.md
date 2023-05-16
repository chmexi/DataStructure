# 深度优先搜索：

![截图](1463ad2dd0c69f2d3cd2270e38a12459.png)

#include <iostream>

using namespace std;

const int N = 10;

int n, path[N];
bool st[N];

void dfs(int u)
{
    if(u == n) 
    {
        for(int i = 0; i < n; i++) cout << path[i] << ' ';
        cout << endl;
    }

```
for(int i = 1; i <= n; i++)
{
    if(!st[i])
    {
        path[u] = i;
        st[i] = true;
        dfs(u+1);
        st[i] = false;
    }
}
```

}
