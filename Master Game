
Description: Game of rock paper scissors
*/

import java.util.*;

public class rockFinalCAses {
  
 public static void main(String[] args) {
   
   Random rand = new Random();
   
   int Instruct = (-1); //Value to pull up instructions at ANY point
   int Quit = (-99); //Value to quit game at ANY point 
   
   
   //Game Intro
   System.out.println("///////////////////////////////////////\n//WELCOME" +  
                      "TO ROCK, PAPER, SCISSORS!!!//\n//////////////////////////////////////\n");
   
   System.out.print("You will be asked to choose either ROCK, PAPER or SCISSORS. \n\nROCK BEATS SCISSORS.\n" +
                    "SCISSORS BEAT PAPER\nPAPER BEATS ROCK. \n\nWhoever gets more 3 points first wins.\n");
   System.out.print("To read this set of instructions at any time, type " + Instruct + 
                    ". To quit this game at any time input " + (Quit) + "\n");
   
   //Ask do you want to play
   System.out.println("\nDo you understand and wish to play? (1 - YES, ANY # - NO)");
   int start = Input(Quit, Instruct, Double.NEGATIVE_INFINITY, Double.POSITIVE_INFINITY);
   
   //While loop if user wants to play
   while (start == 1) {
     
     int userScore = 0;
     int compScore = 0;
   
     //Continues to repeat game untill someone wins
   while (userScore != 3 && compScore != 3) {
     
     
     //Array for valid move
     int[] moves = {1, 2, 3};
     
     //Assigning variable to each valid move
     int rock = moves[0];
     int scissors = moves[1];
     int paper = moves[2];
     
     
     //Generates Computers Move
     int computerChoices = ((rand.nextInt(3) + 1));
     
     //Asks for users choice
     System.out.println("Pick one of the following.. 1 - ROCK, 2 - SCISSORS, 3 - PAPER");
     int userPlay = Input(Quit, Instruct, 1, 3);
     /*Asks for input and checks it against the value to quit 
      * and instructions as well as the set range of appropriate values (calls method)
      */
     
     //Opening switch statement for the number of stars in each bar
     
     for (int i=0; i<3; i++)
       switch (i) {
       case 1:
         userPlay = computerChoices;
         System.out.println("TIE. NO POINTS SCORED"); //USER PLAY EQUALS COMPUTERS CHOICE
         break;
         
       case 2:
         userPlay = rock; //USER PLAY EQUALS ROCK
         if (computerChoices == scissors) {
           System.out.println("Rock crushes scissors, I got scissors, you got rock. You WINNN!!");
           userScore++;
           System.out.println("Your score is " + userScore + ". My score is " + compScore + "\n");
         }
         
         else if (computerChoices == paper) {
           System.out.println("Paper beats Rock, as I had paper and you had a rock. You LOSE!!");
           compScore++;
           System.out.println("Your score is " + userScore + ". My score is " + compScore + "\n");
         }
         break;
         
       case 3:
         userPlay = scissors; //USER PLAY EQUALS SCISSORS
         if (computerChoices == rock) {
           System.out.println("Rock crushes scissors, as I had the rock and demolished your scissors. You LOSE!!");
           compScore++;
           System.out.println("Your score is " + userScore + ". My score is " + compScore + "\n");
         } 
         //If user plays scissors and computer paper then user wins.
         else if (computerChoices == paper) {
           System.out.println("Scissors beats paper, as your lukcy self had scissors while I had paper. You Win!!!");
           userScore++;
           System.out.println("Your score is " + userScore + ". My score is " + compScore + "\n");
         }
         break;
         
       case 4:
         userPlay = paper; //USERPLAY EQUALS PAPER
         if (computerChoices == rock) {
           System.out.println("Paper eats rock, as you had the paper which flattened my rock. You Win!!");
           userScore++;
           System.out.println("Your score is " + userScore + ". My score is " + compScore + "\n");
         } 
                                
         else if (computerChoices == scissors) {
           System.out.println("Scissors eat paper, as I had the scissors that shredded your paper. You Lose!!!");
           compScore++;
           System.out.println("Your score is " + userScore + ". My score is " + compScore + "\n");
         }
         break;

     }//CLOSE SWITCH
   }//CLOSING while loop for score
   
   //When someone wins, ask if they want to play again
   if (userScore != 3 || compScore != 3) {
     System.out.println("Do you wish to play again? (1 - YES, ANY # - NO)");
     start = Input(Quit, Instruct, Double.NEGATIVE_INFINITY, Double.POSITIVE_INFINITY);
   }//closing if
   
   } //Close start game while loop
   
   //Close game if they don't want to play
   System.out.println("OK!");
   System.exit(0);
   
 }//closing main method
 
 
 
 //Asking for input and checking it method
 public static int Input(int Quit, int Instruct, double min, double max) {
   Scanner myInput = new Scanner(System.in); //Start scanner
   
   //Asks for input
  int Input = myInput.nextInt();
  
  //Infinite Loop
  while (true) {
    //Checking if user wants to close game
    while (Input == Quit) {
      System.out.println("Goodbye.");
      System.exit(0);
    }
    //Checking if user wants to bring up instructions
   while (Input == Instruct) {
     System.out.println("You will be asked to choose either ROCK, PAPER or SCISSORS. ROCK BEATS SCISSORS." +
                        "SCISSORS BEAT PAPER AND PAPER BEATS ROCK. Whoever gets 3 points first wins.\n");
     Input = Input(Quit, Instruct, 1, 3);
   }
   
   
   //Checking users input against min value
   while (Input < min) {
    System.out.println("Choose a valid number");
    Input = Input(Quit, Instruct, 1, 3);
   }
   //Checking users input against max value
   while (Input > max) {
     System.out.println("Choose a valid number");
     Input = Input(Quit, Instruct, 1, 3);
   }
   myInput.close();
   return Input;
  } //Ending infinite loop
 } //End of method
} //End Class
