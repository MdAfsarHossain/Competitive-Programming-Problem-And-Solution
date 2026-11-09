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

## Problem: 3 (Check if a Number is Prime)

**Description:** Given an integer `N` (where `1 <= N <= 10^6`), determine whether it is a prime number. A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.

**Sample Input:**

```
17
```

**Sample Output:**

```
Yes
```

**Sample Input:**

```
15
```

**Sample Output:**

```
No
```

**Solution:**

```C++
#include <bits/stdc++.h>
using namespace std;

bool isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= sqrt(n); ++i) {
        if (n % i == 0) return false;
    }
    return true;
}

int main() {
    int N;
    cin >> N;

    if (isPrime(N)) {
        cout << "Yes" << endl;
    } else {
        cout << "No" << endl;
    }

    return 0;
}
```

---

## Problem: 4 (Reverse a String)

**Description:** Given a string `S`, reverse the string and print the reversed string. The length of the string `S` is between `1` and `10^5`.

**Sample Input:**

```
hello
```

**Sample Output:**

```
olleh
```

**Solution:**

```C++
#include <bits/stdc++.h>
using namespace std;

int main() {
    string S;
    cin >> S;
    reverse(S.begin(), S.end());
    cout << S << endl;
    return 0;
}
```

---

## Problem: 5 (Calculate Factorial)

**Description:** Given a non-negative integer N (where `0 <= N <= 12`), calculate and print its factorial. The factorial of a non-negative integer n, denoted by n!, is the product of all positive integers less than or equal to n.

**Sample Input:**

```
5
```

**Sample Output:**

```
120
```

**Solution:**

```C++
#include <iostream>
using namespace std;

int main() {
    int N;
    cin >> N;

    long long factorial = 1;
    for (int i = 1; i <= N; ++i) {
        factorial *= i;
    }

    cout << factorial << endl;
    return 0;
}
```

---

## Problem: 6 (Sum of Array Elements)

**Description:** Given an array of N integers (where `1 <= N <= 10^5` and `1 <= A[i] <= 10^9`), calculate and print the sum of all elements.

**Sample Input:**

```
5
1 2 3 4 5
```

**Sample Output:**

```
15
```

**Solution:**

```C++
#include <bits/stdc++.h>
using namespace std;

int main() {
    int N;
    cin >> N;

    long long sum = 0;  // sum can reach 10^14, so int is not enough
    for (int i = 0; i < N; ++i) {
        int x;
        cin >> x;
        sum += x;
    }

    cout << sum << endl;
    return 0;
}
```

---

## Problem: 7 (Find the Maximum Element)

**Description:** Given an array of N integers (where `1 <= N <= 10^5` and `-10^9 <= A[i] <= 10^9`), find and print the largest element.

**Sample Input:**

```
6
3 -1 7 2 9 4
```

**Sample Output:**

```
9
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

    cout << *max_element(A.begin(), A.end()) << endl;
    return 0;
}
```

---

## Problem: 8 (Check Palindrome String)

**Description:** Given a string `S` (length between `1` and `10^5`, no spaces), determine whether it reads the same forwards and backwards. Print `Yes` if it is a palindrome, otherwise print `No`.

**Sample Input:**

```
madam
```

**Sample Output:**

```
Yes
```

**Sample Input:**

```
hello
```

**Sample Output:**

```
No
```

**Solution:**

```C++
#include <bits/stdc++.h>
using namespace std;

int main() {
    string S;
    cin >> S;

    string R = S;
    reverse(R.begin(), R.end());

    if (S == R) {
        cout << "Yes" << endl;
    } else {
        cout << "No" << endl;
    }

    return 0;
}
```

---
