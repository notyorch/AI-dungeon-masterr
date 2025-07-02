#include <stdio.h>
#include <stdbool.h>

int main() {
	// Declaring
	int choice = 0;
	int health = 100;
	bool hasKey = false;
	bool isAlive = true;
	int validInput = 0;
	int temp = 0; // 
	char bufferClearer; // To clear input
	
	// Main game loop
	while (isAlive == true) {
		// Printing the intro
		printf("\n");
		printf("*********************************************\n");
		printf(" WELCOME TO THE DUNGEON ADVENTURE GAME!!!! \n");
		printf("*********************************************\n");
		printf("You wake up in a scary dark dungeon!!!\n");
		printf("There are two creepy doors in front of you.\n");
		printf("Type 1 to go through left door.\n");
		printf("Type 2 to go through right door.\n");
		printf("What do you want to do??? ");
		validInput = scanf("%d", &choice);
		
		// Checking input
		if (validInput != 1) {
			printf("Hey! That's not a number! Try again!\n");
			while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
			continue;
		}
		if (choice != 1 && choice != 2) {
			printf("Dude, only 1 or 2 please! Try again!\n");
			while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
			continue;
		}
		
		// First choice
		if (choice == 1) {
			// Left door path
			printf("\n");
			printf("You went through the left door!\n");
			printf("OMG there's a huge sleeping dragon in here!\n");
			printf("What do you want to do now???\n");
			printf("Type 1 to sneak past the dragon.\n");
			printf("Type 2 to fight the dragon like a hero.\n");
			printf("Choose: ");
			validInput = scanf("%d", &choice);
			
			// Checking input again
			if (validInput != 1) {
				printf("Not a number, try again!\n");
				while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
				continue;
			}
			if (choice != 1 && choice != 2) {
				printf("Come on, only 1 or 2! Try again!\n");
				while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
				continue;
			}
			
			// Sneaking or fighting
			if (choice == 1) {
				// Sneak path
				printf("You're trying to sneak past the dragon...\n");
				printf("Wow, you made it! The dragon is still sleeping!\n");
				printf("You see a shiny key on a table thing.\n");
				printf("You grab the key! Nice!\n");
				hasKey = true;
				
				// Another choice point
				printf("\n");
				printf("There's a big locked door at the back!\n");
				printf("What do you want to do now???\n");
				printf("Type 1 to use the key (if you have it).\n");
				printf("Type 2 to smash the door with your hands.\n");
				printf("Choose: ");
				validInput = scanf("%d", &choice);
				
				// Input check again
				if (validInput != 1) {
					printf("That's not a number! Try again!\n");
					while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
					continue;
				}
				if (choice != 1 && choice != 2) {
					printf("Only 1 or 2, please! Try again!\n");
					while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
					continue;
				}
				
				if (choice == 1) {
					// Trying to use key
					if (hasKey == true) {
						printf("You use the key! The door opens!\n");
						printf("WHOA! There's a huge pile of treasure!\n");
						printf("YOU WON THE GAME!!!! CONGRATS!!!!\n");
						printf("----------------------------------------\n");
						printf("Want to play again? Type 1 for yes, anything else for no: ");
						validInput = scanf("%d", &choice);
						if (validInput != 1 || choice != 1) {
							printf("Thanks for playing! Bye!\n");
							isAlive = false;
						} else {
							printf("Starting new game!\n");
							hasKey = false;
							health = 100;
							temp = 0; // Resetting
						}
					} else {
						printf("Oh no! You don't have a key!\n");
						printf("The door won't open. You're stuck!\n");
						printf("GAME OVER!!!!\n");
						printf("----------------------------------------\n");
						printf("Want to play again? Type 1 for yes, anything else for no: ");
						validInput = scanf("%d", &choice);
						if (validInput != 1 || choice != 1) {
							printf("Thanks for playing! Bye!\n");
							isAlive = false;
						} else {
							printf("Starting new game!\n");
							hasKey = false;
							health = 100;
							temp = 0;
						}
					}
				} else {
					// Breaking door
					printf("You're trying to smash the door!\n");
					printf("Oh no! It's super loud!\n");
					printf("The dragon wakes up! It breathes fire!\n");
					printf("You lose 100 health points!\n");
					health = health - 100;
					if (health <= 0) {
						printf("You're totally burned! You died!\n");
						printf("GAME OVER!!!!\n");
						printf("----------------------------------------\n");
						printf("Want to play again? Type 1 for yes, anything else for no: ");
						validInput = scanf("%d", &choice);
						if (validInput != 1 || choice != 1) {
							printf("Thanks for playing! Bye!\n");
							isAlive = false;
						} else {
							printf("Starting new game!\n");
							hasKey = false;
							health = 100;
							temp = 0;
						}
					}
				}
			} else {
				// Fighting dragon
				printf("You try to fight the dragon!\n");
				printf("The dragon is way too strong!\n");
				printf("It breathes fire all over you!\n");
				printf("You lose 100 health points!\n");
				health = health - 100;
				if (health <= 0) {
					printf("You're burned to a crisp! You died!\n");
					printf("GAME OVER!!!!\n");
					printf("----------------------------------------\n");
					printf("Want to play again? Type 1 for yes, anything else for no: ");
					validInput = scanf("%d", &choice);
					if (validInput != 1 || choice != 1) {
						printf("Thanks for playing! Bye!\n");
						isAlive = false;
					} else {
						printf("Starting new game!\n");
						hasKey = false;
						health = 100;
						temp = 0;
					}
				}
			}
		} else {
			// Right door path
			printf("\n");
			printf("You went through the right door!\n");
			printf("There's a big locked chest in the room!\n");
			printf("What do you want to do???\n");
			printf("Type 1 to try opening the chest.\n");
			printf("Type 2 to ignore it and keep going.\n");
			printf("Choose: ");
			validInput = scanf("%d", &choice);
			
			// Input check
			if (validInput != 1) {
				printf("That's not a number! Try again!\n");
				while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
				continue;
			}
			if (choice != 1 && choice != 2) {
				printf("Only 1 or 2, come on! Try again!\n");
				while ((bufferClearer = getchar()) != '\n' && bufferClearer != EOF);
				continue;
			}
			
			if (choice == 1) {
				// Opening chest
				printf("You try to open the chest!\n");
				printf("OH NO! It's a trap!\n");
				printf("Poison gas comes out!\n");
				printf("You lose 50 health points!\n");
				health = health - 50;
				if (health <= 0) {
					printf("The poison was too much! You died!\n");
					printf("GAME OVER!!!!\n");
					printf("----------------------------------------\n");
					printf("Want to play again? Type 1 for yes, anything else for no: ");
					validInput = scanf("%d", &choice);
					if (validInput != 1 || choice != 1) {
						printf("Thanks for playing! Bye!\n");
						isAlive = false;
					} else {
						printf("Starting new game!\n");
						hasKey = false;
						health = 100;
						temp = 0;
					}
				} else {
					printf("You're still alive, somehow!\n");
					printf("You find an exit behind the chest!\n");
					printf("YOU ESCAPED! YOU WON THE GAME!!!!\n");
					printf("----------------------------------------\n");
					printf("Want to play again? Type 1 for yes, anything else for no: ");
					validInput = scanf("%d", &choice);
					if (validInput != 1 || choice != 1) {
						printf("Thanks for playing! Bye!\n");
						isAlive = false;
					} else {
						printf("Starting new game!\n");
						hasKey = false;
						health = 100;
						temp = 0;
					}
				}
			} else {
				// Ignoring chest
				printf("You ignore the chest.\n");
				printf("Smart move! You find an exit!\n");
				printf("YOU ESCAPED! YOU WON THE GAME!!!!\n");
				printf("----------------------------------------\n");
				printf("Want to play again? Type 1 for yes, anything else for no: ");
				validInput = scanf("%d", &choice);
				if (validInput != 1 || choice != 1) {
					printf("Thanks for playing! Bye!\n");
					isAlive = false;
				} else {
					printf("Starting new game!\n");
					hasKey = false;
					health = 100;
					temp = 0;
				}
			}
		}
	}
	
	// Just to print something
	printf("\nGG, i guess...\n");
	return 0;
}
