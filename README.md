## Problem: 1 (Count Frequency of Elements)

**Description:** Given an array of N integers (where `1 <= N <= 10^5` and values are in range `1 <= A[i] <= 10^5`), count how many times each number appears and print the frequency for all unique elements in increasing order.

**Sample Input:**

```
7
3 1 2 2 4 3 1
```

**Sample Output:**

```
1: 2
2: 2
3: 2
4: 1
```

**Solution:**

```C++
#include <bits/stdc++.h>
using namespace std;

int main() {

    int N;
    cin >> N;
    vector<int> A(N);

    for (int i = 0; i < N; ++i)
        cin >> A[i];

    map<int, int> freq;  // map keeps keys sorted
    for (int x : A)
        freq[x]++;

    for (auto [key, val] : freq)
        cout << key << ": " << val << '\n';

    return 0;
}

```

---

## Problem: 2 (Find the First Repeating Element)

**Description:** Given an array of N integers `(1 ≤ N ≤ 10⁵)`, find the `first element` that repeats more than `once`. If there is no such element, print `-1`.

**Sample Input:**

```
7
1 5 3 4 3 5 6
```

**Sample Output:**

```
3
3 is the first element that appears again later.
```

**Solution:**

```C++
#include <bits/stdc++.h>
using namespace std;

int main() {
    int N;
    cin >> N;
    vector<int> A(N);
    for (int i = 0; i < N; ++i) {
        cin >> A[i];
    }

    unordered_map<int, int> count;
    for (int x : A) {
        count[x]++;
    }

    for (int x : A) {
        if (count[x] > 1) {
            cout << x << '\n';
            return 0;
        }
    }

    cout << -1 << '\n';
    return 0;
}
```

---
