#include <stdio.h>

// Function to display the vending machine menu
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

    if (choice == 1) {
        printf("You selected Soda. Please insert AED 5.00.\n");
        // Add code here to handle the Soda selection
    } else if (choice == 2) {
        printf("You selected Chips. Please insert AED 3.00.\n");
        // Add code here to handle the Chips selection
    } else if (choice == 3) {
        printf("You selected Candy. Please insert AED 2.00.\n");
        // Add code here to handle the Candy selection
    } else {
        printf("Invalid choice. Please select a valid option (1/2/3).\n");
    }

    return 0;
}
