# OOPsLabSolution
LAB Solution Assignment

import java.util.Scanner;

public class Administrator{
	
	String firstname;
	String lastname;
	String pass;
	String f;
	String l;
	int z=0;
	
	public void Employee(String m, String n)
	{
		firstname = m;
		lastname = n;
		
		System.out.print("\nYour name is registered as " + firstname + " " + lastname);
	}
	
	public void password(int q)
	{
		z = q;
		Administrator B1 = new Administrator();
		Scanner scan = new Scanner(System.in);
		if(z == 1)
		{
			System.out.println("Your password is successfully generated.");
			B1.run();
		}
		
		else
		{
			System.out.println("\n\nIn case to generate password, you need to generate email first. Would you like to generate email?\n1. YES\n2. NO");
			int num = scan.nextInt();
				switch(num)
				{
					case 1:
					{
						B1.generate();
					}
				
					case 2:
					{
					System.out.println("Sorry, you have ended the application");
					break;
					}
					
					default:
					{
						System.out.println("Wrong Choice\n\n");
						B1.run();
				}	}
			
		}
	}
	
	public void display(String x,String y)
	{
		firstname = x;
		lastname = y;
		System.out.println("Your credentials are generated as follows:");
		System.out.println("You email is ===> " + firstname + lastname +"@techIT.com");
		String pass = "TechIT@#"+lastname+"123";
		System.out.println("You password is ===> " + pass);
		Administrator E1 = new Administrator();

		E1.run();
	}
	
	public void generate()
	{
		Scanner obj = new Scanner(System.in);
		Administrator A1 = new Administrator();
		System.out.println("\n\nPlease enter your first name");
		String firstname = obj.next();
		System.out.println("\n\nPlease enter your last name");
		String lastname = obj.next();
		A1.Employee(firstname,lastname);
		System.out.println(" and your email is successfully generated.\n");
		z = 1;
		A1.run();
	}
	
	public void run()
	{
		Scanner value = new Scanner(System.in);
		Administrator D1 = new Administrator();
		int z=0;


		System.out.println("We have the following departments\n\n1. Technical\n2. Admin\n3. Human Resource\n4. Legal\n\nPlease select a department to use the services");
		int number = value.nextInt();
		
		if(number<5)
		{
	
	System.out.println("\n\nThis application can do the following");
	System.out.println("1. Generate an Email\n2. Generate a random password\n3. Display the Credentials\n4. Exit");
	int result = value.nextInt();
	
	switch(result)
	{
		case 1:
		D1.generate();
		break;
		
		case 2:
		D1.password(z);
		break;
		
		case 3:
		D1.display(firstname,lastname);
		break;
		
		case 4:
		break;
		
		default:
		System.out.println("You have entered a wrong choice");
		break;
		
		}}
		else
		{
			System.out.println("Wrong Choice");
		}
	}

		
public static void main(String args[])
{

	Scanner object = new Scanner(System.in);
		
	System.out.println("Welcome to Tech IT World company\n\nPlease select your choice:\n1. If you want to proceed with Application\n2. Exit from the application");
	int digit = object.nextInt();
	
	if(digit == 1)
	{
		Administrator C1 = new Administrator();
		C1.run();
	}
	
	else
	{
		System.out.println("Thank you! Please visit again.");
	}
	
	
}}
