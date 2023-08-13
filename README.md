# amstrong_number_checker
#include <stdio.h>
#include <math.h>

int main() {
    int num, power = 0, original_num, digit, result = 0;
    printf("WHAT IS THE NUMBER: ");
    scanf("%d", &num);

    original_num = num; // Save the original number

    while (num > 0) {
        num /= 10;
        power += 1;
    }

    num = original_num; // Restore the original number

    while (num > 0) {
        digit = num % 10;
        result += pow(digit, power);
        num /= 10;
    }

    if (result == original_num) {
        printf("ARMSTRONG NUMBER\n");
    } else {
        printf("NOT AN ARMSTRONG NUMBER\n");
    }

    return 0;
}
