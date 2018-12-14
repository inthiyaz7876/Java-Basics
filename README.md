# Java-Basics
Java Basics 

What is encapsulation?
----------------------
The whole idea behind encapsulation is to hide the implementation details from users. If a data member is private it means it can only be accessed within the same class. No outside class can access private data member (variable) of other class.

Example of Encapsulation in Java
---------------------------------
How to implement encapsulation in java:
1) Make the instance variables private so that they cannot be accessed directly from outside the class. You can only set and get values of these variables through the methods of the class.
2) Have getter and setter methods in the class to set and get the values of the fields.

class EncapsulationDemo{
    private int ssn;
    private String empName;
    private int empAge;

    //Getter and Setter methods
    public int getEmpSSN(){
        return ssn;
    }

    public String getEmpName(){
        return empName;
    }

    public int getEmpAge(){
        return empAge;
    }

    public void setEmpAge(int newValue){
        empAge = newValue;
    }

    public void setEmpName(String newValue){
        empName = newValue;
    }

    public void setEmpSSN(int newValue){
        ssn = newValue;
    }
}
public class EncapsTest{
    public static void main(String args[]){
         EncapsulationDemo obj = new EncapsulationDemo();
         obj.setEmpName("Mario");
         obj.setEmpAge(32);
         obj.setEmpSSN(112233);
         System.out.println("Employee Name: " + obj.getEmpName());
         System.out.println("Employee SSN: " + obj.getEmpSSN());
         System.out.println("Employee Age: " + obj.getEmpAge());
    } 
}
Output:

Employee Name: Mario
Employee SSN: 112233
Employee Age: 32
**********************
In above example all the three data members (or data fields) are private which cannot be accessed directly. These fields can be accessed via public methods only. Fields empName, ssn and empAge are made hidden data fields using encapsulation technique of OOPs.
===================================================================================================================================
Java Access Modifiers – Public, Private, Protected & Default
--------------------------------------------------------------
You must have seen public, private and protected keywords while practising java programs, these are called access modifiers. An access modifier restricts the access of a class, constructor, data member and method in another class. In java we have four access modifiers:
1. default
2. private
3. protected
4. public

1. Default access modifier

When we do not mention any access modifier, it is called default access modifier. The scope of this modifier is limited to the package only. This means that if we have a class with the default access modifier in a package, only those classes that are in this package can access this class. No other class outside this package can access this class. Similarly, if we have a default method or data member in a class, it would not be visible in the class of another package. Lets see an example to understand this:
Default Access Modifier Example in Java
-------------------------------------
Note : Please go through Packages before you understand Default
Packages in java and how to use them:
In java we have several built-in packages, for example when we need user input, we import a 
1> build in package:
import java.util.Scanner
Here:
    → java is a top level package
    → util is a sub package
    → and Scanner is a class which is present in the sub package util.
Advantages of using a package in Java
    Reusability
    Better Organization
    Name Conflicts
2> User defined package
 Calculator.java file created inside a package letmecalculate

package letmecalculate;

public class Calculator {
   public int add(int a, int b){
	return a+b;
   }
   public static void main(String args[]){
	Calculator obj = new Calculator();
	System.out.println(obj.add(10, 20));
   }
}
Now lets see how to use this package in another program.

import letmecalculate.Calculator;
public class Demo{
   public static void main(String args[]){
	Calculator obj = new Calculator();
	System.out.println(obj.add(100, 200));
   }
}
Lets start the 'default' exmaple.
---------------------------------


