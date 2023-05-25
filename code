 /* jogo para curso formação em C */

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
        int seconds = time(0);
        srand(seconds);
        int randomnumber = rand();

        int secretnumber = randomnumber % 100;     /* a variavel secretnumber so poderá ser um valor entre 0 e 99 */
        int guessnumber;
        int attempts = 1;
        double score = 1000.0;

        int difficulty;
        printf("Which game mode would you like to play?\n");
        printf("(1) Easy, (2) Medium, (3) Hard\n\n");
        printf("Game mode: ");
        scanf("%d", &difficulty);

        int guesses;
        switch(difficulty) {
                case 1:
                        guesses = 15;
                        break;
                case 2:
                        guesses = 10;
                        break;
                default:
                        guesses = 5;
                        break;
        }

        int right = 0;

        printf(" ___________________________ \n");
        printf("        Guess Game         \n");
        printf("|___________________________|\n");
        printf("| The machine has chosen a  |\n");
        printf("| number, try to guess it!  |\n");
        printf(" ___________________________ \n");
        printf("\n");
        printf("You have %d attempts.\n", guesses);

        for(int i = 1; i <= guesses; i++) {
                printf("Attempt number %d\n", attempts);
                printf("Guess: ");
                scanf("%d", &guessnumber);

                if (guessnumber < 0) {
                        printf("You can't guess a negative number!\n");
                        continue;       /* faz o loop continuar sem quebrar ele */
                }

                printf(".\n");
                printf(".\n");
                printf(".\n");

                right = (guessnumber == secretnumber);
                int greater = (guessnumber > secretnumber);

                if (right) {
                        break;
                }
                else if (greater) {
                        printf("You're wrong!\n");
                        printf("The number you guessed is greater than the secret number...\n");
                }
                else {
                        printf("You're wrong!\n");
                        printf("The number you guessed is lesser than the secret number...\n");
                }
                attempts++;

                double truescore = abs(guessnumber - secretnumber) / 2.0;
                score = score - truescore;
        }
        if(right) {
                printf("You got it right! You took %d attempts.\n", attempts);
                printf("Score: %.0f\n", score);
        } else {
                printf("You couldn't guess it! The number was %d. Try again.\n", secretnumber);
        }

        printf("Game over.\n");
        return 0;
}






















