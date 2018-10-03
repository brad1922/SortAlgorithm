# SortAlgorithm
Create a sort algorithm with a small group during class.
/* Adrien Simmons Braxton Gambrell Daniel Varas
 * 
 * This program asks the user to enter the size of the array, takes in numbers, then sorts the array using a selection sort.
 * 
 */
package Sort;

import java.util.Scanner;

public class SortAlgorithm {

	public static int[] SortAlgorithm(int[]arr) {
		        
		// Method that takes array of numbers, runs through each index and gradually sorts each number
		
		        for (int i = 0; i < arr.length - 1; i++)
		        {
		            int index = i;
		            for (int j = i + 1; j < arr.length; j++)
		                if (arr[j] < arr[index]) 
		                    index = j;
		      
		            int smallerNumber = arr[index];  
		            arr[index] = arr[i];
		            arr[i] = smallerNumber;
		        }
		        return arr;
		    }
		     
		    public static void main(String a[]){
		         
		    	int arr1[], num; // initializes the array used and the array's size
		    	
		    	Scanner scanner=new Scanner(System.in);
		    	
		    	System.out.println("Enter the value of array");
		    	
		    	 num =scanner.nextInt();
		    	
		    	arr1 = new int[num]; // sets array equal to the value of num
		    	
		    	System.out.println("Enter " + num + " integers");
		    	
		    	// for loop runs through and places a value in each index 
		    	
		    	for (int i=0; i< num; i++) {
		    		
		    		arr1[i] = scanner.nextInt();
		    	}
		    	
		    	   System.out.println("Unsorted:");
		    	   
		    	   for (int i=0; i< num; i++) {
			    		
			    	System.out.print(arr1[i]);
			    	System.out.print(" ");
			    	}
		       
		    	// Used as a separate array to place the sorted algorithm. Also calls the method from the top
		    
		    	  System.out.println("\n");
		    	  
		        int[] arr2 = SortAlgorithm(arr1);
		        
		        System.out.println("Sorted: " );
		        
		        for(int i:arr2){
		            System.out.print(i);
		            System.out.print(" ");
		        }
		    }
		}
