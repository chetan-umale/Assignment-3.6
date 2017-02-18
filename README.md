Q1-Can you overload a method with the same return type? Explain your
answer with proper logic.

answer:
1.If a class has multiple methods having same name but different in parameters, it is known as Method Overloading.
2.There are two ways to overload the method in java
a)By changing number of arguments
b)By changing the data type

3.In java, method overloading is not possible by changing the return type of the method only because of ambiguity.


example:

class Adder{  
static int add(int a,int b){return a+b;}  
static double add(int a,int b){return a+b;}  
}  
class TestOverloading3{  
public static void main(String[] args){  
System.out.println(Adder.add(11,11));//ambiguity  
}}  

output:

Compile by: javac TestOverloading3.java

Overloading3.java:3: error: method add(int,int) is already defined in class Adder
static double add(int a,int b){return a+b;} 
^
1 error



Q2-Write a program in Java using Arrays, that sorts the element in a
descending order.



import java.util.Scanner;


public class acad {
	   public static void main(String a[])
	    {
	        //Numbers which need to be sorted
	        int numbers[] = {23,5,23,1,7,12,3,34,0};
	 
	        //Displaying the numbers before sorting
	        System.out.print("Before sorting, numbers are ");
	        for(int i = 0; i < numbers.length; i++)
	        {
	            System.out.print(numbers[i]+" ");
	        }
	        System.out.println();
	 
	        //Sorting in descending order using bubble sort
	        bubbleSortInDescendingOrder(numbers);
	 
	        //Displaying the numbers after sorting
	        System.out.print("Before sorting, numbers are ");
	        for(int i = 0; i < numbers.length; i++)
	        {
	            System.out.print(numbers[i]+" ");
	        }
	 
	    }
	 
	    //This method sorts the input array in desecnding order
	    public static void bubbleSortInDescendingOrder(int numbers[])
	    {
	        int temp;
	 
	        for(int i = 0; i < numbers.length; i++)
	        {
	            for(int j = 1; j < (numbers.length-i); j++)
	            {
	                //if numbers[j-1] < numbers[j], swap the elements
	                if(numbers[j-1] < numbers[j])
	                {
	                    temp = numbers[j-1];
	                    numbers[j-1]=numbers[j];
	                    numbers[j]=temp;
	                }
	            }
	        }
	    }

}
