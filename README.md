# Mahasena-CC


---

### ✅ **The Problem Recap:**

You are given:

* A number `N` (the number of soldiers)
* A list of `N` integers — each represents how many weapons a soldier has.

**Goal:**
Print `"READY FOR BATTLE"` if more soldiers have an **even number** of weapons than odd, otherwise print `"NOT READY"`.

---

### 🔍 **Code Explanation**

```cpp
#include <iostream>
using namespace std;
```

* This includes the I/O library and allows us to use `cin`, `cout`, etc.

---

```cpp
int main() {
```

* Main function: where the program starts running.

---

```cpp
    int n;
    cin >> n;
```

* `n` stores the number of soldiers.
* `cin >> n;` takes input from the user.

---

```cpp
    int weapon;
    int lucky = 0, unlucky = 0;
```

* `weapon` is a temporary variable to store each soldier’s weapon count.
* `lucky` counts how many soldiers have an **even** number of weapons.
* `unlucky` counts how many have an **odd** number.

---

```cpp
    for (int i = 0; i < n; ++i) {
        cin >> weapon;
        if (weapon % 2 == 0)
            lucky++;
        else
            unlucky++;
    }
```

* This loop runs `n` times to read weapon counts for each soldier.
* `weapon % 2 == 0` checks if the number is even.
* Even → increment `lucky`, else → increment `unlucky`.

---

```cpp
    if (lucky > unlucky)
        cout << "READY FOR BATTLE" << endl;
    else
        cout << "NOT READY" << endl;
```

* If more soldiers are “lucky” (have even weapon counts), print `"READY FOR BATTLE"`.
* Otherwise, print `"NOT READY"`.

---

### 📦 Example

Input:

```
5
2 3 4 5 6
```

* Even numbers: 2, 4, 6 → 3 soldiers
* Odd numbers: 3, 5 → 2 soldiers

Output:

```
READY FOR BATTLE
```

This C++ program reads the number of soldiers and how many weapons each one holds. It then counts how many soldiers have an even number of weapons (considered "lucky") and how many have an odd number (considered "unlucky"). Using a simple loop, it checks each number to see if it's divisible by 2, increasing the appropriate counter.

At the end, it compares the count of lucky vs. unlucky soldiers. If the number of lucky soldiers is greater, it prints "READY FOR BATTLE"; otherwise, it prints "NOT READY". This logic follows Kattapa’s belief that a stronger army has more soldiers with even weapon counts
