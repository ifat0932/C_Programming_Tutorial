#include <stdio.h>
#include <stdlib.h>
#include <time.h>

// Game logic function to determine the winner
int checkWinner(char user, char computer) {
    // 0 = Draw, 1 = User wins, -1 = Computer wins
    if (user == computer) {
        return 0;
    }
    
    if ((user == 'r' && computer == 's') || 
        (user == 'p' && computer == 'r') || 
        (user == 's' && computer == 'p')) {
        return 1;
    } else {
        return -1;
    }
}

int main() {
    char userChoice, computerChoice;
    int randomNumber;

    // Seed the random number generator with time to ensure different random numbers on every run
    srand(time(NULL));
    randomNumber = rand() % 100;

    // Determine the computer's choice based on the random number
    if (randomNumber < 33) {
        computerChoice = 'r'; 
    } else if (randomNumber >= 33 && randomNumber < 66) {
        computerChoice = 'p'; 
    } else {
        computerChoice = 's'; 
    }

    // --- Elegant UI Design (Game Name & Rules Box) ---
    printf("\n======================================================\n");
    printf("||                                                  ||\n");
    printf("||        WELCOME TO ROCK, PAPER, SCISSORS!         ||\n");
    printf("||                                                  ||\n");
    printf("======================================================\n");
    printf("||  GAME RULES & CONTROLS:                          ||\n");
    printf("||  ----------------------                          ||\n");
    printf("||  1. Enter 'r' for Rock     [ Rock beats Scissors]||\n");
    printf("||  2. Enter 'p' for Paper    [ Paper beats Rock ]  ||\n");
    printf("||  3. Enter 's' for Scissors [Scissors beats Paper]||\n");
    printf("||                                                  ||\n");
    printf("======================================================\n\n");

    // Taking user input
    printf("👉 Your Choice (r/p/s): ");
    scanf(" %c", &userChoice);

    // Input validation
    if (userChoice != 'r' && userChoice != 'p' && userChoice != 's') {
        printf("\n❌ Invalid input! Please enter 'r', 'p', or 's'.\n");
        return 1;
    }

    // Displaying choices made by user and computer
    printf("\n🧑 You chose: %c\n", userChoice);
    printf("🤖 Computer chose: %c\n", computerChoice);

    // Determine and display the final result
    int result = checkWinner(userChoice, computerChoice);

    printf("\n======================================================\n");
    if (result == 0) {
        printf("||              RESULT: It's a Tie! 🤝              ||\n");
    } else if (result == 1) {
        printf("||         🎉 RESULT: You Won the Game! 🎉          ||\n");
    } else {
        printf("||       🤖 RESULT: Computer Won! Try Again. 🤖      ||\n");
    }
    printf("======================================================\n\n");

    return 0;
}
