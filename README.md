# guess_a_number
java code game in which user gusseing the number.

import java.util.*;

import java.util.Random;

class game

{
	public int number;
	
	public int inputnumber;
	
	public int noofguesses=0;

	public int gettwonumber()
	{
		return noofguesses;
	}
	public void settwonumber(int noofguesses)
	{
		this.noofguesses=noofguesses;
	}
	
	game()
	{
		Random ran=new Random();
		System.out.println("Guess the number");
		this.number=ran.nextInt(100);
	}
	void takeuserinput()
	{
		Scanner sc=new Scanner(System.in);
		inputnumber = sc.nextInt();
	}
	boolean iscorrectnumber()
	{
		noofguesses++;
		if(inputnumber==number)
		{
			System.out.format("yes u guessed it right.");
			return true;
		}
		else if(inputnumber<number)
		{
			System.out.println("Too less...");
		}
		else if(inputnumber>number)
		{
			System.out.println("Too high...");
		}
		return false;
	}
}

class guess_number
{
	public static void main(String args[])
	{
		boolean b=false;
		
		game g=new game();
		
		while(!b){
		
		g.takeuserinput();
		
	        b=g.iscorrectnumber();
		
		System.out.println(b);
		
		}
		
	}
	
}
