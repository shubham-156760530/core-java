# CORE JAVA CONTENT

## JAVA Collections:

- We have to import java.util.* package for using Collection Framework in java.
- The java.util package provides a framework of classes and interfaces for working with collections of objects.
- Collections in Java are used to store, retrieve, and manipulate groups of objects.
- There are multiple classes in Collection framework, here I mentioned some of the important classes related to different data structures.
  - ArrayList
  - LinkedList
  - HashMap
  - HashSet
  - Example of ArrayList Usage;
  -     import java.io.*;
        import java.util.*;
  
        class Base {
            
            public static int max(int a, int b){
                if (a > b) return a;
                return b;
            }
            
            public static int checkProfit(ArrayList<Integer> arr1){
                int profit = 0, curr_profit = 0;
                for (int i = 1; i < arr1.size(); i++){
                    if ((arr1.get(i)-arr1.get(i-1)) <= 0){
                        continue;
                    }
                    profit = profit + max (curr_profit, arr1.get(i)-arr1.get(i-1));
                }
                return profit;
            }
            
            public static void main(String []args){
                ArrayList<Integer> arr1 = new ArrayList<Integer>();
                arr1.add(1);
                arr1.add(5);
                arr1.add(3);
                arr1.add(8);
                arr1.add(12);
                int profit = checkProfit(arr1);
                System.out.println("maximum profit : "+profit);
            }
        }

## JAVA Regex

- Java does not have a built-in Regular Expression class, but we can import the java.util.regex package to work with regular expressions. The package includes the following classes:
  - Pattern Class - Defines a pattern (to be used in a search)
  - Matcher Class - Used to search for the pattern
  - PatternSyntaxException Class - Indicates syntax error in a regular expression pattern
  - Example of regex usage:
  -     /*package whatever //do not write package name here */
        import java.io.*;
        import java.util.*;
        import java.util.regex.Pattern;
        import java.util.regex.Matcher;
        
        class GFG {
        	public static void main (String[] args) {
        		Pattern pattern = Pattern.compile("w3schools", Pattern.CASE_INSENSITIVE);
                Matcher matcher = pattern.matcher("Visit W3Schools!");
                boolean matchFound = matcher.find();
                if (matchFound){
                    System.out.println("Match found");
                }
                else {
                    println("Match not found");
                }
        	}
        }
  - Example Explained
    - In this example, The word "w3schools" is being searched for in a sentence.
      - First, the pattern is created using the Pattern.compile() method. The first parameter indicates which pattern is being searched for and the second parameter has a flag to indicates that the search should be case-insensitive. The second parameter is optional.
      - The matcher() method is used to search for the pattern in a string. It returns a Matcher object which contains information about the search that was performed.
      - The find() method returns true if the pattern was found in the string and false if it was not found.
- Flags : Flags in the compile() method change how the search is performed. Here are a few of them:
  - Pattern.CASE_INSENSITIVE - The case of letters will be ignored when performing a search.
  - Pattern.LITERAL - Special characters in the pattern will not have any special meaning and will be treated as ordinary characters when performing a search.
  - Pattern.UNICODE_CASE - Use it together with the CASE_INSENSITIVE flag to also ignore the case of letters outside of the English alphabet
- [https://www.w3schools.com/java/java_regex.asp]
 
