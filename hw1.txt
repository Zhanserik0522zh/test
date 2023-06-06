#include <iostream>
using namespace std;
int fibonacci(int n) {
    if (n <= 1)
        return n;

    int prev = 0;
    int curr = 1;

    for (int i = 2; i <= n; i++) {
        int temp = curr;
        curr = prev + curr;
        prev = temp;
    }

    return curr;
}

int main() {
    int n;
    cout << "Enter the value of n: ";
    cin >> n;
    
    cout << "The " << n << "th Fibonacci number is: " << fibonacci(n) <<endl;

    return 0;
}