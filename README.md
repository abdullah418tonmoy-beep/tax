//tax

#include <stdio.h>

int main() {
    double income, tax = 0;

    printf("Enter your total income: ");
    scanf("%lf", &income);

    if (income <= 250000) {
        tax = 0;
    }
    else if (income <= 500000) {
        tax = (income - 250000) * 0.05;
    }
    else if (income <= 1000000) {
        tax = (250000 * 0.05) + (income - 500000) * 0.20;
    }
    else {
        tax = (250000 * 0.05) + (500000 * 0.20) + (income - 1000000) * 0.30;
    }

    printf("Total Payable Tax: %.2lf\n", tax);

    return 0;
}
