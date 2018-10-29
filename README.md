# labnim
import java.util.Scanner;
public class Nim {
    public static void main() 
    {
        Scanner in = new Scanner(System.in);
        //two players can play this game
        System.out.println("Player 1, Enter your name: ");
        String first = in.nextLine();
        System.out.println("Player 2, Enter your name: ");
        String second = in.nextLine();
        
        //Allows the players to customize how many sticks to start with
        System.out.println("How many sticks would you like to start with?");
        int sticks = in.nextInt();
        //keeps track of whose turn it is
        int turnCount = 0;
        
        //a while loop keeps executing this code until there are no more sticks 
        while (sticks > 0) {
            printSticks(sticks);
            System.out.println();
            System.out.println("Begin removing sticks. Player 1 goes first, then Player 2.");
            System.out.println("Would you like to remove one or two sticks?");
            int n = in.nextInt();
            
            //a conditional statement makes sure that only 1 or 2 sticks can be removed
            if(n==1){
                System.out.print("One stick removed");
                sticks--;
                System.out.println();
                turnCount++;
            }
            else if(n==2){
                System.out.print("Two sticks removed");
                sticks = sticks-2;
                System.out.println();
                turnCount++;
            }
        }
        
         //turnCount keeps track of which player wins
        if(turnCount % 2 == 1){
            System.out.println("Player 2 wins!");
        }
        else if(turnCount % 2 ==0){
            System.out.println("Player 1 wins!");
        }
    }
    
        
    public static void printSticks(int sticks) {
        for (int i = 0; i < sticks; i++) {
            System.out.print("|");
        }
    }
    }
    
