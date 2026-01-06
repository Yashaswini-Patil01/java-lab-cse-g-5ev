#  ADDITIONAL EXPERIMENT-2:
## 2) Title: Sum of the fist n Fibonacci numbers
## Source Code:
```java
class Fibonacis {
    int firstNumber;
    int secondNumber;
    int thirdNumber;
    int sum;
    int sizeofFibsequence;
    Fibonacis(int size) {
    firstNumber =0;
    secondNumber =1;
    thirdNumber =0;
    sum =0;
    sizeofFibsequence=size;
   }
    void generateFibsequence() {
      while(sizeofFibsequence>0) {
       if(sizeofFibsequence>1)
    System.out.print(firstNumber +".");
    else
    System.out.print(firstNumber +",");
    sizeofFibsequence--;
    sum+=firstNumber;
    thirdNumber=firstNumber+secondNumber;
    firstNumber=secondNumber;
    secondNumber=thirdNumber;
   }
  }
    int getFibsum() {
      if(sum>0)
      return sum;
    else {
      generateFibsequence();
       return sum;
   }
  }
}
import java.util.Scanner;
  class main {
   public static void main(String args[]) {
  System.out.print("enter the sizeofFibsequence :");
    Scanner sc=new Scanner(System.in);
    int size =sc .nextInt();
       if(size>0) {
    Fibonacis Fib =new Fibonacis(size);
  System.out.print("Fibonacis series are :");
     Fib.generateFibsequence();
  System.out.println("the sum of Fibonacis series:"+ Fib.getFibsum());
 }
  else
  System.out.println("Fibonacis sequence and sum can not be calculate");
 }
}
```
## output:
![output](fs.png)
  
    
