# operator-overloading-cpp
C++ implementation of operator overloading with a simple class-based example.
```cpp
#include <bits/stdc++.h>
using namespace std;
class A
{
    int weight;
public:
    A(int weight = 0)
    {
        this->weight = weight;
    }
    A add(A &obj)
    {
        A temp;
        temp.weight += this->weight + obj.weight;
        return temp;
    }
    A operator+ (const A &second_obj)
    {
        return A(this->weight + second_obj.weight); 
    }
    int get_weight();
};

int A ::get_weight()
{
    return weight;
}

signed main()
{
    int a, b; cin >> a >> b;
    A p1(a), p2(b);
    A total1 = p1.add(p2);
    A total2 = p1 + p2;
    cout << total1.get_weight() << '\n';
    cout << total2.get_weight() << '\n';
    return 0;
}

```
