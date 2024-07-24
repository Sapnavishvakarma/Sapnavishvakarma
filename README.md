A Java program that takes a sentence as input from the user and counts the number of vowels and consonants:

```java
import java.util.Scanner;

public class VowelConsonantCounter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a sentence: ");
        String sentence = scanner.nextLine().toLowerCase(); // Convert to lowercase for case insensitivity

        int vowels = 0;
        int consonants = 0;

        // Loop through each character in the sentence
        for (int i = 0; i < sentence.length(); i++) {
            char ch = sentence.charAt(i);
            // Check if the character is a letter
            if (Character.isLetter(ch)) {
                // Check if the letter is a vowel
                if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                    vowels++;
                } else {
                    consonants++;
                }
            }
        }

        System.out.println("Number of vowels: " + vowels);
        System.out.println("Number of consonants: " + consonants);

        scanner.close();
    }
}

				
