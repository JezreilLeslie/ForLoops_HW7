# ForLoops_HW7
This is Homework 7

For Loops and Methods: Addition Game

INTRODUCTION:
This assignment is a remake of our Addition Game Assignment. This assignment teaches us to use for loops and methods to write code.

OUTLINE:
//Call the addition game method
//Set up “rules”
//Set up loop to go through the number of rounds
//Set up Scanner

CODE:
import java.util.Scanner

public class Addition_Game_ForLoops {
	public static void main(String[] args) {
	
	}
	public static void additionGameMethod() {
		
		int score = 5;
		int hardness = 2;
		int stopIndex = 0;
	
		//Set up my for loop to go through the number of rounds
		int numberOfRounds = 3;
		for(int roundNumber = 1;
		roundNumber <= numberOfRounds;
		roundNumber = roundNumber + 1){
			//System.out.println("Inside the for loop. Round: " + roundNumber);
			System.out.print("Round" + roundNumber + "of" + numberOfRounds + ". ");
			boolean isAnswerCorrect = getAndCheckStudentAnswer(hardness);
			if(isAnswerCorrect){
				System.out.print("your score was" + score + " and is now");
				score = score + hardness
				System.out.print(score + ". ");
				
				if(roundNumber<numberOfRounds){
					System.out.print("Your hardness was " + hardness + " and is now");
					hardness = hardness * hardnessStep;
					System.out.println(hardness + ".");
				}
		}else{
				System.out.print("Your score is" + score + ". ");
				if(roundNumber<numberOfRounds){
					System.out.print("Your hardness was " + hardness + " ans is now ");
					if(hardness>5){
						hardness = hardness / hardnessStep;
					}
					System.out.println(hardness + ".");
				}
	    }	
		}
		System.out.print("\nThe game is complete. ");
		System.out.println("Your final score was " + score);
	}
		
	public static boolean getAndCheckStudentAnswer(int hardness) {
		//System.out.println("Inside get and check student answer method.");
		int number1 = (int)(Math.random()*hardness);
		int number2 = (int)(Math.random()*hardness);
		System.out.print("Add " + number1 + " and" + number2 +": ");
		//Scanner input = new Scanner(System.in);
		//int studentAnswer = input.nextInt();
		Scanner get = new Scanner(System.in);
		int studentAnswer = get.nextInt();
		if(studentAnswer == (number1 + number2)){
			System.out.print("Correct. ");
			return true;
		}else{
			System.out.println("Nice try, but the correct answer was"
					+ (number1 + number2) + ".");
			return false;
		}
	}

CONSOLE:
What integer is 1 + 0?
Please enter integers only.
1
Your answer was correct.
Your score is now: 10
The next hardness will be: 100
End of round 1.
What integer is 49 + 52?
Please enter integers only.
101
Your answer was correct.
Your score is now: 110
The next hardness will be: 1000
End of round 2.
What integer is 708 + 904?
Please enter integers only.
1600
Your answer was not correct.
The correct answer was: 1612
Your hardness is now: 100
End of round 3.
What integer is 6 + 80?
Please enter integers only.
86
Your answer was correct.
Your score is now: 210
The next hardness will be: 1000
End of round 4.
Your final score is: 210

SUMMARY:
This assignment has taught us to use for loops. For loops makes coding easier by making the workload less and making coding more efficient. Using for loops can be really helpful when it comes to solving bigger problems.

