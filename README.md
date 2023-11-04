#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main() 
{
   
    int numberToGuess, userGuess, attempts = 0;

    
    srand(time(0));


    numberToGuess = rand() % 100 + 1;
    
    printf("Welcome to the Guess the Number game!\n");
    do {
        printf("Enter your guess (1-100): ");
        scanf("%d", &userGuess);
        attempts++;
        
        if (userGuess > numberToGuess) {
            printf(" high! Try again.\n");
        } 
        else if (userGuess < numberToGuess) {
            printf(" low! Try again.\n");
        }
        else {
            printf("Congratulations! You guessed the number %d in %d attempts.\n", numberToGuess, attempts);
        }
    }
    while (userGuess != numberToGuess);
    
    return 0; 
}
