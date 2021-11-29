# OOPsLabSolution
LAB Solution Assignment
import java.util.Scanner;

public class FirstJavaProgram{

public static void main(String args[])
{
	Scanner obj = new Scanner(System.in);
	
	System.out.println("Please help me with your name");
	String fname = obj.next();
	System.out.println("Please help me with last name");
	String lname = obj.next();
	System.out.println("Please press 1 if your name is :" + fname + " " + lname);
	int result = obj.nextInt();
	
	if(result == 1)
	{
		System.out.println("Nice to meet you " + fname + " " + lname +", I hope you are doing well.");
	}
	
	else
	{
		System.out.println("Sorry your name does not matched");
	}
	
	System.out.println("Hello " + fname + " " + lname + ", What you want to today");
	System.out.println("1. Check Your Account Information");
	System.out.println("2. Fetch your loan details");
	System.out.println("3. Cash Withdrawal");
	System.out.println("4. Fetch personal details");
	System.out.println("5. Exit");
	
	int number = obj.nextInt();
	
	switch(number)
	{
		case 0:
		System.out.println("I will check the account information");
		break;
		
		case 2:
		System.out.println("I will fetch the loan details");
		break;
		
		case 3:
		System.out.println("I will withdraw the cash");
		break;
		
		case 4:
		System.out.println("I will fetch the personal details");
		break;
		
		case 5:
		System.out.println("I want to exit");
		break;
		
		default:
		System.out.println("Please provide the correct input");
		break;
	}

	
}

}
