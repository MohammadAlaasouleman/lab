#include <stdio.h>


void displayMenu() {
    printf("Vending Machine Menu:\n");
    printf("1. Soda -  AED 5.00\n");
    printf("2. Chips - AED 3.00\n");
    printf("3. Candy - AED 2.00\n");
}

int main(void) {
    displayMenu();

    int choice;
    printf("Enter your choice (1/2/3): ");
    scanf("%d", &choice);

    int sodaStock = 5;
    int chipsStock = 10;
    int candyStock = 8;

    switch (choice) {
        case 1:
            if (sodaStock > 0) {
                printf("You selected Soda. Please insert AED 5.00.\n");
               

                double insertedMoney = 0.0;
                while (insertedMoney < 5.0) {
                    double amount;
                    printf("Insert money: AED ");
                    scanf("%lf", &amount);
                    insertedMoney += amount;
                }

                if (insertedMoney >= 5.0) {
                    printf("Payment successful. Enjoy your Soda!\n");
                    sodaStock--; 
                }
            } else {
                printf("Soda is out of stock. Please refill it.\n");
            }
            break;
        case 2:
            if (chipsStock > 0) {
                printf("You selected Chips. Please insert AED 3.00.\n");
                

                double insertedMoney = 0.0;
                while (insertedMoney < 3.0) {
                    double amount;
                    printf("Insert money: AED ");
                    scanf("%lf", &amount);
                    insertedMoney += amount;
                }

                if (insertedMoney >= 3.0) {
                    printf("Payment successful. Enjoy your Chips!\n");
                    chipsStock--; 
                }
            } else {
                printf("Chips are out of stock. Please refill them.\n");
            }
            break;
        case 3:
            if (candyStock > 0) {
                printf("You selected Candy. Please insert AED 2.00.\n");
             

                double insertedMoney = 0.0;
                while (insertedMoney < 2.0) {
                    double amount;
                    printf("Insert money: AED ");
                    scanf("%lf", &amount);
                    insertedMoney += amount;
                }

                if (insertedMoney >= 2.0) {
                    printf("Payment successful. Enjoy your Candy!\n");
                    candyStock--; 
                }
            } else {
                printf("Candy is out of stock. Please refill it.\n");
            }
            break;
        default:
            printf("Invalid choice. Please select a valid option (1/2/3).\n");
    }

    return 0;
}
