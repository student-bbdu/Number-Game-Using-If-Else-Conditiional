# Number-Game-Using-If-Else-Conditiional

import java.util.Random;
import java.util.Scanner;


public class Numbergame {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int guess;
        System.out.println("Enter the Guess number : ");
        guess=sc.nextInt();
        Random r =new Random();
        int randomnumber = r.nextInt(100) + 1;
        int maximumAttempt = 3;
        int currentAttempt = 0;
        while(currentAttempt < maximumAttempt){
           System.out.println("Enter The Guess number : ");
            String Input = sc.nextLine();
            if(!Input.isEmpty()){
                System.out.println("You Entered : " + Input);
                currentAttempt++;
                if ( guess == randomnumber){
                System.out.println("Correct");
                } 
                else if( guess > randomnumber - 5 && guess < randomnumber + 5 ){
                System.out.println("Too Low");
                }
                else{
                System.out.println("To High");
                }
            }
        }
        System.out.println("Limit Exceed");  
    }
}
