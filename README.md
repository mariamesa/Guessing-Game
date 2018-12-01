# Guessing-Game
This program plays a simple guessing game with the user.

import java.util.Scanner;

public class GuessingGame {
    public static void main(String[] args) {
        // Explain the rules of the game
        System.out.println("Hello! Are you ready to play the guessing game?" +"\n"
                           + "The rules are simple. Guess a number between 0 and 100 and I will let you know if your number "
                           + "is too high or too low. Keep guessing until you get the right number." + "\n" +"Good Luck!"
                           + "\n");

        //Declare variables for count, math.random and guess
        int count= 1;
        double correctNum= (int) (Math.random() * 100);
        int guess;


        //Put in a scanner user input
        System.out.println("I am thinking of a number between 0 and 100." + "\n" + "Enter a guess: ");
        Scanner sc= new Scanner(System.in);
        guess= sc.nextInt();


        //Put in a while loop for wrong user input.
        while (guess != correctNum) {
            if (guess > correctNum) {
                System.out.println("Nope, my number is lower than " + guess + ". Guess again!");
                guess = sc.nextInt();
            }

            else if (guess < correctNum) {
                System.out.println("Nope, my number is higher than " + guess + ". Guess again!");
                guess = sc.nextInt();
            }

            count++;

        }

        System.out.println("Nice! You guessed the number in " + count + " tries!");




    }
}
