# EXPERIMENT-4
## 4a) Title: 
## Source Code:
```java
class Person {
    String name;
    int age; 

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    Employee(String name, int age, double annualSalary, int yearOfJoining, String nationalInsuranceNumber) {
        super(name, age);
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("National Insurance Number: " + nationalInsuranceNumber);
    }
}

public class TestEmployee {
    public static void main(String[] args) {
        Employee emp1 = new Employee(
                "yashi",
                26,
                500000.0,
                2029,
                "NI12345"
        );

        emp1.displayEmployeeDetails();
    }
}
```
## Output:
![output](p1.png)

## 4b) Title: 
## Source Code:
```java
class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals.");
        System.out.println("Pedal Type: " + pedalType);
    }
}


class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine.");
        System.out.println("Engine Capacity: " + engineCapacity + " cc");
    }
}


class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor and battery.");
        System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}


public class TestVehicle {
    public static void main(String[] args) {

        ElectricBike eBike = new ElectricBike();
        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 150;
        eBike.batteryCapacity = 500;
        eBike.showBicycleInfo();      
        eBike.showMotorbikeInfo();     
        eBike.showElectricBikeInfo();  
 }
}
```
## Output:
![output](v1.png)


## 4c) Title: 
## Source Code:
```java
abstract class Figure {
    double dim1;
    double dim2;

    Figure(double d1, double d2) {
        dim1 = d1;
        dim2 = d2;
    }

    abstract double area();
}

class Rectangle extends Figure {

    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    double area() {
        return dim1 * dim2;
    }
}


class Triangle extends Figure {

    Triangle(double base, double height) {
        super(base, height);
    }

 
    double area() {
        return 0.5 * dim1 * dim2;
    }
}


public class TestFigure {
    public static void main(String[] args) {

        // Figure reference to Rectangle
        Figure f1 = new Rectangle(10, 5);
        System.out.println("Area of Rectangle = " + f1.area());

        // Figure reference to Triangle
        Figure f2 = new Triangle(8, 6);
        System.out.println("Area of Triangle = " + f2.area());
    }
}
```
## Output:
![output](f1.png)
