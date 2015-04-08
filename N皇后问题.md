```c++

#include <iostream>
#include <stdlib.h>
using namespace std;

#define N 8
int sum =0;
int x [N+1]={0};

bool canPlaceQuene (int t){
      for (int i=1; i<t ;i++)
     {
           if (x [t] == x[i ] || (abs( x[t ]-x[ i]) == abs(t -i)))
          {
               return 0;
          }
     }
      return 1;
}


//对比: C++实现全排列 --- 递归实现
void queneNum (int k){
      if (k > N)
     {
           sum++;
     } else{
           for (int i=1; i<=N ;i++)
          {
               x[k ] = i;    
               //判断第k 个皇后能不能在 i 处放; 能放,则处理第k+1个
               if (canPlaceQuene (k))
              {
                    queneNum(k +1);
              }
          }
     }
}

int main (){
      queneNum(1);
      cout << sum << endl;
      return 0;
}

```
