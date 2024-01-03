Removing Duplicates elements from an array in Java
Here, in this page we will discuss the program for removing duplicates elements from an array in java programming language. We are given with an array and need to print the array that only consist of distinct elements.
Removing Duplicates elements from an array in Java
Method Discussed :
Method 1 : Using Set Data Structure
Method 2 : Without Using Extra Space.
Let’s discuss both methods one by one in brief.

Method 1 :
Declare a set data structure.
Insert the elements of array in set.
Print the set
Time and Space Complexity :
Time Complexity : O(n)
Space Complexity : O(n)
Remove duplicates in Java
Set in Java
The set interface is present in java.util package and extends the Collection interface is an unordered collection of objects in which duplicate values cannot be stored.
It is an interface that implements the mathematical set.
This interface contains the methods inherited from the Collection interface and adds a feature that restricts the insertion of the duplicate elements.
Related Pages
Finding the Longest Palindrome in an Array

Counting Distinct Elements in an Array

Finding Non Repeating elements in an Array

Removing Duplicate elements from an array

Finding Minimum scalar product of two vectors

Method 1 : Code in Java
Run
import java.util.*;
class Main
{
  public static void main (String[] args)
  {
     int arr[] = {10, 20, 20, 30, 40, 40, 40, 50, 50};
     int n = arr.length;
     Set hash_Set = new HashSet();
for (int i=0; i<n; i++)
hash_Set.add(arr[i]);

System.out.print(hash_Set);
}
}
Output :
[50, 20, 40, 10, 30]
Method 2 :
In this method we will not use extra space.

Create a function say duplicate that will return the index value.
if(n==0) or (n==1) then return n.
Otherwise take a variable say j set j =0;
Run a loop from index 0 to n-1
If(arr[i]!=arr[i+1]), Then set arr[j++] = arr[i]
Finally, return the value of j
Time and Space Complexity :
Time Complexity : O(n)
Space Complexity : O(1)
Method 2 : Code in Java
Run
class Main
{
   static int removeDuplicates(int arr[], int n)
   {
      if (n==0 || n==1)
         return n;
int j = 0;
for (int i=0; i<n-1; i++)
if (arr[i] != arr[i+1])
arr[j++] = arr[i];
arr[j++] = arr[n-1];

return j;
}

public static void main (String[] args)
{
int arr[] = {10, 20, 20, 30, 40, 40, 40, 50, 50};
int n = arr.length;

n = removeDuplicates(arr, n);

for (int i=0; i<n; i++)
System.out.print(arr[i]+" ");
}
}
Output :
10 20 30 40 50
