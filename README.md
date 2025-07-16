# RockPaperScissors Java Game First Demo
// This is My first Git Repository.
// Auther- Om Raut

	import java.util.Random;
	import java.util.Scanner;

	public class RockPaperScissors {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        String[] choices = {"rock", "paper", "scissors"};

        System.out.println("Enter your choice (rock, paper, or scissors):");
        String playerChoice = scanner.nextLine().toLowerCase();

        String computerChoice = choices[random.nextInt(choices.length)];

        System.out.println("Computer chose: " + computerChoice);

        if (playerChoice.equals(computerChoice)) {
            System.out.println("It's a tie!");
        } else if (
                (playerChoice.equals("rock") && computerChoice.equals("scissors")) ||
                        (playerChoice.equals("paper") && computerChoice.equals("rock")) ||
                        (playerChoice.equals("scissors") && computerChoice.equals("paper"))
        ) {
            System.out.println("You win!");
        } else {
            System.out.println("You lose!");
        }

        scanner.close();
    }
}
