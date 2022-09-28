# Palindrome.java

import java.util.*;
public class Palindrome 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
   
     String original = sc.nextLine();
		original = original.replace(" ", "");
		original = original.toLowerCase();

		String reverse = "";
		for(int i = original.length() - 1; i >= 0; i--) {
			reverse += original.charAt(i);
			System.out.println(reverse);
		}
		
		boolean palindrome = true;
		for(int i = 0; i < original.length(); i++) {
			if(original.charAt(i) != reverse.charAt(i)) {
				palindrome = false;
			}
		}
		
		if(palindrome) {
			System.out.println("You entered a palindrome");
		} else {
			System.out.println("You did not enter a palindrome");
		}
	}
}

