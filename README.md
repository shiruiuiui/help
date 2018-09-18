# ahhh
// add your 6-item heading here 

// any imports go here
import java.util.Scanner;

public class BodyMassIndex 
{
	// Define constants for unit conversions
	
	public static final double KILOGRAMS_PER_POUND = 0.453592;
	public static final double CM_PER_IN = 2.54;
	public static final double CM_TO_M = 1000;
	
	
	// Do not make any changes to the main!
	public static void main(String[] args) 
	{
		// 80-point version
		// Input user's weight and height in metric units and calculate BMI
		calculateMetricBMI();
		System.out.println();
		
		// 100-point version
		// Input user's weight and height in imperial units and calculate BMI
		calculateImperialBMI();
		System.out.println();
	}
	
	/** 
	 */
	 
	
	public static void calculateMetricBMI()
	{
		// complete for 80 pt version
		
		Scanner reader = new Scanner(System.in);
		System.out.print("Enter your weight in kilograms: ");
		int weightKilo = reader.nextInt();
		System.out.print("Enter your height in centimeters:  ");
		int heightCm = reader.nextInt();
		System.out.println();
		
		// call getBMI
		double x = getBMI(weightKilo, heightCm);
		
	/*	System.out.println("A body mass index of 20 - 25 is considered normal");
		System.out.printf("Your BMI is: %.2f", bmi);
		System.out.println();
	*/
		
	} 
		
	
	/** 
	 */ 
	public static double getBMI(int weightKG, int heightCM)
	{
		// complete for 80 pt version
		double bmi = (double)((double)weightKG / Math.pow((double)heightCM / 100, 2));
		
		System.out.println("A body mass index of 20 - 25 is considered normal");
		System.out.printf("Your BMI is: %.2d", bmi);
		System.out.println();
		return bmi;
	
	}
	
	
	/** 
	 */


	public static void calculateImperialBMI()
	{
		// complete for 100 pt version
		
		Scanner reader = new Scanner(System.in);
		System.out.print("Enter your weight in kilograms: ");
		int weightKilo = reader.nextInt();
		System.out.print("Enter your height in centimeters:  ");
		int heightCm = reader.nextInt();
		System.out.println();
		
		//converting
		/*convertPoundsToKG(int numKG);
		convertInchesToCM(int numCM);*/
			
		double x = getBMI(weightKilo, heightCm);	
			
	/*	System.out.println("A body mass index of 20 - 25 is considered normal");
		System.out.println("Your BMI is " + bmi);
		System.out.println();
	*/	
		//prompts user to enter data in pounds and inches
		System.out.print("Enter your weight in pounds: ");
		double weightPounds = reader.nextDouble();
		System.out.print("Enter your height in inches: ");
		double heightInches = reader.nextDouble();
		System.out.println();
	}
	
	/** 
	 */
	public static int convertPoundsToKG(int numPounds)
	{
		// complete for 100 pt version
		int lbToKilo = numPounds * (int) KILOGRAMS_PER_POUND;
		return lbToKilo;
	}
	
	/** 
	 */
	public static int convertInchesToCM(int numInches)
	{
		// complete for 100 pt version
		int inchesToCm = numInches * (int) CM_PER_IN;
		return inchesToCm;
	}
}
