GUESS-A-NUMBER-LAB-1-WEEK-10
============================

LAB#1 WEEK 10 GUESS-A-NUMBER


// BY REINA OLARTE  CMS 112
//  LAB#1 WEEK 10


import java.util.Scanner;// imports the scanner class

public class GuessANumber
{
	public static void main( String[]args)
	{
		//Create the Scanner to input the number
		Scanner input = new Scanner(System.in);

		//instantiate random number
		RandomNumber GuessedNumber = new RandomNumber();

		//Declaring the variables
		int UsuaryNumber;
		int computerNumber;
		boolean SIGA = true;
		String SINO;
		

		while(SIGA)
		{
			computerNumber = GuessedNumber.GetANumber();

			System.out.println("Hi!!! Welcome to the Guessing game\nPlease enter a digit from 0 to 10:");
			UsuaryNumber = input.nextInt();

			if (computerNumber == UsuaryNumber)
			{
				System.out.println("You Guessed the right number");
				System.out.printf("Your number %d, Random number %d" , UsuaryNumber, computerNumber);
			}

			else
				{
					if (computerNumber < UsuaryNumber)
					{
						System.out.println("You Guessed to High");
						System.out.printf("Your number %d, Random number %d" , UsuaryNumber, computerNumber);
					}
					else
					{	System.out.println("You Guessed to Low");
					System.out.printf("Your number %d, Random number %d" , UsuaryNumber, computerNumber);
					}//end else	
				}//end else
			System.out.println("\nDo you want to continue?\nPress Y for yess N for no");
			SINO = input.next();

			if (SINO.toUpperCase().startsWith("Y"))
			{
				SIGA = true;
			}
			else
			{
				SIGA = false;
			}


		}//end loop
	}//End main

}//End class

