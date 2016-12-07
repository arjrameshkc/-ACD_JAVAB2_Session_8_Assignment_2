# -ACD_JAVAB2_Session_8_Assignment_2
package com.session8;

public class NegativeAgeException extends RuntimeException   {
	
	
	String errorMessage;
	 
    public NegativeAgeException(String errorMessage)
    {
        this.errorMessage = errorMessage;
    }
 
    @Override
    public String toString()
    {
        return errorMessage;
    }
    
 
}
package com.session8;

import java.util.Scanner;

public class NegativeAge {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
			 
        System.out.println("Enter Your Age");
        Scanner sc = new Scanner(System.in); 
        int age = sc.nextInt();         

        try
        {
            if(age < 0)
            {
                throw new NegativeAgeException("age cannot be negative");       
            }
        }
        catch(NegativeAgeException ex)
        {
            System.out.println(ex);    
        }
	}
}
