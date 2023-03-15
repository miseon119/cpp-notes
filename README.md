# cpp-notes

## std::transform

```cpp
#include <iostream>
#include <algorithm>
#include <vector>

int main() {
    std::vector<int> v1 = {1, 2, 3, 4, 5};
    std::vector<int> v2(v1.size());

    std::transform(v1.begin(), v1.end(), v2.begin(), [](int i){ return i * i; });

    for (auto i : v2) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
}

```

In this example, std::transform applies the lambda function `[](int i){ return i * i; }` to each element in v1, and stores the results in v2. The resulting vector v2 contains the squared values of the elements in v1.

