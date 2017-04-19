package test;

import java.io.FileNotFoundException;
import java.io.IOException;

/**
 * Write a Java method that takes a Collection of Integers as a parameter and returns 
 * the second largest value in the list.
 * @author Rocio 
 *
 */
public class secondLargest {

	public static int secondLarge(int[] integerList) {
		// TODO Auto-generated constructor stub
		//initializing variable maxTop and assigning first element of array
		int maxTop = integerList[0];
		//initializing variable maxSec to zero
		int maxSec = 0;
		for (int i=1; i<integerList.length; i++){
			if (integerList[i] >= maxTop){
				maxSec = maxTop;
				maxTop = integerList[i];
			}
			if ((integerList[i] < maxTop) && (integerList[i] > maxSec)){
				maxSec = integerList[i];
			}			
		}
		//returning the second largest number
		return maxSec;
	}
		 
	public static void main(String[] args){
		
		//declare, create and initialize the integerList array
		int [] integerList = {10, 15, 25, 30, 5, 3, 800, 15, 68, 11, 35};
		
		//initialize variable that holds the second largest value from the method
		int secondMax= secondLarge(integerList);
		
		//printing the result
		System.out.println("The second largest value of the collection of integers is: " + secondMax); 
	}

}

