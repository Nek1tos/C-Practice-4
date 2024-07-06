# C-Practice-4

#include <stdio.h>

int count_equal_divisors(int n) {
    int count = 0;
    for (int i = 1; i * i <= n; i++) {
        if (n % i == 0) {
            int quotient = n / i;
            int remainder = n % i;
            if (quotient == remainder) {
                count++;
            }
        }
    }
    return count;
}

int main() {
    int n;
    printf("Enter a natural number: ");
    scanf("%d", &n);
    printf("Number of equal divisors: %d\n", count_equal_divisors(n));
    return 0;
}
