#include <stdio.h>

struct Expense {
    char name[50];
    float amount;
};

int main() {
    struct Expense e[100];
    int choice, count = 0, i;
    float total = 0, budget, balance;

    printf("================================\n");
    printf("     DAILY EXPENSE TRACKER\n");
    printf("================================\n");

    printf("Enter your daily budget: Rs.");
    scanf("%f", &budget);

    do {
        printf("\n----- EXPENSE MENU -----\n");
        printf("1. Add Expense\n");
        printf("2. View Expenses\n");
        printf("3. Total Expenses\n");
        printf("4. Remaining Balance\n");
        printf("5. Exit\n");

        printf("\nEnter your choice: ");
        scanf("%d", &choice);

        switch(choice) {

            case 1:
                if(count < 100) {
                    printf("Enter expense name: ");
                    scanf(" %49[^\n]", e[count].name);

                    printf("Enter amount: Rs.");
                    scanf("%f", &e[count].amount);

                    if(e[count].amount < 0) {
                        printf("Invalid amount!\n");
                    } else {
                        total += e[count].amount;
                        count++;
                        printf("Expense added successfully!\n");
                    }
                } else {
                    printf("Expense limit reached!\n");
                }
                break;

            case 2:
                printf("\n----- EXPENSE DETAILS -----\n");

                if(count == 0) {
                    printf("No expenses recorded.\n");
                }

                for(i = 0; i < count; i++) {
                    printf("%d. %s - Rs.%.2f\n",
                           i + 1, e[i].name,
                           e[i].amount);
                }
                break;

            case 3:
                printf("\nTotal Expenses: Rs.%.2f\n", total);
                break;

            case 4:
                balance = budget - total;
                printf("\nDaily Budget: Rs.%.2f\n", budget);
                printf("Total Expenses: Rs.%.2f\n", total);
                printf("Remaining Balance: Rs.%.2f\n", balance);

                if(balance < 0) {
                    printf("Budget exceeded!\n");
                }
                break;

            case 5:
                printf("\nThank you for using Daily Expense Tracker!\n");
                break;

            default:
                printf("\nInvalid choice! Try again.\n");
        }

    } while(choice != 5);

    return 0;
}
