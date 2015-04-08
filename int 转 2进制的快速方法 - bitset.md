```C++
#include <iostream>
#include <bitset>
#include <string>

using namespace std;
int main (){
      int n = INT_MAX;
      bitset<32> myBits (n);
      string mystring ;
      mystring = myBits.to_string();
      cout << mystring << endl;
      return 0;
}

```
-----
```
bitset<32> myBits (int(65535));     //10进制到2进制, myBits.to_string();
bitset<32> myBits (string(1010010110101));     //2进制到10进制, myBits.to_ulong();
```
